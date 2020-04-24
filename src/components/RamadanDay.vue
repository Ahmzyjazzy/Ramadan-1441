<template>
  <div class="quote-container">
    <h1 class="header">Ramadan Day {{day}}</h1>
    <p class="quote">{{quote}}</p>
    <p class="author">{{author}}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    day: Number,
    quote: String,
    author: String,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
.quote-container {
    display: grid;
    grid-template-rows: 15% 80% 5%;
    height: 90vh;
    width: 90vw;
    transform: translate(-50%, -50%);
    position: absolute;
    top: 50%;
    left: 50%;
    justify-content: center;

    h1, 
    p {
      text-shadow: 0 2px 4px rgba(13,0,77,.08), 0 3px 6px rgba(13,0,77,.08), 0 8px 16px rgba(13,0,77,.08);
    }

    .quote {
      font-size: 25px;
      line-height: 1.5em;
    }

    .author {
      font-size: 18px;
      font-style: italic;
      align-self: end;
      justify-self: end;
    }
}
</style>
