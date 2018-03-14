<template>
    <header>
        <div class="resume-head">
            <section class="title">
                <div class="name">
                    <h1>王尼玛</h1>
                </div>
                <div class="job">
                    <h2>暴走大事件主持人</h2>
                </div>
            </section>
            <section class="other-info">
                <div class="personal-info">
                    <ul>
                        <li>男 / 1992.10</li>
                        <li>浙江海洋大学 · 计算机科学与技术</li>
                        <li>本科 / 2016年毕业</li>
                    </ul>
                </div>
                <div class="personal-contact">
                    <ul>
                        <li>
                            <a href="https://nima.com">
                                <span class="contact-link">gwuhaolin@icloud.com</span>
                                <img class="iconfont" src="~assets/img/github.svg"/>
                            </a>
                        </li>
                        <li>
                            <a href="mailto:gwuhaolin@icloud.com">
                                <span class="contact-link">gwuhaolin@icloud.com</span>
                                <img class="iconfont" src="~assets/img/github.svg"/>
                            </a>
                        </li>
                        <li>
                            <a href="tel:1745324934">
                                <span class="contact-link">18681569574</span>
                                <img class="iconfont" src="~assets/img/github.svg"/>
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
                    vertical-align: middle;
                    margin-left: 2px;
                }
            }
        }
    }
</style>
