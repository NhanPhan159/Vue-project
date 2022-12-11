<template>
  <div class="about">
    <h1>This is an about page</h1>
    {{info}}
    <el-button type="primary">Primary</el-button>
    <i class="el-icon-edit"></i>
  </div>
</template>

<script>
import axios from 'axios'
export default{ 
  data() {
    return{
      info : null
    }
  },
  mounted () {
    axios
      .get('https://thanhnhan.pythonanywhere.com/teachers/1/')
      .then(response => (this.info = response.data))
  }
}
</script>