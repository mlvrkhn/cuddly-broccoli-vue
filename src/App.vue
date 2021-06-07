<template>
  <div class="container">
    <Header title="Hash me out"/>
    <Input /> 
    <Button name="Submit" @klikaj="handleClick"/>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Input from './components/Input.vue'
import Button from './components/Button.vue'

export default {
  name: 'App',
  components: {
    Header,
    Input,
    Button
  },
  methods: {
    handleClick() {
      console.log('kliknąc');
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
  background: #000;
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
</style>
