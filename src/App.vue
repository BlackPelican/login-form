<template>
  <div id="app" class="flex flex--cc">
    <TheForm />
  </div>
</template>

<script>
import TheForm from "./components/TheForm.vue";

export default {
  name: "App",
  components: {
    TheForm
  }
};
</script>

<style>
@import url("https://fonts.googleapis.com/css?family=Open+Sans:300,400,600,700&display=swap");

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

:root {
  --c-whiteish: #f1e4e4;
  --c-red: #fe6b47;
  --c-reddark: #cd493a;
  --c-grey: #ccc;
  --c-fontlight: #aaa;
  --c-fontdark: #888;
}

html,
body {
  position: relative;
  width: 100%;
  height: 100%;
  font-family: "Open Sans";
}

#app {
  height: 100%;
  width: 100%;
  background: var(--c-whiteish);
}

.round-corners {
  border-radius: 1vmin;
}

.flex {
  display: flex;
}

.flex--row {
  flex-direction: row;
}

.flex--column {
  flex-direction: column;
}

.shadow {
  box-shadow: 0 4px 6px #33333333;
}

.border,
.input.border {
  border: 1px solid var(--c-grey);
}

.flex--cc {
  justify-content: center;
  align-items: center;
}

.input {
  height: 8vmin;
  border: none;
  padding: 0 2vmin;
  color: var(--c-fontdark);
  font-size: 2.5vmin;
  letter-spacing: 0.1vmin;
}

.input:focus {
  outline: none;
  border: 1px solid var(--c-fontdark);
}

.input::placeholder {
  color: var(--c-fontlight);
}

.input,
.wrap--inputs,
.wrap--password {
  width: 100%;
}

.wrap--inputs {
  top: 12vmin;
  height: 16vmin;
  width: 100%;
  position: absolute;
}

.wrap--inputs .input {
  height: 50%;
}

.wrap--password {
  height: 8vmin;
}

.wrap--password .input {
  height: 100%;
  border-top: none;
}

.wrap--inputs .wrap--password .input--password {
  border-radius: 0 0 0 1vmin;
}

.wrap--password .input--password-repeat {
  border-radius: 0 0 1vmin 0;
  border-left: 1px solid transparent;
}

.input--email {
  border-bottom: 1px solid var(--c-grey);
  border-radius: 1vmin 1vmin 0 0;
}

.wrap--inputs .input--password {
  border-top: 1px solid transparent;
  border-radius: 0 0 1vmin 1vmin;
}

.input--password:focus {
  border-top: 1px solid var(--c-fontdark);
}

.input--password-repeat:focus {
  border: 1px solid var(--c-fontdark);
}
</style>
