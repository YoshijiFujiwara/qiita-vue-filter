<template>
    <div class="media">
        <img class="mr-3" src="https://via.placeholder.com/150" alt="Generic placeholder image">
        <div class="media-body">
            <h5 class="mt-0">{{ heading | searchHighlight(search) }}</h5>
            {{ body | searchHighlight(search) }}
        </div>
    </div>
</template>

<script>
export default {
    props: ['heading', 'body', 'search'],
    filters: {
        searchHighlight (value, search) {
            // 検索キーワードが入力されているとき
            if (search) {
                // 検索キーワードに一致する部分を、spanタグに置換すればいいね
                return value.replace(search, `<span class="bg-warning">${search}</span>`)
            }
            // 検索キーワードが入力されていない場合は、ハイライトしない
            return value
        }
    }
}
</script>
