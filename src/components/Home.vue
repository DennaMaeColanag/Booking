<script>
export default {
    data() {
        return {

        }
    },
    methods: {
        
    },
}


</script>

<template>

    <!-- Hero Section -->
    <section id="home"
        class="relative min-h-screen flex items-center justify-center gradient-bg overflow-hidden bg-slate-600">
        <div class="absolute inset-0">
            <div
                class="absolute top-1/4 left-1/4 w-72 h-72 bg-indigo-300 rounded-full mix-blend-multiply filter blur-xl opacity-70 animate-float">
            </div>
            <div class="absolute top-3/4 right-1/4 w-72 h-72 bg-purple-300 rounded-full mix-blend-multiply filter blur-xl opacity-70 animate-float"
                style="animation-delay: 2s;"></div>
        </div>

        <div class="relative z-10 text-center px-4 sm:px-6 lg:px-8">
            <div class="animate-fadeInUp">
                <h1 class="text-4xl sm:text-6xl lg:text-7xl font-bold text-white mb-6">
                    Transform Your Body,
                    <span class="block bg-purple-200 bg-clip-text text-transparent">
                        Elevate Your Life!
                    </span>
                </h1>
                <p class="text-xl sm:text-2xl text-indigo-100 mb-8 max-w-3xl mx-auto">
                    Welcome to Curls n' Crunches! We believe that fitness is about more than just looking good—it is
                    about
                    celebrating what your body can achieve and clearing your mind.
                </p>
                <div class="flex flex-col sm:flex-row gap-4 justify-center">
                    <button 
                        class="bg-white text-indigo-600 px-8 py-4 rounded-lg font-semibold hover:bg-indigo-50 transform hover:scale-105 transition-all duration-300 shadow-lg flex items-center justify-center cursor-pointer">

                        Get Started
                    </button>
                    <button
                        class="glass-effect border text-white px-8 py-4 rounded-lg font-semibold hover:bg-white/20  hover:font-bold transform hover:scale-105 transition-all duration-300 flex items-center justify-center cursor-pointer">
                        Learn More
                    </button>
                </div>
            </div>
        </div>
    </section>

</template>