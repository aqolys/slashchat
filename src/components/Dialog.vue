<template>
  <div class="dialog">
    <div class="dialog__avatar">
      <img src="@/assets/temp/avatar.jpg" alt="" />
      <div class="dialog__count" v-if="unread">
        <span>{{ unread }}</span>
      </div>
    </div>
    <div class="dialog__data">
      <p class="dialog__title">
        <span class="dialog__name">{{ name }}</span>
        <span class="dialog__date">{{ date }}</span>
      </p>
      <p class="dialog__subtitle">
        <span class="dialog__last-msg">{{ lastMsg }}</span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  props: ["avatar", "name", "date", "lastMsg", "unread"],
};
</script>

<style lang="scss" scoped>
.dialog {
  display: flex;
  width: 100%;
  cursor: pointer;
  user-select: none;
  padding: 20px 20px 15px 20px;
  transition: all 0.5s;

  &__avatar {
    position: relative;
    img {
      width: 54px;
      border-radius: 100%;
    }
  }

  &__count {
    position: absolute;
    border: 1px solid #cbe3ff;
    box-shadow: inset 0px 0px 8px 2px #cbe3ff;
    min-width: 27px;
    min-height: 27px;
    background: #fff;
    border-radius: 100%;
    display: flex;
    justify-content: center;
    right: 0;
    bottom: 0;
  }

  &__data {
    width: 100%;
    padding: 0.0625rem 0.4375rem 0.0625rem 0.5625rem;
  }

  &__title {
    display: flex;
    align-items: flex-start;
  }

  &__name {
    flex-grow: 1;
  }

  &__subtitle,
  &__date {
    color: #808080;
    font-weight: 300;
  }

  &:nth-child(1) {
    padding-top: 20px;
    border-radius: 50px 50px 0 0;
  }

  &:last-child {
    padding-top: 15px;
    padding-bottom: 20px;
  }

  &:hover {
    // background: #cbe3ff;
  }
}
</style>