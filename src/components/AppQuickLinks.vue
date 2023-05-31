<script>
export default {
    props: {
        title: String,
        link: String,
    }
}
</script>

<template>
    <li><a href="#">{{ title }}</a></li>
</template>

<style lang="scss" scoped>
li {
    white-space: nowrap;
    a {
        text-decoration: none;
        color: white;
        &:hover {
            text-decoration: underline;
        }
    }
}
</style>
