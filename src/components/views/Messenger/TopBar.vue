<template>
  <div class="messenger-topbar">
    <div class="messenger-topbar__profile">
      <img src="@/assets/temp/avatar.jpg" alt="" />
      <span>Corbin Smidzik</span>
    </div>
    <div class="messenger-topbar__close"><span>Close</span></div>
    <div class="messenger-topbar__actions"><img src="@/assets/icons/actions.svg" alt="" /></div>
  </div>
</template>

<script>
export default {};
</script>

<style lang='scss'>
.messenger-topbar {
  height: 48px;
  display: flex;
  gap: 25px;
  align-items: stretch;
  justify-content: space-between;
  user-select: none;

  & > div {
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.05), 0px 4px 7px rgba(0, 0, 0, 0.05),
      inset -5px -5px 20px rgba(250, 0, 255, 0.08), inset 5px 5px 10px rgba(0, 71, 255, 0.05);
    display: flex;
    align-items: center;
    padding: 0 15px;
    border-radius: 30px;
    cursor: pointer;
  }

  &__profile {
    gap: 10px;
    flex: 1;

    img {
      width: 30px;
      border-radius: 100%;
    }
  }

  &__actions {
    width: 48px;
    justify-content: center;
    padding: 0 0 0 0 !important;
  }
}
</style>