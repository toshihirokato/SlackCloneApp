<template>
  <div class="chats-container">
    <message v-for="message in messages" :message="message" :key="message.id" />
  </div>
</template>

<script>
import Message from '~/components/Message'

export default {
  //! プロパティの受け取り
  props: ['messages'],
  components: {
    Message
  },
  mounted() {
    console.log(this.messages);
  }
}
</script>

<style>
.chats-container {
  padding: 16px;
}
</style>
