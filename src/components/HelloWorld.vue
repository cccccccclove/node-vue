<template>
  <div>
  </div>
</template>

<script>
import select from './select.vue'
const axios = require('axios')
export default {
  components: { select },
  data() {
    return {

    }
  },
  created() {
    let users
    axios.post('http://localhost:8080/user/saveOrUpdate',{
      username:"小碗",
      password:'123',
      gender:'女',
      id:1
    }).then((res) => {
      users = res.data
    })
    console.log(users)
  },
}
</script>