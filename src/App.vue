<script setup>
import EventBucket from './components/EventBucket.vue'
// This starter template is using Vue 3 <script setup> SFCs
// Check out https://v3.vuejs.org/api/sfc-script-setup.html#sfc-script-setup

</script>

<template>
  <div class="cont">
    <event-bucket :events="today">Detta händer idag</event-bucket>
    <div class="btn">
      <img src="./assets/add.png" alt="">
      <p>Lägg till händelse</p>
    </div>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      today: [{title: 'bruh', time: '10.10 - 20.20', desc: 'a little desc'}, {title: 'bruh', time: '10.10 - 20.20', desc: 'a little descLorem ipsum dolor sit amet, conceiur bla bla bla Lorem ipsum dolor sit amet, conceiur bla bla bla'}]
    }    
  }
}
</script>

<style>
body {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 0;
  height: 100%;
  background-color: #F9F9F9;
}

.cont {
  font-family: 'Montserrat';
  height: 100vh;
  margin: 0;
}

.btn {
  display: flex;
  justify-content: center;
  align-items: center;
  background-color: #458fff;
  color: #fff;
  padding: 10px;
  margin: 20px;
  max-width: 570px;
  width: 88vw;
  border-radius: 7px;
}

.btn p {
  font-size: 20px;
  margin: 0;
}

.btn img {
  margin-right: 6px;
  width: 30px;
  height: 30px;
}

</style>
