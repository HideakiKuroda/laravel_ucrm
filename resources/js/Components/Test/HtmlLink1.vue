<script setup>
import { Link } from '@inertiajs/inertia-vue3';
defineProps({ links: Array })
</script>
    <template>
        <div v-if="links.length > 3">
    <template v-for="(link, index) in links" :key="index">
    <div v-if="link.url === null" class="mr-1 mb-1 px-4 py-3 text-sm leading-4
    text-gray-400 border rounded">
      <template v-if="!isNaN(link.label)">
        {{ link.label }}
      </template>
      <template v-else v-html="link.label">
      </template>
    </div>
    <Link v-else
    class="mr-1 mb-1 px-4 py-3 text-sm leading-4 border rounded
    hover:bg-white focus:border-indigo-500 focus:text-indigo-500"
    :class="{ 'bg-blue-700 text-white': link.active }" :href="link.url">
      <template v-if="!isNaN(link.label)">
        {{ link.label }}
      </template>
      <template v-else v-html="link.label">
      </template>
    </Link>
  </template>
</div>
</template>