<template>
  <div id="home">
    <p class="header">PV Chat</p>
    <text-box placeholder="enter a nickname" @changed="nicknameChanged" />
    <div class="spacer"></div>
    <p v-if="!connected" class="subheader">connecting to peer network...</p>
    <div v-else>
      <p class="subheader green">connection established</p>
      <p class="subheader">
        share your id with a friend: <span class="green">{{ your_id }}</span>
      </p>
      <div class="spacer"></div>
      <p><i>or</i></p>
      <div class="spacer"></div>
      <text-box
        placeholder="connect with your friend's id"
        @submitted="friendIdSubmitted"
      />
    </div>
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
      connected: false,
      nickname: "",
      your_id: "",
      friend_id: ""
    };
  },
  methods: {
    nicknameChanged(nickname) {
      this.nickname = nickname;
    },
    friendIdSubmitted(friend_id) {
      this.friend_id = friend_id;
      this.$router.push("Chat");
    }
  }
};
</script>

<style scoped>
.spacer {
  margin-bottom: 5rem;
}
.green {
  color: rgb(4, 128, 4);
}
</style>
