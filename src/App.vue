<template>
  <div>
    <div>
      <h1>Participants list</h1>
      <ol>
        <li v-for="name in list">
          {{ name.first }} {{ name.last }}
        </li>
      </ol>
    </div>

    <h3>New participant</h3>
    <form @submit.prevent="addNewParticipant()">
      <label>First name </label>
      <input type="text" v-model="newName.first">
      <label>Last name </label>
      <input type="text" v-model="newName.last">
      <button>Add new participant</button>
    </form>
  </div>
</template>

<script>
    export default {
        data() {
            return {
                newName: {first: '' , last: ''},
                list: []
            };
        },
        methods: {
                // dunno, what's next?

            addNewParticipant() {
              this.list.push(this.newName),
              this.newName = {}
        }
        }
    };
