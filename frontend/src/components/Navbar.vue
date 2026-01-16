<script setup>
  defineProps({
    userData: Object
  });

  const emit = defineEmits(['logout']);
</script>

<template>
  
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark px-3 px-sm-4 py-3">
    <div class="container-fluid p-0 d-flex justify-content-between">    
      <div class="d-flex align-items-center">
        <button class="btn btn-outline-light d-lg-none me-2 me-sm-3 border-0" type="button" data-bs-toggle="offcanvas" data-bs-target="#mobileSidebar">
          <i class="bi bi-list fs-3"></i>
        </button>
        <a class="navbar-brand d-flex align-items-center fw-bold fs-5 fs-sm-4" href="#">
            Banking Web App
        </a>
      </div>
      <div class="d-flex align-items-center gap-2">
          <button @click="emit('logout')" class="btn btn-outline-danger btn-sm d-flex align-items-center">
        <i class="bi bi-box-arrow-right d-none d-sm-inline me-0 me-sm-2"></i> 
            Logout
          </button>
      </div>
    </div>
  </nav>

</template>

<style scoped>
</style>