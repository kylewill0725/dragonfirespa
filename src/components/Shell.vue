<template>
    <p>{{msg}}</p>
</template>
<script lang="ts">
import Vue from 'vue'
export default Vue.extend({
    name: 'Shell',
    props: {
        msg: String
    }
})
</script>
