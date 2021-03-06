<template>
  <form id="textbox" @submit.prevent="submitted">
    <input :placeholder="placeholder" v-model="value" @input="changed" />
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
    submitted() {
      this.$emit("submitted", this.value);
    },
    changed() {
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
