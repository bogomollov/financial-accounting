<script setup>
import Checkbox from '@/Components/Checkbox.vue';
import GuestLayout from '@/Layouts/GuestLayout.vue';
import InputError from '@/Components/InputError.vue';
import InputLabel from '@/Components/InputLabel.vue';
import PrimaryButton from '@/Components/PrimaryButton.vue';
import TextInput from '@/Components/TextInput.vue';
import { Head, Link, useForm } from '@inertiajs/vue3';

defineProps({
    canResetPassword: {
        type: Boolean,
    },
    status: {
        type: String,
    },
});

const form = useForm({
    name: '',
    password: '',
    remember: false,
});

const submit = () => {
    form.post(route('login'), {
        onFinish: () => form.reset('password'),
    });
};
</script>

<template>
    <GuestLayout>
        <Head title="Авторизация" />

        <form @submit.prevent="submit">
            <div>
                <InputLabel for="name" value="Имя пользователя" />

                <TextInput
                    id="name"
                    type="text"
                    class="mt-1 block w-full"
                    v-model="form.name"
                    required
                    autofocus
                    autocomplete="username"
                />

                <InputError class="mt-2" :message="form.errors.name" />
            </div>

            <div class="mt-5">
                <InputLabel for="password" value="Пароль" />

                <TextInput
                    id="password"
                    type="password"
                    class="mt-1 block w-full"
                    v-model="form.password"
                    required
                    autocomplete="current-password"
                />

                <InputError class="mt-2" :message="form.errors.password" />
            </div>

            <div class="block mt-5">
                <label class="flex items-center label-checkbox">
                    <Checkbox name="remember" v-model:checked="form.remember" />
                    <span class="ms-2">Запомнить меня</span>
                </label>
            </div>

            <div class="flex items-center justify-end mt-5 form-quest">
                <Link
                    :href="route('register')"
                    class="focus:outline-none"
                >
                    Еще нету аккаунта?
                </Link>

                <PrimaryButton class="ms-5" :class="{ 'opacity-25': form.processing }" :disabled="form.processing">
                    Войти в аккаунт
                </PrimaryButton>
            </div>
        </form>
    </GuestLayout>
</template>