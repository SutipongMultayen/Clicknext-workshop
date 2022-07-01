<template>
  <div>
    <Slide />
    <Content />
    <Footer />
  </div>
</template>

<script>
import Slide from '@/components/Slide'
import Content from '@/components/Content'
import Footer from '@/components/Footer'
export default {
  components: { Content, Slide, Footer },
}
</script>
