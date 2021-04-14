<template>
    <div class="flex items-center justify-center flex-col h-screen bg-gray-100">
        <h1 class="text-6xl font-bold">A <span class="animate-pulse" style="color: #B47AEA">fine</span> selection of beers.</h1>
        <div>
            <a href="https://github.com/kobito-kun/VueJS/tree/master/a-project"><button class="font-bold text-white text-2xl bg-blue-500 m-4 py-4 duration-300 px-8 rounded-lg transform hover:scale-110" style="min-width:150px">GitHub</button></a>
            <a href="https://kobi.lol"><button class="font-bold text-white text-2xl bg-blue-500 m-4 py-4 px-8 rounded-lg transform hover:scale-110 duration-300" style="min-width:150px;">Kobi</button></a>
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