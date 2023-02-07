<template>
    <div class="container">
        <div class="user-input">
            <div class="input-group mt-5 mb-3 search-controls">
                <input
                    id="user-input"
                    type="text" 
                    class="form-control" 
                    placeholder="Find your favorite movie" 
                    v-model="user_text"
                    aria-label="movie finder" 
                    aria-describedby="button-addon2"
                >
                <button 
                    class="btn btn-secondary" 
                    type="button" 
                    id="button-addon2"
                    @click="searchTheOMDB"
                >
                    Search
                </button>
            </div>
        </div>
        <div class="result-output">
            <searchItem :items="Items" />
        </div>
    </div>
</template>


<script>
import SearchItem from '@/components/searchItem.vue'

window.apiKey = "d2e9bfa0"

export default {
    name: "GetItems",

    components: {
        SearchItem
    },
    data () {
        return {
            Items: [],
            user_text: "",
        }
    },
    
    methods: {
        searchTheOMDB: async function() {
            try {
                const setting = {
                    method: 'GET'
                }

                const url = `http://www.omdbapi.com/?apikey=d2e9bfa0&s=${this.user_text}`
                const data = await fetch(url, setting)
                const json = await data.json()
                this.Items = json.Search
                console.log({json})
            }
            catch(e) {
                console.log({e});
            }
        }
    }
}
</script>


<style >
    
    body { 
        background: url(@/assets/img/wp5556216.jpg) no-repeat center center fixed; 
        background-position: center center;
        background-repeat: no-repeat;
        background-attachment: fixed;
        background-size: cover;

        -webkit-background-size: cover;
        -moz-background-size: cover;
        -o-background-size: cover;
        background-size: cover;
    }
    </style>
    <style>
.container {
    display: flex;
    flex-direction: column;
    justify-content: center;
    background-color: rgba(228, 228, 228, .923);
}
#user-input {
    font-size: 1.3em;
}
.user-input {
    width: 35%;
    align-self: center;
}
.results-output {
    align-self: center;
}
.search-controls {
    align-self: center;
}
.item-container {
    align-self: center;
    background-color: #FFF;
    margin: 9px;
    padding: 19px;
    border-radius: var(--bs-border-radius);
}
.results-header {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
}

.btn-custom {
    width: 184px;
    font-weight: 700;
    font-size: 1.1em;
}
.movie-item {
    font-size: 1.2em;
    text-align: left;
}
hr {
    margin-bottom: 23px;
}
nav {
    background-color: rgba(228, 228, 228, .923);
    margin-bottom: 23px;
    font-size: 1.2em;

}
</style>