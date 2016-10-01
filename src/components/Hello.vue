<div id="app">
  <ul>
    <li class="user" v-for="user in users" transition>
      <span>{{user.name}} - {{user.email}}</span>
      <button v-on:click="removeUser(user)">X</button>
    </li>
  </ul>
  <form id="form" v-on:submit.prevent="addUser">
    <input v-model="newUser.name">
    <input v-model="newUser.email">
    <input type="submit" value="Add User">
  </form>
  <ul class="errors">
    <li v-show="!validation.name">Name cannot be empty.</li>
    <li v-show="!validation.email">Please provide a valid email address.</li>
  </ul>
</div>
