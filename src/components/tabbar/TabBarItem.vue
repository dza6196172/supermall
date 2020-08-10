<template>
     <div class="tab-bar-item" @click="itemClick">
       <div v-if="!isActive"><slot name="item-icon"></slot></div>
       <div v-else><slot name="item-icon-active"></slot></div>
       <div :class="{active:isActive}"><slot name="item-text"></slot></div>
     </div>
</template>
<script>
export default {
  name:'TabBarItem',
  data() {
    return {
    }
  },
  computed: {
    isActive(){
      return this.$route.path.indexOf(this.path) !==-1
    }
  },
  props: {
      path: String,
      activeColor: {
        type: String,
        default: 'red'
      }
    },
  methods: {
    itemClick(){
      this.$router.replace(this.path)
    }
  },
}
</script>

<style scoped>


</style>