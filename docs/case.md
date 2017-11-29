# 简易电子邀请函页面设计

## 一、电子邀请函页面的功能：

- 电子邀请函首先环保和电煤是时代的趋势，在外人看来利用互联网进行传播的个人或企业必定是跟得上时代的，且传播很方便咯；其次，电子邀请函是动态直观的，可以比传统邀请函更有创意，而且现在电子邀请函制作平台那么多，操作也很简单。

## 二、设计思路：

- 整个页面分为会议主题、会议内容、会议组织、主讲嘉宾、会议地址5个部分，由于这个页面面对的客户可能是电脑用户也可能是手机用户，因此布局采用响应式布局，框架选择 foundation 框架。
- 背景效果采用幻灯片效果，vegas 是 BootCDN 开发的一款让背景具有幻灯片效果的 CSS。 
- 页面切换效果采用的是 jQuery 的全屏滚动插件 jquery.fullPage.js。
- 背景音乐采用的是 jquery 的 jquery.jplayer.js 插件。

##三、设计步骤

### Index . html

- 字体属性

  - ```
    <link rel="stylesheet" href="./css/pageloader.css">
    <link rel="stylesheet" href="./fonts/opensans/stylesheet.css">
    <link rel="stylesheet" href="./fonts/asap/stylesheet.css">
    <link rel="stylesheet" href="./css/ionicons.min.css">
    ```

- 框架

  - ```
    <link rel="stylesheet" href="./css/foundation.min.css">
    <link rel="stylesheet" href="./js/vendor/jquery.fullPage.css">
    <link rel="stylesheet" href="./js/vegas/vegas.min.css">
    ```

- Jplayer 相关属性

  - ```
    #jp_container_1 { position: fixed; top: 5%; left: 2% }
    #jp_container_1 a { font-size: 26px; color: #ffffff }
    #jp_container_1 a:hover { color: #f4645f }
    ```

- 加载页面

  - ```
    <div class="page-loader" id="page-loader">
        <div><i class="ion ion-loading-d"></i>
        <p>第二届未来计算机国际研讨会</p>
        </div>
    </div>
    ```

- 背景循环

  - ```
    <div class="page-cover" id="s-cover">
              <div class="cover-bg pos-abs full-size slide-show">
                  <i class='img' data-src='./img/bg-slide3.jpg'></i>
                  <i class='img' data-src='./img/bg-slide2.jpg'></i>
                  <i class='img' data-src='./img/bg-slide1.jpg'></i> 
              </div>
              <div class="cover-bg-mask pos-abs full-size bg-color" data-bgcolor="rgba(0, 0, 0, 0.41)"></div>
    </div>
    ```

- 计时器

  - ```
    <div class="pane-when " id="s-when">
        <div class="content"> 
            <div class="clock clock-countdown">
                  <div class="site-config" data-date="1/1/2018 14:00:00" data-date-timezone="+8"></div>
                <div class="elem-center">
                    <div class="digit">
                    <span class="days">81</span>
                    <span class="txt">天</span> 
                    </div>
                 </div>
                <div class="elem-bottom">
                    <div class="deco"></div>
                    <span class="hours">18</span>
                    <span class="thin">小时</span> 
                    <span class="minutes">45</span>
                    <span class="thin">分钟</span>
                    <span class="seconds">36</span>
                    <span class="thin">秒</span>
                </div>
            </div>
        <footer>
                  <p>2018年 <strong>1月1日</strong></p>
        </footer>
        </div>
    </div>
    ```

- 主页

  - ```
    <div class="section page-home page page-cent" id="s-home">
        <section class="content">
            <header class="header">
                <div class="h-left">
                    <h2>诚邀参加</h2>
                </div>
                <div class="h-right">
                    <h3>第二届未来计算机</h3>
                    <h4 class="subhead"><a href="#register">国际研讨会</a></h4>
                </div>
            </header>
        </section>
        <footer class="p-footer p-scrolldown">
            <a href="#register">
                <div class="arrow-d">
                    <div class="before">Scroll</div>
                    <div class="after">Down</div>
                    <div class="circle">
                        <i class="ion ion-mouse"></i>
                    </div>
                </div>
            </a>
        </footer>
    </div>
    ```

