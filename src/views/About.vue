<template>
  <div class="about">
    <h1>This is an about page</h1>

    <Tree :value="treeData"></Tree>
  </div>
</template>

<script lang="ts">
import 'he-tree-vue/dist/he-tree-vue.css'
import { Tree, Draggable } from 'he-tree-vue'

export default {
  components: { Tree: Tree.mixPlugins([Draggable]) },
  data() {
    return {
      treeData: [
        {
          text: 'node 1',
        },
        {
          text: 'node 2',
          children: [
            {
              text: 'node 2-1',
            }
          ]
        }
      ]
    }
  },
}
</script>