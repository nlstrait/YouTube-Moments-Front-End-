!<template>
    <div class="excerpt">
        <p>"{{ text }}"</p>
        <span class="timestamp">{{ timestamp }}</span>
    </div>
</template>

<script>
export default {
    name: 'Excerpt',
    props: {
        text: String,
        timestamp: String,
    }
}
</script>

<style>
.excerpt {
    background-color: #F1F1F1;
    max-width: 500px;
    min-width: 300px;
    border-radius: 5px;
    text-align: left;
    padding-bottom: 5px;
    padding: 5px;
}
p {
    margin: 0;
    padding: 5px;
}
.timestamp {
    font-weight: bold;
    color: #818181;
    font-size: 87%;
    padding-left: 10px;
}
</style>