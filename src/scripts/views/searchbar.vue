<template>
    <div>
        <group-title>base:{{search}}</group-title>
        <group>
            <cell>
                <searchbar v-model="search" :autoBlur="false">
                    <searchbar-placeholder>
                        <icon name="search" left size="lg"></icon>搜索
                    </searchbar-placeholder>
                    <searchbar-btn>
                        <span class="text-primary">搜索</span>
                    </searchbar-btn>
                </searchbar>
            </cell>
        </group>
        <group-title>circle</group-title>
        <group>
            <cell>
                <!-- 默认autoBlur为true,点击页面其他位置，会触发blur事件 -->
                <searchbar shape="circle">
                    <searchbar-placeholder>
                        <icon name="search" left size="lg"></icon>搜索
                    </searchbar-placeholder>
                    <searchbar-btn>
                        <span class="text-primary">搜索</span>
                    </searchbar-btn>
                </searchbar>
            </cell>
        </group>
    </div>
</template>

<script>
    export default {
        data() {
            return {
                search: '123',
            };
        },
        watch: {
            search(value) {
                console.log('search', value);
            },
        },
    };
</script>
