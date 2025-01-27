<template>
<footer>
    <div class="container">
        <div class="row align-items-center justify-content-center">
            <div class="col-lg-6">
            <div class="footer-logo">
                <img src="../assets/images/footer-logo.png" alt="" class="img-fluid">
               
            </div>
        </div>
        <div class="col-lg-6">
            <div class="fotter-midia">
                <ul>
                    <li><a href="#"><i class="fa-brands fa-facebook"></i></a></li>
                    <li><a href="#"><i class="fa-brands fa-twitter"></i></a></li>
                    <li><a href="#"><i class="fa-brands fa-youtube"></i></a></li>
                </ul>
            </div>
        </div>
        </div>
      
       
    </div>
</footer>




</template>

<script>



</script>
<style scoped>
.fotter-midia ul{
    list-style: none;
    display:flex;
    justify-content:center;
    padding-left: 0;
    margin-bottom: 0;
    align-items: center;
}
.fotter-midia ul li a{
    margin: 0 10px;
}
.fotter-midia ul li a i{
    color: var(--light-yellow);
}
footer {
    background-color: var(--main_black);
    padding: 18px 0;
}
</style>