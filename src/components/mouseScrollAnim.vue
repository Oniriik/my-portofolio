<template>
  <div class="mouseScrollAnim" >
    <div class="middle" >
      <div class="mouse" ></div>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
    scroll(){
      document.getElementById('page-wrapper').scrollBy({ 
      top: 40,
      behavior: 'smooth' 
    });
      }
  },
};
</script>

<style>
.middle {
    position: absolute;
}

.mouse {
  width: 100px;
  height: 180px;
  border: 4px solid #686868;
  border-radius: 60px;
}

.mouse::before {
  content: "";
  width: 25px;
  height: 25px;
  position: absolute;
  top: 30px;
  background-color: #686868;
  left: 50%;
  transform: translateX(-50%);
  border-radius: 50%;
  opacity: 1;
  animation: mouse 2s infinite;
}

@keyframes mouse {
  from {
    opacity: 1;
    top: 30px;
  }
  to {
    opacity: 0;
    top: 150px;
  }
}

.mouseScrollAnim {
    opacity: 0;
    display: flex;
    justify-content: center;
    margin-top: 4rem;
    transform: scale(0.2);
}


@media (max-width: 800px) {
  .mouseScrollAnim {
    margin-top: 6rem;
}
}
</style>