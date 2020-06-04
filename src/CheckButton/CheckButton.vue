<template>
  <button 
  :class="['btn', 
        'btn--check', 
        {'btn--cross' : crossed} ]"
  @click="switchBtn"
></button>
</template>

<script>
export default {
  name: 'CheckButton',
  data() {
    return {crossed: true}
  },
  methods: {
    switchBtn() {
      this.crossed = !this.crossed;
    }
  }
}
</script>

<style lang="css">
  .btn {
    width: 3rem;
    height: 3rem;
    border-radius: 1.5rem;
    border: none;
    outline: none;
    background-size: 2.5rem;
    background-position: center;
    background-repeat: no-repeat;
  }

  .btn--check {
    background-image: url('img/check.svg');
    background-color: green;
  }

  .btn--cross {
    background-image: url('img/cross.svg');
    background-color: red;
  }
</style>