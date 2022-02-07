<template>
  <div class="Order">
    <center>
      <h1>Your order</h1>
    </center>
    <center>
      <img class="pancakes" alt="logo" src="../assets/pancakes.jpg" />
      <input @click="onclick()" type="button" class="plus" />
      <input type="button" class="minus" />
    </center>

    <center>
      <img class="french" alt="logo" src="../assets/french.jpg" />
      <input type="button" class="plus" />
      <input type="button" class="minus" />
    </center>
    <center>
      <img class="muesli" alt="logo" src="../assets/muesli.jpg" />
      <input type="button" class="plus" />
      <input type="button" class="minus" />
    </center>
    <input type="submit" :value="'Buy' + cost" />
  </div>
</template>

<script>
export default {
  props: {
    msg: String,
    currentDate: Date,
  },
  data() {
    return {
      cost: 0,
    };
  },
  methods: {
    onclick() {
      console.log("Klick");
      this.cost++;
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.Order {
  font-size: 30px;
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-weight: bold;
  margin: 0px;
  padding: 0px;
}
.french {
  height: 112px;
  width: auto;
  border-radius: 10px;
}
.muesli {
  height: 112px;
  width: auto;
  border-radius: 10px;
}

.pancakes {
  height: 112px;
  width: auto;
  border-radius: 10px;
}
.plus {
  margin: 15px;
}
</style>
