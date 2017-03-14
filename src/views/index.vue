<template>
    <div id="app">

<!--button部分代码-->
        <i-button>Default</i-button>
        <i-button type="primary">Primary</i-button>
        <i-button type="ghost">Ghost</i-button>
        <i-button type="dashed">Dashed</i-button>
        <i-button type="text">Text</i-button>
        <br><br>
        <i-button type="info">信息按钮</i-button>
        <i-button type="success">成功按钮</i-button>
        <i-button type="warning">警告按钮</i-button>
        <i-button type="error">错误按钮</i-button>
        <br/>

        <i-button type="primary" shape="circle" icon="ios-search"></i-button>
        <i-button type="primary" icon="ios-search">搜索</i-button>
        <i-button type="primary" shape="circle" icon="ios-search">搜索</i-button>
        <i-button type="primary" shape="circle">圆角按钮</i-button>
        <br><br>
        <i-button type="ghost" shape="circle" icon="ios-search"></i-button>
        <i-button type="ghost" icon="ios-search">搜索</i-button>
        <i-button type="ghost" shape="circle" icon="ios-search">搜索</i-button>
        <i-button type="ghost" shape="circle">圆角按钮</i-button>
        <br/>


        <i-button type="primary" size="large">Large</i-button>
        <i-button type="primary">Default</i-button>
        <i-button type="primary" size="small">Small</i-button>
        <br><br>
        <i-button type="primary" shape="circle" size="large">Large</i-button>
        <i-button type="primary" shape="circle">Default</i-button>
        <i-button type="primary" shape="circle" size="small">Small</i-button>
        <br/>

        <i-button type="success" long>确认提交</i-button>
        <br><br>
        <i-button type="error" long>确认删除</i-button>
        <br/>


        <i-button>Default</i-button>
        <i-button disabled>Default(Disabled)</i-button>
        <br>
        <i-button type="primary">Primary</i-button>
        <i-button type="primary" disabled>Primary(Disabled)</i-button>
        <br>
        <i-button type="ghost">Ghost</i-button>
        <i-button type="ghost" disabled>Ghost(Disabled)</i-button>
        <br>
        <i-button type="dashed">Dashed</i-button>
        <i-button type="dashed" disabled>Dashed(Disabled)</i-button>
        <br>
        <i-button type="text">Text</i-button>
        <i-button type="text" disabled>Text(Disabled)</i-button>
        <br/>

        <i-button type="primary" loading>Loading...</i-button>
        <i-button type="primary" :loading="loading" @click="toLoading">
            <span v-if="!loading">Click me!</span>
            <span v-else>Loading...</span>
        </i-button>
        <i-button type="primary" :loading="loading2" icon="checkmark-round" @click="toLoading2">
            <span v-if="!loading2">Click me!</span>
            <span v-else>Loading...</span>
        </i-button>
        <br/>

        <h4>基本</h4>
        <br><br>
        <Button-group>
            <i-button>取消</i-button>
            <i-button type="primary">确定</i-button>
        </Button-group>
        <Button-group>
            <i-button disabled>昨日</i-button>
            <i-button disabled>今日</i-button>
            <i-button disabled>明日</i-button>
        </Button-group>
        <Button-group>
            <i-button type="primary">L</i-button>
            <i-button>M</i-button>
            <i-button type="ghost">M</i-button>
            <i-button type="dashed">R</i-button>
        </Button-group>
        <br><br>
        <h4>配合图标</h4>
        <br><br>
        <Button-group>
            <i-button type="primary">
                <Icon type="chevron-left"></Icon>
                前进
            </i-button>
            <i-button type="primary">
                后退
                <Icon type="chevron-right"></Icon>
            </i-button>
        </Button-group>
        <Button-group>
            <i-button type="primary" icon="ios-skipbackward"></i-button>
            <i-button type="primary" icon="ios-skipforward"></i-button>
        </Button-group>
        <Button-group>
            <i-button type="ghost" icon="ios-color-wand-outline"></i-button>
            <i-button type="ghost" icon="ios-sunny-outline"></i-button>
            <i-button type="ghost" icon="ios-crop"></i-button>
            <i-button type="ghost" icon="ios-color-filter-outline"></i-button>
        </Button-group>
        <br><br>
        <h4>圆角</h4>
        <br><br>
        <Button-group shape="circle">
            <i-button type="primary">
                <Icon type="chevron-left"></Icon>
                前进
            </i-button>
            <i-button type="primary">
                后退
                <Icon type="chevron-right"></Icon>
            </i-button>
        </Button-group>
        <Button-group shape="circle">
            <i-button type="primary" icon="ios-skipbackward"></i-button>
            <i-button type="primary" icon="ios-skipforward"></i-button>
        </Button-group>
        <Button-group shape="circle">
            <i-button type="ghost" icon="ios-color-wand-outline"></i-button>
            <i-button type="ghost" icon="ios-sunny-outline"></i-button>
            <i-button type="ghost" icon="ios-crop"></i-button>
            <i-button type="ghost" icon="ios-color-filter-outline"></i-button>
        </Button-group>
        <br><br>
        <h4>尺寸</h4>
        <br><br>
        <Button-group size="large">
            <i-button type="ghost">Large</i-button>
            <i-button type="ghost">Large</i-button>
        </Button-group>
        <Button-group>
            <i-button type="ghost">Default</i-button>
            <i-button type="ghost">Default</i-button>
        </Button-group>
        <Button-group size="small">
            <i-button type="ghost">Small</i-button>
            <i-button type="ghost">Small</i-button>
        </Button-group>
        <br><br>
        <Button-group size="large" shape="circle">
            <i-button type="ghost">Large</i-button>
            <i-button type="ghost">Large</i-button>
        </Button-group>
        <Button-group shape="circle">
            <i-button type="ghost">Default</i-button>
            <i-button type="ghost">Default</i-button>
        </Button-group>
        <Button-group size="small" shape="circle">
            <i-button type="ghost">Small</i-button>
            <i-button type="ghost">Small</i-button>
        </Button-group>
        <br/>


        <Button-group vertical>
            <i-button type="ghost" icon="social-facebook"></i-button>
            <i-button type="ghost" icon="social-twitter"></i-button>
            <i-button type="ghost" icon="social-googleplus"></i-button>
            <i-button type="ghost" icon="social-tumblr"></i-button>
        </Button-group>
        <br/>

