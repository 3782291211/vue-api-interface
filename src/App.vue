<template>
  <NavigationBar />
  <Header title="API interface" />
  <router-view></router-view>
</template>

<script>
import NavigationBar from './components/NavigationBar.vue';
import Header from './components/Header.vue';

export default {
  name: 'App',
  components: {
    Header,
    NavigationBar
  },
  compatConfig: { MODE: 3 }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Luckiest+Guy&display=swap');

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: whitesmoke;
}

body {
  background-color: rgb(35, 33, 33) !important;
}

h2 {
  margin: 15px auto !important;
  font-size: 40px !important;
}

li {
  list-style: none;
}

.card {
    text-align: left;
}

.card-title {
    color: rgb(25, 30, 44);
    font-weight: 900;
    font-size: 24px;
}

.card-subtitle {
    font-size: 20px
}

.card-text {
    margin: 2px 0
}

.card-body {
  height: 260px !important;
}

.d-flex {
    width: 70%;
    float: right
}

.--hide-overflow {
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
}

span {
    font-weight: bold;
}

.grid {
  width: 90%;
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(400px, max-content));
  justify-content: center;
  gap: 15px;
  margin: 0 auto;
  max-width: 1600px;
}

.alert {
  width: fit-content;
  max-width: 700px;
  margin: 30px auto;
}

.alert-success {
  width: 70%;
  max-width: 900px;
}

.spinner-border {
  width: 90px !important;
  height: 90px !important;
  font-size: 30px;
  margin: 30px auto 10px;
}

.button-group {
  margin-bottom: 20px;
}

.loading {
  margin-bottom: 50px;
}

section {
    margin-bottom: 60px
}

.back-to-top {
  margin-bottom: 70px;
  font-size: 16px !important
}

.glass {
  /* From https://css.glass */
background: rgba(245, 162, 73, 0.888);
border-radius: 16px;
box-shadow: 0 0 20px rgb(251, 187, 98);
backdrop-filter: blur(9.1px);
-webkit-backdrop-filter: blur(9.1px);
border: 1px solid rgba(76, 117, 131, 0.43);
width: 90%;
max-width: 1000px;
margin: 20px auto 40px;
padding: 20px 0
}

</style>