- 第二页

  - ```
    <div class="section page-register page page-cent"  id="s-register">
        <section class="content">
            <header class="p-title">
                <h3>会议内容：<i class="ion ion-compose"></i></h3>
            </header>
            <div>
                <p class="invite"><br/>第二届国际计算机会议将于2018年1月1日在XXX召开，会议秉承xxx的会议理念</p>
            </div>
        </section>
        <footer class="p-footer p-scrolldown">
            <a href="#about-us">
                <div class="arrow-d">
                    <div class="before">About</div>
                    <div class="after">Lorem</div>
                    <div class="circle">
                        <i class="ion ion-mouse"></i></div>
                </div>
            </a>
        </footer>
    </div>
    ```

- 第三页

  - ```
    <div class="section page-about page page-cent" >
        <section class="content">
            <header class="p-title">
                <h3>会议组织：
                    <i class="ion ion-android-information"> </i>
                </h3>
                <h4 class="subhead">大会主席：
                    <article class="text">
                        <p>中国工程院院士  中南大学</p>
                        <p>加拿大三院院士  滑铁卢教授</p>
                    </article>
                </h4>
                <h4 class="subhead">会议组织组织委员会主席：
                    <article class="text">
                        <p>XXXXXXXXXXXXXXXXX</p>
                        <p>XXXXXXXXXXXXXXXXX</p>
                    </article>
                </h4>
            </header>
        </section>
        <footer class="p-footer p-scrolldown">
            <a href="#contact">
                <div class="arrow-d">
                    <div class="before">Contact</div>
                    <div class="after">Message</div>
                    <div class="circle">
                        <i class="ion ion-mouse"></i>
                    </div>
                </div>
            </a>
        </footer>
    </div>
    ```

- 第四页

  - ```
    <div class="section page-about page page-cent" >
        <section class="content">
            <header class="p-title">
                <h3>主讲嘉宾 <i class="ion ion-android-information"> </i> </h3>
            </header>
            <div>
                <img  src="../img/test.png" class="a" >
                <p class="subhead">XXXXXXXXXXXXXXXX</p>
            </div>
            <div>
                <img  src="../img/test.png" class="a" >
                <p class="subhead">..............</p>
            </div>
        </section>
        <footer class="p-footer p-scrolldown">
            <a href="#contact">
            <div class="arrow-d">
                <div class="before">Contact</div>
                <div class="after">Message</div>
                <div class="circle"><i class="ion ion-mouse"></i></div>
            </div>
            </a>
        </footer>
    </div>
    ```

- 第五页

  - ```
    <div class="section page-contact page page-cent  bg-color" data-bgcolor="rgba(95, 25, 208, 0.88)s" id="s-contact">
        <div class="slide" id="s-information" data-anchor="information">
            <section class="content">
                <header class="p-title">
                    <h3>地址<i class="ion ion-location"> </i> </h3>
                    <ul class="buttons">
                        <li class="show-for-medium-up">
                            <a title="About" href="#about-us" >
                                <i class="ion ion-android-information"></i>
                            </a>
                        </li>
                        <li>
                            <a title="Message" href="#contact/message">
                                <i class="ion ion-email"></i>
                            </a>
                        </li>
                    </ul>
                </header>
                <div class="contact">
                    <div class="row">
                        <div class="medium-6 columns left">
                            <ul>
                                <li>
                                    <h4>会议地点：</h4>
                                    <p>西华大学</p>
                                </li>
                                <li>
                                    <h4>地址：</h4>
                                    <p>xxx路999号 <br>红光广场</p>
                                </li>
                                <li>
                                    <h4>学校电话</h4>
                                    <p> 028-xxxxxxxxxx</p>
                                </li>
                            </ul>
                        </div>
                        <div class="medium-6 columns social-links right">
                            <ul>
                                <li class="show-for-medium-up">
                                    <h4>查看地图</h4>
                                    <p>
                                        <a href="http://map.baidu.com/?newmap=1&s=inf&uid=a61500c52fa38761f72310b0&wd=%E8%A5%BF%E5%8D%8E%E5%A4%A7%E5%AD%A6&all=1&c=86&from=alamap&tpl=map_singlepoint" target="_blank">点击查看在线地图</a>
                                    </p>
                                </li>
                                </li>
                                <li>
                                    <p class="small"><strong>期待您的到场！</strong></p>
                                </li>
                            </ul>
                        </div>
                    </div>
                </div>
            </section>
        </div>
        <div class="slide" id="s-message" data-anchor="message">
            <section class="content">
                <header class="p-title">
                    <li class="show-for-medium-up">
                        <a title="About" href="#about-us">
                            <i class="ion ion-android-information"></i>
                        </a>
                    </li>
                    <li>
                        <a title="Contact" href="#contact/information">
                            <i class="ion ion-location"></i>
                        </a>
                    </li>
                </header>
            </section>
        </div>
    </div>
    ```

