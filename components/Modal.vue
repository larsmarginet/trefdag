<script setup>
defineProps({
    title: String,
    headerSrc: String
})
</script>

<template>
    <div class="modal">
        <div class="modal__inner">
            <img class="modal__close" src="~/assets/icons/close.svg" />

            <div v-if="headerSrc" class="modal__header">
                <img :src="headerSrc" class="modal__header-img" />
            </div>
            
            <div class="modal__content">
                <p class="modal__title">{{ title }}</p>

                <div class="modal__description">
                    <slot name="content"></slot> 
                </div>

                <div class="modal__actions">
                    <slot name="actions"></slot> 
                </div>
            </div>
        </div>
    </div>
</template>

<style lang="scss" scoped>
.modal {
    position: absolute;
    z-index: 99;
    width: var(--body-width);
    height: var(--body-height);
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgba(0, 0, 0, 0.2);
}

.modal__inner {
    position: relative;
    z-index: 100;
    margin: 16px;
    background-color: white;
    width: 100%;    
}

.modal__header {
    height: 100px;
    width: 100%;
    overflow: hidden;

    img {
        width: 100%;
        object-fit: cover;
        object-size: center;
    }
}

.modal__content {
    padding: 30px;
}

.modal__title {
    font-family: var(--flanders-art-sans-medium);
    margin: 0 0 16px 0;
}

.modal__description {
    margin: 0 0 16px 0;
}

.modal__close {
    position: absolute;
    right: 16px;
    top: 16px;
}
</style>