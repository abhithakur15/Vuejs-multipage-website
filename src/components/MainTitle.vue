<template>
<div class="main-title">
    <span class="d-flex align-items-center gap-2 mb-3"><img src="../assets/images/span2.png" alt="" class="img-fluid">{{ text }}</span>
<h2 class="text-white">
    {{ text1 }}
</h2>
</div>




</template>

<script>
export default {
  name: 'MainTitle',
  props: {
    text: String,
    text1: String
  }
}

</script>

<style scoped>
.main-title span{
    color: var(--light-yellow);
    font-size: 16px;
    font-weight: 700;
}
.main-title h2{
    font-size: 44px;
    font-weight: 600;
}
</style>