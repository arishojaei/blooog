<template>
  <div class="loading">
        <div class="lds-ripple">
            <div></div>
            <div></div>
        </div>
  </div>
</template>

<script>
export default {
    name: 'loading'
}
</script>

<style scoped>
.loading {
    width: 100%;
    height: 100vh;
    background: #fff;
    position: fixed;
    top: 0;
    z-index: 99999;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: all 250ms;
}
.lds-ripple {
    display: inline-block;
    position: relative;
    width: 64px;
    height: 64px;
}

.lds-ripple div {
    position: absolute;
    border: 4px solid #000;
    opacity: 1;
    border-radius: 50%;
    animation: lds-ripple 1s cubic-bezier(0, 0.2, 0.8, 1) infinite;
}

.lds-ripple div:nth-child(2) {
    animation-delay: -0.5s;
}

@keyframes lds-ripple {
    0% {
        top: 28px;
        left: 28px;
        width: 0;
        height: 0;
        opacity: 1;
    }

    100% {
        top: -1px;
        left: -1px;
        width: 58px;
        height: 58px;
        opacity: 0;
    }
}
</style>