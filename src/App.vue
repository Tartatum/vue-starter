<template>
  <div>  
    <h1>{{ "Clicked " +nbr +" times" }}</h1>
    <button @click="iAmClicked()">Click me!</button>
  </div>
</template>
 
<script>
    export default {
        data() {
            return {
           nbr : 0,
              }
        },
        methods: {
            iAmClicked() {
                this. nbr += 1;
            }
        }
    };
</script>