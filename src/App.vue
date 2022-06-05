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
    <input type="text" v-model="name" />
    <button @click="resetInput">Reset Input</button>
    <p>Your Name: {{ fullname }}</p>
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
      // confirmedName: '',
    };
  },
  computed: {
    fullname(): string {
      console.log('running again');
      if (this.name === '') {
        return '';
      }
      return this.name + ' ' + 'Schwarzmuller';
    },
  },
  methods: {
    // outputFullname() {
    //   console.log('running again...');
    //   if (this.name === '') {
    //     return '';
    //   }
    //   return this.name + ' ' + 'Schwarzmuller';
    // },
    // confirmInput() {
    //   this.confirmedName = this.name;
    // },
    submitForm() {
      console.log('submitted!');
    },
    setName(event: Event) {
      this.name = (event.target as HTMLInputElement).value;
    },
    add(num: number) {
      this.counter += num;
    },
    reduce(num: number) {
      this.counter -= num;
    },
    resetInput() {
      this.name = '';
    },
  },
});
</script>
