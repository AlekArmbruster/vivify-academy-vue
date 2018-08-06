<template>
  <div>
    <h1>Contact List</h1>
    <table>
      <thead>
        <th>Name</th>
        <th>Email</th>
      </thead>
      <tbody>
        <tr v-for="(contact, key) in contacts" :key="key">
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
        {name: "John", email: "example@gmail.com"},
        {name: "Jack", email: "example2@gmail.com"},
        {name: "Susan", email: "example3@gmail.com"},
        {name: "Jasmin", email: "example4@gmail.com"}
      ]
    };
  }
}
</script>
