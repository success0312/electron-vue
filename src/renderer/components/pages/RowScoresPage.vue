<template lang="pug">
include _mixins
#barba-wrapper
    .page(class=outClass)
        block header
            AppHeader
        .page__content
            block content 
                .p-container
                    .container
                        .p-container__wrapper
                            .container.container--smaller

                                router-link(:to="'/submissions'").page-back
                                    .icon.icon-arrow-back
                                    span Report Summary
                        
                                .p-box.report
                                    // summary
                                    .report-summary
                                        .report-summary__col
                                            .report-summary__head risk analysis
                                            .report-summary__text.report-summary__text--red Errors Per Row 
                                        .report-summary__label.report-summary__label--red failed
                                        .report-summary__col
                                            .report-summary__head batch id
                                            .report-summary__text 1020
                                        .report-summary__col
                                            .report-summary__head batch
                                            .report-summary__text Monday June 12th 2017 11:00AM PST
                                        .report-summary__col
                                            .report-summary__head download
                                            a(href="#").report-summary__text
                                                +icon('ico-download')
                                    
                                    
                                    // table
                                    table.p-table.p-table--full(js-stacktable)
                                        thead
                                            tr
                                                td #
                                                td Row ID
                                                td Count of Errors
                                                td Count of Warnings
                                                td Overall Status
                                                
                                        tbody
                                            tr.p-table__status-warn(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 1099432
                                                td 0
                                                td 25
                                                td Warning
                                            tr(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 1024214
                                                td 0
                                                td 0
                                                td Sucess
                                            tr(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 124125412
                                                td 0
                                                td 23
                                                td Error
                                            tr.p-table__status-warn(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 1099432
                                                td 0
                                                td 25
                                                td Warning
                                            tr(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 1024214
                                                td 0
                                                td 0
                                                td Sucess
                                            tr(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 124125412
                                                td 0
                                                td 23
                                                td Error        
                                            tr.p-table__status-warn(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 1039232
                                                td 0
                                                td 25
                                                td Warning
                                            tr(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 0102312
                                                td 10
                                                td 20
                                                td Sucess
                                            tr(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 124125412
                                                td 0
                                                td 23
                                                td Pending
                                            tr(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 124125412
                                                td 0
                                                td 23
                                                td Error
                                            tr.p-table__status-warn(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 1099432
                                                td 0
                                                td 25
                                                td Warning
                                            tr(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 1024214
                                                td 0
                                                td 0
                                                td Sucess
                                            tr.p-table__status-warn(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 1099432
                                                td 0
                                                td 25
                                                td Warning
                                            tr(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 1024214
                                                td 0
                                                td 0
                                                td Sucess
                                            tr(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 124125412
                                                td 0
                                                td 23
                                                td Error        
                                            tr.p-table__status-warn(js-modal data-mfp-src='#modal-1')
                                                td #
                                                td 1039232
                                                td 0
                                                td 25
                                                td Warning
                                .p-container__more
                                    a(href="#" js-load-more).btn.btn-more
                                        span Load more
                                        
                //- include components/_modal
        block footer
            AppFooter
</template>

<script>
import AppHeader from './Header.vue'
import AppFooter from './Footer.vue'

export default {
  name: 'row-scores-page',
  components: {
    AppHeader,
    AppFooter
  },
  methods: {
  }
}
</script>

<style lang="sass" scoped>
@import "../../assets/styles/app.sass";
</style>