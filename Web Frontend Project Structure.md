#### Web Frontend Project Structure
- `assets`
  - images resources / css resources
  - `css`
    - `variables.scss` Color scheme for admin panel
  - `fonts`
    - custom fonts for website
- `components`
  - shared components and customized components
  - `charts`
    - different charts integrated from chart.js
- `configs`
  - `prod.json` Production Config json
    - `mailer` smtp credentials
    - `servers`
      - `api`
        - `host` Host name for admin panel
      - `public`
        - `host` Host name for app api
    - `firebase` Firebase push token
- `layouts`
  - `default` default layout for all pages if not specify,
  - `login` customized login layout which has to be specified in login page
- `locales`
  - translations in json format
- `mixins`
  - shared functions
- `pages` pages to store all webpage content, you can create folder to store all pages
  - `index.vue` default page for the whole website
- `plugins` Common functions
  - `bootstrap.js` define all customized components here in order to use them
- `static` Static files to be put on server
- `store` Place to store all global settings, call with $store.
- `types` typings definitions
- `nuxt.config.js` Nuxt framework config file
  - `head` -> `meta` SEO tags
- `vuetify.options.js` Vuetify framework options, store customized color variables with light dark mode.
- `package.json`
  - store scripts and required libraries setting.

#### Vue page structure
- basci structure for single page

 - website page content, you can make good use of Vuetify Documentation (https://vuetifyjs.com/en/components/grids/#grid-system) to find out different components.
 <template>  
    ...
 </tempalte>

 - script content which can define functions, data, and webpage setting here.
 - lifecycle is : beforeCreate -> created -> beforeMount -> mounted -> beforeDestroy -> destroyed
 - components: define imported components here which enables it for usage
 - data: define own data variables here
 - computed: define own variables with getters and setters properties.
 - head: webpage title and seo setting
 - methods: define own functions here
 - layout: if you want to use custom layout, you have to add definition e.g `layout: login`
 <script>
 export default {
    fetch({ store }) {
        store.commit("SET_TITLE", {
            title: { $t: "pages.alert" }
        });
    },
    components: {
    },
    data() {
        return {
        }
    },
    computed: {
    },
    head() {
    },
    methods: {
    },
    async mounted() {
    }
 }
 </script>

 - css content, scoped means css inside will only apply in this page. if without scoped, css will become global.
 <style scoped>
 </style>

#### Basic Knowledge
- global css
   - `margin and padding` there are default css in vuetify. e.g `ma-4` means `margin: 16px`, `mt-6` means `margin-top: 24px`. You can learn from (https://vuetifyjs.com/en/styles/spacing/)
   - `color` there are default color css. e.g `red lighten-2` means `#E57373`. You can learn from (https://vuetifyjs.com/en/styles/colors/)
   - `font style` there are default font class. e.g `title`, `subtitle-1`. (https://vuetifyjs.com/en/styles/text-and-typography/)
   - `grid structure` you can use `v-row` and `v-col` to design webpage content. (https://vuetifyjs.com/en/components/grids/#grid-system)

