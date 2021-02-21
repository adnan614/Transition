<template>
  <div class="container">
    <transition name="appear">
        <div class="p-3 mb-2 bg-success text-white"
          v-if="display">
         Hello
    </div>
    
    </transition>
    
    <button @click="display=!display" class="btn btn-primary">Toggle</button>

  </div>
</template>

<script>
export default {
  data(){
    return{
      display: false
    }
  }
}
</script>

<style >
  .appear-enter{
      opacity: 0;
      transform: translateX(500px);
  }
  .appear-enter-active{
      transition: all .2s ease;
  }

  .appear-leave{

  }

  .appear-leave-active{
      opacity: 0;
      transform: translateX(500px);
      transition: all .2s ease;
  }
</style>