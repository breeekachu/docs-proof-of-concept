<template>
  <div>
    <button @click="change(-1)">-</button>
    <span>{{ count }}</span>
    <button @click="change(1)">+</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    change(val) {
      this.count += val;
    },
  },
};
</script>
