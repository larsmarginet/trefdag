<script setup>
defineProps({
    label: String
})
</script>

<template>
    <button class="button">{{ label }}</button>
</template>

<styles lang="scss">
.button {
    background-color: #0055CC;
    border: none;
    outline: none;
    color: white;
    font-size: 16px;
    padding: 10px 30px;
    border-radius: 3px;
    font-family: var(--flanders-art-sans-medium);
    cursor: pointer; 
    transition: background-color 250ms ease-in-out;

    &:hover {
        background-color: #00429D;
    }
}
</styles>