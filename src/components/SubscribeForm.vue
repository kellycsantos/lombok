<template>
  <div class="emailInput">
    <h3 v-if="!inscrito">Receba alerta de novos artigos</h3>
    <ValidationProvider rules="email" v-slot="{ errors }">
      <form @submit.prevent="assinatura">
        <span v-if="!inscrito">
          <input type="text" class="input-email" v-model="email" />
          <h5 class="error">{{ errors[0] }}</h5>
          <input type="submit" value="Inscreva-se" class="btn-subscribe" />
        </span>
        <h3 v-if="inscrito">
          Agradecemos a inscrição, em breve receberá artigos incriveis para ler!
        </h3>
      </form>
    </ValidationProvider>
  </div>
</template>

<script lang="ts">
import Vue from "vue";

import { extend, ValidationProvider } from "vee-validate";
import { required, email } from "vee-validate/dist/rules";

extend("required", {
  ...required,
  message: "This field is required",
});
extend("email", {
  ...email,
  message: "Preencha seu email corretamente",
});

export default Vue.extend({
  name: "InputEmail",
  components: {
    ValidationProvider,
  },
  props: {
    inscricao: Boolean,
  },
  data() {
    return {
      email: "",
      errors: [],
      inscrito: false,
    };
  },
  methods: {
    assinatura() {
      const regex = /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,4}$/i;

      if (this.email != "") {
        if (regex.test(this.email)) {
          console.log("email valido");
          this.inscrito = true;
        }
      }
    },
  },
});
</script>

<style>
.input-email {
  height: 35px;
  width: 80vw;
  background: #eff1ee;
  border: none;
  margin: 15px 0;
}

.input-email:focus {
  outline: 1px solid rgb(6, 61, 11);
}
.error {
  color: rgb(218, 6, 6);
}

.btn-subscribe {
  border: 1px solid black;
  display: inline-block;
  background: none;
  width: 60vw;
  height: 40px;
  max-width: 300px;
  cursor: pointer;
  transition: 0.2s linear;
}

@media screen and (min-width: 768px) {
  .input-email {
    max-width: 50vw;
    width: 600px;
    height: 45px;
  }
  .btn-subscribe {
    height: 40px;
    max-width: 200px;
  }

  .btn-subscribe:hover {
    background: #436b43;
    color: #f2f4f1;
    border: none;
  }
}
</style>
