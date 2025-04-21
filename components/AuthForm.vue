<template>
    <div class="px-4 mt-8 sm:mx-auto sm:w-full sm:max-w-md sm:px-0">
        <div class="px-4 py-8 bg-white shadow sm:rounded-lg sm:px-10">
            <form action="" class="space-y-6">
                <!-- Input -->
                 <Input 
                 v-if="variant === 'REGISTER'"
                 :disabled="isLoading" required id="name" label="Name" name="name" v-model="name" type="text"/>
                 <!-- Input Email -->
                 <Input :disabled="isLoading" required id="email" label="Email" name="email" v-model="email" type="email"/>
                <!-- Input Password -->
                <Input :disabled="isLoading" required id="password" label="Password" name="password" v-model="password" type="password"/>
                <!-- Button submit -->
                 <Button :disabled="isLoading" fullWidth type="submit">
                    {{ variant === 'LOGIN' ? 'Sign In' : 'Register' }}
                 </Button>
            </form>
        </div>
    </div>
</template>

<script setup lang="ts">
const isLoading = ref<boolean>(false);
const name = ref<string>("");
const email = ref<string>("");
const password = ref<string>("");

type VARIANT = 'LOGIN' | 'REGISTER';
const variant = ref<VARIANT>('LOGIN');
</script>

<style scoped>

</style>