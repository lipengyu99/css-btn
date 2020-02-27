<template>
    <div class="landmark">

    </div>
</template>

<script>
export default {

}
</script>

<style>
@keyframes jump {
    0%{
        transform: translateY(0px)
    }
    50%{
        transform: translateY(-10px)
    }
    100%{
        transform: translateY(0px)
    }
}
.landmark{
    position: relative;
    display: block;
    width: 30px;
    height: 30px;
    border-radius: 100%;
    background-image: linear-gradient(0deg,red,#f8f484);
    filter: drop-shadow(0 2px 2px #973340a3);
    animation: jump infinite 2s ease;
}
.landmark::before{
    position: absolute;
    content: '';
    bottom: 0;
    left: 50%;
    z-index: -2;
    width: 10px;
    height: 10px;
    background-image: linear-gradient(-45deg,red,rgb(243,29,30));
    
    margin-left: -5px;
    transform: scale(1.3) translateY(2px) rotate(45deg)
}
.landmark::after{
    position: absolute;
    content: '';
    top: 50%;
    left: 50%;
    display: block;
    background-color: white;
    width: 10px;
    height: 10px;
    border-radius: 100%;
    margin-left: -5px;
    margin-top: -5px;
    box-shadow: inset 0 1px 1px rgba(0, 0, 0, 0.4)
}
</style>
