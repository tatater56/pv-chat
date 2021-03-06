<template>
  <div id="home">
    <p class="header">PV Chat {{ value }}</p>
    <text-box placeholder="text" @submitted="submitted" @changed="changed" />
  </div>
</template>

<script>
import TextBox from "@/components/TextBox";

export default {
  name: "Home",
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
