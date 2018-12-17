<template>
    <div v-if="list.length > 0">
        <h4> Participants </h4>
        <ol class="list-group">
            <li class="list-group-item" v-for="person in list">
                {{ person.first }}
                {{ person.last }}
            </li>
        </ol>
    </div>
</template>

<script>
    export default {
        props: ['list']
    };
</script>