<template>
  <div class="row" id="Dictionary">
    <div class="input-group">
      <b-form-input style="margin-left: 10px" v-model="wordText" placeholder="Enter a word for its definition, origin, and usage."></b-form-input>
      <span class="input-group-btn">
        <button
          type="submit"
          style="margin-left: 10px; margin-right: 10px"
          class="btn btn-primary"
        v-on:click="formSubmit">Go</button>
      </span>
    </div>
  </div>
</template>

<script>
export default {
  name: "Dictionary",
  data() {
    return {
      wordText: ""
    };
  },
  methods: {
    formSubmit(e) {
      // alert(this.wordText);
      // console.log(this.wordText)  // eslint-disable-line no-console
      this.$emit("formSubmit", this.wordText);
      e.preventDefault();
    }
  }
};
</script>

<style>
/* #transForm {
  border-radius: 10px;
  border: 1px #ccc solid;
} */
</style>