<template>
    <div class="modal-view">
        <div class="modal-view__contents">
            <slot></slot>
        </div>
    </div>
</template>
<style scoped>
.modal-view {
    background: rgba(0, 0, 0, 0.5);
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    display: flex;
    align-items: center;
    justify-content: center;
}
.modal-view__contents {
    background: #fff;
    border-radius: 5px;
}
</style>