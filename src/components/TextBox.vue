<template>
  <form id="textbox" @submit.prevent="signalSubmit">
    <input :placeholder="placeholder" v-model="value" @input="signalChange" />
  </form>
</template>

<script>
export default {
  name: "TextBox",
  props: {
    placeholder: String
  },
  data() {
    return {
      value: ""
    };
  },
  methods: {
    signalSubmitted() {
      this.$emit("submitted", this.value);
    },
    signalChanged() {
      this.$emit("changed", this.value);
    }
  }
};
</script>

<style scoped>
#textbox input {
  width: 100%;
}
</style>
