<template>
    <div class="cardinfo-container">
        <cardInfo title="Frontend" iconName="desktop"
         :cardlanguages=" [
                            {
                              name: 'Vue, React',
                            },
                            {
                              name: 'Clojure',
                            },
                            {
                              name: 'JavaScript',
                            }
                            ]"></cardInfo>
        <cardInfo title="Backend" iconName="gears"
         :cardlanguages=" [
                            {
                              name: 'Node, Express',
                            },
                            {
                              name: 'Python, Flask',
                            },
                            {
                              name: 'PHP',
                            },
                            {
                              name: 'GraphQL',
                            },
                            
                            ]"></cardInfo>
        <cardInfo title="Database" iconName="database"
         :cardlanguages=" [
                            {
                              name: 'FireBase',
                            },
                            {
                              name: 'MySQL/ SQLAlchemy/ NoSQL',
                            },
                            {
                              name: 'MongoDB',
                            }
                            ]"></cardInfo>
    </div>
</template>
<style scoped>
.cardinfo-container{
    margin-bottom: 7rem;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
}
</style>
<script>
import cardInfo from "../components/CardInfo.vue";

export default ({
    name: "cardinfos",
    components: {
        cardInfo
    }
})
</script>
