<script setup>
import UpdatePasswordForm from './Partials/UpdatePasswordForm.vue';
import UpdateProfileInformationForm from './Partials/UpdateProfileInformationForm.vue';
import { Head } from '@inertiajs/vue3';

defineProps({
    mustVerifyEmail: {
        type: Boolean,
    },
    status: {
        type: String,
    },
});
</script>

<template>
    <Head title="Личный кабинет" />
        <div class="sm:flex py-12 lk-background">
            <div class="max-w-7xl mx-auto sm:px-6 lg:px-8 space-y-6">
                <div class="p-4 sm:p-8">
                    <UpdateProfileInformationForm
                        :must-verify-email="mustVerifyEmail"
                        :status="status"
                        class="max-w-xl"
                    />
                </div>

                <div class="p-4 sm:p-8">
                    <UpdatePasswordForm class="max-w-xl" />
                </div>
            </div>
        </div>
</template>
<style>
.lk-background {
    background-color: var(--black);
}
.border-block {
    border: 1px solid var(--gray);
    border-radius: 10px;
    padding: 24px;
}
</style>