<template>
    <div class="row">
        <quote-selector v-for="(quote, index) in quotes"
                        @click.native="deleteQuote">
        </quote-selector>
        <appQuote>{{ quote }}</appQuote>
    </div>
</template>

<script>
    import Quote from './components/Quote.vue';

    export default {
        props: ['quote'],
        components: {
            data: function () {
                return {
                    quote: ''
                }
            }
        },
        methods: {
            deleteQuote: function (index) {
                this.$emit('quotesDeleted', index)
            }
        }
    }
</script>
