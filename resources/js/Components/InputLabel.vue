<script setup>
defineProps({
    value: {
        type: String,
    },
});
</script>

<template>
    <label class="block">
        <span v-if="value">{{ value }}</span>
        <span v-else><slot /></span>
    </label>
</template>
<style>
label {
    color: var(--white);
    font-size: var(--p);
    margin-bottom: 10px;
}
</style>