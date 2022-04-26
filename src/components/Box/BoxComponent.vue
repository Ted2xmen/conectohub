<template>
    <span class="px-2 py-0  mx-2 leading-loose rounded-lg w-8 h-8 bg-green-600 text-white text-sm">
        {{number}}
    </span>
</template>


<script>
export default {
    props: [
        "number"
    ]
}
</script>