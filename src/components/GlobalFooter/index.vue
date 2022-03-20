<template>
  <global-footer v-if="visibility" class="footer custom-render">
    <template v-slot:links>
      <!-- <a href="https://www.github.com/vueComponent/pro-layout" target="_blank">Pro Layout</a>
      <a href="https://www.github.com/vueComponent/ant-design-vue-pro" target="_blank">Github</a>
      <a href="https://www.github.com/sendya/" target="_blank">@Sendya</a>-->
    </template>
    <template v-slot:copyright>
      <span style="margin-right: 6px">{{ copyright }}</span>
      <a :href="link.url" target="_blank">{{ link.text }}</a>
    </template>
  </global-footer>
</template>

<script>
import { GlobalFooter } from '@/layouts/ProLayout'

const uncompileStr = (code) => {
  code = unescape(code)
  var c = String.fromCharCode(code.charCodeAt(0) - code.length)
  for (var i = 1; i < code.length; i++) {
    c += String.fromCharCode(code.charCodeAt(i) - c.charCodeAt(i - 1))
  }
  return c
}

export default {
  name: 'ProGlobalFooter',
  components: {
    GlobalFooter
  },
  data () {
    return {
      visibility: true,
      copyright: '商城管理系统',
      link: {
        text: 'VanShop',
        url: "#"
      }
    }
  },
  methods: {

  }
}
</script>
