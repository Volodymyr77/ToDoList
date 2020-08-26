<template>
  <div>
    <input type="text" v-model="text" />
    <ul>
      <li v-for="(item, i) in arr" :key="i">
        <span>{{item}}</span>
      </li>
    </ul>
    <button @click="add" v-if="arr.length <=10">add todo</button>
    <button @click="remove(i)">delete</button>
  </div>
</template>

<script>
export default {
  name: 'App',

  data() {
    return {
      text: '',
      arr: [],
    };
  },
  methods: {
    add() {
      this.arr.push(this.text);
      this.text = '';
    },

    remove(i) {
      this.arr.splice(i, 1);
    },
  },
};
</script>

<style>
</style>

