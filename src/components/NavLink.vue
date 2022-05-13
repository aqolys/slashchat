<template>
  <router-link :to="dir">{{ text }}</router-link>
</template>

<script>
export default {
  props: ["text", "dir"],
};
</script>

<style lang="scss" scoped>
router-link {
  font-size: 30px;
}
</style>