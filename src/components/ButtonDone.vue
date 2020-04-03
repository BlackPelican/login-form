<template>
  <button @click="toggleLogin" id="button-done" class="round-corners">{{cta}}</button>
</template>

<script>
export default {
  props: {
    login: Boolean
  },
  name: "ButtonDone",
  computed: {
    cta() {
      return this.login ? "Log In" : "Register";
    }
  },
  methods: {
    toggleLogin() {
      this.$emit("toggleLogin");
    }
  }
};
</script>

<style scoped>
#button-done {
  width: 100%;
  height: 8vmin;
  background: var(--c-red);
  border: none;
  outline: none;
  font-size: 2.5vmin;
  color: #fff;
  cursor: pointer;
  font-weight: 600;
  letter-spacing: 0.1vmin;
  transition: transform 200ms ease-in-out;
}

#button-done:active {
  transform: scale(0.95);
}

#button-done:hover {
  text-decoration: underline;
}
</style>