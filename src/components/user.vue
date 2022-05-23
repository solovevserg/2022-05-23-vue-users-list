<template>
    <div>
        <span v-if="user.verified">⭐</span>
        {{ user.name }} ({{ user.age }} y.o.)
    </div>
</template>

<script>
export default {
    props: ['user'],
}
</script>