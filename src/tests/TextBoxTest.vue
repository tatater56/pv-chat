<template>
  <div id="TextBoxTest">
    <p class="header">TextBoxTest {{ value }}</p>
    <text-box placeholder="text" @submitted="submitted" @changed="changed" />
  </div>
</template>

<script>
import TextBox from "@/components/TextBox";

export default {
  name: "TextBoxTest",
  components: {
    TextBox
  },
  data() {
    return {
      value: ""
    };
  },
  methods: {
    submitted(value) {
      this.value = value;
      alert(this.value);
    },
    changed(value) {
      this.value = value;
    }
  }
};
</script>
