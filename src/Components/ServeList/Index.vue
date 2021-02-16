<template>
    <div class="container">
        <ServerButton isHome /> 

        <div class="separator"></div>

        <ServerButton :mentions="3"/>
        <ServerButton />
        <ServerButton hasNotification />
        <ServerButton :mentions="36" hasNotification />
        <ServerButton />
        <ServerButton />
        <ServerButton  :mentions="41" hasNotification/>

    </div>
</template>
<script>

import ServerButton from "./ServerButton"

export default {
    components: {ServerButton}
}
</script>
<style scoped lang="scss">
    .container {
        grid-area: SL;
        display: flex;
        flex-direction: column;
        align-items: center;
        background-color: var(--tertiary);

        padding: 11px 0;
        max-height: 100vh;
        transition: .2s;
    }

    .separador {
        width: 32px;
        border-bottom: solid 2px var(--quartenary);
        margin-bottom: 8px;
    }
</style>