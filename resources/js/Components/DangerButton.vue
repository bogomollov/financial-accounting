<template>
    <button
        class="inline-flex items-center px-4 py-2 border border-transparent button-danger"
    >
        <slot />
    </button>
</template>
<style>
.button-danger {
    padding: 6px 12px;
    border-radius: 5px;
    font-size: var(--p);
    color: var(--white);
    font-weight: 500;
    background-color: var(--red);
    width: fit-content;
}
</style>
