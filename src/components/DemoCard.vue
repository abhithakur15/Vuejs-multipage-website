<template>
<div class="demo-card">
  <div class="icon">
    <img :src="require(`@/assets/images/${path}.png`)" alt="" class="img-fluid">
  </div>
<div class="text">
    <h4 class="text-white">{{ text }}</h4>
    <p class="text-white">{{ text1 }}</p>

</div>
</div>
</template>
<script>
export default {
  name: 'DemoCard',
  props: {
    text: String,
    text1: String,
    path:String
  }
}

</script>
<style scoped>

.demo-card{
  display:flex;
  gap: 10px;
}
.icon{
  background-color: var(--main_black);
    border-radius: 50%;
    height: 60px;
    width: 135px;
    display: inline-flex;
    justify-content: center;
    align-items: center;
    margin-bottom: 15px;
}

</style>