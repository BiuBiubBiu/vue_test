<template>
    <ul v-for="(parent,index) in treeData" :key="index">
        <li>
            <div @click="expand(item,index)"><checkbox>{{item.title}}</checkbox></div>
            <ul v-if="parent.children && parent.children.length"
                v-show="parent.expand"
                v-for="(child,cIdx)  in parent.children"
                :key="cIdx">
                <li>
                    <div><checkbox>{{child.title}}</checkbox></div>
                    <ul v-if="child.children && child.children.length"
                        v-show="parent.expand"
                        v-for="(item,idx)  in child.children"
                        :key="idx">
                        <li>
                            <div><checkbox>{{item.title}}</checkbox></div>
                        </li>
                    </ul>
                </li>
            </ul>
        </li>
    </ul>
</template>

<script>
  export default {
    name: "text",
    props:{
      treeData:{
        type:'Array',
        default:[]
      }
    },
    data(){
      return {

      }
    },
    methods:{
      expand(item,index){
        return
      }

    },
    created() {

    }
  };
</script>

<style scoped>

</style>
