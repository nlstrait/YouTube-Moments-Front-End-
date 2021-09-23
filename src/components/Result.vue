!<template>
    <div class="result">
        <div class="video-meta">
            <img :src="'https://img.youtube.com/vi/' + result.vid + '/maxresdefault.jpg'" id="thumbnail">
            <h3 id="title">{{ result.title }}</h3>
            <h5 id="channel">{{ result.channel }}</h5>
        </div>
        <ul id="excerpt-list">
            <li v-for="excerpt in result.excerpts" :key="excerpt.text">
                <Excerpt :text="excerpt.text" :timestamp="excerpt.timestamp" />
            </li>
        </ul>
    </div>
</template>

<script>
import Excerpt from './Excerpt.vue'

export default {
    name: 'Result',
    components: {
        Excerpt
    },
    props: ['result'],
}
</script>

<style>
.result {
    display: flex;
    font-size: 18px;
}
.video-meta {
    /* background: #eee; */
    padding: 2px;
    max-width: 336px;
}
#thumbnail {
    width: 100%;
}
#title, #channel {
    padding: 2px;
    padding-left: 5px;
    margin: 0;
    text-align: left;
}
#title {
    font-size: 18px;
}
#channel {
    font-weight: normal;
    padding-left: 6px;
}
#excerpt-list {
    padding-left: 24px;
}
li {
    list-style: none;
    margin-bottom: 24px;
}
</style>