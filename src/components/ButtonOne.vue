<template>

<a :href="path"  class="btn-1">{{ text }}
    <span class="arrow1">
        <i class="fa-solid fa-arrow-right"></i>
    </span>
    <span class="arrow2">
        <i class="fa-solid fa-arrow-right"></i>
    </span>
</a>

</template>
<script>
export default {
  name: 'ButtonOne',
  props: {
    text: String,
    path:String
  }
}

</script>

<style scoped>
.btn-1{
    background-color: var(--light-yellow);
    color:var(--black);
    font-weight: 500;
    letter-spacing: 1.2px;
    padding: 16px 10px 16px 22px;
    border-radius: 25px;
    transition: all 0.4s;
    font-size: 18px;
}
.btn-1 span{
    display: inline-block;
    transform: rotate(-45deg) translateX(0px);
    font-size: 17px;
}
.btn-1 .arrow1 {
    transition: all 0.4s;
    opacity: 1;
}
.btn-1 .arrow2 {
    transform: translateY(-8px) rotate(-45deg) translateX(-52px);
    transition: all 0.4s;
    opacity: 0;
}
.btn-1:hover .arrow1 {
    transition: all 0.4s;
    transform: translateY(-7px) rotate(-45deg) translateX(45px);
    opacity: 0;
}
.btn-1:hover .arrow2 {
    transform: translateY(-15px) rotate(-45deg) translateX(-21px);
    transition: all 0.4s;
    opacity: 1;
}
</style>