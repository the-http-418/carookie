<template>
  <div class="hello">
    <img id="caropic" alt="caro" src="https://techwarts.tech/assets/img/IMG_1061%20Cropped.jpg"/>
    <h1>Hey! I'm Caro, but you can call me CJ.</h1>
    <h3>
      I make amazing cookies!
    </h3>
    
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
/* .hello {
  background-image: url'(https://images.unsplash.com/photo-1499636136210-6f4ee915583e?ixid=MXwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHw%3D&ixlib=rb-1.2.1&auto=format&fit=crop&w=700&q=80');
} */
#caropic {
  max-width: 50%;
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
