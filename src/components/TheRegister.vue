<template>
  <form id="the-register" class="flex flex--column">
    <input class="input input--username border round-corners" type="text" placeholder="Username" />
    <div class="wrap--inputs">
      <input class="input input--email border" type="text" placeholder="Email Address" />
      <div class="wrap--password flex">
        <input class="input input--password border" type="password" placeholder="Password" />
        <input class="input input--password-repeat border" type="password" placeholder="Repeat PW" />
      </div>
    </div>
  </form>
</template>

<script>
export default {
  name: "TheRegister"
};
</script>

<style scoped>
#the-register {
  position: relative;
  height: 100%;
}
</style>