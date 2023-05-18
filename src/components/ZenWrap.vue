<template>
    <div class="boxs">
        <slot></slot>
    </div>
</template>

<style scoped>
    .boxs {
        display: flex;
        display: -webkit-box;
        display: -moz-flex;
        display: -webkit-flex;
    }

    :deep(.box) {
        flex-basis: 0;
        -webkit-box-flex: 1;
        flex-grow: 1;
        flex-shrink: 1;
        padding: .75rem;
        text-align: center;
    }
</style>