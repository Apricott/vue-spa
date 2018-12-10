<template>
  <div>
    <div v-if="list.length > 0">
      <h1>Participants list</h1>
      <ol>
        <li v-for="person in list">
          {{ person.first }} {{ person.last }}
        </li>
      </ol>
    </div>

    <h3>New participant</h3>
    <form @submit.prevent="addNewParticipant()">
      <label>First name </label>
      <input type="text" v-model="newPerson.first">
      <label>Last name </label>
      <input type="text" v-model="newPerson.last">
      <button>Add new participant</button>
    </form>
  </div>
</template>

<script>
  export default {
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
        this.newPerson= {}
      }
    }
  };
  </script>
