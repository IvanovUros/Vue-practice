<template>
    <div>
        <h2>
            Hello {{ name }} a.k.a {{ heroName }}
        </h2>
    </div>
</template>

<script>
    export default {
        name: 'GreetTest',
        props: ['name', 'heroName'],
    }
</script>

<style scoped>

</style>