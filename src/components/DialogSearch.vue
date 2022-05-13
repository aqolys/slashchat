<template>
  <div class="search">
    <input type="text" placeholder="Search for dialogs" />
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.search {
  position: relative;

  input {
    border: 2px solid #cecece;
    border-radius: 30px;
    font-size: 16px;
    font-weight: 300;
    width: 100%;
    padding: 10px 15px 10px 40px;
    font-family: Kanit, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, Oxygen, Ubuntu,
      Cantarell, "Open Sans", "Helvetica Neue", sans-serif;
    outline: none;
    background: #f2f2f2;
  }

  &::before {
    content: "";
    width: 27px;
    height: 27px;
    position: absolute;
    top: calc(50% - 13px);
    left: 10px;
    background-image: url("../assets/icons/UilSearch.svg");
    background-size: cover;
    opacity: 0.2;
  }
}
</style>