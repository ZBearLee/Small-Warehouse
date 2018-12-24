<template>
  <div class="animation-container">
    <div class="patient-list patient-list-new">
      <transition name="rectangle-transform">
        <div class="list-bar nbs-unselect bar-unfold" @click="patientListShow()">
          <div class="info">
            <div>待入院</div>
            <div>
              患者列表(
              <em class="num">8</em>)
            </div>
          </div>
          <div class="info-right">
            <span class="icon-person">
              <img src="@/assets/img/animation/icon_inhos_person.png">
            </span>
            <span class="icon-right">
              <img src="@/assets/img/animation/icon_inhos_list_right.png">
            </span>
          </div>
        </div>
      </transition>
      <div class="list-data" style="display: block;" v-show="isPatientListShow">
        <div class="title">
          <span style="padding-right:2px">
            <img src="@/assets/img/animation/discharge_leftbar_list.png">
          </span>
          <span>
            待出院患者(
            <em class="num">8</em>人)
          </span>
        </div>
        <div
          class="list list-data-scrollbar"
          data-scrollbar="true"
          tabindex="1"
          style="overflow: hidden; outline: none; height: auto;"
        >
          <div class="scroll-content">
            <ul>
              <li puid="8024f0d0ba2311e89a828c16451ca2b6">
                <div class="content">
                  <div class="inline">
                    <span class="name">刘斯萍</span>
                    <span class="sex"></span>
                    <span class="age">45岁</span>
                  </div>
                  <div class="inline">
                    <span class="inpatno">729425</span>
                    <span class="step nbs-unselect">第1步</span>
                  </div>
                </div>
              </li>
              <li puid="bf17eed032bd4a228fa91f547f482d3f">
                <div class="content">
                  <div class="inline">
                    <span class="name">肖保丽</span>
                    <span class="sex"></span>
                    <span class="age">40岁</span>
                  </div>
                  <div class="inline">
                    <span class="inpatno">563514</span>
                    <span class="step nbs-unselect">第4步</span>
                  </div>
                </div>
              </li>
              <li puid="32c13b3f54e34cc0bd3cdc411a5e7e62">
                <div class="content">
                  <div class="inline">
                    <span class="name">曹运平</span>
                    <span class="sex"></span>
                    <span class="age">54岁</span>
                  </div>
                  <div class="inline">
                    <span class="inpatno">563513</span>
                  </div>
                </div>
              </li>
              <li puid="3974215e3a4a47ec8da16df196789cf8">
                <div class="content">
                  <div class="inline">
                    <span class="name">蒋有荣</span>
                    <span class="sex"></span>
                    <span class="age">44岁</span>
                  </div>
                  <div class="inline">
                    <span class="inpatno">563499</span>
                    <span class="step nbs-unselect">第3步</span>
                  </div>
                </div>
              </li>
              <li puid="7f31bf749a764123a3f981c7e533cad2">
                <div class="content">
                  <div class="inline">
                    <span class="name">邱群</span>
                    <span class="sex"></span>
                    <span class="age">62岁</span>
                  </div>
                  <div class="inline">
                    <span class="inpatno">563491</span>
                    <span class="step nbs-unselect">第1步</span>
                  </div>
                </div>
              </li>
              <li puid="962e97d8a4354a3c9ada1d0ab19c91ab">
                <div class="content">
                  <div class="inline">
                    <span class="name">何绪炳</span>
                    <span class="sex"></span>
                    <span class="age">50岁</span>
                  </div>
                  <div class="inline">
                    <span class="inpatno">563461</span>
                    <span class="step nbs-unselect">第2步</span>
                  </div>
                </div>
              </li>
              <li puid="1b1cec72b7204796ba2afc0257f54b77">
                <div class="content">
                  <div class="inline">
                    <span class="name">汪春华</span>
                    <span class="sex"></span>
                    <span class="age">57岁</span>
                  </div>
                  <div class="inline">
                    <span class="inpatno">563457</span>
                    <span class="step nbs-unselect">第2步</span>
                  </div>
                </div>
              </li>
              <li puid="b39a2106dcfa43e29f612e17be6989d0">
                <div class="content">
                  <div class="inline">
                    <span class="name">黄汉铭</span>
                    <span class="sex"></span>
                    <span class="age">21岁</span>
                  </div>
                  <div class="inline">
                    <span class="inpatno">563455</span>
                    <span class="step nbs-unselect">第4步</span>
                  </div>
                </div>
              </li>
            </ul>
            <div class="scrollbar-track scrollbar-track-x">
              <div class="scrollbar-thumb scrollbar-thumb-x"></div>
            </div>
            <div class="scrollbar-track scrollbar-track-y">
              <div class="scrollbar-thumb scrollbar-thumb-y"></div>
            </div>
          </div>
          <div class="scrollbar-track scrollbar-track-x" style="display: none;">
            <div
              class="scrollbar-thumb scrollbar-thumb-x"
              style="width: 169px; transform: translate3d(0px, 0px, 0px);"
            ></div>
          </div>
          <div class="scrollbar-track scrollbar-track-y" style="display: none;">
            <div
              class="scrollbar-thumb scrollbar-thumb-y"
              style="height: 528px; transform: translate3d(0px, 0px, 0px);"
            ></div>
          </div>
        </div>
        <div class="footer-bar nbs-unselect" @click="patientListShow()">
          <i class="el-icon-caret-top" style="color:#ccc"></i>
          收起
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      isPatientListShow: true
    };
  },
  methods: {
    patientListShow() {
      this.isPatientListShow = !this.isPatientListShow;
    }
  }
};
</script>
<style lang="scss" scoped>
* {
  padding: 0;
  margin: 0;
}

