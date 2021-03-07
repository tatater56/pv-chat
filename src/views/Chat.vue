<template>
  <div id="chat">
    <p class="header sized">Chatting with {{ friend_nickname }}</p>
    <chat-window class="fill" />
    <text-box class="sized" />
  </div>
</template>

<script>
import TextBox from "@/components/TextBox.vue";
import ChatWindow from "@/components/ChatWindow.vue";

export default {
  name: "Chat",
  components: {
    TextBox,
    ChatWindow
  },
  data() {
    return {
      friend_nickname: "unknown"
    };
  }
};
</script>

<style scoped>
#chat {
  height: 100%;
  display: flex;
  flex-flow: column;
}

.sized {
  flex: 0 1 auto;
}

.fill {
  flex: 1 1 auto;
}
</style>
