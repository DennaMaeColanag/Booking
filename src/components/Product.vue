<script>

export default {
    emits:['send-services'],
    data() {
        return {

            services: [
                {
                    id: 1,
                    img: "blob:https://gemini.google.com/51a89b5d-602f-40f8-9b70-a4763058be47",
                    name: "Cardiorespiratory Endurance",
                    details: " The ability of your heart and lungs to fuel your body with oxygen during sustained physical activity (e.g., running, cycling).",

                },

                {
                    id: 2,
                    img: "https://levelsprotein.com/cdn/shop/articles/Sandbag-exercises.jpg?v=1604343144&width=2048",
                    name: "Muscular Strength & Endurance",
                    details: " The ability of your muscles to perform continuous, repetitive contractions without getting tired",

                },

                {
                    id: 3,
                    img: "https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRJ8VZ3JsZo1CNQmdaD5qdiQrY9lH7JKdbBq8bGnGtX1PB9aqUlor9MV8c&s=10",
                    name: "Bone and Muscle Longevity",
                    details: "Strengthens bones (increasing density to prevent osteoporosis) and preserves vital muscle mass as you age.",

                },

                {
                    id: 4,
                    img: "https://www.ewmotiontherapy.com/hubfs/Flexibility%20science.png",
                    name: "Flexibility",
                    details: "The range of motion available at your joints, which allows for smooth, unrestricted movement (e.g., stretching, bending).",

                },

                {
                    id: 5,
                    img: "https://health.ucdavis.edu/media-resources/contenthub/health-news/2023/07/thumbnail/woman-stretching-waking-th.jpg",
                    name: "Mood Enhancement",
                    details: " Helps you fall asleep faster, deepens sleep cycles, and leaves you feeling more rested in the morning.",

                },

                {
                    id: 6,
                    img: "https://www.wellnessfamilydentistry.com/thedentalsitecontent/1002158/blog/medium_12-simple-ways-to-increase-your-energy-and-mobility.jpg",
                    name: "Increased Daily Energy",
                    details: "Enhances your stamina and efficiency of the cardiovascular system, leaving you with more energy to tackle your daily tasks.",

                },

            ]

        }
    },
    methods: {
        getStarted(index) {
            this.$emit('send-services', this.services[index]);
            // console.log(this.services[index])
        },
        

    },
}

</script>

<template>

    <section class="py-10" id="services">

        <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">Our Services</h2>

        <div class="grid grid-cols-3 gap-8 container mx-auto px-4">

            <div v-for="(service, index) in services" :key="service.id" class="">
                <div
                    class="bg-slate-100 rounded-lg shadow-md overflow-hidden hover:scale-103 transition duration-300 cursor-pointer">

                    <img :src="service.img" alt=""
                        class="w-full h-64 object-cover hover:scale-103 transition duration-300">

                    <div class="p-6 text-center">

                        <h3 class="text-xl font-medium text-gray-800 mb-2">{{ service.name }}</h3>
                        <p class="text-gray-700 text-base">{{ service.details }}</p>
                    </div>

                    <div class="flex justify-center items-center mb-5 ">
                        <button @click="getStarted(index)" class="px-5 py-3 bg-slate-500 rounded-lg hover:scale-103 transition duration-300 cursor-pointer">Get
                            Started!</button>
                    </div>
                </div>
            </div>

        </div>
    </section>
</template>