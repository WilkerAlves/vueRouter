<script>
export default {
  name: "App"
};
</script>


<template>
  <div id="app">
    <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
    <router-link class="navbar-brand" to="/" >Brincando VueRouter</router-link>
    <div>
      <ul class="navbar-nav">
        <li class="nav-item">
            <router-link class="nav-link" to="/blog">Blog</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/services">Services</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/contact">contact</router-link>
        </li>
      </ul>
    
  </div>
</nav>
    <transition name="moveInUp">
         <router-view/>
  </transition>
  </div>
</template>


<style>
#app {
}

.moveInUp-leave-active{
  animation: moveInUp .3s ease-in;
}

@keyframes moveInUp{
 0%{
  transform: translateY(0);
 }
  100%{
  transform: translateY(-400px);
 }
}

.moveInUp-enter-active{
  animation: fadeIn 1s ease-in;
}
@keyframes fadeIn{
  0%{
    opacity: 0;
  }
  50%{
    opacity: 0.5;
  }
  100%{
    opacity: 1;
  }
}
</style>