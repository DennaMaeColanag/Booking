<script>
export default {
    props: ['serviceName'],
    emits: ['send-item', 'close'],
    data() {

        return {
            inputName: '',

        }
    },
    methods: {
        closeModal(b) {
            this.$emit('close', b)
        },

        SubmitSuccessfully() {
            alert('Submit Successfully');

            this.$emit('send-item', this.inputName)
            console.log(this.inputName)
            this.closeModal()
        },

    },
}
</script>


<template>

    <div @click="closeModal(false)" class="fixed inset-0 z-50 flex items-center justify-center bg-black/50 backdrop-blur"></div>

    <div  v-for="i in serviceName" class="fixed inset-0 z-50 flex items-center justify-center bg-black/50">

        <div class="bg-white rounded-2xl shadow-xl w-full max-w-3xl p-8">
            <div class="flex justify-between items-center mb-6">
                <h2 class="text-2xl font-bold">Register</h2>
                <div>
                    {{ i.name }}
                </div>
                <button @click="closeModal(false)" type="button" class="text-2xl font-bold hover:text-red-500">
                    ×
                </button>
            </div>

            <div class="flex flex-col gap-5">
                <div>
                    <label class="block mb-2 font-medium">Name</label>

                    <input v-model="inputName" type="text" class="w-full border rounded-lg px-4 py-3" />
                </div>

                <div>
                    <label class="block mb-2 font-medium">Email</label>

                    <textarea class="w-full border rounded-lg px-4 py-3"></textarea>
                </div>

                <div class="flex gap-5">
                    <div class="flex-1">
                        <label class="block mb-2 font-medium">Per Hour</label>

                        <select class="w-full border rounded-lg px-4 py-3">
                            <option value="" disabled>Select Hour</option>

                            <option value="0">select hour</option>
                            <option value="1">1-5 hours</option>
                            <option value="2">6-10 hours</option>

                        </select>
                    </div>

                    <div class="flex-1">
                        <label class="block mb-2 font-medium">Contact Number</label>

                        <input type="number" class="w-full border rounded-lg px-4 py-3" />
                    </div>
                </div>

                <div class="flex gap-5">
                    <div class="flex-1">
                        <label class="block mb-2 font-medium">Per Month</label>

                        <input type="text" class="w-full border rounded-lg px-4 py-3" />
                    </div>

                    <div class="flex-1">
                        <label class="block mb-2 font-medium">Date</label>

                        <input type="date" class="w-full border rounded-lg px-4 py-3" />
                    </div>
                </div>

                <div class="flex justify-end gap-3 pt-3">

                    <button type="button"
                        class="px-5 py-2 border border-gray-300 rounded-lg hover:bg-gray-100">
                        Cancel
                    </button>

                    <button @click="SubmitSuccessfully" type="submit"
                        class="px-5 py-2 bg-blue-700 text-white rounded-lg hover:bg-blue-800">
                        Submit
                    </button>
                </div>
            </div>
        </div>
    </div>

</template>
