<template>
    <form :class="formConfig.class" :id="formConfig.formId">
      <div v-for="(field, i) in formConfig.fields" :key="i">
        <template v-if="field.tag == 'input'">
          <div class="mb-3">
          <label v-if="field.label" for="exampleInputEmail1" :class="field.className"> {{ field.label.text }}</label>
          <input
            :type="field.type"
            :class="field.inputClass"
            :id="field.inputId"
            :placeholder="field.placeholder"
          />
          <div v-if="field.help" :id="field.help.id" :class="field.help.className">
            {{ field.help.text }}
          </div>
        </div>
        </template>

        <template v-if="field.tag == 'select'">
          <select :class="field.selectClass" :id="field.selectId">
            <option selected >Open this select menu</option>
            <option :value="option.value" v-for="(option, k) in field.options" :key="k">{{ option.name }}</option>
          </select>
        </template>
      </div>
    </form>
</template>

<script>
export default {
  name: "Form",
  props: {
    formConfig: {
      type: Object,
      require: true
    }
  },
  data(){
    return {
      
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
