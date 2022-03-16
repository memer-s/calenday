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
  width: 100%;
}

main {
  max-width: 800px;
}

.event {
  padding: 10px;
  border-radius: 10px;
  background-color: #458fff;
}

small,
h3,
p {
  margin: 0;
}

h2 {
  text-align: center;
}
</style>