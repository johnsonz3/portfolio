<template>
    <div>
        <div class="circle">
            <font-awesome-icon :icon="{ prefix: 'fas', iconName: iconName }" class="icon-desktop"/>
        </div>
        <div class="cardInfo-container">
            <div class="page-title">{{title}}</div>
              <div v-for="item in cardlanguages" :key="item.name" class="ts-containers">
                <font-awesome-icon :icon="{ prefix: 'fas', iconName: 'check' }" class="checkmark"/>
                {{item.name}}
              </div>
        </div>
    </div>
</template>
<style scoped>
.ts-containers{
    text-align: left;
    padding-left: 1rem;
    padding-top: 1rem;

}
.checkmark {
    color: rgb(91, 206, 91);
}
.circle {
    width: 5.5rem;
    height: 5.5rem;
    background-color: blueviolet;
    position: relative;
    border-radius: 100%;
    top:4rem;
    padding: 1.2rem;
    margin-left: auto;
    margin-right: auto;
}
.cardInfo-container{
    border-radius: 0.5rem;
    padding: 2.5rem 1rem 1rem 1rem;
    width: 18rem;
    height: 25rem;
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
}
.icon-desktop {
    color: white;
    font-size: 2.5rem;
}
</style>
<script>
export default ({
    name: "cardInfo",
    props: {
        title: String,
        iconName: String,
        cardlanguages: Array
    }
})
</script>
