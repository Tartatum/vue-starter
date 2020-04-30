<template>
  <div>
    <div>
      <h1>Participants list</h1>
      <ol>
        <li v-for="person in participants">
          {{person.firstname }} {{ person.lastname}}
        </li>
        
      </ol>
    </div>

    <h3>New participant</h3>
    <form @submit.prevent="addNewParticipant()">
      <label>Firstname</label>
      <input type="text" v-model="newParticipants.firstname">
      <label>Lastname</label>
      <input type="text" v-model="newParticipants.lastname">
      <button>Add new participant</button>
    </form>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        participants:[
         {firstname : "John", lastname : "Doe"},
         {firstname : "Robin", lastname : "Hood"},
         {firstname : "Chuck", lastname : "Norris"},
         {firstname : "Some", lastname : "Wan"}
        ],
        newParticipants:{},
      };
    },
    methods: {
      addNewParticipant() {
        this.participants.push(this.newParticipants)
        this.newParticipants ={};
      }
    }
  };
</script>