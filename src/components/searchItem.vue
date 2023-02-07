<template>
    <div class="item-container">
        <div class="results-header mb-5">
            <h1>Search Results</h1>
            <div class="btn-header mt-1">
                <button 
                    class="btn btn-secondary btn-custom"
                    type="button"
                >Back</button>
                <button
                    class="btn btn-secondary btn-custom"
                    type="button"
                >Next</button>
            </div>
        </div>

        <div class="movie-item text-left">
            <div class="row justify-content-md-center" v-for="(item, index) in items" :key="index">
                <div class="col-md-10" @click="showDetail(item.imdbID)">
                    <p class="results-format">{{item.index}}{{ item.Title }}</p>
                </div>
                <div class="col-md-2">
                    <p class="year-format">({{ item.Year }})</p>
                </div>
                <hr>
            </div>
        </div>
    </div>
</template>

<script>
import router from '@/router';

    export default {
        name: "SearchItems",
        
        props: ['items'],
        
        data: () => ({
            results: true,
        }),

        methods: {
            showDetail(id) {
                console.log({id})
                router.push(
                    `/details/${id}`
                )
            }
        }
    }
</script>

<style>
    .item-container {
        display: flex;
        flex-direction: column;
        justify-content: center;
    }
    .movie-item {
        padding: 9px 23px;
        cursor: pointer;
    }
    /* .btn-header {
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    } */
    .results-header {
        /* width: 50%; */
        align-self: center;
    }
    .results-format {
        font-weight: 200;
        font-size: 1.5em;
    }
    .year-format {
        font-style: italic;
        font-size: 1.2em;
        font-weight: 200;
    }
</style>