<template>
  <div id="home">
    <p class="header">PV Chat</p>
    <text-box placeholder="enter a nickname" @changed="nicknameChanged" />
    <div class="spacer"></div>
    <p class="subheader">tell your friend your id: {{ your_id }}</p>
    <div class="spacer"></div>
    <p><i>or...</i></p>
    <div class="spacer"></div>
    <text-box
      placeholder="connect with your friend's id"
      @changed="friendIdChanged"
    />
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
      nickname: "",
      your_id: "...",
      friend_id: ""
    };
  },
  methods: {
    nicknameChanged(nickname) {
      this.nickname = nickname;
    },
    friendIdChanged(friend_id) {
      this.friend_id = friend_id;
    }
  }
};
</script>

<style scoped>
.spacer {
  margin-bottom: 5rem;
}
</style>
