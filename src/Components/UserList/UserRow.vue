<template>
    <div class="user-row">
        <div class="avatar" :class="{'bot-avatar': isBot }">
            <div class="online" v-if="online"></div>
            <div class="offline" v-else></div>
        </div>
        <strong>{{ nickname }}</strong>
        <div class="bot" v-if="isBot">Bot</div>
    </div>
</template>

<script>
export default {
    props: {
        isBot: Boolean,
        nickname: String,
        online: Boolean
    }
}
</script>



<style lang="scss" scoped>
    .user-row {
        display: flex;
        margin-top: 5px;
        padding: 5px;
        align-items: center;
        cursor: pointer;
        border-radius: 5px;
        background: transparent;
        transition: .2s;

        &:hover {
            background: rgba(255,255,255,.1);
        }

        strong {
            margin-left: 13px;
            font-weight: 500;
            color: var(--white);
            opacity: .7;
            white-space: nowrap;
            text-overflow: ellipsis;
        }

        .avatar {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            flex-shrink: 0;
            background-color: var(--primary);
            position: relative;

            &.bot-avatar {
                background-color: var(--mention-detail)
            }

            .online::before {
                content: "";
                width: 9px;
                height: 9px;
                background-color: green;
                position: absolute;

                border-radius: 50%;
                bottom: -5px;
                right: -5px;

                border: 4px solid var(--secondary);
            }

            .offline::before {
                content: "";
                    width: 9px;
                    height: 9px;
                    background-color: red;
                    position: absolute;

                    border-radius: 50%;
                    bottom: -5px;
                    right: -5px;

                    border: 4px solid var(--secondary);
            }
        }

        .bot {
            margin-left: 9px;
            background-color: var(--discord);
            color: var(--white);
            padding: 4px 5px;
            border-radius: 4px;
            text-transform: uppercase;
            font-size: 11px;
            font-weight: bold;
        }
    }
</style>