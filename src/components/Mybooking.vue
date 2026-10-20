<script>
export default {

    props: ['booking', 'mao'],

    data() {
        return {


        }
    },
    methods: {
        navi(page) {
            this.$emit('goTo', page)
        },

        deleteBtn(a) {
            this.booking.splice(a, 1);



        }

    },
}
</script>

<template>

    <div class=" w-full h-screen flex justify-center items-center">

        <div class="flex flex-col h-150 w-200 relative px-10 py-5 bg-zinc-100 drop-shadow-lg gap-5">

            <div class="text-center">
                <h1 class="text-[35px] font-bold">My Booking</h1>
            </div>

            <div v-for="(i, index) in booking"
                class="h-35 w-full bg-zinc-200 flex justify-center gap-2 items-center rounded-md">

                <div v-for="a in mao" class="text-sm font-sans">
                    {{ a }}
                </div>

                <div class="grid grid-cols-2">
                    <div class="gap-5 flex justify-center items-center  w-full px-5">

                        <div class="flex  items-center gap-5">
                            <img :src="i.img" alt="" class="w-35">
                            <h3 class="font-semibold text-md text-black">{{ i.name }}</h3>
                        </div>


                    </div>
                </div>

                <button @click="deleteBtn(index)"
                    class="px-5 py-3  cursor-pointer rounded-xl mx-6 hover:scale-105 duration-100 bg-red-500">Delete</button>

            </div>

        </div>
    </div>
</template>