<template>
    <div class="container">
        <!--ToDo: Use the Header component selector-->
        <!--Bind data props quoteCount and set it equal to the quote length-->
        <!--Bind data props maxQuotes and set it equal to the maxQuotes created below-->

        <!--ToDo: Use the NewQuote component selector-->
        <!--Initiate an $emit event listener called quoteAdded that is equal to newQuote-->

        <!--ToDo: Use the QuoteGrid component selector-->
        <!--Bind data props quotes and set it equal to the quotes array created below-->
        <!--Call quoteDeleted that is emitted from the QuoteGrid Component and pass the deleteQuote method created below-->
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
                quotes: [
                    {quote: 'Default message'},
                ],
                maxQuotes = 10
            }
        },
        methods: {
            // ToDo: Create a method that checks when a newQuote is created and takes the parameter quote.
            // This method will check if the quotes (Array Data Object) length is greater than or equal to the max quotes allowed
            // If it is return an alert telling the user to delete a quote
            // Outside of conditional, push quote (method parameter) to the quotes array

            // ToDo: Create a method deleteQuote that takes in a parameter of index
            // This method will splice the quotes array by (index, 1)
        },
        components: {
            // ToDo: Initiate the QuoteGrid, NewQuote, and Header Components with Custom Selectors
        }

    }
</script>

<style>
</style>
