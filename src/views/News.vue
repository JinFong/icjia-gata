<template lang="html">

<div>
<section class="page">
<page-header :header="title" />


  <div class="container">

	<div class="col-md-12">

    <newsfeed

      />


	</div>
</div>





</section>
</div>



</template>

<script>
const description = `News & Announcements`
const title = "News & Announcements"
const created = '2017-03-26'
const type  = 'page'
const status = 'live'
import utilities from '@/utilities'
import PageHeader from '@/components/PageHeader'
import Newsfeed from 'components/Newsfeed'

export default {
  name: 'NewsAndInformation',
  pageData:  {
    created,
    description,
    title,
    type,
    status
  },
  metaInfo: {
      // title will be injected into parent titleTemplate
      title,
      meta: [
        { vmid: 'description', name: 'description', content: utilities.stripTags(description)}
    ]
  },
  components: {

    PageHeader,
  Newsfeed,

  },
  data () {
    return {
      title
    }
  },
}
</script>

<style lang="css">
</style>
