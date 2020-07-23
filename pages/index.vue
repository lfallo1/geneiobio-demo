<template>
  <div class="container">
    <div>
      <Logo />
      <h1 class="title">
        geneiobio-demo
      </h1>
      <div class="links">
        <a
          href="https://nuxtjs.org/"
          target="_blank"
          rel="noopener noreferrer"
          class="button--green"
        >
          Documentation
        </a>
        <a
          href="https://github.com/nuxt/nuxt.js"
          target="_blank"
          rel="noopener noreferrer"
          class="button--grey"
        >
          GitHub
        </a>
      </div>
    </div>
  </div>
</template>

<script>

  import axios from 'axios'

export default {
  created(){
    setTimeout(() => {
      axios.request({
        // `url` is the server URL that will be used for the request
        url: 'http://localhost:8080/MyGene2/api/external/geneiobio/token/12345',
        method: 'get',
        headers: {
          'X-Auth-Token': 'bc9b7e9c-ab1b-11e7-abc4-cec278b6b50b'
        },
        withCredentials: true

      });
    },3000);
  }
}
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}

.title {
  font-family:
    'Quicksand',
    'Source Sans Pro',
    -apple-system,
    BlinkMacSystemFont,
    'Segoe UI',
    Roboto,
    'Helvetica Neue',
    Arial,
    sans-serif;
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}
</style>
