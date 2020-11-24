<template>

    <a-list rowKey="id" :grid="{gutter: 24, lg: 3, md: 2, sm: 1, xs: 1}" :dataSource="dataSource">
        <a-list-item slot="renderItem" slot-scope="item,index">
            <template>
                <a-card :hoverable="true">
                    <img slot="cover" alt="cover" :src="item.avatar" :style="{backgroundColor: colorList[index],textAlign: 'center', padding: '20px'}" />
                    <a-card-meta :title="item.title">
                    </a-card-meta>
                </a-card>
            </template>
        </a-list-item>
    </a-list>

</template>

<script>



export default {
    name: 'CardList',
    data() {
        this.tabList = [
            { key: 'tab1', tab: '快速开始' },
            { key: 'tab2', tab: '产品简介' },
            { key: 'tab3', tab: '产品文档' }
        ]
        return {
            colorList: ['#66d1ff', '#cc0000', '#fb503b', '#66d1ff', '#cc0000', '#fb503b', '#66d1ff', '#cc0000', '#fb503b'],
            tabActiveKey: 'tab1',

            extraImage: 'https://gw.alipayobjects.com/zos/rmsportal/RzwpdLnhmvDJToTdfDPe.png',
            dataSource: [
                {
                    title: '华强北',
                    avatar: 'https://resources.ninghao.net/icon/docker.png',
                    content: '在中台产品的研发过程中，会出现不同的设计规范和实现方式，但其中往往存在很多类似的页面和组件，这些类似的组件会被抽离成一套标准规范。'
                },
                {
                    title: '华新',
                    avatar: 'https://resources.ninghao.net/icon/rails.png',
                    content: '在中台产品的研发过程中，会出现不同的设计规范和实现方式，但其中往往存在很多类似的页面和组件，这些类似的组件会被抽离成一套标准规范。'
                },
                {
                    title: '市民中心',
                    avatar: 'https://resources.ninghao.net/icon/laravel.png',
                    content: '在中台产品的研发过程中，会出现不同的设计规范和实现方式，但其中往往存在很多类似的页面和组件，这些类似的组件会被抽离成一套标准规范。'
                },
                {
                    title: '中心公园',
                    avatar: 'https://resources.ninghao.net/icon/swift.png',
                    content: '在中台产品的研发过程中，会出现不同的设计规范和实现方式，但其中往往存在很多类似的页面和组件，这些类似的组件会被抽离成一套标准规范。'
                },
                {
                    title: '音乐厅',
                    avatar: 'https://resources.ninghao.net/icon/html5.png',
                    content: '在中台产品的研发过程中，会出现不同的设计规范和实现方式，但其中往往存在很多类似的页面和组件，这些类似的组件会被抽离成一套标准规范。'
                },
                {
                    title: '宝安体育馆',
                    avatar: 'https://resources.ninghao.net/icon/code.png',
                    content: '在中台产品的研发过程中，会出现不同的设计规范和实现方式，但其中往往存在很多类似的页面和组件，这些类似的组件会被抽离成一套标准规范。'
                },
                {
                    title: '邓小平广场',
                    avatar: 'https://resources.ninghao.net/icon/semantic-ui.png',
                    content: '在中台产品的研发过程中，会出现不同的设计规范和实现方式，但其中往往存在很多类似的页面和组件，这些类似的组件会被抽离成一套标准规范。'
                },
                {
                    title: '红岭e出口',
                    avatar: 'https://resources.ninghao.net/icon/mysql.png',
                    content: '在中台产品的研发过程中，会出现不同的设计规范和实现方式，但其中往往存在很多类似的页面和组件，这些类似的组件会被抽离成一套标准规范。'
                },
            ]
        }
    },
    methods: {
        testFun() {
            this.$message.info('快速开始被点击！')
        }
    }
}
</script>

<style lang="less" scoped>
    @import '~@/components/index.less';
    /deep/ .ant-card-meta-title {
        text-align: center;
    }
    .card-list {
        /deep/ .ant-card-body:hover {
            .ant-card-meta-title > a {
                color: @primary-color;
            }
        }

        /deep/ .ant-card-meta-title {
            margin-bottom: 12px;

            & > a {
                display: inline-block;
                max-width: 100%;
                color: rgba(0, 0, 0, 0.85);
            }
        }

        /deep/ .meta-content {
            position: relative;
            overflow: hidden;
            text-overflow: ellipsis;
            display: -webkit-box;
            height: 64px;
            -webkit-line-clamp: 3;
            -webkit-box-orient: vertical;

            margin-bottom: 1em;
        }
    }

    .card-avatar {
        width: 48px;
        height: 48px;
        border-radius: 48px;
    }

    .ant-card-actions {
        background: #f7f9fa;

        li {
            float: left;
            text-align: center;
            margin: 12px 0;
            color: rgba(0, 0, 0, 0.45);
            width: 50%;

            &:not(:last-child) {
                border-right: 1px solid #e8e8e8;
            }

            a {
                color: rgba(0, 0, 0, 0.45);
                line-height: 22px;
                display: inline-block;
                width: 100%;
                &:hover {
                    color: @primary-color;
                }
            }
        }
    }

    .new-btn {
        background-color: #fff;
        border-radius: 2px;
        width: 100%;
        height: 188px;
    }
</style>
