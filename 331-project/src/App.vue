<template>
  <nav>
    <router-link to="/about">About</router-link> |
    <router-link to="/more">More</router-link> |
  </nav>
  <router-view />
   <footer>
        <p>Copyright 2022 {{ title }}</p>
    </footer>
</template>
<script>
export default {
  inject: ["vaccinate"],
  props: {
      title: {
        type: String,
        required: true
      }
    },
    data(){
        return{
        }
    }
}
</script>
<style>
footer{
    background: #222;
    padding: 6px;
}
p{
        color: lightgreen;
        text-align: center;
}


@keyframes yellowfade {
  from {
    background: yellow;
  }
  to {
    background: transparent;
  }
}

#flashMessage {
  animation-name: yellowfade;
  animation-duration: 3s;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
h4 {
  font-size: 20px;
}
</style>
