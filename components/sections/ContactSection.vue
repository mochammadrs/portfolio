<script lang="ts" setup>
import type { FormError } from '#ui/types'

const state = ref({
  name: '',
  email: '',
  message: ''
})

const validate = (): boolean => {
  if (!state.value.name || !state.value.email || !state.value.message) {
    alert('Please fill in all fields.');
    return false;
  }
  return true;
}

function submit () {
  if (!validate()) return;
  
  console.log('Form submitted:', state.value)
}
</script>

<template>
    <section id="contact" class="relative min-h-screen flex justify-center py-20 md:py-32">
        <img 
        src="~/assets/images/BgContact.svg" 
        alt="Traced Contact"
        class="absolute w-full h-auto top-[40px] object-cover">
        <div class="relative bg-white w-[1258px] rounded-md shadow-md container flex flex-col items-center mx-auto">
            <h2 class="text-[#F44336] text-5xl font-bold z-10 py-4">Get In Touch</h2>
            <div class="grid grid-cols-2">
                <div class="w-[512px] h-[380px] flex justify-center items-center">
                    <h2 class="text-[#000C24] font-semibold text-6xl">Drop me a line. <br>
                        I would like to hear from you.</h2>
                </div>
                <div class="w-[512px] h-[380px] flex justify-center items-center">
                <form class="space-y-4" @submit.prevent="submit" >
              <div>
                <input 
                  v-model="state.name"
                  type="text" 
                  placeholder="Name"
                  class="w-[450px] p-2 border border-gray-300 dark:border-gray-700 rounded-md transition text-black"
                >
              </div>

              <div>
                <input 
                  v-model="state.email"
                  type="email" 
                  placeholder="Email"
                  class="w-[450px] p-2 border border-gray-300 dark:border-gray-700 rounded-md transition text-black"
                >
              </div>

              <div>
                <textarea 
                  v-model="state.message"
                  placeholder="Message" 
                  :rows="4"
                  class="w-[450px] p-2 border border-gray-300 dark:border-gray-700 rounded-md transition text-black"
                />
              </div>

              <div>
                <button 
                  type="submit"
                  class="w-[150px] bg-gray-900 dark:bg-gray-800 hover:bg-gray-700 text-white py-2 px-4 rounded-md transition-colors"
                >
                  Send Message
                </button>
              </div>
            </form>
                </div>
            </div>
        </div>
    </section>
</template>