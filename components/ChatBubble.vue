<script setup>
defineProps({
    text: String,
    time: String
})
</script>

<template>
<div class='chat-bubble'> 
    <p class="chat-bubble__text">{{ text }}</p>

    <span class="chat-bubble__time">{{ time }}</span>
</div>
</template>

<style lang='scss' scoped>
.chat-bubble {
    flex: 0 1 auto;
    align-self: flex-start;
    display: flex;
    flex-direction: column;
    border-radius: 8px;
    padding: 8px;
    background-color: #F7F9FC;
    min-width: 140px;
}

.chat-bubble__text {
    margin: 0 4px;
    font-size: 16px;
}

.chat-bubble__time {
    font-size: 12px;
    align-self: flex-end;
    color: #505050;
}

.chat-bubble--answer {

}
</style>