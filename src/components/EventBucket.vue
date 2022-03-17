<template>
  <section>
    <h2><slot></slot></h2>
    <main>
      <div v-for="(event, index) in events" v-bind:key="index" class="event">
        <small>{{ event.time }}</small>
        <h3>{{ event.title }}</h3>
        <p>{{ event.desc }}</p>
      </div>
    </main>
  </section>
</template>

<script>
export default {
  props: ["events"],
};
</script>

<style scoped>

section {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  font-family: 'Roboto Condensed', sans-serif;
}

section h3 {
  font-family: 'Montserrat';
}

main {
  padding: 4px;
  max-width: 600px;
  width: 92vw;
  background-color: #fff;
  border-radius: 7px;
}

.event {
  color: #fff;
  width: auto;
  padding: 10px;
  margin: 10px;
  border-radius: 10px;
  background-color: #458fff;
}

small,
h3,
p {
  margin: 0;
}

h2 {
  margin-top: 40px;
  margin-bottom: 20px;
  font-size: 34px;
  text-align: center;
  font-weight: 400;
}
</style>