<template>
  <div class="container">
    <Header title="Hash me out"/>
    <form @submit.prevent="handleSubmit">
      <input class="input" v-model="message" placeholder="Word to encrypt"/> 
      <Button name="Submit" @handle-submit="handleClick"/>
      <p>{{message}}</p>
    </form>
  </div>
</template>

<script>
import Header from './components/Header.vue'
// import Input from './components/Input.vue'
import Button from './components/Button.vue'

export default {
  name: 'App',
  components: {
    Header,
    // Input,
    Button
  },
  data() {
    return {
      message: '',
    }
  }, 
  methods: {
    handleSubmit() {
      // this.message = message;
      console.log('chillin');
    }
  }
}



// export function getMd5(string) {
//     return fetch('https://api.hashify.net/hash/md5/hex', {
//         method: 'POST',
//         body: string,
//     })
//         .then(resp => {
//             if(resp.ok) {
//                 return resp.json();
//             }
//             return Promise.reject(resp);
//         })
//         .then(data => data.Digest);
// }

</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
body {
  font-family: 'Poppins', sans-serif;
}
form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.container {
  max-width: 500px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 1px solid steelblue;
  padding: 30px;
  border-radius: 5px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
.btn {
  display: inline-block;
  background: rgb(26, 89, 182);
  color: #fff;
  border: none;
  padding: 10px 20px;
  margin: 5px;
  border-radius: 5px;
  cursor: pointer;
  text-decoration: none;
  font-size: 15px;
  font-family: inherit;
}
.btn:focus {
  outline: none;
}
.btn:active {
  transform: scale(0.98);
}
.btn-block {
  display: block;
  width: 100%;
}
.input {
  display: flex;
  justify-content: center; 
  align-items: center;
  margin-bottom: 20px;
  height: 30px;
  border: 1px solid steelblue;
  border-radius: 5px;
  font-size: large;
  padding: 1rem;
}
.input:focus {
    outline: none;
}
.input::placeholder {
  text-align: center;
}
</style>
