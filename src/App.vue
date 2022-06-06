<template>
  <!-- Vue Events -->
  <!-- <header>
    <h1>Vue Events</h1>
  </header>
  <section id="events">
    <h2>Events in Action</h2>
    <button @click="add(10)">Add 10</button>
    <button @click="reduce(5)">Subtract 5</button>
    <p v-once>Starting Counter: {{ counter }}</p>
    <p>Result: {{ counter }}</p>
    <input type="text" v-model="name" />
    <input type="text" v-model="lastName" />
    <button @click="resetInput">Reset Input</button>
    <p>Your Name: {{ fullname }}</p>
    <form @submit.prevent="submitForm">
      <input type="text" />
      <button>Sign Up</button>
    </form>
  </section> -->
  <!-- Vue Events -->

  <!-- Vue Dynamic Styling -->
  <header>
    <h1>Vue Dynamic Styling</h1>
  </header>
  <section id="styling">
<<<<<<< HEAD
    <div class="demo" :class="boxAClasses" @click="boxSelected('A')"></div>
    <div
      :class="['demo', { active: boxBSelected }]"
      @click="boxSelected('B')"
    ></div>
    <div
      class="demo"
      :class="{ active: boxCSelected }"
      @click="boxSelected('C')"
    ></div>
=======
    <div class="demo"></div>
    <div class="demo"></div>
    <div class="demo"></div>
>>>>>>> c0e30520529dfbc0d6a78574d5ea07354f163377
  </section>
  <!-- Vue Dynamic Styling -->
</template>

<style>
@import './assets/base.css';
</style>

<script lang="ts">
import { defineComponent } from 'vue';

<<<<<<< HEAD
export default defineComponent({
  data() {
    return {
      boxASelected: false,
      boxBSelected: false,
      boxCSelected: false,
    };
  },
  computed: {
    boxAClasses() {
      const boxA = this.boxASelected as boolean;
      return { active: boxA };
    },
  },
  methods: {
    boxSelected(box: string) {
      if (box === 'A') {
        this.boxASelected = !this.boxASelected;
      } else if (box === 'B') {
        this.boxBSelected = !this.boxBSelected;
      } else if (box === 'C') {
        this.boxCSelected = !this.boxCSelected;
      }
    },
  },
});
=======
export default defineComponent({});
>>>>>>> c0e30520529dfbc0d6a78574d5ea07354f163377

// Vue Events
// import { defineComponent } from 'vue';

// export default defineComponent({
//   data() {
//     return {
//       counter: 10,
//       name: '',
//       lastName: '',
//       // fullname: '',
//       // confirmedName: '',
//     };
//   },
//   watch: {
//     counter(value: number) {
//       if (value > 50) {
//         setTimeout(() => {
//           this.counter = 0;
//         }, 2000);
//       }
//     },
//     //   name(value: string) {
//     //     if (value === '') {
//     //       this.fullname = '';
//     //     } else {
//     //       this.fullname = value + ' ' + this.lastName;
//     //     }
//     //   },
//     //   lastName(value: string) {
//     //     if (value === '') {
//     //       this.fullname = '';
//     //     } else {
//     //       this.fullname = this.name + ' ' + value;
//     //     }
//     //   },
//   },
//   computed: {
//     fullname(): string {
//       console.log('running again');
//       if (this.name === '' || this.lastName === '') {
//         return '';
//       }
//       return this.name + ' ' + this.lastName;
//     },
//   },
//   methods: {
//     // outputFullname() {
//     //   console.log('running again...');
//     //   if (this.name === '') {
//     //     return '';
//     //   }
//     //   return this.name + ' ' + 'Schwarzmuller';
//     // },
//     // confirmInput() {
//     //   this.confirmedName = this.name;
//     // },
//     // submitForm() {
//     //   console.log('submitted!');
//     // },
//     setName(event: Event) {
//       this.name = (event.target as HTMLInputElement).value;
//     },
//     add(num: number) {
//       this.counter += num;
//     },
//     reduce(num: number) {
//       this.counter -= num;
//     },
//     resetInput() {
//       this.name = '';
//     },
//   },
// });
// Vue Events
</script>
