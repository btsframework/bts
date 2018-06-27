<template>
  <div class="bts-collapse-item"
       :class="{ 'bts-collapse-item-active': active }">
    <div class="bts-collapse-header" role="tab"
         :aria-expanded="active"
         @click="onHeaderClick">
      <i class="arrow"></i>
      {{header}}
    </div>
    <v-transition type="collapse">
      <div class="bts-collapse-content" role="tabpanel"
           v-show="active"
           :class=" { 'bts-collapse-content-active': active }">
        <div class="bts-collapse-content-box">
          <slot></slot>
        </div>
      </div>
    </v-transition>
  </div>
</template>
<script type="text/babel">
  export default {
    name: 'VPanel',
    props: {
      index: {
        type: String,
        required: true
      },
      header: {
        type: String
      }
    },
    data() {
      return {
        store: {},
        active: false
      }
    },
    methods: {
      onHeaderClick() {
        this.store.commit(this.active ? 'closePanel' : 'openPanel', { index: this.index })
      }
    }
  }
</script>
