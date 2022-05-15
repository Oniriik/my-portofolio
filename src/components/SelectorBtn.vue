<template>

<div class="btn" >
  <label  class="switch"><input type="checkbox" @click="$emit('toggle')"/><div></div></label>
</div>  
</template>

<script>
export default {
}
</script>

<style scoped>
.btn {
  position: relative;
  text-align: center;
}

.switch input {
  position: absolute;
  opacity: 0;
}


.switch {
  display: inline-block;
  height: 1em;
  width: 2em;
  background: #BDB9A6;
  border-radius: 1em;
}

.switch div {
  height: 1em;
  width: 1em;
  border-radius: 1em;
  background: #FFF;
  -webkit-transition: all 700ms;
     -moz-transition: all 700ms;
          transition: all 700ms;
}

.switch input:checked + div {
  -webkit-transform: translate3d(100%, 0, 0);
     -moz-transform: translate3d(100%, 0, 0);
          transform: translate3d(100%, 0, 0);
}

</style>