<template>
    <div>
    <div v-for="home in homes" :key="home.objectID" style="float:left;margin:10px">
        <home-card :home="home"/>
    </div>
    </div>
</template>

<script>
import homes from '~/data/homes'

export default{
// Meta tag Section Start
head(){
        return {
            title: 'Homepage',
            meta: [{
                name: 'description',
                content: 'This is a test',
                hid: 'description'
            }]
        }
    },
    /// Meta tag Section End

    data(){
        return {
            homes: homes.slice(0,3)
        }
    }
}
</script>