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
    padding-inline: 1rem;
    a {
    text-decoration: none;
    color: white;
    font-weight: 700;
    &:hover {
        text-decoration-line: underline;
        cursor: cell;
    }
}
}
</style>



