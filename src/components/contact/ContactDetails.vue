<script>
export default {
  props: ['contacts'],
};
</script>
<template>
    <body class="bg-blue-400">
      <div class="w-full">
        <div class="text-left max-w-xl px-6">
          <h2 class="font-general-medium text-2xl text-primary-light mt-12 mb-8">
            Contact details
          </h2>
          <ul class="font-general-regular">
            <li class="flex" v-for="contact in contacts" :key="contact.id">
              <i :data-feather="contact.icon" class="w-5 text-light mr-4"></i>
              <a href="#" class="text-lg mb-4 text-ternary-light"
                :class="contact.icon === 'mail' || contact.icon === 'phone' ? 'hover:underline cursor-pointer' : ''"
                aria-label="Website and Phone">
                {{ contact.name }}
              </a>
            </li>
          </ul>
        </div>
      </div>
    </body>
  </template>
  

  
  <style scoped>
    /* You can add any additional styles here */
  </style>
  