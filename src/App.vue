<template>
  <div>
    <h3>New participant</h3>
    <participants-list :list="list"></participants-list>
    <new-participant-form @added="addNewParticipant($event)"></new-participant-form>
  </div>
</template>

<script>
  import ParticipantsList from "./ParticipantsList.vue";
  import NewParticipantForm from "./NewParticipantForm.vue";

  export default {
    components: {
        ParticipantsList,
        NewParticipantForm
    },
    data() {
      return {
    // newPerson: {first: '' , last: ''},
        list: []
      };
    },
    methods: {
      // dunno, what's next?

      addNewParticipant($event)
       //   if (!this.newPerson.last) {
        //      return;}
              {
              this.list.push($event)
          }
      }
      };
  </script>