<!--input 输入框-->
        <i-input :value.sync="value" placeholder="请输入..." style="width: 300px"></i-input>
        <br/>

        <i-input size="large" placeholder="large size"></i-input>
        <br>
        <i-input placeholder="default size"></i-input>
        <br>
        <i-input size="small" placeholder="small size"></i-input>
        <br/>


        <i-input icon="ios-clock-outline" placeholder="请输入..." style="width: 200px"></i-input>
        <br/>

        <i-input type="textarea" placeholder="请输入..."></i-input>
        <i-input type="textarea" :rows="4" placeholder="请输入..."></i-input>
        <br/>



        <i-input type="textarea" :autosize="true" placeholder="请输入..."></i-input>
        <i-input type="textarea" :autosize="{minRows: 2,maxRows: 5}" placeholder="请输入..."></i-input>
        <br/>



        <i-input disabled placeholder="请输入..."></i-input>
        <i-input disabled type="textarea" placeholder="请输入..."></i-input>
        <br/>



        <i-input>
            <span slot="prepend">http://</span>
            <span slot="append">.com</span>
        </i-input>
        <br>
        <i-input>
            <i-select :model.sync="select1" slot="prepend" style="width: 80px">
                <i-option value="http">http://</i-option>
                <i-option value="https">https://</i-option>
            </i-select>
            <i-select :model.sync="select2" slot="append" style="width: 70px">
                <i-option value="com">.com</i-option>
                <i-option value="org">.org</i-option>
                <i-option value="io">.io</i-option>
            </i-select>
        </i-input>
        <br>
        <i-input>
            <i-select :model.sync="select3" slot="prepend" style="width: 80px">
                <i-option value="day">日活</i-option>
                <i-option value="month">月活</i-option>
            </i-select>
            <i-button slot="append" icon="ios-search"></i-button>
        </i-input>
        <br/>


        <!--Radio 单选框-->
        <Radio :checked.sync="single">Radio</Radio>
        <br/>


        <Radio-group :model.sync="phone">
            <Radio value="apple">
                <Icon type="social-apple"></Icon>
                <span>Apple</span>
            </Radio>
            <Radio value="android">
                <Icon type="social-android"></Icon>
                <span>Android</span>
            </Radio>
            <Radio value="windows">
                <Icon type="social-windows"></Icon>
                <span>Windows</span>
            </Radio>
        </Radio-group>
        <Radio-group :model.sync="animal">
            <Radio value="金斑蝶"></Radio>
            <Radio value="爪哇犀牛"></Radio>
            <Radio value="印度黑羚"></Radio>
        </Radio-group>
        <br/>

        <Radio :checked.sync="disabledSingle" disabled>Radio</Radio>
        <Radio-group :model.sync="disabledGroup">
            <Radio value="金斑蝶" disabled></Radio>
            <Radio value="爪哇犀牛"></Radio>
            <Radio value="印度黑羚"></Radio>
        </Radio-group>
        <br/>

        <Radio-group :model.sync="vertical" vertical>
            <Radio value="apple">
                <Icon type="social-apple"></Icon>
                <span>Apple</span>
            </Radio>
            <Radio value="android">
                <Icon type="social-android"></Icon>
                <span>Android</span>
            </Radio>
            <Radio value="windows">
                <Icon type="social-windows"></Icon>
                <span>Windows</span>
            </Radio>
        </Radio-group>
        <br/>


        <Radio-group :model.sync="button1" type="button">
            <Radio value="北京"></Radio>
            <Radio value="上海"></Radio>
            <Radio value="深圳"></Radio>
            <Radio value="杭州"></Radio>
        </Radio-group>
        <Radio-group :model.sync="button2" type="button">
            <Radio value="北京"></Radio>
            <Radio value="上海" disabled></Radio>
            <Radio value="深圳"></Radio>
            <Radio value="杭州"></Radio>
        </Radio-group>
        <Radio-group :model.sync="button3" type="button">
            <Radio value="北京" disabled></Radio>
            <Radio value="上海" disabled></Radio>
            <Radio value="深圳" disabled></Radio>
            <Radio value="杭州" disabled></Radio>
        </Radio-group>
        <br/>

        <!--Checkbox 多选框-->
        <Checkbox-group :model.sync="social">
            <Checkbox value="twitter">
                <Icon type="social-twitter"></Icon>
                <span>Twitter</span>
            </Checkbox>
            <Checkbox value="facebook">
                <Icon type="social-facebook"></Icon>
                <span>Facebook</span>
            </Checkbox>
            <Checkbox value="github">
                <Icon type="social-github"></Icon>
                <span>Github</span>
            </Checkbox>
            <Checkbox value="snapchat">
                <Icon type="social-snapchat"></Icon>
                <span>Snapchat</span>
            </Checkbox>
        </Checkbox-group>
        <Checkbox-group :model.sync="fruit">
            <Checkbox value="香蕉"></Checkbox>
            <Checkbox value="苹果"></Checkbox>
            <Checkbox value="西瓜"></Checkbox>
        </Checkbox-group>
        <br/>

        <Checkbox :checked.sync="checked" :disabled="disabled">
            <span v-if="checked">选中</span>
            <span v-else>取消</span>
            -
            <span v-if="!disabled">可用</span>
            <span v-else>不可用</span>
        </Checkbox>
        <br>
        <i-button type="primary" @click="checked = !checked">
            <span v-if="!checked">选中</span>
            <span v-else>取消</span>
        </i-button>
        <i-button type="primary" @click="disabled = !disabled">
            <span v-if="disabled">可用</span>
            <span v-else>不可用</span>
        </i-button>
        <br/>

        <div style="border-bottom: 1px solid #e9e9e9;padding-bottom:6px;margin-bottom:6px;">
            <Checkbox
                    :indeterminate="indeterminate"
                    :checked="checkAll"
                    @click.prevent="handleCheckAll">全选</Checkbox>
        </div>
        <Checkbox-group :model.sync="checkAllGroup" @on-change="checkAllGroupChange">
            <Checkbox value="香蕉"></Checkbox>
            <Checkbox value="苹果"></Checkbox>
            <Checkbox value="西瓜"></Checkbox>
        </Checkbox-group>
        <br/>

        <!--Table 表格-->
        <i-table :columns="columns1" :data="data1"></i-table>
        <i-table stripe :columns="columns1" :data="data1"></i-table>
        <i-table border :columns="columns1" :data="data1"></i-table>















    </div>
</template>

<script>
    export default {

    };
</script>

<style>
    html {
        height: 100%;
    }
    
    body {
        display: flex;
        align-items: center;
        justify-content: center;
        height: 100%;
    }
    
    #app {
        color: #2c3e50;
        margin-top: -100px;
        max-width: 600px;
        font-family: Source Sans Pro, Helvetica, sans-serif;
        text-align: center;
    }
    
    #app a {
        color: #42b983;
        text-decoration: none;
    }
    
    .logo {
        width: 100px;
        height: 100px
    }
</style>