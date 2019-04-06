<template>
    <div class="navbar">
        <button class="btn btn-light" @click="minimize">
            <i class="bx bx-minus"></i>
        </button>
        <button class="btn btn-danger" @click="close">
            <i class="bx bx-x"></i>
        </button>
    </div>
</template>

<script>
    export default {
        name: 'navbar',
        methods: {
            minimize() {
                const {remote} = require('electron');
                remote.BrowserWindow.getFocusedWindow().minimize();
            },
            close() {
                const {remote} = require('electron');
                remote.BrowserWindow.getFocusedWindow().close()
            }
        }
    }
</script>

<style lang="scss">
    .navbar {
        display: flex;
        align-items: center;
        justify-content: flex-end;
        padding: 0;
        button {
            font-size: 18px;
            border-radius: 0;
        }
    }
</style>