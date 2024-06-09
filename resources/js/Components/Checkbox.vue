<script setup>
import { computed } from 'vue';

const emit = defineEmits(['update:checked']);

const props = defineProps({
    checked: {
        type: [Array, Boolean],
        required: true,
    },
    value: {
        default: null,
    },
});

const proxyChecked = computed({
    get() {
        return props.checked;
    },

    set(val) {
        emit('update:checked', val);
    },
});
</script>

<template>
    <input
        type="checkbox"
        :value="value"
        v-model="proxyChecked"
        class="hidden-checkbox"
    />
    <div class="checkbox">
        <svg class="checkmark" xmlns="http://www.w3.org/2000/svg" width="12" height="12" viewBox="0 0 24 24"><path fill="#101010" d="M20.285 2l-11.285 11.567-5.286-5.011-3.714 3.716 9 8.728 15-15.285z"/></svg>
    </div>
</template>
<style>
    input[type="checkbox"] {
        height: auto;
        position: absolute;
        -webkit-appearance: none;
        -moz-appearance: none;
        appearance: none;
    }
    .checkbox {
        position: relative;
        width: 17px;
        height: 17px;
        border-radius: 5px;
        background: var(--white);
    }
    .checkmark {
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        height: auto;
        display: none;
    }
    .label-checkbox input:checked ~ .checkbox .checkmark{
        display: block;
    }
</style>