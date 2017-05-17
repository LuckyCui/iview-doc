<template>
    <i-article>
        <article>
            <h1>Menu</h1>
            <Anchor title="Brief Introduction" h2></Anchor>
            <p>Provide navigation menu for web pages. Usually located at the top or the left side of the page.</p>
            <blockquote>Attention：Use <code>i-menu</code> if not under template/render mode.</blockquote>
            <Anchor title="Examples" h2></Anchor>
            <Demo title="Head Navigator" vertical hide-code>
                <div slot="demo">
                    <Menu mode="horizontal" :theme="theme1" active-name="1">
                        <Menu-item name="1">
                            <Icon type="ios-paper"></Icon>
                            内容管理
                        </Menu-item>
                        <Menu-item name="2">
                            <Icon type="ios-people"></Icon>
                            用户管理
                        </Menu-item>
                        <Submenu name="3">
                            <template slot="title">
                                <Icon type="stats-bars"></Icon>
                                统计分析
                            </template>
                            <Menu-group title="使用">
                                <Menu-item name="3-1">新增和启动</Menu-item>
                                <Menu-item name="3-2">活跃分析</Menu-item>
                                <Menu-item name="3-3">时段分析</Menu-item>
                            </Menu-group>
                            <Menu-group title="留存">
                                <Menu-item name="3-4">用户留存</Menu-item>
                                <Menu-item name="3-5">流失用户</Menu-item>
                            </Menu-group>
                        </Submenu>
                        <Menu-item name="4">
                            <Icon type="settings"></Icon>
                            综合设置
                        </Menu-item>
                    </Menu>
                    <br>
                    <p>切换主题</p>
                    <Radio-group v-model="theme1">
                        <Radio label="light"></Radio>
                        <Radio label="dark"></Radio>
                        <Radio label="primary"></Radio>
                    </Radio-group>
                </div>
                <div slot="desc">
                    <p>Horizontal head navigation menu.</p>
                    <p>Select a theme by setting <code>theme</code> prop to <code>light</code>, <code>dark</code>, <code>primary</code>.</p>
                    <p>Set <code>on-select</code> event to get the name of the clicked menu item, then you can control the router or do custom operations.</p>
                </div>
                <i-code lang="html" slot="code">{{ code.base }}</i-code>
            </Demo>
            <Demo title="Side Navigator" vertical hide-code>
                <div slot="demo">
                    <Row>
                        <Col span="8">
                            <Menu :theme="theme2">
                                <Submenu name="1">
                                    <template slot="title">
                                        <Icon type="ios-paper"></Icon>
                                        内容管理
                                    </template>
                                    <Menu-item name="1-1">文章管理</Menu-item>
                                    <Menu-item name="1-2">评论管理</Menu-item>
                                    <Menu-item name="1-3">举报管理</Menu-item>
                                </Submenu>
                                <Submenu name="2">
                                    <template slot="title">
                                        <Icon type="ios-people"></Icon>
                                        用户管理
                                    </template>
                                    <Menu-item name="2-1">新增用户</Menu-item>
                                    <Menu-item name="2-2">活跃用户</Menu-item>
                                </Submenu>
                                <Submenu name="3">
                                    <template slot="title">
                                        <Icon type="stats-bars"></Icon>
                                        统计分析
                                    </template>
                                    <Menu-group title="使用">
                                        <Menu-item name="3-1">新增和启动</Menu-item>
                                        <Menu-item name="3-2">活跃分析</Menu-item>
                                        <Menu-item name="3-3">时段分析</Menu-item>
                                    </Menu-group>
                                    <Menu-group title="留存">
                                        <Menu-item name="3-4">用户留存</Menu-item>
                                        <Menu-item name="3-5">流失用户</Menu-item>
                                    </Menu-group>
                                </Submenu>
                            </Menu>
                        </Col>
                        <Col span="8">
                            <Menu :theme="theme2" active-name="1-2" :open-names="['1']">
                                <Submenu name="1">
                                    <template slot="title">
                                        <Icon type="ios-paper"></Icon>
                                        内容管理
                                    </template>
                                    <Menu-item name="1-1">文章管理</Menu-item>
                                    <Menu-item name="1-2">评论管理</Menu-item>
                                    <Menu-item name="1-3">举报管理</Menu-item>
                                </Submenu>
                                <Submenu name="2">
                                    <template slot="title">
                                        <Icon type="ios-people"></Icon>
                                        用户管理
                                    </template>
                                    <Menu-item name="2-1">新增用户</Menu-item>
                                    <Menu-item name="2-2">活跃用户</Menu-item>
                                </Submenu>
                                <Submenu name="3">
                                    <template slot="title">
                                        <Icon type="stats-bars"></Icon>
                                        统计分析
                                    </template>
                                    <Menu-group title="使用">
                                        <Menu-item name="3-1">新增和启动</Menu-item>
                                        <Menu-item name="3-2">活跃分析</Menu-item>
                                        <Menu-item name="3-3">时段分析</Menu-item>
                                    </Menu-group>
                                    <Menu-group title="留存">
                                        <Menu-item name="3-4">用户留存</Menu-item>
                                        <Menu-item name="3-5">流失用户</Menu-item>
                                    </Menu-group>
                                </Submenu>
                            </Menu>
                        </Col>
                        <Col span="8">
                            <Menu :theme="theme2" :open-names="['1']" accordion>
                                <Submenu name="1">
                                    <template slot="title">
                                        <Icon type="ios-paper"></Icon>
                                        内容管理
                                    </template>
                                    <Menu-item name="1-1">文章管理</Menu-item>
                                    <Menu-item name="1-2">评论管理</Menu-item>
                                    <Menu-item name="1-3">举报管理</Menu-item>
                                </Submenu>
                                <Submenu name="2">
                                    <template slot="title">
                                        <Icon type="ios-people"></Icon>
                                        用户管理
                                    </template>
                                    <Menu-item name="2-1">新增用户</Menu-item>
                                    <Menu-item name="2-2">活跃用户</Menu-item>
                                </Submenu>
                                <Submenu name="3">
                                    <template slot="title">
                                        <Icon type="stats-bars"></Icon>
                                        统计分析
                                    </template>
                                    <Menu-group title="使用">
                                        <Menu-item name="3-1">新增和启动</Menu-item>
                                        <Menu-item name="3-2">活跃分析</Menu-item>
                                        <Menu-item name="3-3">时段分析</Menu-item>
                                    </Menu-group>
                                    <Menu-group title="留存">
                                        <Menu-item name="3-4">用户留存</Menu-item>
                                        <Menu-item name="3-5">流失用户</Menu-item>
                                    </Menu-group>
                                </Submenu>
                            </Menu>
                        </Col>
                    </Row>
                    <br>
                    <p>切换主题</p>
                    <Radio-group v-model="theme2">
                        <Radio label="light"></Radio>
                        <Radio label="dark"></Radio>
                    </Radio-group>
                </div>
                <div slot="desc">
                    <p>Vertical navigation menu which can includes sub menus.</p>
                    <p>Set <code>active-name</code> to set the selected menu item. Set <code>open-names</code> to expand the selected sub menu.</p>
                    <p>Set <code>accordion</code> prop to open  accordion mode. Which means only one sub menu can be expanded at the same time.</p>
                    <p>Set <code>theme</code> prop to <code>light</code>, <code>dark</code> to choose a theme, but it doesn't support primary theme.</p>
                </div>
                <i-code lang="html" slot="code">{{ code.vertical }}</i-code>
            </Demo>
            <Demo title="Menu Group" vertical hide-code>
                <div slot="demo">
                    <Menu :theme="theme3" active-name="1">
                        <Menu-group title="内容管理">
                            <Menu-item name="1">
                                <Icon type="document-text"></Icon>
                                文章管理
                            </Menu-item>
                            <Menu-item name="2">
                                <Icon type="chatbubbles"></Icon>
                                评论管理
                            </Menu-item>
                        </Menu-group>
                        <Menu-group title="统计分析">
                            <Menu-item name="3">
                                <Icon type="heart"></Icon>
                                用户留存
                            </Menu-item>
                            <Menu-item name="4">
                                <Icon type="heart-broken"></Icon>
                                流失用户
                            </Menu-item>
                        </Menu-group>
                    </Menu>
                    <br>
                    <p>切换主题</p>
                    <Radio-group v-model="theme3">
                        <Radio label="light"></Radio>
                        <Radio label="dark"></Radio>
                    </Radio-group>
                </div>
                <div slot="desc">
                    <p>Use <code>Menu-group</code> to group the menus. Attention:</p>
                    <ul>
                        <li> <code>Menu-group</code> can only be used in <code>Menu</code> and <code>Submenu</code>.</li>
                        <li> <code>Submenu</code> can only be used in <code>Menu</code>. It cannot be used in <code>Menu-group</code> or <code>Menu-item</code>.</li>
                    </ul>
                </div>
                <i-code lang="html" slot="code">{{ code.group }}</i-code>
            </Demo>
            <div class="api">
                <Anchor title="API" h2></Anchor>
                <Anchor title="Menu props" h3></Anchor>
                <table>
                    <thead>
                        <tr>
                            <th>Property</th>
                            <th>Description</th>
                            <th>Type</th>
                            <th>Default</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>mode</td>
                            <td>The mode of the menu. Optional: <code>horizontal</code>, <code>vertical</code></td>
                            <td>String</td>
                            <td>vertical</td>
                        </tr>
                        <tr>
                            <td>theme</td>
                            <td>Theme. Optional: <code>light</code>, <code>dark</code>, <code>primary</code>, primary can only be used when <code>mode="horizontal"</code></td>
                            <td>String</td>
                            <td>light</td>
                        </tr>
                        <tr>
                            <td>active-name</td>
                            <td>The name of the menu item that is active.</td>
                            <td>String | Number</td>
                            <td>-</td>
                        </tr>
                        <tr>
                            <td>open-names</td>
                            <td>The array of expanded Submenu's name.</td>
                            <td>Array</td>
                            <td>[]</td>
                        </tr>
                        <tr>
                            <td>accordion</td>
                            <td>Enable accordion mode or not. If true, only one Submenu can be expanded at the same time.</td>
                            <td>Boolean</td>
                            <td>false</td>
                        </tr>
                        <tr>
                            <td>width</td>
                            <td>The width of the navigation menu. It only works when <code>mode="vertical"</code>. We recommend you to set it to <code>auto</code> if you're using layouts like <code>Col</code>.</td>
                            <td>String</td>
                            <td>240px</td>
                        </tr>
                    </tbody>
                </table>
                <Anchor title="Menu events" h3></Anchor>
                <table>
                    <thead>
                        <tr>
                            <th>Event Name</th>
                            <th>Description</th>
                            <th>Return Value</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>on-select</td>
                            <td>Emit when select(click) the menu-item.</td>
                            <td>name</td>
                        </tr>
                        <tr>
                            <td>on-open-change</td>
                            <td>Emit when expand / fold the Submenu.</td>
                            <td>An array which includes the name of expanded Submenus</td>
                        </tr>
                    </tbody>
                </table>
                <Anchor title="Menu methods" h3></Anchor>
                <table>
                    <thead>
                        <tr>
                            <th>Method Name</th>
                            <th>Description</th>
                            <th>Parameter</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>updateOpened</td>
                            <td>Update expanded Submenus manually.Attention: Call it in $nextTick.</td>
                            <td>-</td>
                        </tr>
                        <tr>
                            <td>updateActiveName</td>
                            <td>Update selected menu-item manually.Attention: Call it in $nextTick.</td>
                            <td>-</td>
                        </tr>
                    </tbody>
                </table>
                <Anchor title="MenuItem props" h3></Anchor>
                <table>
                    <thead>
                        <tr>
                            <th>Property</th>
                            <th>Description</th>
                            <th>Type</th>
                            <th>Default</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>name</td>
                            <td>Unique identifier of menu-item. Required.</td>
                            <td>String | Number</td>
                            <td>-</td>
                        </tr>
                    </tbody>
                </table>
                <Anchor title="Submenu props" h3></Anchor>
                <table>
                    <thead>
                        <tr>
                            <th>Property</th>
                            <th>Description</th>
                            <th>Type</th>
                            <th>Default</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>name</td>
                            <td>Unique identifier of Submenu. Required.</td>
                            <td>String | Number</td>
                            <td>-</td>
                        </tr>
                    </tbody>
                </table>
                <Anchor title="Submenu slot" h3></Anchor>
                <table>
                    <thead>
                        <tr>
                            <th>Name</th>
                            <th>Description</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>-</td>
                            <td>Menu Item</td>
                        </tr>
                        <tr>
                            <td>title</td>
                            <td>Submenu Title</td>
                        </tr>
                    </tbody>
                </table>
                <Anchor title="MenuGroup props" h3></Anchor>
                <table>
                    <thead>
                        <tr>
                            <th>Property</th>
                            <th>Description</th>
                            <th>Type</th>
                            <th>Default</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td>title</td>
                            <td>Group Title</td>
                            <td>String</td>
                            <td>-</td>
                        </tr>
                    </tbody>
                </table>
            </div>
        </article>
    </i-article>
</template>
<script>
    import iArticle from '../../components/article.vue';
    import iCode from 'iCode';
    import Demo from '../../components/demo.vue';
    import Code from '../../code/menu';
    import Anchor from '../../components/anchor.vue';

    export default {
        components: {
            iArticle,
            iCode,
            Demo,
            Anchor
        },
        data () {
            return {
                code: Code,
                theme1: 'light',
                theme2: 'light',
                theme3: 'light'
            }
        },
        methods: {

        }
    }
</script>