<template>
    <form class="col-md-10 mx-auto">
            <div class="input-group mb-3 shadow-lg p-3 mb-5 bg-white rounded">
                <div class="input-group-prepend">
                    <span class="input-group-text" id="basic-addon1">Search</span>
                </div>
                <input type="text" class="form-control" placeholder="Type Here" @keypress="typed" />
            </div>
        </form>
</template>

<script>
import axios from 'axios';

export default {
    
    methods:{
        typed(event){
            var key = event.target.value;
            axios.get("https://api.spotify.com/v1/search?q="+key+"&type=artist"+-H+"Accept: application/json"+-H+"Content-Type: application/json"+-H+"Authorization: Bearer BQCb3QCC4H-wxAP0_j0hzv1VsvIv2viiJIGDLI09owJZ2HDiOdfkwoKSmFLOPvp6rj55YDy0v9LSES6IYBDsxJDVEXNJ0xBbUkZ6ej71KFNCHhfxWyEWA0r-m7jmHCI31UF2eJG6Nc1Bwn5wPcUNjw2MsuUrKyBwnWb9JPT7K0BeUjYo0zI")
            .then(response=>{
                 console.log(response.data.tracks.items);
            })
           .catch(e=>{
               this.error.push(e)
           })
        }
    }
}
</script>

<style scoped>

</style>