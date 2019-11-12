<template>
    <MyTree :treeData="treeData"></MyTree>
</template>
<script>
  import MyTree from "@/components/myTree.vue"
  export default {
    components:{
      MyTree
    },
    data() {
      return {
        treeData: [
          {
            title: 'parent 1',
            expand: true,
            children: [
              {
                title: 'parent 1-1',
                expand: true,
                children: [
                  {
                    title: 'leaf 1-1-1'
                  },
                  {
                    title: 'leaf 1-1-2'
                  }
                ]
              },
              {
                title: 'parent 1-2',
                expand: true,
                children: [
                  {
                    title: 'leaf 1-2-1'
                  },
                  {
                    title: 'leaf 1-2-1'
                  }
                ]
              }
            ]
          }
        ]
      };
    },
    methods: {
      handleSubmit(name) {

      },
      handleReset(name) {

      }
    }
  };
</script>
