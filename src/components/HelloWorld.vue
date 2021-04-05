<template>
  <div class="hello">
    <img
      id="caropic"
      alt="caro"
      src="https://techwarts.tech/assets/img/IMG_1061%20Cropped.jpg"
    />
    <h1>Hey! I'm Caro, but you can call me CJ.</h1>
    <h2>I make amazing cookies :)</h2>
    <h2>And it's my birthday today!!!!!</h2>
    <h3>Click here to wish me a happy birthday</h3>
    <form>
      <label for="name">Your name</label>
      <br />
      <input type="text" id="name" name="name" placeholder="Your Name" />
      <br />
      <label for="wishes">Your personalized wish</label>
      <br />
      <textarea
        id="wishes"
        name="wishes"
        value="Wish you a very Happy Birthday! 🎊"
        placeholder="Your wishes"
      />
      <br />
      <button v-on:click="wish">Wish</button>
    </form>
  </div>
</template>

<script>
const axios = require("axios");

export default {
  name: "HelloWorld",
  props: {
    msg: String,
  },
  methods: {
    wish: function (event) {
      // console.log("HIIII");
      event.preventDefault();
      var content = "Dear @caro, ";
      content += document.getElementById("name").value;
      // content += " wishes you a very Happy Birthday! 🎊";
      content += ' says, "';
      content += document.getElementById("wishes").value;
      content += '"';

      let data = { content: content };
      axios
        .post(
          // "https://discord.com/api/webhooks/828480703288705055/ndqcUqphtUUpGTs1usNlvmgKt8URDe2v1IHZlQvW-lW-hDmRGJ8m6Gb5osBufg1Wt3yt",
          "https://discord.com/api/webhooks/828495583789842445/kDh0Y3UR3gIq0VX85vKZPbN3kYl0SqlGQlHAG1iLPgzRMyaL_qGrTUm74zvBuPvvqD_W",
          data
        )
        .then(
          alert(
            "You have wished caro. To make sure your wishes reach her, send this link to 3 other people."
          )
        );
    },
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* .hello {
  background-image: url'(https://images.unsplash.com/photo-1499636136210-6f4ee915583e?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=80');
} */
#caropic {
  max-width: 30%;
}
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
