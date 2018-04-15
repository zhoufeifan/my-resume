<template>
    <header>
        <div class="resume-head">
            <section class="title">
                <div class="name">
                    <h1>周非凡</h1>
                </div>
                <div class="job">
                    <h2>Web前端工程师</h2>
                </div>
            </section>
            <section class="other-info">
                <div class="personal-info">
                    <ul>
                        <li>男 / 1992.10</li>
                        <li>浙江海洋大学 · 计算机科学与技术</li>
                        <li>本科 / 2016年毕业</li>
                        <li>期望薪资：15K</li>
                    </ul>
                </div>
                <div class="personal-contact">
                    <ul>
                        <li>
                            <a href="mailto:superzhou7@gmail.com">
                                <span class="contact-link">superzhou7@gmail.com</span>
                                <img class="iconfont" src="~assets/img/email.svg"/>
                            </a>
                        </li>
                        <li>
                            <a href="tel:1745324934">
                                <span class="contact-link">18368082630</span>
                                <img class="iconfont" src="~assets/img/phone.svg"/>
                            </a>
                        </li>
                        <li>
                            <a href="https://github.com/zhoufeifan">
                                <span class="contact-link">https://github.com/zhoufeifan</span>
                                <img class="iconfont" src="~assets/img/github.svg"/>
                            </a>
                        </li>
                        <li>
                            <a href="http://blog.zhoufeifan.tech/">
                                <span class="contact-link">blog.zhoufeifan.tech</span>
                                <img class="iconfont" src="~assets/img/blog.svg"/>
                            </a>
                        </li>
                    </ul>
                </div>
            </section>
        </div>
    </header>
</template>

<script>
    export default {
        name: 'Header',
    };
</script>

<style lang="scss" scoped>
    @import "~assets/mixin.scss";
    .resume-head {
        color: white;
        padding: 30px 50px;
        background-color: $mainColor;
        .title,.other-info{
            display: flex;
        }
        .title{
            border-bottom: 1px solid #dfdfdf;
            margin-bottom: 5px;
            padding-bottom: 5px;
        }
        .job{
            text-align: right;
        }
        .name,.job,.personal-contact,.personal-info{
            flex: 1;
        }
        .other-info{
            font-size: 14px;
            line-height: 22px;
            .personal-info{
                line-height: 22px;
            }
            .personal-contact{
                line-height: 22px;
                text-align: right;
                a{
                    color: white;
                }
                .iconfont{
                  vertical-align: sub;
                  margin-left: 2px;
                  width: 16px;
                }
            }
        }
    }
</style>
