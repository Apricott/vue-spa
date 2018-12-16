<template>
  <div>
    <h3>New participant</h3>
    <participants-list :list="list"></participants-list>
    <form @submit.prevent="addNewParticipant()">
      <div class="form-group">
        <label> First name </label>
        <input type="text" class="form-control" v-model="newPerson.first">
        <label> Last name </label>
        <input class="form-control" v-model="newPerson.last">
        <button class="btn btn-dark">Add new participant</button>
      </div>
    </form>
  </div>
</template>

<script>
  import ParticipantsList from "./ParticipantsList.vue";

  export default {
    components: {ParticipantsList},
    data() {
      return {
        newPerson: {first: '' , last: ''},
        list: []
      };
    },
    methods: {
      // dunno, what's next?

      addNewParticipant() {
        this.list.push(this.newPerson),
        this.newPerson = {}
      }
    }
  };
  </script>
