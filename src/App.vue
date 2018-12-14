<template>
    <div class="container">
        <appHeader :quoteCount="quotes.length" :maxQuotes="maxQuotes"></appHeader>

        <appNewQuote @quoteAdded="newQuote"></appNewQuote>

        <appQuoteGrid :quotes="quotes" @quoteDeleted="deleteQuote"></appQuoteGrid>
        <div class="row">
            <div class="col-sm-12 text-center">
                <div class="alert alert-info">Info: Click on a Quote to delete it!</div>
            </div>
        </div>
    </div>
</template>

<script>
    import QuoteGrid from './components/QuoteGrid.vue';
    import Header from './components/Header.vue';
    import NewQuote from './components/NewQuote.vue';

    export default {
        data: function () {
            return {
                quotes: ['Default Message'],
                maxQuotes: 10
            }
        },
        methods: {
            newQuote: function (myQuote) {
                if (this.quotes.length >= this.maxQuotes) {
                    return alert('Please delete a quote to add a new one.')
                }
                this.quotes.push(myQuote)
            },
            deleteQuote: function (index) {
                this.quotes.splice(index, 1)
            }
        },
        components: {
            appQuoteGrid: QuoteGrid,
            appHeader: Header,
            appNewQuote: NewQuote
        }
    }
</script>

<style>
</style>
