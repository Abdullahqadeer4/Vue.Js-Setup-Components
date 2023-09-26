 <template>
  <h1>Hello from Home Component</h1>
  <div>
     {{data}}
  </div>
  <h2>  {{msg}}  </h2>
  <!-- Click Events -->
  <button v-on:click="Hi"> Press To see Magic </button>
  <br>
  <button v-on:click="By('Dont touch me')">Touch Me</button>
</template>

<script>
export default {
     name: 'HomePage',
     props:{
          data:String,
          msg: String,
     },
  // Methods
  
  methods:{
          Hi()
          {
               console.log("Hello from console")
          },
          By(data)
          {
               alert(data)
          },
          mouse(input)
          {
               alert(input)
          }
     }
   
}
</script>

<style>

</style>
<!-- The name of the components should be always multiword, else it will throw errors. 
I have shown you the use of props as well {data,msg}. Register your componenets in
app.vue file by importing the component and pass it into components.
Also you will need to pass call the component in Templates in App.vue. Check out the app.vue file. -->