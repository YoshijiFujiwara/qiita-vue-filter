<template>
    <div class="media">
        <img class="mr-3" src="https://via.placeholder.com/150" alt="Generic placeholder image">
        <div class="media-body">
            <h5 class="mt-0">{{ heading }}</h5>
            {{ body }}
        </div>
    </div>
</template>

<script>
export default {
    props: ['heading', 'body', 'search']
}
</script>
