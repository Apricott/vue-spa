<template>
  <div>  
    <h1>Times clicked {{ title }}</h1>
    <button @click="iAmClicked()">Click me!</button>
    <button @click="reset()">Start over</button>
  </div>
</template>
 
<script>
    export default {
        data() {
            return {title: 0}
        },
        methods: {
            iAmClicked() {
                this.title += 1;
            }
        }
    };
</script>
