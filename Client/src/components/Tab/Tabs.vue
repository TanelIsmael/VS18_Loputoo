<template>
    <div class="tab-wrapper">
        <ul class="tab-header">
            <li class="header-item" v-for="tab in tabs"
          :key="tab"
          v-bind:class="{
            'header-item__active': activeTab === tab
          }"
          v-on:click="switchTab(tab);">
                <slot :name="tabHeadSlotName(tab)">{{tab}}</slot>
            </li>
        </ul>
        <div class="tab-content">
            <div class="content-item">
                <slot :name="tabPanelSlotName"></slot>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        tabs: Array,
        initialTab: String
    },
    data() {
        return {
        activeTab: this.initialTab
        };
    },
    computed: {
        tabPanelSlotName() {
        return `tab-panel-${this.activeTab}`;
        }
    },
    methods: {
        tabHeadSlotName(tabName) {
        return `tab-head-${tabName}`;
        },

        switchTab(tabName) {
        this.activeTab = tabName;
        }
    }
}
</script>



<style lang="scss" scoped>
    .tab-wrapper {
        color: #ffffff;
        // background: #0099d8;
        font-family: 'Open Sans', sans-serif;

        .tab-header {
            display: inline-flex;
            background: #0099d8;
            border-bottom: 1px solid #0087bc;
            list-style: none;

            .header-item {
                cursor: pointer;
                padding: 20px;
            }

            .header-item__active {
                color:#ffe600;
            }
        }

        .tab-content {
            padding: 20px;
            background: #0099d8;

            .content-item {
                padding-top: 20px;

                div {
                    display: flex;
                    align-items: center;
                    justify-content: space-between;
                    padding: 0 20px 20px 20px;

                    p {
                        font-size: 1rem;
                        line-height: 25.6px;
                    }

                    a {
                        color: #ffe600;
                        font-weight: 900;
                        border-radius: 50px;
                        border: 1px solid #ffe600;
                        padding: .5rem 1.5rem;
                        font-size: 0.875rem;
                    }
                }
            }
        }
    }


    .content-item > div {
        display: flex;
    }
</style>