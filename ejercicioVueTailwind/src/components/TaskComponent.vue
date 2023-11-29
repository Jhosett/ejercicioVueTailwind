<script setup>
const props = defineProps({
    tarea: {
        type: String,
        default: 'Tarea indefinida'
    },
    index: {
        type: Number
    }
})

const emit = defineEmits(['borrarTarea'])

function borrarTarea(index) {
    //console.log('Borrar tarea',index)
    emit('borrarTarea', index)
}
</script>

<template>
    <div class="flex justify-between bg-gray-200 rounded px-4 py-1 mt-1">
      {{ props.tarea }}
      <span class="hover:bg-red-600 hover:cursor-pointer text-center text-white rounded bg-red-400 px-2"
        @click="borrarTarea(props.index)"
      >X</span>
    </div>
</template>