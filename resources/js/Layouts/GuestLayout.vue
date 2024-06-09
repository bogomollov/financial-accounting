<script setup>
</script>

<template>
    <div class="min-h-screen flex sm:justify-center items-center pt-6 sm:pt-0 guestlayout">
        <div
            class="w-full sm:max-w-md mt-6 overflow-hidden guestlayout-border"
        >
            <slot />
        </div>
    </div>
</template>
<style>
.guestlayout {
    background-color: var(--black);
    border-width: 0px;
}
.guestlayout-border {
    border: 1px solid var(--gray);
    border-radius: 10px;
    padding: 24px;
}
</style>