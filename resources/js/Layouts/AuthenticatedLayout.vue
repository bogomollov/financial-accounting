<script setup>
import { ref } from 'vue';
import Dropdown from '@/Components/Dropdown.vue';
import DropdownLink from '@/Components/DropdownLink.vue';

const showingNavigationDropdown = ref(false);
</script>

<template>
    <div class="sm:flex sm:items-center username-burger-menu">
        <div class="relative">
            <Dropdown align="right" width="48">
                <template #trigger>
                    <span class="inline-flex">
                        <button type="button"
                            class="inline-flex items-center transition ease-in-out duration-150 button-lk">
                            {{ $page.props.auth.user.name }}

                            <svg class="ms-2 -me-0.5 h-4 w-4" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20"
                                fill="currentColor">
                                <path fill-rule="evenodd"
                                    d="M5.293 7.293a1 1 0 011.414 0L10 10.586l3.293-3.293a1 1 0 111.414 1.414l-4 4a1 1 0 01-1.414 0l-4-4a1 1 0 010-1.414z"
                                    clip-rule="evenodd" />
                            </svg>
                        </button>
                    </span>
                </template>

                <template #content>
                    <DropdownLink :href="route('profile.edit')" class="account-button">Личный кабинет</DropdownLink>
                    <DropdownLink :href="route('logout')" method="post" class="exit-button">
                        Выйти
                    </DropdownLink>
                </template>
            </Dropdown>
        </div>
    </div>
</template>
<style>
    .button-lk {
        background-color: transparent;
        color: var(--white);
        font-size: 18px;
        border: none;
    }
    .account-button, .exit-button {
        text-decoration: none;
        color: var(--white);
        font-size: var(--p);
    }
</style>