<template>
    <span class="divider">
        <div class="vertical">
          <span class="vertical-line"></span>
          <span class="vertical-line"></span>
        </div>
      </span>
</template>
<style>
.divider {
    position: relative;
    display: flex;
    justify-content: center;
    margin: 20px 50px;
    border-top: 1px solid var(--lightCyan);
}

.vertical {
    position: relative;
    top: -12px;
    height: 30px;
    padding: 0 20px;
    background-color: var(--darkGrayisBlue);
}

.vertical-line {
    position: relative;
    margin: 0 3px;
    border-right: 5px solid var(--lightCyan);
    border-radius: 40px;
}
</style>