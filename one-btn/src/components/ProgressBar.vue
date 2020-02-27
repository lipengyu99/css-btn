<template>
    <div class="progress-bar">
        
    </div>
</template>

<script>
export default {

}
</script>

<style>
.progress-bar{
    position: relative;
    display: flex;
    width: 60px;
    height: 20px;
    border-radius: 8px;
    background-color: #eee;
    transform: translateY(-34%);
}
.progress-bar::before{
    position: absolute;
    content: '';
    z-index: 1;
    display: block;
    height: 20px;
    width: 50%;
    background-image: linear-gradient(0deg, #ff7a3b, #ffc107);
    border-radius: 8px;
    filter: drop-shadow(2px 0 1px rgba(0,0,0,0.2));
    transition: all 0.2s ease;
    box-shadow: 0 1px 2px 0 #ff7a3ba3;
}
.progress-bar::after{
    position: absolute;
    content: '50%';
    font-size: 12px;
    font-weight: bold;
    transform: scale(0.9) translate-(50%,20%);
}
.progress-bar:active::before{
    width: 100%;
}
.progress-bar:active::after{
    content: '100%';
}
</style>
