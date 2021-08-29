<script>
import page from 'page'
import routes from './routes'
import { h, markRaw } from 'vue'

const DefaultComponent = markRaw({
    render: () => h('div', 'Loading…')
  })

export default {
  name: 'App',
  //ViewComponent: null,
  data: () => ({
      ViewComponent: null
  }),

  render () {
      return h(this.ViewComponent || DefaultComponent)
  },

  created () {
      for (let route in routes) {
      page(route, () => {
          this.ViewComponent = markRaw(require('./pages/' + routes[route] + '.vue').default)
      })
      }

      page()
  }
}
</script>
