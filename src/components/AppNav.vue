<script>
export default {
    props: {
        title: String,
        link: String,
    }
}
</script>

<template>
    <div>
        <li><a :href="link">{{ title }}</a></li>
    </div>
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
            cursor: pointer;
        }
    }
}

@media (max-width: 768px) {
    div {
        
        li {
           font-size: .8rem;
           white-space: nowrap;
           
        }
    }
}
</style>



