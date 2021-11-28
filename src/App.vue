<template>
  <section>
          <header>
        <h1>My Friends</h1>
      </header>
    <div class="container">
      <user-data @updateData="updateData" />
      <active-user :username="username" :age="age" />
    </div>
  </section>
</template>

<script>
import ActiveUser from "./components/ActiveUser.vue";
import UserData from "./components/UserData.vue";
export default {
  data() {
    return {
      username: "",
      age: "",
    };
  },
  methods: {
    updateData(data) {
      this.username = data.name;
      this.age = data.age;
    },
  },
  components: { ActiveUser, UserData },
};
</script>

<style>
.container {
  display: flex;
  justify-content: space-between;
  max-width: 1000px;
  margin: 0 auto;
}
</style>
