<template>
    <div class="container">
        <br>
        <br>
        <app-searchbar></app-searchbar>
    <div class="row">
        <app-resultarea></app-resultarea>
    </div>
    </div>
</template>

<script>
import SearchBar from './SearchBar';
import ResultArea from './ResultArea';

export default {
    components:{
        'app-searchbar':SearchBar,
        'app-resultarea':ResultArea
    }
}
</script>

<style scoped>

</style>