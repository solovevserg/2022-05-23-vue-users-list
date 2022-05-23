<template>
    <div>
        {{ user.name }} ({{ user.age }} y.o.)
    </div>
</template>

<script>
export default {
    props: ['user'],
}
</script>