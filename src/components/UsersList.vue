<template>
    <div class="card">
        <ul class="list">
            <div class="list-item" v-for="user in users" :key="user.id">
                {{ user }}
            </div>
        </ul>
    </div>
</template>

<script>
import { useUsers } from '../use/users';

export default {
    async setup() {
        const { users } = await useUsers();
        return { users };
    },
};
</script>
