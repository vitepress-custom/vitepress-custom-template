<script setup lang="ts">
import VPLayout from './Layout.vue';
import Home from './components/home.vue';
import iconSearch from './components/icons/iconSearch.vue';
</script>
<template>
    <VPLayout>
        <template #nav-bar-content-before>
            <div class="search-box">
                <iconSearch class="icon" />
                <div class="placeholder">搜索</div>
            </div>
        </template>
        <template #custom-home>
            <Home></Home>
        </template>
    </VPLayout>
</template>
<style lang="scss">
.search-box {
    border-radius: 100px;
    display: block;
    width: 120px;
    height: 28px;
    flex-shrink: 0;
    border: 1px solid var(--vp-c-divider);
    background-color: var(--vp-c-bg-mute);
    padding: 0 12px;
    box-sizing: border-box;
    cursor: pointer;
    display: flex;
    flex-flow: row nowrap;
    align-items: center;
    margin-right: 30px;
    transition: border-color 0.25s, background-color 0.25s;

    &:hover {
        border-color: var(--vp-c-gray);
    }

    .icon {
        width: 14px;
        height: 14px;
        color: var(--vp-c-text-1);
    }

    .placeholder {
        font-size: 12px;
        color: var(--vp-c-text-1);
        margin-left: 6px;
    }
}
</style>