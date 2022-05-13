<template>
  <div class="messenger">
    <Header />
    <div class="messenger__columns">
      <div class="messenger__columns_left">
        <DialogSearch />
        <div class="messenger__chatlist">
          <div class="messenger__chatlist_unread">
            <Dialog
              name="Corbin Smidzik"
              date="16:20"
              lastMsg="hey danil danilenko go collab"
              v-for="i in 2"
              :key="i"
              :unread="i"
            />
          </div>
          <div class="messenger__chatlist_readed">
            <Dialog
              name="Corbin Smidzik"
              date="16:20"
              lastMsg="hey danil danilenko go collab"
              v-for="i in 4"
              :key="i"
            />
          </div>
        </div>
      </div>
      <div class="messenger__columns_right">
        <MessengerTopBar />
        <MessengerHistory />
      </div>
    </div>
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Dialog from "@/components/Dialog.vue";
import DialogSearch from "@/components/DialogSearch.vue";
import MessengerTopBar from "@/components/views/Messenger/TopBar.vue";
import MessengerHistory from "@/components/views/Messenger/History.vue";

export default {
  name: "Messenger",
  components: {
    Header,
    Dialog,
    DialogSearch,
    MessengerTopBar,
    MessengerHistory,
  },
};
</script>

<style lang="scss">
.messenger {
  margin: auto;
  max-width: 80em;
  overflow: hidden;
  height: 100%;

  &__columns {
    display: flex;
    width: 100%;
    height: calc(100% - 60px);
    position: relative;
    margin-top: 30px;
    gap: 30px;

    &_left {
      flex: 1 1 auto;
      min-width: 22rem;
      max-width: calc(1680px / 4);
    }
    &_right {
      flex: 3;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }
  }

  &__chatlist {
    margin-top: 20px;

    &_unread {
      border-radius: 50px;
      margin-bottom: 15px;
      box-shadow: 0px 4px 7px rgba(0, 0, 0, 0.15), inset -5px -5px 20px rgba(170, 170, 170, 0.08),
        inset 5px 5px 10px rgba(0, 71, 255, 0.05);

      // box-shadow: inset -5px -5px 20px rgba(62, 210, 82, 0.2),
      //   inset 5px 5px 10px rgba(0, 71, 255, 0.2);
    }

    &_readed {
      border-radius: 50px;
      box-shadow: 0px 4px 7px rgba(0, 0, 0, 0.06), inset -5px -5px 20px rgba(250, 0, 255, 0.03),
        inset 5px 5px 10px rgba(0, 71, 255, 0.015);
    }
  }
}
</style>