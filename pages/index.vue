<script setup>
const router = useRouter();

const goToChat = () => {
    router.push({ path: "/chat" });
}
</script>

<template>
    <div class="home">
        <Modal title="Hi, ik ben Ellie" header-src="/ellie.jpg">
            <template #content>
                <p>Kan ik je helpen met activiteiten ontdekken?</p>
            </template>

            <template #actions> 
                <Button @click="goToChat" label="Ja, ik wil chatten" />
            </template>
        </Modal>
    </div>
</template>

<style lang="scss" scoped>
.home {
    background-image: url("/assets/images/burgerprofiel-ui.jpg");
    background-size: cover;
    background-position: center;
    width: var(--body-width);
    height: var(--body-height);
}

.home__avatar {
    margin-bottom: 16px;
}
</style>