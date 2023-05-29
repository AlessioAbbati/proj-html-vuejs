<script>
export default {
    props: {
        title: String,
        link: String,
    }
}
</script>

<template>
    <ul class="head_list list-unstyled">
        <li><a href="#">{{ title }}</a></li>
    </ul>
</template>

<style lang="scss" scoped>
a {
    text-decoration: none;
}
</style>



