<template>
  <div class="messenger-input__wrapper">
    <div class="messenger-input" contenteditable="true"></div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
.messenger-input {
  height: 40px;
  padding: 10px;
  border: 1px solid gray;
  word-wrap: break-word;
  border: 0;
  outline: 0;
  overflow-y: auto;
  overflow-x: hidden;

  &__wrapper {
    max-width: 100%;
  }
}
</style>