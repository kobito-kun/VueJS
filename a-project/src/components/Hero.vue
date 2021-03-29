<template>
    <div class="flex items-center justify-center hero-height bg-gray-100">
        <h1 class="text-4xl font-bold">A <span class="text-blue-500">fine</span> selection of beers.</h1>
    </div>
</template>

<script>
export default {
    name: 'Hero',
    data: () => {
        return {
            opened: false,
        }
    }
}
</script>

<style scoped>
.hero-height{
    min-height: 400px;
}
</style>