<template>
  <div>
    <h1>Contact List</h1>
    <form @submit.prevent>
      <label>Name</label>
      <input v-model="newContact.name" type="text" placeholder="name"> <br>
      <label>Email</label>
      <input v-model="newContact.email" type="text" placeholder="email"> <br>
      <button @click="addContact" type="submit">Add Contact</button>
    </form>
    <table>
      <thead>
        <th>Name</th>
        <th>Email</th>
      </thead>
      <tbody>
        <tr v-for="contact in contacts" :key="contact.id">
          <td>{{contact.name}}</td>
          <td>{{contact.email}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
export default {
  name: 'ContactList',
  data() {
    return {
      contacts: [
        {id: 1, name: "John", email: "example@gmail.com"},
        {id: 2, name: "Jack", email: "example2@gmail.com"},
        {id: 3, name: "Susan", email: "example3@gmail.com"},
        {id: 4, name: "Jasmin", email: "example4@gmail.com"}
      ],
      newContact: {}
    };
  },
  methods: {
    addContact() {
      console.log(this.newContact);
      this.contacts.push(this.newContact);
      this.newContact = {};
    }
  }
}
</script>
