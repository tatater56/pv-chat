<template>
  <div id="chat-window" v-chat-scroll>
    <p>test</p>
    <p></p>
    <p v-for="(chatData, index) in chatHistory" :key="index">
      {{ chatData.message }}
    </p>
  </div>
</template>

<script>
export default {
  props: {
    chatHistory: {
      type: Array,
      default: () => []
    }
  }
};
</script>
