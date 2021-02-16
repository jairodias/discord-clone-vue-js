<template>
    <div class="container">
        <div class="profile">
            <div class="avatar"></div>
            <div class="user-data">
                <strong>Jairo Dias</strong>
                <span>#2654</span>
            </div>
        </div>
        <div class="actions">
                <Microphone :size="20" />
                <HeadPhones :size="20" />
                <Settings :size="20" />
            </div>
    </div>
</template>

<script>
import Microphone from "vue-material-design-icons/Microphone";
import HeadPhones from "vue-material-design-icons/Headphones";
import Settings from "vue-material-design-icons/CogOutline";

export default {
    components: {
        Microphone,
        HeadPhones,
        Settings
    }
}
</script>

<style lang="scss" scoped>
    .container {
        grid-area: UI;
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
        padding: 10px;
        background-color: var(--quaternary);
        box-shadow: rgba(0,0,0,.2) 0 1px 0 0;

        .profile {
            display: flex;
            align-items: ceil($number: 0);
        }

        .avatar {
            width: 32px;
            height: 32px;
            border-radius: 50%;
            background-color: var(--gray);
        }

        .user-data {
            display: flex;
            flex-direction: column;
            font-size: 13px;
            margin-left: 8px;

            strong {
                display: block;
                color: var(--white);
            }

            span {
                color: var(--gray)
            }
        }

        .actions {
            color: var(--gray);

            span {
                cursor: pointer;
                transition: .2s;

                &:hover {
                    color: var(--white);
                }
            }
        }
    }
</style>