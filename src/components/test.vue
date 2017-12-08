<template>
  <div class="test">
      <h1>Using {{curly}} => {{title}}</h1>
      <p>Using {{curly}} => {{user.firstName}}</p>
      <p>Using v-text</p> 
      <p v-text="user.lastName"></p>
      <br>
        <p>Using "v-html"</p>
        <span v-html="htmlCode"></span>
      
      <p v-if="showName">{{title}}</p>
      <p v-else>Nothing</p>    
    <h2>v-for</h2>
      <ul>
        <li v-for="item in items">{{item.title}}</li>
      </ul> 
     <h2>v-model (Like ng-model in Angular)</h2>
      <input type="text" v-model="title">

     <h2>Events </h2> 
      <li>v-on</li>
      <button v-on:click="greet">Say Greeting</button>
      <br/>
      <input type="text" v-on:keyup="presskey">  
    <hr>
    <label>First Name </label><input type="text" v-model="user.firstName">
    <br>
    <label>Last Name </label><input type="text" v-model="user.lastName">
    <br>
    <h3>"{{fullName}}"</h3>

    <h2>{{msg}}</h2>
  
  </div>
</template>

<script>
export default {
  name: `test`,
  props:{
    msg:{
      type: String,
      default:'Foobar'
    }
  },
  data() {
    return {
        title: 'Hello World',
        curly:'{{}}',
        htmlCode:'<p>This is in HTML inside a variable see source code</p>',
        user: {
            firstName: 'John',
            lastName: 'Doe'
            },
        showName: false,
        items:[
          {title: 'Item One'},
          {title: 'Item Two'},
          {title: 'Item Three'}
          ]
      }
  },
  methods:{
    greet: () => {alert('Hola Funciono');},
    presskey: () => {console.log('Key Pressed!');}
  },
  computed:{
    fullName: function () { return this.user.firstName+ ' ' +this.user.lastName;
    }
  }
}
</script>

<style scoped>

</style>
