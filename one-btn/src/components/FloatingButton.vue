<template>
    <div class="floating-button">

    </div>
</template>

<script>
export default {

}
</script>

<style>
.floating-button{
    position: relative;
    display: flex;
    width: 40px;
    height: 40px;
   background-image: linear-gradient(45deg, #52ffaf, #2196f3);
   box-shadow: 0 1px 2px 1px #52ffafa3;
   border-radius: 100%;
}
.floating-button::after,.floating-button::before{
    position: absolute;
    content: '';
    left: 50%;
    top: 0;
    display: block;
    background-color: white;
    width: 18px;
    margin-left: -9px;
    border-radius: 3px;
    height: 3px;
    transition: all 0.2s ease;

}.floating-button::before{
    transform: translateY(12px);
    filter: drop-shadow(0 6px 0 white);
}
.floating-button::after{
    transform: translateY(24px);
}
.floating-button:active::before{
    filter: none;
    transform: translateY(18px) rotate(-45deg)
}
.floating-button:active::after{
    transform: translateY(18px) rotate(45deg)
}
</style>
