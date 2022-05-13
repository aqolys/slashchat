<template>
  <div class="messenger-history">
    <MessengerInput />
  </div>
</template>

<script>
import MessengerInput from "@/components/views/Messenger/Input.vue";

export default {
  components: {
    MessengerInput,
  },
};
</script>

<style lang="scss">
.messenger-history {
  box-shadow: 0px 4px 7px rgba(0, 0, 0, 0.15), inset -5px -5px 20px rgba(170, 170, 170, 0.08),
    inset 5px 5px 10px rgba(0, 71, 255, 0.05);
  border-radius: 50px;
  height: calc(100% - 120px);
  // flex: 1;
}
</style>