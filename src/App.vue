<template>
  <div class="row justify-content-center">
    <div class="col-10">
      <Form :formConfig="formConfig"/>
    </div>
  </div>
</template>

<script>
import Form from './components/Form.vue'

export default {
  name: 'App',
  components: {
    Form
  },
  data () {
    return {
      formConfig: {
        formId: "algomas",
        formClass: "",
        fields: [
          {
            tag: "input",
            type: "text",
            inputClass: "form-control",
            inputId: "form-control",
            placeholder: "Texto libre",
            label: {
              className: "form-label",
              text: "Email address"
            },
            help: {
              id: "algo",
              className: "form-text",
              text: "Ayuda"
            }
          },
          {
            tag: "input",
            type: "email",
            inputClass: "form-control",
            inputId: "form-control",
            placeholder: "Nada acá.",
            label: {
              className: "form-label",
              text: "Email address"
            },
            help: {
              id: "algo",
              className: "form-text",
              text: "Ayuda 2"
            }
          },
          {
            tag: "select",
            selectClass: "form-select",
            selectId: "form-control",
            options: [
              {
                name: "Uno",
                valuue: 1
              },
              {
                name: "Dos",
                valuue: 2
              }
            ]
          }
        ]
      }
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
