<template>
  <header>
    <h1>Vue Events</h1>
  </header>
  <section id="events">
    <h2>Events in Action</h2>
    <button @click="add(10)">Add 10</button>
    <button @click="reduce(5)">Subtract 5</button>
    <p v-once>Starting Counter: {{ counter }}</p>
    <p>Result: {{ counter }}</p>
    <input
      v-on:input="setName($event, 'Schawrzmuller')"
      type="text"
      v-on:keyup.enter="confirmInput"
    />
    <p>Your Name: {{ confirmedName }}</p>
    <form @submit.prevent="submitForm">
      <input type="text" />
      <button>Sign Up</button>
    </form>
  </section>
</template>

<style>
@import './assets/base.css';
</style>

<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
  data() {
    return {
      counter: 10,
      name: '',
      confirmedName: '',
    };
  },
  methods: {
    confirmInput() {
      this.confirmedName = this.name;
    },
    submitForm() {
      console.log('submitted!');
    },
    setName(event: Event, lastName: string) {
      this.name = (event.target as HTMLInputElement).value + ' ' + lastName;
    },
    add(num: number) {
      this.counter += num;
    },
    reduce(num: number) {
      this.counter -= num;
    },
  },
});
</script>
