<script setup>

const messages = [
    {
        id: "1",
        content: "hello world",
        position: "left",
        time: "09:15"
    },
    {
        id: "2",
        content: "hello world",
        position: "right",
        time: "09:15"
    },
    {
        id: "3",
        content: "hello world",
        position: "right",
        time: "09:15"
    }
]
</script>

<template>
    <div class="container">
        <div class="header">
            <p>Ellie</p>
        </div>
    
        <div class="chat">
            <ChatBubble v-for="message in messages" :key="message.id" :text="message.content" :time="message.time" />
        </div>
        
        <div class="footer">
            <Button label="send" />
        </div>
    </div>
</template>

<style lang="scss" scoped>
.container {
    height: var(--body-height);
    width: 100%;
    display: grid;
    grid-template-rows: 44px minmax(auto, 1fr) 64px;
}

.chat {
    overflow-y: auto;
    padding: 16px;
    display: flex;
    flex-direction: column-reverse;

    & > * + * {
        margin-bottom: 12px;
    }
}
</style>
