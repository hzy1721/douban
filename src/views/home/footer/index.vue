<script>
export default {
  name: "FooterSection",
  data() {
    return {
      footerNavs: [
        { title: "关于豆瓣", link: "https://www.douban.com/about" },
        { title: "在豆瓣工作", link: "https://www.douban.com/jobs" },
        {
          title: "联系我们",
          link: "https://www.douban.com/about?topic=contactus",
        },
        { title: "法律声明", link: "https://www.douban.com/about/legal" },
        { title: "帮助中心", link: "https://help.douban.com/?app=main" },
        { title: "移动应用", link: "https://www.douban.com/doubanapp/" },
        { title: "豆瓣广告", link: "https://www.douban.com/partner/" },
      ],
    };
  },
};
</script>

<template>
  <div class="footer-section">
    <div class="footer-content">
      <div>
        <div style="display: inline-block; width: 50%">
          © 2005－2022 douban.com, all rights reserved 北京豆网科技有限公司
        </div>

        <div style="display: inline-block; width: 50%; text-align: right">
          <span v-for="(nav, index) in footerNavs">
            <span v-if="index > 0"> · </span>
            <a :href="nav.link">{{ nav.title }}</a>
          </span>
        </div>
      </div>

      <div>
        <a
          href="https://img9.doubanio.com/view/treasury_image/raw/public/8f4d0a09fd60834.jpg"
        >
          营业执照
        </a>
        <a href="https://beian.miit.gov.cn/">京ICP证090015号</a>&nbsp;
        <a href="https://beian.miit.gov.cn/">京ICP备11027288号</a>&nbsp;
        <a href="https://www.douban.com/about?topic=licence"
          >网络视听许可证0110418号</a
        >
      </div>

      <div>
        京网文[2021]2980-826号
        <a
          href="https://img3.doubanio.com/f/shire/80d71f876c40a3ecdfde2fe2afe3b1983a2cac64/pics/licence/publication2018.png"
        >
          新出发京批字第直160029号
        </a>
        （署）网出证（京）字第120号
      </div>

      <div>
        违法和不良信息/涉未成年人有害信息投诉:
        <img loading="lazy"
          src="@/assets/home/footer/tousu_email.jpeg"
          style="height: 16px; vertical-align: top"
        />
      </div>

      <div>违法和不良信息投诉电话：4008353331-9</div>

      <div>
        网络从业者不良行为举报:
        <img loading="lazy"
          src="@/assets/home/footer/jubao_email.jpeg"
          style="height: 16px; vertical-align: top"
        />
      </div>

      <div>
        <img loading="lazy"
          src="@/assets/home/footer/jubao_center_logo.png"
          style="height: 15px; vertical-align: top"
        />

        <a href="http://www.12377.cn/">中国互联网举报中心</a>

        电话：12377

        <img loading="lazy"
          src="@/assets/home/footer/biaoshi.gif"
          style="height: 16px; vertical-align: top"
        />

        <a
          href="http://www.beian.gov.cn/portal/registerSystemInfo?recordcode=11010502000728"
        >
          京公网安备11010502000728
        </a>
      </div>
    </div>
  </div>
</template>

<style>
.footer-section {
  padding-top: 25px;
  padding-bottom: 35px;
}

.footer-content {
  width: 950px;
  margin: 0 auto;
  border-top: 1px dashed #dcdcdc;
  padding: 14px 0;
  color: #999;
}
</style>
