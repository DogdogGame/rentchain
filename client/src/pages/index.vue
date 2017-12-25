<template>
  <div class="index">
    <div class="index_header">
      <tab class="index_tab" defaultColor="#fff" active-color="#ff6649">
        <tab-item selected>
          <span>
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-qiuzu"></use>
            </svg>
          </span>
          <span>综合</span>
        </tab-item>
        <tab-item>
          <span>
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-xunzhaozufangxuqiu"></use>
            </svg>
          </span>
          <span>求租</span>
        </tab-item>
        <tab-item>
          <span>
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-fabuzufangxuqiu"></use>
            </svg>
          </span>
          <span>出租</span>
        </tab-item>
      </tab>
    </div>
    <div class="index_item">
      <view-box>
        <div class="item_box" v-for="i in 10">
          <flexbox>
            <flexbox-item :span="2">
              <div class="user_avator_box">
                <img src="http://via.placeholder.com/50x50" alt="">
              </div>
            </flexbox-item>
            <flexbox-item>
              <div class="user_info_box">
                <div class="name_box">
                  <span>lwsq</span>
                  <span>|</span>
                  <span>#{{i % 2 == 0 ? '出租' : '租房'}}</span>
                </div>
                <div class="date_box">
                  <span>1998-01-26 06:05:50</span>
                </div>
              </div>
            </flexbox-item>
          </flexbox>
          <flexbox>
            <flexbox-item>
              <p class="content_info">
                Lorem ipsum dolor sit amet, consectetur adipisicing elit. Inventore facere excepturi perspiciatis voluptatem molestias, nulla nesciunt nostrum error. Praesentium libero assumenda cupiditate, blanditiis saepe labore id fugiat est iste! Blanditiis!
              </p>
            </flexbox-item>
          </flexbox>
          <flexbox class="item_img_box" v-if="i % 2 == 0">
            <flexbox-item>
              <img src="http://via.placeholder.com/100x100" class="item_info_img" alt="">
            </flexbox-item>
            <flexbox-item>
              <img src="http://via.placeholder.com/100x100" class="item_info_img" alt="">
            </flexbox-item>
            <flexbox-item>
              <img src="http://via.placeholder.com/100x100" class="item_info_img" alt="">
            </flexbox-item>
          </flexbox>
          <flexbox>
            <flexbox-item>
              <div class="hr"></div>
            </flexbox-item>
          </flexbox>
          <flexbox>
            <flexbox-item>
              <div class="item_see_box">
                <svg class="icon" aria-hidden="true">
                  <use xlink:href="#icon-liulan2"></use>
                </svg>
                <span>3972</span>
              </div>
            </flexbox-item>
            <flexbox-item>
            </flexbox-item>
            <flexbox-item>
              <div class="item_see_box">
                <svg class="icon" aria-hidden="true" v-if="false">
                  <use xlink:href="#icon-xihuan"></use>
                </svg>
                <svg class="icon" aria-hidden="true">
                  <use xlink:href="#icon-xihuan1"></use>
                </svg>
                <span>3972</span>
              </div>
            </flexbox-item>
            <flexbox-item>
              <div class="item_see_box">
                <svg class="icon" aria-hidden="true">
                  <use xlink:href="#icon-pinglun"></use>
                </svg>
                <span>3972</span>
              </div>
            </flexbox-item>
          </flexbox>
        </div>
      </view-box>
    </div>
    <div class="index_footer">
      <tabbar defaultColor="#333" active-color="#ff6649">
        <tabbar-item :selected="true">
          <span slot="icon" class="footer_icon_box">
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-zhuye1"></use>
            </svg>
          </span>
          <span slot="icon-active" class="footer_icon_box icon-active">
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-zhuyetc"></use>
            </svg>
          </span>
          <span slot="label" class="footer_label_box">主页</span>
        </tabbar-item>
        <tabbar-item>
          <div slot="icon" class="footer_more_icon_box">
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-add-more"></use>
            </svg>
          </div>
        </tabbar-item>
        <tabbar-item>
          <span slot="icon" class="footer_icon_box">
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-wode1"></use>
            </svg>
          </span>
          <span slot="icon-active" class="footer_icon_box icon-active">
            <svg class="icon" aria-hidden="true">
              <use xlink:href="#icon-wode2"></use>
            </svg>
          </span>
          <span slot="label" class="footer_label_box">我的</span>
        </tabbar-item>
      </tabbar>
    </div>
  </div>
</template>

<script>
  import { Tab, TabItem, ViewBox, Tabbar, TabbarItem, Flexbox, FlexboxItem } from 'vux'
  export default {
    name: 'Index',
    components:{
      Tab,
      TabItem,
      ViewBox,
      Tabbar,
      TabbarItem,
      Flexbox,
      FlexboxItem
    }
  }
</script>

<style scoped>
.index_tab{
  background: #333;
}
.index_footer{
  background: #333;
}

.index_item{
  height: 100%;
  width: 100%;
  overflow-x: hidden;
}
.item_box{
  background: #fff;
  padding: 10px 10px 5px 15px;
  box-shadow: 2px 2px 3px #aaa;
  margin-bottom: 15px;
}
.user_avator_box{
}
.user_avator_box img{
  width: 3.6rem;
  height: 3.6rem;
  border-radius: 3.6rem;
}
.user_info_box{
  font-size: 14px;
  margin-left: 5px;
}
.name_box{
  color: #777;
}
.date_box{
  color: #aaa;
}
.content_info{
  color: #333;
  font-size: 12px;
}
.item_img_box{
  text-align: center;
}
.hr{
  height: 1px;
  background: rgba(200, 200, 200, 0.7);
  width: 100%;
  margin-bottom: 6px;
}
.item_see_box{
  font-size: 12px;
}
.footer_icon_box .icon{
  font-size: 18px;
}
.footer_more_icon_box{
  background: #333;
  width: 45px;
  height: 45px;
  margin-left: -10px;
  line-height: 60px;
  border-radius: 50%;
}
.footer_more_icon_box .icon{
  font-size: 22px;
}
.icon-active{
  color: #ff6649;
}
.footer_label_box{
  color: #777;
}
</style>


