<template>
    <div class="row">
        <div class="form-group col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
            <label for="exampleTextarea">New Quote</label>
            <textarea 
                class="form-control" 
                id="exampleTextarea" 
                rows="3"
                v-model="quote"></textarea>
        </div>
        <div class="form-group col-sm-8 col-sm-offset-2 col-xs-12 col-md-6 col-md-offset-3">
            <button class="btn btn-primary" @click.prevent="addNewQuote">Add Quote</button>
        </div>
    </div>
</template>


<script>
    
    export default {
        data: () => {
            return {
                quote: ''
            }
        },
        methods: {
            addNewQuote() {
                this.$emit('quoteAdded', this.quote);
                this.quote = '';
            }
        }
    };
    
    

</script>


<style>

</style>
