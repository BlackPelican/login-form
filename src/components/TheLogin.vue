<template>
  <form id="the-login" class="flex flex--column">
    <div class="wrap--inputs flex flex--column">
      <input class="input input--email border" type="text" placeholder="Email Address" />
      <input class="input input--password border" type="password" placeholder="Password" />
    </div>
  </form>
</template>

<script>
export default {
  name: "TheLogin"
};
</script>

<style scoped>
#the-login {
  height: 100%;
  position: relative;
}
</style>