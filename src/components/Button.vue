<script setup>
    // const props = defineProps(['label'])
</script>
<template>
    <button class="btn btn-primary px-5">
        <div class="text-green-400 ">
            <span class="bg-blue-500">
                <slot>
                    Click Me
                </slot>
            </span>
        </div>
    </button>
</template>