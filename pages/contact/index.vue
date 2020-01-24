<template>
    <transition>
        <div>
            <keyvisualSection />
            <section id="form" class="section-area form">
                <formSection />
            </section>
        </div>
    </transition>
  
</template>

<script>
import keyvisualSection from '~/components/keyvisual.vue'
import formSection from '~/components/form.vue'
export default {
    components: {
        keyvisualSection,
        formSection
    }
}
</script>