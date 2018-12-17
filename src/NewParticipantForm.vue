<template>
    <div>
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
    export default {
        data() {
            return {
                newPerson: {first: '' , last: ''},
};
        },
        methods: {
            addNewParticipant() {
                this.$emit('added', this.newPerson);
                this.newPerson = {};
            }
        }
    };
</script>