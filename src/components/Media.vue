<template>
    <div class="media">
        <img class="mr-3" src="https://via.placeholder.com/150" alt="Generic placeholder image">
        <div class="media-body">
            <h5 class="mt-0" v-html="$options.filters.searchHighlight(heading, search)"></h5>
            <p v-html="$options.filters.searchHighlight(body, search)"></p>
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
                // 世紀表現で、一致する文字全てをハイライトする
                const searchRegExp = new RegExp(search, 'ig')
                return value.replace(searchRegExp, (match) => {
                    return `<span class="bg-warning">${match}</span>`
                })
            }
            // 検索キーワードが入力されていない場合は、ハイライトしない
            return value
        }
    }
}
</script>
