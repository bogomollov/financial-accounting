<template>
    <button
        class="inline-flex items-center border-transparent focus:outline-none primarybutton"
    >
        <slot />
    </button>
</template>
<style>
    .primarybutton {
        padding: 6px 12px;
        border-radius: 5px;
        font-size: var(--p);
        font-weight: 500;
    }
</style>
