<template>
    <div class="footer-container">
        <div class="contacts">
            <i class="far fa-envelope"></i> johndoe@gmail.com
            <br>
            <i class="fas fa-phone-alt"></i> 111 222 333
        </div>
        <div class="copywright">
            &copy; John Doe 2019
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
    line-height: 150%;
}
.copywright{
    padding: 10px 0 35px 0;
    font-weight: 600;
    font-size: 1.1rem;
}

</style>