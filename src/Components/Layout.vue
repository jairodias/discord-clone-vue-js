<template>
    <div id="grid">
        <ServeList />
        <ServerName />
        <ChannelList />
        <UserInfo />
    </div>
</template>

<script>

import ServeList from "./ServeList/Index.vue";
import ServerName from "./ServerName/Index.vue";
import ChannelList from "./ChannelList/Index.vue";
import UserInfo from "./UserInfo/Index.vue";

export default {
  components: { ServeList, ServerName, ChannelList, UserInfo }
}
</script>

<style scoped>
    #grid {
        display: grid;
        height: 100vh;
        grid-template-columns: 71px 240px auto 240px;
        grid-template-rows: 46px auto 52px;
        grid-template-areas: 
            "SL SN CI CI"
            "SL CL CD UL"
            "SL UI CD UL"
        ;
    }
</style>
