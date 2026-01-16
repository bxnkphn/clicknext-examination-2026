<script setup>
  defineProps({
    currentTab: String
  });

  const emit = defineEmits(['update:currentTab']);
  const selectTab = (tabName) => {
    emit('update:currentTab', tabName);
  };
</script>

<template>
  
  <div class="d-flex flex-column flex-shrink-0 p-3 bg-dark">  
    <ul class="nav nav-pills flex-column gap-2">
      <li class="nav-item">
        <a href="#" class="nav-link d-flex align-items-center py-3" :class="currentTab === 'deposit-withdraw' ? 'active bg-primary bg-gradient shadow-sm' : 'text-white-50 hover-light'" @click.prevent="selectTab('deposit-withdraw')" data-bs-dismiss="offcanvas">
          <i class="bi bi-wallet2 me-3 fs-5"></i> 
          ฝาก-ถอน (Deposit / withdraw)
        </a>
      </li>
      <li>
        <a href="#" class="nav-link d-flex align-items-center py-3" :class="currentTab === 'transaction' ? 'active bg-primary bg-gradient shadow-sm' : 'text-white-50 hover-light'" @click.prevent="selectTab('transaction')" data-bs-dismiss="offcanvas">
          <i class="bi bi-clock-history me-3 fs-5"></i> 
          ประวัติธุรกรรม (History)
        </a>
      </li>
    </ul>
  </div>

</template>

<style scoped>
  .hover-light:hover {
    background-color: rgba(255, 255, 255, 0.1);
    color: white !important;
    border-radius: 0.375rem;
  }
</style>