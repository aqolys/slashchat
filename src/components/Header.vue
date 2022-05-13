<template>
  <div class="header">
    <div>
      <div class="header__logo">
        <img src="@/assets/images/logo.svg" alt="chat://" />
      </div>
      <div class="header__nav">
        <NavLink class="header__nav-item" dir="/" text="Messenger" />
        <NavLink class="header__nav-item" dir="/people" text="People" />
        <NavLink class="header__nav-item" dir="/settings" text="Settings" />
        <NavLink class="header__nav-item" dir="/faq" text="FAQ" />
      </div>
    </div>
    <div>
      <div class="header__buttons">
        <img src="@/assets/icons/UilSearch.svg" alt="Search" />
        <img src="@/assets/icons/IcSharpNotificationsNone.svg" alt="Notifications" />
      </div>
      <div class="header__profile">
        <div></div>
      </div>
    </div>
  </div>
</template>

<script>
import NavLink from "@/components/NavLink.vue";

export default {
  components: {
    NavLink,
  },
};
</script>

<style lang="scss">
.header {
  display: flex;
  justify-content: space-between;
  padding: 10px 0;

  &__logo {
    margin-right: 6em;
  }

  &__nav {
    display: flex;
    gap: 30px;

    &-item {
      padding: 6px 17px 5px;
      border-radius: 14px;

      &:hover {
        background: #f2f2f2;
      }
    }
  }

  &__buttons {
    margin-right: 20px;
    display: flex;
    gap: 20px;

    & > img {
      width: 28px;
    }
  }

  &__profile > div {
    width: 40px;
    height: 40px;
    background: #e6e6e6;
    border: 2px solid #c3c3c3;
    border-radius: 100%;
  }

  & div {
    display: flex;
    align-items: center;
  }

  & a {
    color: black;
    text-decoration: unset;
  }
}
</style>