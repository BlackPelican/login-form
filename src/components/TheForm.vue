<template>
  <div id="the-form" class="flex flex--row shadow">
    <aside class="flex flex--cc flex--column">
      <h1>Welcome!</h1>
      <div class="round flex flex--cc">
        <img src="../img/door.svg" alt="Welcome" />
      </div>
    </aside>
    <main class="flex flex--cc">
      <div class="wrap--form flex flex--column">
        <TheLogin v-if="login" />
        <TheRegister v-else />
        <ButtonDone @toggleLogin="toggleLogin" :login="login" />
      </div>
    </main>
  </div>
</template>

<script>
import TheLogin from "./TheLogin.vue";
import TheRegister from "./TheRegister.vue";
import ButtonDone from "./ButtonDone.vue";

export default {
  name: "TheForm",
  data: function() {
    return {
      login: false
    };
  },
  components: {
    TheLogin,
    TheRegister,
    ButtonDone
  },
  methods: {
    toggleLogin() {
      this.login = !this.login;
    }
  }
};
</script>

<style scoped>
#the-form {
  width: calc(70vmin * 1.6);
  height: 70vmin;
  border-radius: 2vmin;
  overflow: hidden;
}

aside {
  background: var(--c-red);
  flex: 10;
}

main {
  background: #fff;
  flex: 16;
}

.wrap--form {
  width: 60%;
  height: 65%;
  justify-content: space-between;
}

.round {
  height: 20vmin;
  width: 20vmin;
  background: var(--c-reddark);
  border-radius: 50%;
}

.round img {
  height: 70%;
}

aside h1 {
  color: #fff;
  margin-bottom: 4vmin;
  font-size: 4vmin;
}
</style>