!<template>
    <div class="result-list">
        <ul id='result-list'>
            <li v-for="(result, index) in results" :key="index">
                <Result :result="result" />
                <hr v-if="index < results.length - 1">
            </li>
        </ul>
    </div>
</template>

<script>
import Result from './Result.vue'

export default {
    name: 'ResultList',
    components: {
        Result
    },
    props: {
        results: {
            type: Array,
        }
    }
}
</script>

<style>
ul {
    padding: 0;
    margin: 0;
}
.result-list {
    margin: auto;
    margin-top: 24px;
    padding: 10px;
    max-width: 867px;
    /* background: #f9f9f9; */
}
hr {
    height: 2px;
    background: #e9e9e9;
    border: none;
    /* padding: 0px; */
    /* margin: 0px; */
    margin: 15px;
}
</style>