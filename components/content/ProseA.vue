<script setup lang="ts">
    defineProps({
      href: {
        type: String,
        default: ''
      },
      blank: {
        type: Boolean,
        default: false
      }
    })
    </script>
    
    <template>
      <NuxtLink :href="href" class="text-base md:text-lg font-semibold">
        <slot />
      </NuxtLink>
    </template>