.patient-list {
  position: absolute;
  width: 100%;
  top: 10px;
  font-size: 16px;
}
.patient-list .list-bar {
  width: 170px;
  height: 60px;
  background: #304156;
  border: 1px solid #bfcbda;
  border-radius: 0 30px 30px 0;
  cursor: pointer;
}
.patient-list .list-bar > .info {
  float: left;
  height: 44px;
  line-height: 22px;
  padding: 8px 0 0 5px;
  color: #fff;
}
.patient-list .list-bar > .info .num {
  font-style: normal;
}
.patient-list .list-bar > .info-right {
  float: right;
  padding: 10px 3px 0 0;
}
.patient-list .list-bar > .info-right img {
  border: 0;
}
.patient-list .list-bar > .info-right .icon-person img {
  width: 26px;
  height: 33px;
}
.patient-list .list-bar > .info-right .icon-right {
  display: inline-block;
  width: 6px;
}
.patient-list .list-bar > .info-right .icon-right img {
  width: 6px;
  height: 9px;
}
.patient-list .bar-fold > .info-right .icon-right img {
  display: block;
}
.patient-list .bar-unfold {
  border-radius: 0 30px 0 0;
}
.patient-list .bar-unfold > .info-right .icon-right img {
  /*   display: none; */
}
.patient-list .list-data {
  display: none;
  position: absolute;
  background-color: #fff;
  width: 169px;
  z-index: 11;
  border: 1px solid #bfcbda;
  border-radius: 0 0 30px 30px;
}
.patient-list .list-data > .title {
  height: 42px;
  line-height: 42px;
  text-align: center;
  color: #3a71a8;
  background: #efefef;
  margin-top: 10px;
}
.patient-list .list-data > .title .num {
  font-style: normal;
}
.patient-list .list-data > .list-data-scrollbar {
  width: 100%;
  height: 660px;
  overflow: auto;
}
.patient-list .list-data > .list ul {
  width: 100%;
}
.patient-list .list-data > .list ul li {
  list-style: none;
  height: 65px;
  line-height: 65px;
  border-bottom: 1px solid #bfcbda;
  cursor: pointer;
}
.patient-list .list-data > .list ul li.selected {
  background-color: #bfcbda;
}
.patient-list .list-data > .list ul li > .content {
  height: 44px;
  padding-left: 26px;
  font-size: 14px;
  padding-top: 5px;
}
.patient-list .list-data > .list ul li div.inline {
  height: 22px;
  line-height: 22px;
  margin-bottom: 5px;
}
.patient-list .list-data > .list ul li div.inline:last-child {
  margin-bottom: 0;
}
.patient-list .list-data > .list ul li div.inline span.name {
  color: #666;
}
.patient-list .list-data > .list ul li div.inline span.sex {
  margin-left: 2px;
}
.patient-list .list-data > .list ul li div.inline span.sex img {
  width: 12px;
  height: 12px;
}
.patient-list .list-data > .list ul li div.inline span.age {
  margin-left: 10px;
  color: #999;
}
.patient-list .list-data > .list ul li div.inline span.inpatno {
  color: #666;
  font-size: 16px;
}
.patient-list .list-data > .list ul li div.inline span.step {
  margin-left: 10px;
  width: 60px;
  height: 20px;
  background: #7bb845;
  border-radius: 2px;
  padding: 4px 14px 4px 14px;
  font-size: 12px;
  color: #fff;
}
.patient-list .list-data > .list ul li.selected div.inline span.name {
  color: #fff;
}
.patient-list .list-data > .list ul li.selected div.inline span.age {
  color: #fff;
}
.patient-list .list-data > .footer-bar {
  height: 38px;
  line-height: 38px;
  border: 0;
  text-align: center;
  color: #ccc;
  padding-top: 10px;
  cursor: pointer;
}
.rectangle-transform-enter-active {
  animation: bounce-in 0.5s;
}
.rectangle-transform-leave-active {
  animation: bounce-in 0.5s reverse;
}
@keyframes bounce-in {
  0% {
    transform: scale(0);
  }
  50% {
    transform: scale(1.5);
  }
  100% {
    transform: scale(1);
  }
}
</style>

