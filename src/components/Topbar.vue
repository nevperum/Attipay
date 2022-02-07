<template>
  <div class="topbar">
    <div class="left">
      <img class="logo" alt="logo" src="../assets/logo.svg" />
      <span class="title">AttiPay</span>
    </div>
    <div class="right">
      <span class="date">{{ this.currentDate }}</span>
    </div>
  </div>
</template>

<script>
export default {
  created() {
    console.log("topbar created");
    this.handle = setInterval(() => {
      this.currentDate = this.getDate();
    }, 1000);
  },
  destroyed() {
    clearInterval(this.handle);
  },
  data() {
    return {
      currentDate: this.getDate(),
    };
  },
  methods: {
    getDate() {
      return (
        "0" +
        `${new Date().getDate()}` +
        "." +
        "0" +
        `${new Date().getMonth() + 1}` +
        "." +
        `${new Date().getFullYear()}` +
        " " +
        `${new Date().getHours()}` +
        ":" +
        `${new Date().getMinutes()}` +
        ":" +
        `${new Date().getSeconds()}`
      );
    },
  },
};
</script>

<style scoped>
.topbar {
  background-color: #1a705b;
  width: 100%;
  height: 88px;
  display: flex;
  vertical-align: middle;
  padding: 0 70px;
  justify-content: space-between;
  align-items: center;
}

.logo {
  height: 26px;
  width: auto;
  display: inline-block;
  margin-top: 15px;
}

.title {
  color: #fff;
  display: inline-block;
  font-size: 30px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-weight: bold;
  margin-left: 15px;
  margin-bottom: 15px;
}

.date {
  font-size: 18px;
  color: #fff;
  text-align: right;
  font-family: sans-serif;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

.left {
  vertical-align: middle;
}

.right {
  vertical-align: middle;
}
</style>
