<template>
    <div class="footer-container">
        <div class="contacts">
            <a href="mailto:lukaszdyszy0192@gmail.com" target="blank"><i class="far fa-envelope"></i> lukaszdyszy0192@gmail.com</a>
            <br>
            <a href="tel:517989464"><i class="fas fa-phone-alt"></i> 517 989 464 </a>
        </div>
        <div class="copywright">
            &copy; Łukasz Dyszy 2020.
        </div>
    </div>
</template>

<script>
export default {
    name: 'Footer'
}
</script>

<style>

.footer-container{
    background-color: rgb(26, 26, 26);
    color: rgb(197, 197, 197);
    text-align: center;
    border-top: 2px solid black;
}

.contacts{
    padding: 15px 0;
    line-height: 200%;
}
.copywright{
    padding: 10px 0 35px 0;
    font-weight: 600;
    font-size: 1.1rem;
}

</style>