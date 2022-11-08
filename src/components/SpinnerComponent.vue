<template>
    <div class="spinner"></div>
</template>
<style>
.spinner {
    width: 40px;
    height: 40px;
    margin: 0 auto;
    border-radius: 100%;
    background-color: var(--neonGreen);
    -webkit-animation: sk-scaleout 1.0s infinite ease-in-out;
    animation: sk-scaleout 1.0s infinite ease-in-out;
}

@-webkit-keyframes sk-scaleout {
    0% {
        -webkit-transform: scale(0);
    }

    100% {
        opacity: 0;
        -webkit-transform: scale(1.0);
    }
}

@keyframes sk-scaleout {
    0% {
        -webkit-transform: scale(0);
        transform: scale(0);
    }

    100% {
        opacity: 0;
        -webkit-transform: scale(1.0);
        transform: scale(1.0);
    }
}
</style>