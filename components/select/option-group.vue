<template>
  <v-menu-item-group prefixCls="bts-select-dropdown" :title="title">
    <slot></slot>
  </v-menu-item-group>
</template>
<script type="text/babel">
  import VMenu from '../menu'

  export default {
    name: 'VOptionGroup',
    props: {
      title: {
        type: String,
        required: true
      }
    },
    components: {
      VMenuItemGroup: VMenu.ItemGroup
    }
  }
</script>
