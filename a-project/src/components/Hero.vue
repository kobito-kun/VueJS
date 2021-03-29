<template>
    <div class="flex items-center justify-center flex-col hero-height bg-gray-100">
        <h1 class="text-4xl font-bold">A <span class="text-blue-500">fine</span> selection of beers.</h1>
        <div>
            <a href=""><button class="font-bold text-white bg-blue-500 m-4 py-2 px-4 rounded-lg" style="min-width:100px">GitHub</button></a>
            <a href=""><button class="font-bold text-white bg-blue-500 m-4 py-2 px-4 rounded-lg" style="min-width:100px;">Kobi</button></a>
        </div>
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