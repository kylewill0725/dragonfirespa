<template>
    <div ref="list" >
        <slot />
    </div>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    name: 'ScrollableList'
})
</script>
<style scoped>
    @media(orientation: landscape) {
        .list {
            justify-content: center;
            flex-wrap: wrap;
            overflow-x: auto;
        }
    }
    
    @media(orientation: portrait) {
        .list {
            overflow-y: auto;
        }
    }

    .list {
        flex-grow: 1;
        display: flex;
        flex-direction: column;
        touch-action: manipulation;
    }
</style>
