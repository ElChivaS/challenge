<template>
    <div class="container">
        <h3>Seleccionado: "<span>{{ title }}</span>"</h3>
        
        <div class="card mt-5 mb-3">
            <div class="row g-0">
                <div class="col-md-4">
                    <img 
                        src="#" 
                        class="img-fluid rounded-start" 
                        alt="the official poster of {{title}}">
                </div>
                <div class="col-md-8">
                    <div class="card-body">
                        <h5 class="card-title fw-bold">{{title}}</h5><br />
                        <span class="fw-light">{{year}}</span>
                        <p class="card-text">{{type}}</p>
                        <p class="card-text">{{duration}}</p>
                    </div>
                </div>
                <div id="plot">
                    <p class="mt-2 text-left">{{plot}}</p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: "MovieDetails",
    data () {
        return {
            year: "",
            plot: "",
            duration: "",
            title: "",
            type: "",
        }
    },
    methods: {
        async getData() {
            const setting = {
            method: 'GET'
        }
        console.log({id:this.$route.params.movie })
        const url = `http://www.omdbapi.com/?apikey=d2e9bfa0&i=${this.$route.params.movie}`
        const result = await fetch(url, setting)
        const data = await result.json()
        console.log({data})
        this.year = data.year
        this.title= data.title
        this.plot = data.plot
        this.type = data.type
        this.duration = data.duration
        }
    },
    async created () {
        this.getData()
    },
}
</script>