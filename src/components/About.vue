<script>
export default {
    data() {
        return {

        }
    },
    methods: {
        navi(page) {
            this.$emit('goTo', page)
        }
    },
}

</script>

<template>

    <section class="bg-gray-100" id="aboutus">
        <div class="container mx-auto py-16 px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 items-center gap-8">
                <div class="max-w-lg">
                    <h2 class="text-3xl font-bold text-gray-800 mb-8 text-center">About Us</h2>
                    <p class="mt-4 text-gray-600 text-lg">
                        If you are looking for a specific corporate entity, Curls n' Crunches, LLC is a major regional
                        fitness club operator in the United States that primarily operates under the Onelife Fitness
                        brand. Headquartered in McLean, Virginia, the company manages dozens of multi-purpose health
                        clubs across the Mid-Atlantic and Southeast regions, offering extensive gym amenities, personal
                        training, and group exercise classes.
                    </p>
                </div>
                <div class="mt-12 md:mt-0">
                    <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR0yoGjVQ0-BsW13tu6PwfJhdEX7-upr_cRL7Egj0tdvyp2eFJ-9ZO5Ed9-&s=10"
                        alt="About Us Image" class="object-cover rounded-lg shadow-md">
                </div>
            </div>
        </div>
    </section>

    <section class="text-gray-700 body-font mt-10">
        <div class="flex justify-center text-3xl font-bold text-gray-800 text-center">
            Why Us?
        </div>
        <div class="container px-5 py-12 mx-auto">
            <div class="flex flex-wrap text-center justify-center">
                <div class="p-4 md:w-1/4 sm:w-1/2">
                    <div class="px-4 py-6 transform transition duration-500 hover:scale-110">
                        <div class="flex justify-center">
                            <img src="https://cdn-icons-png.flaticon.com/512/69/69966.png" class="w-32 mb-3">
                        </div>
                        <h2 class="title-font font-regular text-2xl text-gray-900">State-of-the-Art Facilities</h2>
                    </div>
                </div>

                <div class="p-4 md:w-1/4 sm:w-1/2">
                    <div class="px-4 py-6 transform transition duration-500 hover:scale-110">
                        <div class="flex justify-center">
                            <img src="https://png.pngtree.com/png-clipart/20250814/original/pngtree-personal-trainer-and-fitness-logo-png-image_21732993.png"
                                class="w-32 mb-3">
                        </div>
                        <h2 class="title-font font-regular text-2xl text-gray-900">Expert & Certified Instructors</h2>
                    </div>
                </div>

                <div class="p-4 md:w-1/4 sm:w-1/2">
                    <div class="px-4 py-6 transform transition duration-500 hover:scale-110">
                        <div class="flex justify-center">
                            <img src="https://image3.jdomni.in/banner/13062021/16/7E/7E/5A9920439E52EF309F27B43EEB_1623568010437.png?output-format=webp"
                                class="w-32 mb-3">
                        </div>
                        <h2 class="title-font font-regular text-2xl text-gray-900">Flexible 24/7 Access / Extended Hours
                        </h2>
                    </div>
                </div>

                <div class="p-4 md:w-1/4 sm:w-1/2">
                    <div class="px-4 py-6 transform transition duration-500 hover:scale-110">
                        <div class="flex justify-center">
                            <img src="https://png.pngtree.com/png-vector/20250513/ourmid/pngtree-keep-clean-sign-vector-png-image_16239790.png"
                                class="w-32 mb-3">
                        </div>
                        <h2 class="title-font font-regular text-2xl text-gray-900">Clean & Safe Environment</h2>
                    </div>
                </div>

            </div>
        </div>
    </section>

</template>