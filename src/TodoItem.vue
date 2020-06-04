<template>
  <div class="oneTask">
        <span class="taskName">{{task}}</span>
        <span class="day">{{doBy}}</span>
        <CheckButton />
  </div>
</template>


<script>
import CheckButton from "./CheckButton/CheckButton.vue";
export default {
  components: {
    CheckButton: CheckButton
  },
  name: "Tasks",
  props: {
    task: String,
    doBy: String,
  }
};
</script>

<style lang="css">
.oneTask {
  background-color: rgb(240, 240, 250);
  box-shadow: 0px 3px 7px rgb(28, 61, 85);
  border-radius: 15px;
  display: flex;
  align-items: center;
  text-align: left;
  justify-content: space-evenly;
  flex-wrap: wrap;
  padding: 10px;
  margin: 15px;
}

.taskName {
  width: 150px;
}

.day {
  width: 100px;
}


</style>