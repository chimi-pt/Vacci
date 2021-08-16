<template>
    <footer class="main-footer">
    <strong>Copyright &copy; 2014-{{currentDate.getFullYear()}} <a href="https://adminlte.io">VacciDash</a>.</strong>
    All rights reserved.
    <div class="float-right d-none d-sm-inline-block">
      <b></b> 
    </div>
  </footer>
</template>

<script>
export default {
    data(){
        return{
            currentDate:new Date,  
        }
    }
}
</script>