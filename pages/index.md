---
layout: default
ref: home
lang: en
permalink: /en/
transparent: true
---

<!-- critical css -->
<style>
  :root {
    font-family: sans-serif;
  }
  .t-container:after {
    clear: both;
  }

  *,
  :after,
  :before {
    -webkit-box-sizing: content-box;
    -moz-box-sizing: content-box;
    box-sizing: content-box;
  }

  a,
  div,
  h1,
  img,
  p,
  span,
  table,
  td,
  tr {
    margin: 0;
    padding: 0;
    border: 0;
  }

  .t-container {
    margin-left: auto;
    margin-right: auto;
    padding: 0;
    width: 100%;
  }

  .t-container {
    max-width: 1200px;
  }

  .t-container:after,
  .t-container:before {
    display: table;
    content: " ";
  }

  .t-col {
    display: inline;
    float: left;
    margin-left: 20px;
    margin-right: 20px;
    width: 100%;
  }

  .t-col_12 {
    max-width: 1160px;
  }

  .t-width {
    width: 100%;
  }

  .t-width_6 {
    max-width: 560px;
  }

  .t-cell {
    display: table-cell;
    vertical-align: middle;
    height: 100%;
    margin-left: 0;
    margin-right: 0;
  }

  @media screen and (max-width:1200px) {
    .t-container {
      max-width: 960px;
      padding: 0;
    }

    .t-col {
      display: inline;
      float: left;
      margin-left: 10px;
      margin-right: 10px;
      width: 100%;
    }

    .t-col_12 {
      max-width: 940px;
    }

    .t-width_6 {
      max-width: 460px;
    }
  }

  @media screen and (max-width:960px) {
    .t-col {
      display: block;
    }

    .t-container {
      max-width: 640px;
    }

    .t-col,
    .t-col_12 {
      width: 100%;
      max-width: 100%;
    }

    .t-col {
      float: none;
      padding-left: 20px;
      padding-right: 20px;
      margin: 0;
      box-sizing: border-box;
    }
  }

  .t-popup {
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    overflow-y: auto;
    opacity: 0;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
    padding: 0 20px;
    background-color: rgba(0,0,0,.6);
    z-index: 9999999;
    display: none;
  }

  .t-popup__container {
    background: #fff;
    margin: 0 auto;
    width: auto;
    position: absolute;
    top: 50%;
    right: 20px;
    left: 20px;
    z-index: 1;
    -moz-transform: translateY(-30%) scale(.9);
    -ms-transform: translateY(-30%) scale(.9);
    -webkit-transform: translateY(-30%) scale(.9);
    -o-transform: translateY(-30%) scale(.9);
    transform: translateY(-30%) scale(.9);
  }

  .t-popup__close {
    position: fixed;
    right: 20px;
    top: 20px;
    width: 23px;
    height: 23px;
    z-index: 9;
  }



  #allrecords {
    -webkit-font-smoothing: antialiased;
    background-color: none;
  }

  #allrecords a {
    color: #ff8562;
    text-decoration: none;
  }

  .t-text {
    font-family: 'Open Sans',serif;
    font-weight: 300;
    color: #000;
  }

  .t-text_xs {
    font-size: 15px;
    line-height: 1.55;
  }

  .t-title {
    font-family: 'Roboto',sans-serif;
    font-weight: 600;
    color: #000;
  }

  .t-title_xxs {
    font-size: 36px;
    line-height: 1.23;
  }

  .t-title_xl {
    font-size: 72px;
    line-height: 1.17;
  }

  .t-uptitle {
    font-family: 'Roboto',sans-serif;
    font-weight: 600;
    color: #000;
    letter-spacing: 2.5px;
  }

  .t-uptitle_xxl {
    font-size: 22px;
    letter-spacing: 2px;
  }

  @media screen and (max-width:1200px) {
    .t-text_xs {
      font-size: 14px;
    }

    .t-uptitle_xxl {
      font-size: 20px;
    }

    .t-title_xxs {
      font-size: 32px;
    }

    .t-title_xl {
      font-size: 68px;
    }
  }

  @media screen and (max-width:640px) {
    .t-text_xs {
      font-size: 12px;
      line-height: 1.45;
    }

    .t-uptitle_xxl {
      font-size: 18px;
    }

    .t-title_xxs {
      font-size: 28px;
    }

    .t-title_xl {
      font-size: 32px;
    }
  }

  @media screen and (max-width:480px) {
    .t-title_xl {
      font-size: 30px;
    }
  }

  .t-records {
    -webkit-font_smoothing: antialiased;
    background-color: none;
  }

  .t-records a {
    color: #ff8562;
    text-decoration: none;
  }

  .t-cover {
    height: 700px;
    width: 100%;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-size: cover;
    background-color: #000;
    background-repeat: no-repeat;
    background-position: center center;
    text-align: center;
    vertical-align: middle;
    position: relative;
    background-attachment: fixed;
    overflow: hidden;
  }

  .t-cover__carrier {
    height: 700px;
    width: 100%;
    background-size: cover;
    -webkit-background-size: cover;
    -moz-background-size: cover;
    -o-background-size: cover;
    background-repeat: no-repeat;
    background-position: center center;
    text-align: center;
    vertical-align: middle;
    position: relative;
    background-attachment: fixed;
  }

  @media screen and (max-device-width:1024px) {
    .t-cover {
      background-attachment: scroll;
    }

    .t-cover__carrier {
      background-attachment: scroll;
    }
  }

  .t-cover__filter {
    height: 700px;
    width: 100%;
    position: absolute;
    top: 0;
    left: 0;
  }

  .t-cover .t-container {
    position: absolute;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
  }

  .t-cover__wrapper {
    height: 700px;
    display: table-cell;
    width: 1200px;
  }

  @media screen and (max-width:640px) {
    .t-cover {
      height: 400px;
      background-attachment: fixed;
    }

    .t-cover__carrier {
      background-attachment: scroll!important;
      background-size: cover;
      background-position: center center;
    }

    .t-cover__filter {
      height: 400px;
    }

    .t-cover__wrapper {
      height: 400px;
    }
  }

  .t-btn {
    display: inline-block;
    font-family: 'Roboto',sans-serif;
    height: 60px;
    border: 0 none;
    font-size: 16px;
    padding-left: 60px;
    padding-right: 60px;
    text-align: center;
    white-space: nowrap;
    vertical-align: middle;
    font-weight: 700;
    background-image: none;
    -webkit-appearance: none;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
  }

  .t-btn td {
    vertical-align: middle;
  }

  @media screen and (max-width:640px) {
    .t-btn {
      white-space: normal;
      padding-left: 30px;
      padding-right: 30px;
    }
  }

  .t-submit {
    font-family: 'Roboto',sans-serif;
    text-align: center;
    height: 60px;
    border: 0 none;
    font-size: 16px;
    padding-left: 60px;
    padding-right: 60px;
    -webkit-appearance: none;
    font-weight: 700;
    white-space: nowrap;
    background-image: none;
    margin: 0;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
    outline: none;
  }

  @media screen and (max-width:640px) {
    .t-submit {
      white-space: normal;
      padding-left: 30px;
      padding-right: 30px;
    }
  }

  .t-input {
    margin: 0;
    font-family: 'Roboto',sans-serif;
    font-size: 100%;
    height: 60px;
    padding: 0 20px;
    font-size: 16px;
    line-height: 1.33;
    width: 100%;
    border: 0 none;
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
    outline: none;
  }

  .t-input::-moz-focus-inner {
    padding: 0;
    border: 0;
  }

  .t-align_center {
    text-align: center;
  }

  .t-valign_middle {
    vertical-align: middle;
  }

  .t-valign_top {
    vertical-align: top;
  }

  .t183__wrapper {
    padding-top: 42px;
    padding-bottom: 42px;
  }

  .t183__uptitle {
    color: #fff;
    padding-bottom: 20px;
    padding-top: 10px;
  }

  .t183__title {
    color: #fff;
    padding: 24px 0 24px 0;
    letter-spacing: 1px;
  }

  .t183__buttons {
    margin-top: 45px;
  }

  .t183 .t-btn:nth-child(2) {
    margin-left: 10px;
  }

  @media screen and (max-width:640px) {
    .t183__title {
      padding-left: 10px;
      padding-right: 10px;
    }

    .t183__uptitle {
      padding-left: 10px;
      padding-right: 10px;
    }

    .t183 .t-btn:nth-child(2) {
      margin-left: 5px;
    }

    .t183 .t-btn {
      margin: 5px;
    }
  }

  .t330__wrapper {
    padding: 40px 45px;
    background: #fff;
  }

  .t330__title {
    margin-bottom: 11px;
  }

  .t330__img {
    width: 100%;
    display: block;
  }

  .t330 .t-popup__container {
    background: transparent;
  }

  @media screen and (max-width:640px) {
    .t330__title {
      margin-bottom: 6px;
    }

    .t330__wrapper {
      padding: 20px;
    }
  }

  .t330__blockinput {
    display: block;
    vertical-align: middle;
    height: 100%;
    padding-right: 0;
    margin-bottom: 25px;
  }

  .t330__blockinput textarea {
    padding-top: 17px;
  }

  .t330__blockbutton {
    display: block;
    text-align: center;
    vertical-align: middle;
    height: 100%;
    width: 100%;
  }

  .t330__submit,
  .t330__input {
    width: 100%;
    height: 54px;
    -webkit-appearance: none;
  }

  @media screen and (max-width:640px) {
    .t330__input-wrapper {
      display: block;
    }

    .t330__blockbutton {
      display: block;
      padding-bottom: 0;
      text-align: center;
    }

    .t330__blockinput textarea {
      padding-top: 5px;
    }

    .t330__blockinput {
      padding-right: 0;
      margin-bottom: 20px;
    }

    .t330__submit,
    .t330__input {
      height: 46px;
      font-size: 14px;
    }

    .t330__input {
      padding: 0 14px;
    }
  }

  .t330__blockinput-errors-text {
    color: #ff7;
    box-sizing: border-box;
    padding: 0 10px 10px 10px;
    font-family: 'Open Sans',serif;
  }

  .t330__blockinput-errors-item {
    padding-top: 10px;
    display: none;
    font-family: 'Open Sans',serif;
  }

  .t330__blockinput-errorbox {
    background: #f66 none repeat scroll 0 0;
    color: #ff7;
    padding: 10px;
    text-align: center;
    margin-bottom: 20px;
    font-family: 'Open Sans',serif;
  }

  .t330__blockinput-success {
    text-align: center;
    background: #FFF;
    color: #222;
    padding: 20px;
    border: 2px solid #2D2;
    margin-bottom: 20px;
    font-family: 'Open Sans',serif;
  }

  .t500__bgimg {
    width: 45px;
    height: 45px;
    max-width: 100%;
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
  }

  .t500__iconwrapper_mobile {
    display: none;
  }

  @media screen and (max-width:960px) {
    .t500__bgimg {
      max-width: 50px!important;
      max-height: 50px!important;
    }

    .t500__iconwrapper_mobile {
      display: table-cell;
    }
  }

  .t581__arrow-icon_mobile {
    display: none;
  }

  @media screen and (max-width:960px) {
    .t581__arrow-icon_mobile {
      display: block;
      width: 20px;
      margin: 0 auto 20px;
      fill: #fff;
    }
  }

</style>


<!--allrecords-->
<div id="allrecords" class="t-records" data-hook="blocks-collection-content-node" data-tilda-project-id="56887" data-tilda-page-id="221056"  >

<div id="rec6651365" class="r" style="padding-top:0px;padding-bottom:0px; " data-animationappear="off" data-record-type="206"   >
<!-- cover -->





<div class="t-cover" id="recorddiv6651365" bgimgfield="img" style="height:100vh; background-image:url('https://static.tildacdn.com/tild6131-3038-4861-b235-313762646263/-/resize/20x/tild383031354833b765313261363635__ttba_hero.jpg');" >

  <div class="t-cover__carrier" id="coverCarry6651365" data-content-cover-id="6651365"  data-content-cover-bg="https://ttbagroup.com/assets/tild383031354833b765313261363635__ttba_hero.jpg" data-content-cover-height="100vh" data-content-cover-parallax="fixed"        style="background-image:url('');height:100vh; "></div>

    <div class="t-cover__filter" style="height:100vh;background-image: -moz-linear-gradient(top, rgba(255,255,255,0.80), rgba(255,255,255,0.80));background-image: -webkit-linear-gradient(top, rgba(255,255,255,0.80), rgba(255,255,255,0.80));background-image: -o-linear-gradient(top, rgba(255,255,255,0.80), rgba(255,255,255,0.80));background-image: -ms-linear-gradient(top, rgba(255,255,255,0.80), rgba(255,255,255,0.80));background-image: linear-gradient(top, rgba(255,255,255,0.80), rgba(255,255,255,0.80));filter: progid:DXImageTransform.Microsoft.gradient(startColorStr='#33ffffff', endColorstr='#33ffffff');"></div>

  <div class="t-container">
        <div class="t-col t-col_12">
      <div class="t-cover__wrapper t-valign_middle" style="height:927px; position: relative;z-index: 1;">
                <div class="t183">
                  <div data-hook-content="covercontent">
                    <div class="t183__wrapper">
                      <div class="t183__uptitle t-uptitle t-uptitle_xxl " style="text-transform:uppercase;" field="subtitle"><div style="color:#414040;" data-customstyle="yes" markdown="div"># DIGITAL MARKETING AGENCY_<br /></div></div>                      <h1 class="t183__title t-title t-title_xl " style="" field="title"><div style="font-size:28px;line-height:40px;text-align:center;font-family:'Open Sans';" data-customstyle="yes"><span style="font-weight: 400;"><span style="color: rgb(36, 35, 35);" data-redactor-style="color: rgb(36, 35, 35);">We understand how digital technology changed business.<br />Our strategy and execution will bring leads, sales,<br />and</span> <span style="color: rgb(237, 75, 58);"><strong>happy customers to your business.</strong></span></span></div></h1>                                            <div class="t183__buttons">
                            <a href="#GrowMyBusiness2" target="" class="t-btn " style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.3);"><table style="width:100%; height:100%;"><tr><td>GROW MY BUSINESS</td></tr></table></a>                            <a href="#rec8631456" target="" class="t-btn " style="color:#454141;border:1px solid #454141;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.3);"><table style="width:100%; height:100%;"><tr><td>OUR CLIENTS</td></tr></table></a>                      </div>
                                          </div>
                  </div>
                </div>
            </div>
        </div>
    </div>


</div>






  <style>
  #rec6651365 .t-btn:hover{
    background-color: #27a827 !important;
    color: #ffffff !important;
    border-color: #27a827 !important;

  }
  #rec6651365 .t-btn{
    -webkit-transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out, border-color 0.2s ease-in-out, box-shadow 0.2s ease-in-out; transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out, border-color 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
  }
  </style>



</div>


<div id="rec10320201" class="r" style=" " data-animationappear="off" data-record-type="330"   >

<style>
#rec10320201 input::-webkit-input-placeholder {color:#000000; opacity: 0.5;}
#rec10320201 input::-moz-placeholder          {color:#000000; opacity: 0.5;}
#rec10320201 input:-moz-placeholder           {color:#000000; opacity: 0.5;}
#rec10320201 input:-ms-input-placeholder      {color:#000000; opacity: 0.5;}
#rec10320201 textarea::-webkit-input-placeholder {color:#000000; opacity: 0.5;}
#rec10320201 textarea::-moz-placeholder          {color:#000000; opacity: 0.5;}
#rec10320201 textarea:-moz-placeholder           {color:#000000; opacity: 0.5;}
#rec10320201 textarea:-ms-input-placeholder      {color:#000000; opacity: 0.5;}
</style>
<div class="t330">
  <div class="t-popup" data-tooltip-hook="#GrowMyBusiness2" >
    <div class="t-popup__close">
      <svg width="23px" height="23px" viewBox="0 0 23 23" version="1.1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink">
        <g stroke="none" stroke-width="1" fill="#fff" fill-rule="evenodd">
          <rect transform="translate(11.313708, 11.313708) rotate(-45.000000) translate(-11.313708, -11.313708) " x="10.3137085" y="-3.6862915" width="2" height="30"></rect>
          <rect transform="translate(11.313708, 11.313708) rotate(-315.000000) translate(-11.313708, -11.313708) " x="10.3137085" y="-3.6862915" width="2" height="30"></rect>
        </g>
      </svg>
    </div>
    <div class="t-popup__container t-width t-width_6">
        <img class="t330__img t-img" src="https://static.tildacdn.com/tild6564-3331-4031-a634-366639383436/-/empty/ttba_moto.jpg" data-original="https://static.tildacdn.com/tild6564-3331-4031-a634-366639383436/ttba_moto.jpg" imgfield="img" >        <div class="t330__wrapper t-align_center" style=";">
          <div class="t330__title t-title t-title_xxs"><div style="font-size:16px;" data-customstyle="yes"><span style="font-weight: 400;">We always respond in less than 4 hours.<br /><br /></span></div></div>                    <form id="form10320201" name='form10320201' role="form" action='https://forms.tildacdn.com/procces/' method='POST' data-formactiontype="2" data-inputbox=".t330__blockinput"  data-success-url="https://ttbagroup.com/en/request-submitted" class="js-form-proccess">                                                                  <input type="hidden" name="formservices[]" value="67787a8c45c4f24353fc05cdd55eaa8d" class="js-formaction-services">

                                                                                  <div>
                          <div class="js-errorbox-all t330__blockinput-errorbox" style="display:none;">
                              <div class="t330__blockinput-errors-text t-text t-text_xs">
                                  <p class="t330__blockinput-errors-item js-rule-error js-rule-error-all"></p>
                            <p class="t330__blockinput-errors-item js-rule-error js-rule-error-req">Required field</p>
                            <p class="t330__blockinput-errors-item js-rule-error js-rule-error-email">Please correct e-mail address</p>
                            <p class="t330__blockinput-errors-item js-rule-error js-rule-error-name">Name Wrong. Correct please</p>
                            <p class="t330__blockinput-errors-item js-rule-error js-rule-error-phone">Please correct phone number</p>
                            <p class="t330__blockinput-errors-item js-rule-error js-rule-error-string">Please enter letter, number or punctuation symbols.</p>
                              </div>
                          </div>
                          <div class="js-successbox t330__blockinput-success t-text t-text_xs" style="display:none;">
                                                            Thank You! Your request has been submitted.
                                                      </div>
                        </div>
                        <div class="t330__input-wrapper">
                                                                              <div class="t330__blockinput">
                              <input type="text" name="Name" class="t330__input t-input js-tilda-rule " value="" placeholder="Your Name"  onfocus="this.placeholder = ''" onblur="this.placeholder = 'Your Name'" data-tilda-req="1" data-tilda-rule="none" style="color:#000000; border:1px solid #c9c9c9; background-color:#ffffff; border-radius: 5px; -moz-border-radius: 5px; -webkit-border-radius: 5px;">
                          </div>
                                                                                                        <div class="t330__blockinput">
                              <input type="text" name="Email" class="t330__input t-input js-tilda-rule " value="" placeholder="Your Email"  onfocus="this.placeholder = ''" onblur="this.placeholder = 'Your Email'" data-tilda-req="1" data-tilda-rule="email" style="color:#000000; border:1px solid #c9c9c9; background-color:#ffffff; border-radius: 5px; -moz-border-radius: 5px; -webkit-border-radius: 5px;">
                          </div>
                                                                                                        <div class="t330__blockinput">
                              <input type="text" name="phone" class="t330__input t-input js-tilda-rule " value="" placeholder="Your Phone Number"  onfocus="this.placeholder = ''" onblur="this.placeholder = 'Your Phone Number'" data-tilda-req="1" data-tilda-rule="phone" style="color:#000000; border:1px solid #c9c9c9; background-color:#ffffff; border-radius: 5px; -moz-border-radius: 5px; -webkit-border-radius: 5px;">
                          </div>



                                                                              <div class="t330__blockinput">
                              <textarea name="Subject" class="t330__input t-input js-tilda-rule " placeholder="What do you want to discuss?"  onfocus="this.placeholder = ''" onblur="this.placeholder = 'What do you want to discuss?'"  style="color:#000000; border:1px solid #c9c9c9; background-color:#ffffff; border-radius: 5px; -moz-border-radius: 5px; -webkit-border-radius: 5px;height:68px" rows="2"></textarea>
                          </div>
                                                    <div class="t330__blockbutton">
                              <button type="submit" class="t330__submit t-submit" style="color:#ffffff;background-color:#ed4b3a;border-radius:5px; -moz-border-radius:5px; -webkit-border-radius:5px;">SEND</button>                          </div>
                         </div>
          </form>
        </div>
      </div>
    </div>
</div>
<script type="text/javascript">
document.addEventListener('DOMContentLoaded', function(){
  setTimeout(function(){
    t330_initPopup('10320201');
  }, 500);
});
</script>


</div>


<div id="rec8631456" class="r" style="padding-bottom:0px; "  data-record-type="270"   >
<div class="t270" ></div>
<script type="text/javascript">
  document.addEventListener('DOMContentLoaded', function(){
    setTimeout(function(){
      var $root = $('html, body');
      $('a[href*="#"]:not([href="#"],.carousel-control,.t-carousel__control,[href^="#price"],[href^="#popup"])').click(function() {
        var target = $(this.hash);
        if (target.length == 0){ target = $('a[name="' + this.hash.substr(1) + '"]'); }
        if (target.length == 0){
          return true;
        }
        $root.animate({ scrollTop: target.offset().top + 3 }, 500);
        return false;
      });
    }, 500);
  });

</script>

</div>


<div id="rec6651706" class="r" style="padding-top:60px;padding-bottom:30px;background-color:#ffffff; "  data-record-type="43"   data-bg-color="#ffffff">
<!-- T030 -->
<div class="t030">
  <div class="t-container t-align_center">
    <div class="t-col t-col_10 t-prefix_1">
      <div class="t030__title t-title t-title_xxs" field="title" style=""><div style="font-size:26px;color:#000000;" data-customstyle="yes"><span style="font-weight: 300;">THEY TRUST US WITH THEIR BUSINESS</span></div></div>      <div class="t030__descr t-descr t-descr_md" field="descr" style=""><div style="font-family:'Open Sans';" data-customstyle="yes"></div></div>    </div>
  </div>
</div>
</div>


<div id="rec14697472" class="r" style="padding-bottom:30px; "  data-record-type="250"   >
<!-- T222 -->
<div class="t222">
    <div class="t222__container t-container">
                <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3730-3464-4138-a465-616162356165/-/empty/Pegasielogo_0.png" data-original="https://ttbagroup.com/assets/Pegasielogo_0.png" imgfield="img"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3064-6565-4832-a364-323665356366/-/empty/santodomingo.png" data-original="https://ttbagroup.com/wp-content/uploads/tilda/56887/pages/221056/tild3064-6565-4832-a364-323665356366__santodomingo.png" imgfield="img2"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3237-6461-4531-b731-353036343837/-/empty/GlobalPublicAffairs01.png" data-original="https://ttbagroup.com/assets/GlobalPublicAffairs01.png" imgfield="img3"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild6336-3962-4736-a462-643336623131/-/empty/joel_name05.png" data-original="https://ttbagroup.com/assets/joel_name05.png" imgfield="img4"  />
                    </div>
                                <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3733-3232-4336-a532-613664303862/-/empty/uniprix_logo.jpg" data-original="https://ttbagroup.com/assets/uniprix_logo.jpg" imgfield="img5"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3732-3532-4436-b534-333332633539/-/empty/Logos_Aguibb02.png" data-original="https://ttbagroup.com/assets/Logos_Aguibb02.png" imgfield="img6"  />
                    </div>
                    </div>
</div>
</div>


<div id="rec14697477" class="r" style="padding-top:0px;padding-bottom:15px; "  data-record-type="250"   >
<!-- T222 -->
<div class="t222">
    <div class="t222__container t-container">
                <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3461-6263-4737-b334-343461316335/-/empty/nutrivilla_logo.png" data-original="https://static.tildacdn.com/tild3461-6263-4737-b334-343461316335/nutrivilla_logo.png" imgfield="img"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3838-3031-4263-b634-613362396432/-/empty/remax.png" data-original="https://static.tildacdn.com/tild3838-3031-4263-b634-613362396432/remax.png" imgfield="img2"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild6666-6166-4264-b564-316239383633/-/empty/logos_framesz02.png" data-original="https://static.tildacdn.com/tild6666-6166-4264-b564-316239383633/logos_framesz02.png" imgfield="img3"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3732-3237-4365-b938-666362373538/-/empty/AAEAAQAAAAAAAAkdAAAAJGE5NzUwMjE4LWQyYzMtNDdlOS05ZGNjLTM1NWI5NjIxMmI1ZA.jpg" data-original="https://static.tildacdn.com/tild3732-3237-4365-b938-666362373538/AAEAAQAAAAAAAAkdAAAAJGE5NzUwMjE4LWQyYzMtNDdlOS05ZGNjLTM1NWI5NjIxMmI1ZA.jpg" imgfield="img4"  />
                    </div>
                                <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3032-6536-4636-a563-626434633732/-/empty/VolkswagenLogo.png" data-original="https://static.tildacdn.com/tild3032-6536-4636-a563-626434633732/VolkswagenLogo.png" imgfield="img5"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
            <a href="http://www.shopsvelte.com/collections/shapewear-leggings" target='_blank'>            <img class="t-img" src="https://static.tildacdn.com/tild6536-6235-4230-b966-633961313437/-/empty/logosvelteshapewear.png" data-original="https://static.tildacdn.com/tild6536-6235-4230-b966-633961313437/logosvelteshapewear.png" imgfield="img6" alt="shapewear leggings online store" />
            </a>        </div>
                    </div>
</div>
</div>


<div id="rec14697528" class="r" style="padding-top:0px;padding-bottom:30px; "  data-record-type="250"   >
<!-- T222 -->
<div class="t222">
    <div class="t222__container t-container">
                <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3535-6338-4635-a162-623733353838/-/empty/logos_frameso06.png" data-original="https://static.tildacdn.com/tild3535-6338-4635-a162-623733353838/logos_frameso06.png" imgfield="img"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3631-3138-4664-b232-373834306161/-/empty/logos_framesx05.png" data-original="https://static.tildacdn.com/tild3631-3138-4664-b232-373834306161/logos_framesx05.png" imgfield="img2"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild6439-3964-4733-a134-376630626566/-/empty/logos_framesx04.png" data-original="https://static.tildacdn.com/tild6439-3964-4733-a134-376630626566/logos_framesx04.png" imgfield="img3"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild6435-3032-4537-b439-323633366331/-/empty/logos_framesx02.png" data-original="https://static.tildacdn.com/tild6435-3032-4537-b439-323633366331/logos_framesx02.png" imgfield="img4"  />
                    </div>
                                <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3462-3062-4039-a633-393730653166/-/empty/logos_framesx03.png" data-original="https://static.tildacdn.com/tild3462-3062-4039-a633-393730653166/logos_framesx03.png" imgfield="img5"  />
                    </div>
                        <div class="t-col t222__col_2 t-col_2 t222__greyonhovercolor">
                        <img class="t-img" src="https://static.tildacdn.com/tild3133-3664-4736-a263-336532306638/-/empty/Pub_logo_new.jpg" data-original="https://static.tildacdn.com/tild3133-3664-4736-a263-336532306638/Pub_logo_new.jpg" imgfield="img6"  />
                    </div>
                    </div>
</div>
</div>


<div id="rec14698262" class="r" style="padding-top:30px;padding-bottom:45px;background-color:#ffffff; "  data-record-type="529"   data-bg-color="#ffffff">
<!-- t529 -->
<div class="t529">
      <div class="t529__container t-container">
                                    <div class="t529__col t-col t-col_6">
                <div class="t529__bubble t529__bubble_left" style="background: #f0f0f0; ">
          <div class="t529__text t-text t-text_sm" field="li_text__1478014691630" style=" ">We approached TTBA Group for SEO consultation and social media planning. Company brought us a quality research in short time and proposed amazing marketing tactics. We would definitely recommend this company.</div>
        </div>
        <div class="t529__bubble-tail" style="border-color: #f0f0f0 transparent transparent #f0f0f0;"></div>
                <div class="t529__name-wrapper">
          <div class="t-cell">
          <div class="t529__bgimg t-img" data-original="https://static.tildacdn.com/tild3162-6465-4136-b830-363736313335/13423722_10156986491610162_8176569292665050059_n.jpg" bgimgfield="li_img__1478014691630" style=" background-image: url('https://static.tildacdn.com/tild3162-6465-4136-b830-363736313335/-/resize/20x/13423722_10156986491610162_8176569292665050059_n.jpg');"   ></div>          </div>
          <div class="t-cell">
            <div class="t529__name t-name t-name_xs" field="li_title__1478014691630" style="  ">Polina <span style="font-weight: 300;">(COO, A/Maze Escape Game</span><span style="font-weight: 300;">)</span></div>            <div class="t529__descr t-descr t-descr_xxs" field="li_descr__1478014691630" style="  ">Google Review</div>          </div>
        </div>
      </div>
                                        <div class="t529__col t-col t-col_6">
                <div class="t529__bubble t529__bubble_left" style="background: #f0f0f0; ">
          <div class="t529__text t-text t-text_sm" field="li_text__1478014727987" style=" ">Leo and Konstantin from TTBA came to see us at ViaMedica. They prepared an excellent in-depth presentation and highlighted the areas that we have to work on. Their recommendations were very clear and on point. We were very satisfied with the consultation. Thank you guys!</div>
        </div>
        <div class="t529__bubble-tail" style="border-color: #f0f0f0 transparent transparent #f0f0f0;"></div>
                <div class="t529__name-wrapper">
          <div class="t-cell">
          <div class="t529__bgimg t-img" data-original="https://static.tildacdn.com/tild3661-6266-4231-b931-343663623931/photo1.jpg" bgimgfield="li_img__1478014727987" style=" background-image: url('https://static.tildacdn.com/tild3661-6266-4231-b931-343663623931/-/resize/20x/photo1.jpg');"   ></div>          </div>
          <div class="t-cell">
            <div class="t529__name t-name t-name_xs" field="li_title__1478014727987" style="  ">Athena Raptis <span style="font-weight: 300;">(Manager, ViaMedica</span><span style="font-weight: 300;">)</span></div>            <div class="t529__descr t-descr t-descr_xxs" field="li_descr__1478014727987" style="  ">Google Review</div>          </div>
        </div>
      </div>
                                  <div class="t-clear t529__separator" style=""></div>
                  <div class="t529__col t-col t-col_6">
                <div class="t529__bubble t529__bubble_left" style="background: #f0f0f0; ">
          <div class="t529__text t-text t-text_sm" field="li_text__1478014761774" style=" ">Great dynamic team, good support and suggestions. Overall good experience!</div>
        </div>
        <div class="t529__bubble-tail" style="border-color: #f0f0f0 transparent transparent #f0f0f0;"></div>
                <div class="t529__name-wrapper">
          <div class="t-cell">
          <div class="t529__bgimg t-img" data-original="https://static.tildacdn.com/tild6663-6339-4835-a130-313931663763/svelte201505121032.jpg" bgimgfield="li_img__1478014761774" style=" background-image: url('https://static.tildacdn.com/tild6663-6339-4835-a130-313931663763/-/resize/20x/svelte201505121032.jpg');"   ></div>          </div>
          <div class="t-cell">
            <div class="t529__name t-name t-name_xs" field="li_title__1478014761774" style="  ">Liliana Turecki <span style="font-weight: 300;">(Owner, Svelte Shapewear)</span></div>            <div class="t529__descr t-descr t-descr_xxs" field="li_descr__1478014761774" style="  ">Google Review</div>          </div>
        </div>
      </div>
                                        <div class="t529__col t-col t-col_6">
                <div class="t529__bubble t529__bubble_left" style="background: #f0f0f0; ">
          <div class="t529__text t-text t-text_sm" field="li_text__1478014798002" style=" ">Excellent service! Rapid communication! Professional work!</div>
        </div>
        <div class="t529__bubble-tail" style="border-color: #f0f0f0 transparent transparent #f0f0f0;"></div>
                <div class="t529__name-wrapper">
          <div class="t-cell">
          <div class="t529__bgimg t-img" data-original="https://static.tildacdn.com/tild6131-6262-4637-a135-353036353137/3d6b7dcc075a47b792e119e291734b49.jpg" bgimgfield="li_img__1478014798002" style=" background-image: url('https://static.tildacdn.com/tild6131-6262-4637-a135-353036353137/-/resize/20x/3d6b7dcc075a47b792e119e291734b49.jpg');"   ></div>          </div>
          <div class="t-cell">
            <div class="t529__name t-name t-name_xs" field="li_title__1478014798002" style="  ">Ayman Saifi <span style="font-weight: 300;">(Vice President, Nutrivilla Foods</span><span style="font-weight: 300;">)</span></div>            <div class="t529__descr t-descr t-descr_xxs" field="li_descr__1478014798002" style="  ">Google Review</div>          </div>
        </div>
      </div>
            </div>


</div>
</div>


<div id="rec14698527" class="r" style="padding-top:15px;padding-bottom:60px; "  data-record-type="208"   >
<!-- T142A -->
<div class="t142A">
  <div class="t-container_100">
  <div class="t142A__wrapone">
    <div class="t142A__wraptwo">
            <a href="#GrowMyBusiness2" target="" class="t-btn " style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;font-weight:500;box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.3);"><table style="width:100%; height:100%;"><tr><td>SPEAK WITH US</td></tr></table></a>            <a href="#rec14698725" target="" class="t-btn  t142A__marginleft20px" style="border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;font-weight:500;box-shadow: 0px 0px 5px 0px rgba(0, 0, 0, 0.3);"><table style="width:100%; height:100%;"><tr><td>WHY TTBA?</td></tr></table></a>         </div>
  </div>
  </div>
</div>





  <style>
  #rec14698527 .t-btn:hover{
    background-color: #27a827 !important;
    color: #ffffff !important;
    border-color: #27a827 !important;

  }
  #rec14698527 .t-btn{
    -webkit-transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out, border-color 0.2s ease-in-out, box-shadow 0.2s ease-in-out; transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out, border-color 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
  }
  </style>



</div>


<div id="rec6964768" class="r" style="padding-top:0px;padding-bottom:0px; "  data-record-type="179"   >
<!-- cover -->





<div class="t-cover" id="recorddiv6964768" bgimgfield="img" style="height:90vh; background-image:url('https://static.tildacdn.com/tild6632-3332-4435-a335-643961353765/-/resize/20x/Old_Port_Montreal.jpg');" >

  <div class="t-cover__carrier" id="coverCarry6964768" data-content-cover-id="6964768"  data-content-cover-bg="https://static.tildacdn.com/tild6632-3332-4435-a335-643961353765/Old_Port_Montreal.jpg" data-content-cover-height="90vh" data-content-cover-parallax="fixed"        style="background-image:url('');height:90vh; "></div>

    <div class="t-cover__filter" style="height:90vh;background-image: -moz-linear-gradient(top, rgba(0,0,0,0.70), rgba(0,0,0,0.70));background-image: -webkit-linear-gradient(top, rgba(0,0,0,0.70), rgba(0,0,0,0.70));background-image: -o-linear-gradient(top, rgba(0,0,0,0.70), rgba(0,0,0,0.70));background-image: -ms-linear-gradient(top, rgba(0,0,0,0.70), rgba(0,0,0,0.70));background-image: linear-gradient(top, rgba(0,0,0,0.70), rgba(0,0,0,0.70));filter: progid:DXImageTransform.Microsoft.gradient(startColorStr='#4c000000', endColorstr='#4c000000');"></div>

<!-- T164 -->
<div class="t164">
  <div class="t-container">
    <div class="t-cover__wrapper t-valign_middle" style="height:90vh;">
          <div class="t-col t-col_8 t-prefix_2 t-align_left">
            <div data-hook-content="covercontent">
            <div class="t164__wrapper">
                                    <div class="t164__descr t-descr t-descr_xxxl" field="descr"><div style="font-size:34px;" data-customstyle="yes">The BIG shift. </div></div>           <div class="t164__text t-text t-text_md" field="text"><div style="font-size:20px;" data-customstyle="yes">Technology has changed what it means to be a marketer today. <br /> In 2006, agencies pitched multi-million dollar campaigns with little more than reach and impressions as measurements of success. 11 years later, we can isolate and measure every step of a customer's journey and retrace every dollar invested to the <strong>revenues</strong> it generated. <br /> <br />The technological progress we've made in the last decade makes it impossible to ignore the value and the accessibility of <strong>Data Driven Marketing</strong> for  business. What's even better is that anyone from P&amp;G to a general contractor can track their marketing investments and make decisions based on numbers and figures, not a salesman's pitch from the 90's. <br /> <br />As web marketing consultants, we believe that online presence along with brand reputation and well-optimized marketing channels are <strong>key revenue drivers for your business</strong>. We are here to guide you into a successful campaign, that starts with your strategy. <br /></div></div>            </div>
            </div>
          </div>
    </div>
  </div>
</div>



</div>

</div>


<div id="rec6651367" class="r" style="padding-top:60px;padding-bottom:0px;background-color:#fafafa; "  data-record-type="60"   data-bg-color="#fafafa">
<!-- T050 -->
<div class="t050">
  <div class="t-container t-align_center">
    <div class="t-col t-col_10 t-prefix_1">
            <h3 class="t050__title t-title t-title_xxl" field="title" style=""><div style="font-size:52px;color:#494949;" data-customstyle="yes"><span style="font-weight: 300;">Our Expertise</span></div></h3>          </div>
  </div>
</div>
</div>


<div id="rec6966544" class="r" style="padding-top:0px;padding-bottom:0px;background-color:#fafafa; "  data-record-type="219"   data-bg-color="#fafafa">
<!-- T191 -->
<div class="t191">
  <div class="t-align_center">
  <hr class="t191__line t-width t-width_2" style="background-color:#dc4444;opacity:1;">
  </div>
</div>
</div>


<div id="rec8004138" class="r" style="padding-bottom:0px;background-color:#fafafa; "  data-record-type="193"   data-bg-color="#fafafa">
<!-- T175 -->
<div class="t175">
    <div class="t-container t-container_flex">
                <div class="t-col t-col_6  t-col_flex t-align_center">
            <img src="https://static.tildacdn.com/tild3661-3335-4562-a132-366533363837/-/empty/TTBA_expertise01.png" data-original="https://static.tildacdn.com/tild3661-3335-4562-a132-366533363837/TTBA_expertise01.png" imgfield="img" class="t175__img t-img"  />
        </div>
                <div class="t-col t-col_6  t-col_flex">
            <div class="t175__textwrapper">
            <div class="t175__title t-title t-title_md" field="title"><div style="color:#636363;" data-customstyle="yes">Digital Marketing</div></div>            <div class="t175__descr t-descr t-descr_xl" field="descr"><div style="color:#3f3d3d;" data-customstyle="yes"><a href="https://ttbagroup.com/en/marketing-services-montreal/seo-search-engine-optimization/" style="color: rgb(63, 61, 61);">Search Engine Optimization (SEO)</a><br /><a href="https://ttbagroup.com/en/marketing-services-montreal/social-media-management/" style="color: rgb(63, 61, 61);">Social Media &amp; Reputation Management</a><br /><a href="https://ttbagroup.com/en/marketing-services-montreal/online-advertising" style="color: rgb(63, 61, 61);">Online Advertising (PPC &amp; Adwords)</a></div></div>            <div class="t175__text t-text t-text_sm" field="text">In 2015, 64% of all in-store sales were influenced by the internet. Facebook now has 1.55 billion active users and there are <strong>2.9 billion</strong> Google searches every-single-day.<br />We are way past talking about how important it is for a business to have a solid online presence. We're past talking about the importance of mobile optimization, social media or organic search. Today, we're talking about how you can measure your <strong>ROI</strong> in digital marketing.</div>            </div>
        </div>
            </div>
</div>
</div>


<div id="rec8004142" class="r" style="padding-top:15px;padding-bottom:30px; "  data-record-type="193"   >
<!-- T175 -->
<div class="t175">
    <div class="t-container t-container_flex">
                <div class="t-col t-col_6  t-col_flex">
            <div class="t175__textwrapper">
            <div class="t175__title t-title t-title_md" field="title"><div style="color:#636363;" data-customstyle="yes">Creative Production</div></div>            <div class="t175__descr t-descr t-descr_xl" field="descr"><div style="color:#3f3d3d;" data-customstyle="yes">B<a href="https://ttbagroup.com/en/marketing-services-montreal/branding-and-graphic-design/" style="color: rgb(63, 61, 61);">randing &amp; Graphic Design</a><br />V<a href="https://ttbagroup.com/en/marketing-services-montreal/video-production/" style="color: rgb(63, 61, 61);">ideo Production</a><br />W<a href="https://ttbagroup.com/en/marketing-services-montreal/website-design/" style="color: rgb(63, 61, 61);">ebsite Design</a></div></div>            <div class="t175__text t-text t-text_sm" field="text">A clear, distinct and trustworthy brand image is what allows your business to charge a premium for your product or service. When price, quality and accessibility are equal, your audience will rely on their perception of your <strong>brand</strong> to make a decision.<br /><br />We are witnessing this decade's gold rush. Every company is rushing for a website, a Facebook page, an Instagram account, pictures and reviews. If you want to break through all that noise, your brand, your <strong>online identity</strong> and your sales tools have to communicate a clear value, a differentiated approach and undeniable trust. </div>            </div>
        </div>
                <div class="t-col t-col_6  t-col_flex t-align_center">
            <img src="https://static.tildacdn.com/tild3561-3535-4639-a163-363731303836/-/empty/TTBA_expertise02.png" data-original="https://static.tildacdn.com/tild3561-3535-4639-a163-363731303836/TTBA_expertise02.png" imgfield="img" class="t175__img t-img"  />
        </div>
            </div>
</div>
</div>


<div id="rec8004146" class="r" style="padding-top:15px;padding-bottom:0px;background-color:#fafafa; "  data-record-type="193"   data-bg-color="#fafafa">
<!-- T175 -->
<div class="t175">
    <div class="t-container t-container_flex">
                <div class="t-col t-col_6  t-col_flex t-align_center">
            <img src="https://static.tildacdn.com/tild3030-3561-4439-b036-323437303837/-/empty/TTBA_expertise03.png" data-original="https://static.tildacdn.com/tild3030-3561-4439-b036-323437303837/TTBA_expertise03.png" imgfield="img" class="t175__img t-img"  />
        </div>
                <div class="t-col t-col_6  t-col_flex">
            <div class="t175__textwrapper">
            <div class="t175__title t-title t-title_md" field="title"><div style="color:#636363;" data-customstyle="yes">Strategy &amp; Consulting</div></div>                        <div class="t175__text t-text t-text_sm" field="text">Businesses are often afraid of the word strategy or of the process of collecting data that will be used to create intricate campaigns with KPI's and statistics and.... As much as our work can get complicated, we like to make it simple for our clients. <br /><br />Strategy is getting from <strong>point A to point B</strong>. There are a million different ways of how that can be achieved. Our mandate as strategy consultants is to find the most efficient and cost-effective way of getting your business to point B. <br /><br />You can then execute that strategy yourself or you can hire our team to close the gap between strategy and <strong>actual results</strong> with the forecasts, the objectives and the KPI's that were promised.</div>            </div>
        </div>
            </div>
</div>
</div>


<div id="rec6966157" class="r" style="padding-top:30px;padding-bottom:30px; "  data-record-type="65"   >
<!-- T056 -->
<div class="t056">
  <div class="t-container t-align_center">
    <div class="t-col t-col_10 t-prefix_1">
      <h3 class="t056__title t-name t-name_xl" field="title" style=""><div style="font-size:72px;line-height:60px;color:#6b6b6b;" data-customstyle="yes"><span style="font-size: 46px;"><span style="font-weight: 300;" data-redactor-style="font-weight: 300;"><span style="font-size: 42px;" data-redactor-tag="span">WE ARE</span><br /></span></span><span style="font-size: 62px;">SYSTEMATIC</span></div></h3>      <div class="t056__descr t-text t-text_sm" field="descr" style=""><div style="font-size:22px;" data-customstyle="yes"></div></div>    </div>
  </div>
</div>
</div>


<div id="rec6651368" class="r" style="padding-top:0px;background-color:#ffffff; "  data-record-type="328"   data-bg-color="#ffffff">
<!-- T328 -->
<div class="t328">
  <div class="t-container t328__container">
    <div class="t-width t-width_10 t328__mainblock">
      <div class="t328__col">
        <div class="t328__block">
                    <div class="t328__title t-name t-name_lg" field="title" style="color:#2a327a;">Research &amp; Analysis</div>          <div class="t328__descr t-descr t-descr_xs" field="descr"><div style="font-size:18px;" data-customstyle="yes">Every project starts with an industry analysis and a market research. It is crucial to evaluate existing KPI's, analyze performance of current tactics, monitor competitors and their market positioning. </div></div>                  </div>
      </div>
      <div class="t328__line" style="background-color:#dc4444;"></div>
      <div class="t328__circle" style="background-color:#2a327a;border: 2px solid #ffffff;"></div>
    </div>
  </div>
</div>
</div>


<div id="rec6651369" class="r" style=" "  data-record-type="328"   >
<!-- T328 -->
<div class="t328">
  <div class="t-container t328__container">
    <div class="t-width t-width_10 t328__mainblock">
      <div class="t328__col t328__flipped">
        <div class="t328__block">
                    <div class="t328__title t-name t-name_lg" field="title" style="color:#2a327a;">Strategy &amp; Action Plan<br /></div>          <div class="t328__descr t-descr t-descr_xs" field="descr"><div style="font-size:18px;" data-customstyle="yes">We devise the most feasible strategy that will get your campaign to hit your objectives. Good strategy means a clearly designed action plan with concrete KPI's. <br /></div></div>                  </div>
      </div>
      <div class="t328__line" style="background-color:#dc4444;"></div>
      <div class="t328__circle" style="background-color:#2a327a;border: 2px solid #ffffff;"></div>
    </div>
  </div>
</div>
</div>


<div id="rec6651370" class="r" style="padding-bottom:0px; "  data-record-type="328"   >
<!-- T328 -->
<div class="t328">
  <div class="t-container t328__container">
    <div class="t-width t-width_10 t328__mainblock">
      <div class="t328__col">
        <div class="t328__block">
                    <div class="t328__title t-name t-name_lg" field="title" style="color:#2a327a;">Execution &amp; Control</div>          <div class="t328__descr t-descr t-descr_xs" field="descr"><div style="font-size:18px;" data-customstyle="yes">Our project management team uses the right tools and tactics to implement the agreed upon strategy, getting your business to the center of action. </div></div>                  </div>
      </div>
      <div class="t328__line" style="background-color:#dc4444;"></div>
      <div class="t328__circle" style="background-color:#2a327a;border: 2px solid #ffffff;"></div>
    </div>
  </div>
</div>
</div>


<div id="rec6966250" class="r" style="padding-bottom:45px; "  data-record-type="328"   >
<!-- T328 -->
<div class="t328">
  <div class="t-container t328__container">
    <div class="t-width t-width_10 t328__mainblock">
      <div class="t328__col t328__flipped">
        <div class="t328__block">
                    <div class="t328__title t-name t-name_lg" field="title" style="color:#2a327a;">Monitoring &amp; Optimization</div>          <div class="t328__descr t-descr t-descr_xs" field="descr"><div style="font-size:18px;" data-customstyle="yes">Data analysis and change implementation are the focus of our on-going efforts. We isolate the most effective channels and increase the cost efficiency of your campaign.  <br /></div></div>                  </div>
      </div>
      <div class="t328__line" style="background-color:#dc4444;"></div>
      <div class="t328__circle" style="background-color:#2a327a;border: 2px solid #ffffff;"></div>
    </div>
  </div>
</div>
</div>


<div id="rec6966724" class="r" style="padding-top:15px;padding-bottom:0px; "  data-record-type="60"   >
<!-- T050 -->
<div class="t050">
  <div class="t-container t-align_center">
    <div class="t-col t-col_10 t-prefix_1">
            <div class="t050__title t-title t-title_xxl" field="title" style=""><div style="font-size:52px;color:#494949;" data-customstyle="yes"><span style="font-weight: 300;">Case Studies</span></div></div>          </div>
  </div>
</div>
</div>


<div id="rec6966755" class="r" style="padding-top:15px;padding-bottom:60px; "  data-record-type="61"   >
<!-- T051 -->
<div class="t051">
  <div class="t-container">
    <div class="t-col t-col_12 ">
      <div class="t051__text t-text t-text_md" field="text">Our list of satisfied clients and successful case studies speak for themselves. <br />We're more than happy to present some of our latest and proudest achievements!</div>
    </div>
  </div>
</div>
</div>


<div id="rec12550511" class="r" style="padding-bottom:0px; " data-animationappear="off" data-record-type="335"   >
<!-- T335 -->

<div class="t335">
  <div class="t-container_100">
    <div class="t335__col t-cell t-cell_25 t-align_center ">
      <a href="https://ttbagroup.com/en/marketing-projects/marketing-strategy-for-online-gift-boutique/" target="_blank">        <div class="t335__table" style="height:50vh;">
          <div class="t335__cell t-align_center t-valign_middle">
            <div class="t335__bg t335__animation_fast t335__bg_animated t-bgimg" bgimgfield="img" data-original="https://static.tildacdn.com/tild3261-6634-4930-b930-303032626137/receiveexperiencesmobile.jpg" style="background-image:url('https://static.tildacdn.com/tild3261-6634-4930-b930-303032626137/-/resize/20x/receiveexperiencesmobile.jpg');"></div>
            <div class="t335__overlay t335__animation_fast" data-tu-ondrag-hide="yes" style="background-image: -moz-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -webkit-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -o-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -ms-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50));"></div>
            <div class="t335__textwrapper t335__animation_fast ">
              <div class="t335__textwrapper__content">
                                <div class="t335__title t-name t-name_md" field="title" >WISHBOX<br /></div>                <div class="t335__text t-descr t-descr_xxs" field="text" ><span style="font-weight: 400;">Branding and digital marketing strategy for e-commerce gift boutique</span></div>                                                  <div class="t335__button-container">
                    <div class="t335__button-wrapper">
                      <div class="t335__submit t-btn t335__submit_small" style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;">SEE CASE STUDY</div>
                    </div>
                  </div>
                                              </div>
              </div>

          </div>
        </div>
      </a>    </div>
        <div class="t335__col t-cell t-cell_25 t-align_center ">
      <a href="https://ttbagroup.com/en/marketing-projects/branding-package-design-food-company/" target="_blank">        <div class="t335__table" style="height:50vh;">
          <div class="t335__cell t-align_center t-valign_middle">
            <div class="t335__bg t335__animation_fast t335__bg_animated t-bgimg" bgimgfield="img2" data-original="https://static.tildacdn.com/tild3764-6361-4839-b238-336264616364/11110301_10100297913625984_4032540126710449837_n.jpg" style="background-image:url('https://static.tildacdn.com/tild3764-6361-4839-b238-336264616364/-/resize/20x/11110301_10100297913625984_4032540126710449837_n.jpg');"></div>
            <div class="t335__overlay t335__animation_fast" data-tu-ondrag-hide="yes" style="background-image: -moz-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -webkit-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -o-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -ms-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50));"></div>
            <div class="t335__textwrapper t335__animation_fast ">
              <div class="t335__textwrapper__content">
                                <div class="t335__title t-name t-name_md" field="title2" >NUTRIVILLA</div>                <div class="t335__text t-descr t-descr_xxs" field="text2" ><span style="font-weight: 400;">Branding and packaging design for a food and nutrition company</span></div>                                                  <div class="t335__button-container">
                    <div class="t335__button-wrapper">
                      <div class="t335__submit t-btn t335__submit_small" style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;">SEE CASE STUDY</div>
                    </div>
                  </div>
                                              </div>
              </div>

          </div>
        </div>
      </a>    </div>
            <div class="t335__col t-cell t-cell_25 t-align_center ">
      <a href="https://ttbagroup.com/en/marketing-projects/360-branding-and-marketing-for-night-club-in-montreal/" target="_blank">        <div class="t335__table" style="height:50vh;">
          <div class="t335__cell t-align_center t-valign_middle">
            <div class="t335__bg t335__animation_fast t335__bg_animated t-bgimg" bgimgfield="img3" data-original="https://static.tildacdn.com/tild3131-6232-4035-b239-343135646531/1452525_602307046503879_863044764_n.jpg" style="background-image:url('https://static.tildacdn.com/tild3131-6232-4035-b239-343135646531/-/resize/20x/1452525_602307046503879_863044764_n.jpg');"></div>
            <div class="t335__overlay t335__animation_fast" data-tu-ondrag-hide="yes" style="background-image: -moz-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -webkit-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -o-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -ms-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50));"></div>
            <div class="t335__textwrapper t335__animation_fast ">
              <div class="t335__textwrapper__content">
                                <div class="t335__title t-name t-name_md" field="title3" >HABITAT</div>                <div class="t335__text t-descr t-descr_xxs" field="text3" ><span style="font-weight: 400;">360 Branding. Marketing &amp; social media strategy for Montreal's nightclub</span></div>                                                  <div class="t335__button-container">
                    <div class="t335__button-wrapper">
                      <div class="t335__submit t-btn t335__submit_small" style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;">SEE CASE STUDY</div>
                    </div>
                  </div>
                                              </div>
              </div>

          </div>
        </div>
      </a>    </div>
            <div class="t335__col t-cell t-cell_25 t-align_center ">
      <a href="https://ttbagroup.com/en/marketing-projectssocial-media-marketing-for-pub-in-montreal-2/" target="_blank">        <div class="t335__table" style="height:50vh;">
          <div class="t335__cell t-align_center t-valign_middle">
            <div class="t335__bg t335__animation_fast t335__bg_animated t-bgimg" bgimgfield="img4" data-original="https://static.tildacdn.com/tild6433-3865-4234-b965-316635336365/Web1.jpg" style="background-image:url('https://static.tildacdn.com/tild6433-3865-4234-b965-316635336365/-/resize/20x/Web1.jpg');"></div>
            <div class="t335__overlay t335__animation_fast" data-tu-ondrag-hide="yes" style="background-image: -moz-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -webkit-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -o-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50)); background-image: -ms-linear-gradient(top, rgba(0,0,0,0.50), rgba(0,0,0,0.50));"></div>
            <div class="t335__textwrapper t335__animation_fast ">
              <div class="t335__textwrapper__content">
                                <div class="t335__title t-name t-name_md" field="title4" >PUB ST PAUL</div>                <div class="t335__text t-descr t-descr_xxs" field="text4" >Social media &amp; marketing strategy for the famous Pub St Paul</div>                                                  <div class="t335__button-container">
                    <div class="t335__button-wrapper">
                      <div class="t335__submit t-btn t335__submit_small" style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;">SEE CASE STUDY</div>
                    </div>
                  </div>
                                              </div>
              </div>

          </div>
        </div>
      </a>    </div>
      </div>
</div>

<script type="text/javascript">
    document.addEventListener('DOMContentLoaded', function() {
        t335.initeffect('12550511');
    });

</script>


</div>


<div id="rec12550540" class="r" style="padding-top:0px;padding-bottom:0px; " data-animationappear="off" data-record-type="335"   >
<!-- T335 -->

<div class="t335">
  <div class="t-container_100">
    <div class="t335__col t-cell t-cell_25 t-align_center ">
      <a href="https://ttbagroup.com/en/logo-book/" target="_blank">        <div class="t335__table" style="height:50vh;">
          <div class="t335__cell t-align_center t-valign_middle">
            <div class="t335__bg t335__animation_fast  t-bgimg" bgimgfield="img" data-original="https://static.tildacdn.com/tild3866-3563-4433-b433-316632666331/LogoBook2.png" style="background-image:url('https://static.tildacdn.com/tild3866-3563-4433-b433-316632666331/-/resize/20x/LogoBook2.png');"></div>
            <div class="t335__overlay t335__animation_fast" data-tu-ondrag-hide="yes" style="background-image: -moz-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -webkit-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -o-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -ms-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60));"></div>
            <div class="t335__textwrapper t335__animation_fast t335__textwrapper_animated">
              <div class="t335__textwrapper__content">
                                <div class="t335__title t-name t-name_md" field="title" >LOGO BOOK</div>                <div class="t335__text t-descr t-descr_xxs" field="text" >Various branding projects</div>                                                  <div class="t335__button-container">
                    <div class="t335__button-wrapper">
                      <div class="t335__submit t-btn t335__submit_small" style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;">SEE LOGOS</div>
                    </div>
                  </div>
                                              </div>
              </div>

          </div>
        </div>
      </a>    </div>
        <div class="t335__col t-cell t-cell_25 t-align_center ">
      <a href="https://ttbagroup.com/en/marketing-projects/brand-book-design-online-accessories-store/" target="_blank">        <div class="t335__table" style="height:50vh;">
          <div class="t335__cell t-align_center t-valign_middle">
            <div class="t335__bg t335__animation_fast  t-bgimg" bgimgfield="img2" data-original="https://static.tildacdn.com/tild6666-6430-4832-b864-376235616563/LXRBookMockup_small.png" style="background-image:url('https://static.tildacdn.com/tild6666-6430-4832-b864-376235616563/-/resize/20x/LXRBookMockup_small.png');"></div>
            <div class="t335__overlay t335__animation_fast" data-tu-ondrag-hide="yes" style="background-image: -moz-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -webkit-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -o-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -ms-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60));"></div>
            <div class="t335__textwrapper t335__animation_fast t335__textwrapper_animated">
              <div class="t335__textwrapper__content">
                                <div class="t335__title t-name t-name_md" field="title2" >LXR BRAND BOOK</div>                <div class="t335__text t-descr t-descr_xxs" field="text2" >Brand Book design project</div>                                                  <div class="t335__button-container">
                    <div class="t335__button-wrapper">
                      <div class="t335__submit t-btn t335__submit_small" style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;">VIEW PROJECT</div>
                    </div>
                  </div>
                                              </div>
              </div>

          </div>
        </div>
      </a>    </div>
            <div class="t335__col t-cell t-cell_25 t-align_center ">
      <a href="https://www.youtube.com/watch?v=Ygf6Cm73Bic" target="_blank">        <div class="t335__table" style="height:50vh;">
          <div class="t335__cell t-align_center t-valign_middle">
            <div class="t335__bg t335__animation_fast  t-bgimg" bgimgfield="img3" data-original="https://static.tildacdn.com/tild6363-6139-4361-a539-376165373836/santo_domingo.png" style="background-image:url('https://static.tildacdn.com/tild6363-6139-4361-a539-376165373836/-/resize/20x/santo_domingo.png');"></div>
            <div class="t335__overlay t335__animation_fast" data-tu-ondrag-hide="yes" style="background-image: -moz-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -webkit-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -o-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -ms-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60));"></div>
            <div class="t335__textwrapper t335__animation_fast t335__textwrapper_animated">
              <div class="t335__textwrapper__content">
                                <div class="t335__title t-name t-name_md" field="title3" >VIDEO COMMERCIAL</div>                <div class="t335__text t-descr t-descr_xxs" field="text3" >Video production for Cafe Santo Domingo</div>                                                  <div class="t335__button-container">
                    <div class="t335__button-wrapper">
                      <div class="t335__submit t-btn t335__submit_small" style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;">WATCH VIDEO</div>
                    </div>
                  </div>
                                              </div>
              </div>

          </div>
        </div>
      </a>    </div>
            <div class="t335__col t-cell t-cell_25 t-align_center ">
      <a href="https://vimeo.com/103976031" target="_blank">        <div class="t335__table" style="height:50vh;">
          <div class="t335__cell t-align_center t-valign_middle">
            <div class="t335__bg t335__animation_fast  t-bgimg" bgimgfield="img4" data-original="https://static.tildacdn.com/tild3130-6462-4431-b536-613766623535/ScreenShot20161117at125545PM.png" style="background-image:url('https://static.tildacdn.com/tild3130-6462-4431-b536-613766623535/-/resize/20x/ScreenShot20161117at125545PM.png');"></div>
            <div class="t335__overlay t335__animation_fast" data-tu-ondrag-hide="yes" style="background-image: -moz-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -webkit-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -o-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60)); background-image: -ms-linear-gradient(top, rgba(0,0,0,0.60), rgba(0,0,0,0.60));"></div>
            <div class="t335__textwrapper t335__animation_fast t335__textwrapper_animated">
              <div class="t335__textwrapper__content">
                                <div class="t335__title t-name t-name_md" field="title4" >COCO BELLA</div>                <div class="t335__text t-descr t-descr_xxs" field="text4" >Video commercial</div>                                                  <div class="t335__button-container">
                    <div class="t335__button-wrapper">
                      <div class="t335__submit t-btn t335__submit_small" style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;">WATCH VIDEO</div>
                    </div>
                  </div>
                                              </div>
              </div>

          </div>
        </div>
      </a>    </div>
      </div>
</div>

<script type="text/javascript">
    document.addEventListener('DOMContentLoaded', function() {
        t335.initeffect('12550540');
    });

</script>


</div>


<div id="rec6651859" class="r" style="padding-top:0px;padding-bottom:0px; " data-animationappear="off" data-record-type="408"   >
<!-- t408 -->
<!-- cover -->





<div class="t-cover" id="recorddiv6651859" bgimgfield="img" style="height:800px; background-image:url('https://static.tildacdn.com/tild6336-3866-4166-b736-313536616531/-/resize/20x/9fa06e06b67f400d9b4032327801858d.jpg');" >

  <div class="t-cover__carrier" id="coverCarry6651859" data-content-cover-id="6651859"  data-content-cover-bg="https://static.tildacdn.com/tild6336-3866-4166-b736-313536616531/9fa06e06b67f400d9b4032327801858d.jpg" data-content-cover-height="800px" data-content-cover-parallax="fixed"        style="background-image:url('');height:800px; "></div>

    <div class="t-cover__filter" style="height:800px;background-image: -moz-linear-gradient(top, rgba(18,18,18,0.70), rgba(18,18,18,0.90));background-image: -webkit-linear-gradient(top, rgba(18,18,18,0.70), rgba(18,18,18,0.90));background-image: -o-linear-gradient(top, rgba(18,18,18,0.70), rgba(18,18,18,0.90));background-image: -ms-linear-gradient(top, rgba(18,18,18,0.70), rgba(18,18,18,0.90));background-image: linear-gradient(top, rgba(18,18,18,0.70), rgba(18,18,18,0.90));filter: progid:DXImageTransform.Microsoft.gradient(startColorStr='#4c121212', endColorstr='#19121212');"></div>
<div class="t408">
  <div class="t-container">
    <div class="t-cover__wrapper t-valign_middle" style="height:800px;">
      <div class="t408__wrapper" data-hook-content="covercontent">
                <div class="t408__textwrapper t-width t-width_10">
                    <h3 class="t408__title t-title t-title_md" field="title"><div style="font-size:46px;" data-customstyle="yes"><span style="font-weight: 400;">WHY TTBA GROUP</span><br /></div></h3>                  </div>
                <div class="t408__blockswrapper">
          <div class="t408__col t-col t-col_4">
            <div class="t408__wrapper">
                            <div class="t408__title t-name t-name_md" field="title1"><div style="font-size:26px;" data-customstyle="yes">Best Value</div></div>              <div class="t408__descr t-descr t-descr_xxs" field="descr1"><div style="font-size:20px;" data-customstyle="yes"><span style="font-weight: 300;">We focus on providing the most efficient return on every marketing dollar spent. We tried and tested a lot in internet marketing. Today,  we have a solution for every stage of your business. </span><br /><br /></div></div>            </div>
          </div>
                    <div class="t408__col t-col t-col_4">
            <div class="t408__wrapper">
                            <div class="t408__title t-name t-name_md" field="title2"><div style="font-size:26px;" data-customstyle="yes">Data Driven</div></div>              <div class="t408__descr t-descr t-descr_xxs" field="descr2"><div style="font-size:20px;" data-customstyle="yes"><span style="font-weight: 300;">We base all of our recommendations on research, analytical data and the experience we've accumulated over the years building campaigns for businesses in various industries. </span><br /><br /></div></div>            </div>
          </div>
                              <div class="t408__col t-col t-col_4">
            <div class="t408__wrapper">
                            <div class="t408__title t-name t-name_md" field="title3"><div style="font-size:26px;" data-customstyle="yes">Transparency</div></div>              <div class="t408__descr t-descr t-descr_xxs" field="descr3"><div style="font-size:20px;" data-customstyle="yes"><span style="font-weight: 500;"></span><span style="font-weight: 300;">We make sure our clients are always included in the dialogue and understand every step of their campaign or strategy. Our goal is to see them eventually implement these tactics by themselves.<br /></span><br /><span style="font-weight: 500;"></span><span style="font-weight: 500;"></span></div></div>            </div>
          </div>
                            </div>
              </div>
    </div>
  </div>
</div>


</div>


</div>


<div id="rec12551103" class="r" style="padding-top:30px;padding-bottom:0px; "  data-record-type="219"   >
<!-- T191 -->
<div class="t191">
  <div class="t-align_center">
  <hr class="t191__line t-width t-width_2" style="background-color:#dc4444;opacity:1;">
  </div>
</div>
</div>


<div id="rec14963021" class="r" style="padding-top:15px;padding-bottom:75px; "  data-record-type="500"   >
<!-- t500 -->

<div class="t500">
    <div class="t-section__container t-container">
    <div class="t-col t-col_12">
      <div class="t-section__topwrapper t-align_center">
        <h2 class="t-section__title t-title t-title_xs " field="btitle"><div style="font-size:42px;font-family:'Roboto';color:#5d5d5d;" data-customstyle="yes"><span style="font-weight: 300;">Increase sales with the TTBA approach.</span></div></h2>             </div>
    </div>
  </div>

<div class="t500__container t-container">
<div class="t-cell t-cell_25 t500__cell-left">
  <div class="t500__item t-item ">
      <div class="t500__iconwrapper_mobile t-cell t-valign_top">
            <div class="t500__bgimg  t-bgimg" bgimgfield="img" data-original="https://static.tildacdn.com/tild6230-6233-4735-a535-303938356663/icons09.png" style="width:70px; height:70px; background-image: url('https://static.tildacdn.com/tild6230-6233-4735-a535-303938356663/-/resize/20x/icons09.png');"   ></div>

    </div>
    <div class="t500__textwrapper t-cell t-valign_top">
    <div class="t-name t-name_lg" field="title" style="">
  <div style="font-size:20px;" data-customstyle="yes">Website Design<br /></div></div>    <div class="t500__descr t-descr t-descr_xs" field="descr" style="">
  Whether it's a WordPress or a custom-made web design project, we'll make sure the final product is perfect. We follow the latest web design trends and pay extra attention to user experience.</div>  </div>
      <div class="t500__iconwrapper t-cell t-valign_top">
            <div class="t500__bgimg  t-bgimg" bgimgfield="img" data-original="https://static.tildacdn.com/tild6230-6233-4735-a535-303938356663/icons09.png" style="width:70px; height:70px; background-image: url('https://static.tildacdn.com/tild6230-6233-4735-a535-303938356663/-/resize/20x/icons09.png');"   ></div>

    </div>
    </div><div class="t-clear"></div>
  <div class="t500__item t500__item_padding-top t-item ">
      <div class="t500__iconwrapper_mobile t-cell t-valign_top">
            <div class="t500__bgimg  t-bgimg" bgimgfield="img2" data-original="https://static.tildacdn.com/tild3033-3035-4330-b264-303531346466/icons11.png" style="width:70px; height:70px; background-image: url('https://static.tildacdn.com/tild3033-3035-4330-b264-303531346466/-/resize/20x/icons11.png');"   ></div>
          </div>
    <div class="t500__textwrapper t-cell t-valign_top">
    <div class="t-name t-name_lg" field="title2" style="">
  <div style="font-size:20px;" data-customstyle="yes">Branding &amp; Graphic Design</div></div>   <div class="t500__descr t-descr t-descr_xs"" field="descr2" style="">
  Helping shape your brands personality. We translate your company's message through a clear expression of your business' core principles and beliefs.</div>  </div>
      <div class="t500__iconwrapper t-cell t-valign_top">
            <div class="t500__bgimg  t-bgimg" bgimgfield="img2" data-original="https://static.tildacdn.com/tild3033-3035-4330-b264-303531346466/icons11.png" style="width:70px; height:70px; background-image: url('https://static.tildacdn.com/tild3033-3035-4330-b264-303531346466/-/resize/20x/icons11.png');"   ></div>
          </div>
    </div><div class="t-clear"></div>
  <div class="t500__item t500__item_padding-top t-item ">
      <div class="t500__iconwrapper_mobile t-cell t-valign_top">
            <div class="t500__bgimg  t-bgimg" bgimgfield="img3" data-original="https://static.tildacdn.com/tild3364-6461-4135-b234-666630613034/icons07.png" style="width:70px; height:70px; background-image: url('https://static.tildacdn.com/tild3364-6461-4135-b234-666630613034/-/resize/20x/icons07.png');"   ></div>
          </div>
    <div class="t500__textwrapper t-cell t-valign_top">
    <div class="t-name t-name_lg" field="title3" style="">
  <div style="font-size:20px;" data-customstyle="yes">Video Production</div></div>    <div class="t500__descr t-descr t-descr_xs" field="descr3" style="">
  From ideation to the storyboard, we put your vision into the script. With the right casting, great locations and skilled cameramen, your video will conquer all.</div>  </div>
      <div class="t500__iconwrapper t-cell t-valign_top">
            <div class="t500__bgimg  t-bgimg" bgimgfield="img3" data-original="https://static.tildacdn.com/tild3364-6461-4135-b234-666630613034/icons07.png" style="width:70px; height:70px; background-image: url('https://static.tildacdn.com/tild3364-6461-4135-b234-666630613034/-/resize/20x/icons07.png');"   ></div>
          </div>
    </div><div class="t-clear"></div>
</div>
<div class="t-cell t-cell_50">
<img class="t500__img t-img " src="https://static.tildacdn.com/tild3066-3435-4164-b534-333265353931/-/empty/funnel_ttba3.jpg" data-original="https://static.tildacdn.com/tild3066-3435-4164-b534-333265353931/funnel_ttba3.jpg" imgfield="img7" >
</div>
<div class="t-cell t-cell_25 t500__cell-right">
  <div class="t500__item t-item ">
      <div class="t-cell t-valign_top">
            <div class="t500__bgimg  t-bgimg" bgimgfield="img4" data-original="https://static.tildacdn.com/tild3836-3431-4934-a533-613461323139/icons05.png" style="width:70px; height:70px; background-image: url('https://static.tildacdn.com/tild3836-3431-4934-a533-613461323139/-/resize/20x/icons05.png');"   ></div>
          </div>
    <div class="t500__textwrapper t-cell t-valign_top">
    <div class="t-name t-name_lg" field="title4" style="">
  <div style="font-size:20px;" data-customstyle="yes">Search Engine Optimization</div></div>    <div class="t500__descr t-descr t-descr_xs" field="descr4" style="">
  Aside from the technical algorithm. SEO is about providing a good user experience to your visitors. We make sure your website gives value to those who are searching for your target keywords.</div>  </div>
  </div><div class="t-clear"></div>
  <div class="t500__item t500__item_padding-top t-item ">
      <div class="t-cell t-valign_top">
            <div class="t500__bgimg  t-bgimg" bgimgfield="img5" data-original="https://static.tildacdn.com/tild3064-6261-4936-b636-626535393530/icons06.png" style="width:70px; height:70px; background-image: url('https://static.tildacdn.com/tild3064-6261-4936-b636-626535393530/-/resize/20x/icons06.png');"   ></div>
          </div>
    <div class="t500__textwrapper t-cell t-valign_top">
    <div class="t-name t-name_lg" field="title5" style="">
  <div style="font-size:20px;" data-customstyle="yes">Online Advertising</div></div>    <div class="t500__descr t-descr t-descr_xs" field="descr5" style="">
  Your pay-per-click advertising campaign on steroids! Understand your audience, generate qualified leads from Facebook or Google and see sales pour-in tomorrow!</div> </div>
  </div><div class="t-clear"></div>
  <div class="t500__item t500__item_padding-top t-item ">
      <div class="t-cell t-valign_top">
            <div class="t500__bgimg  t-bgimg" bgimgfield="img6" data-original="https://static.tildacdn.com/tild6433-6666-4866-b263-323236343131/icons12.png" style="width:70px; height:70px; background-image: url('https://static.tildacdn.com/tild6433-6666-4866-b263-323236343131/-/resize/20x/icons12.png');"   ></div>
          </div>
    <div class="t500__textwrapper t-cell t-valign_top">
    <div class="t-name t-name_lg" field="title6" style="">
  <div style="font-size:20px;" data-customstyle="yes">Social Media</div></div>    <div class="t500__descr t-descr t-descr_xs" field="descr6" style="">
  We use social media as an integral part of almost every digital marketing campaign. We help businesses capitalize on social media as a marketing asset.</div> </div>
  </div><div class="t-clear"></div>
</div>
</div>



</div>
</div>


<div id="rec12550547" class="r" style="padding-top:15px;padding-bottom:75px; "  data-record-type="191"   >
<!-- T142 -->
<div class="t142">
  <div class="t-container_100">
    <div class="t142__wrapone">
    <div class="t142__wraptwo">
          <a href="https://ttbagroup.com/en/marketing-case-studies-and-creative-portfolio/" target=""><div class="t-btn t142__submit " style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;font-weight:500;">SEE MORE PROJECTS</div></a>
        </div>
    </div>
  </div>
</div>

<script type="text/javascript">
  document.addEventListener('DOMContentLoaded', function() {
    t142_checkSize('12550547');
  });
</script>






  <style>
  #rec12550547 .t-btn:hover{
    background-color: #e00d0d !important;
    color: #ffffff !important;
    border-color: #ed4b3a !important;

  }
  #rec12550547 .t-btn{
    -webkit-transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out, border-color 0.2s ease-in-out, box-shadow 0.2s ease-in-out; transition: background-color 0.2s ease-in-out, color 0.2s ease-in-out, border-color 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
  }
  </style>



</div>


<div id="rec12503009" class="r" style=" "  data-record-type="581"   >
<!-- cover -->





<div class="t-cover" id="recorddiv12503009" bgimgfield="img" style="height:560px; background-image:url('https://static.tildacdn.com/tild3733-3863-4435-b039-333265613065/-/resize/20x/blob.jpg');" >

  <div class="t-cover__carrier" id="coverCarry12503009" data-content-cover-id="12503009"  data-content-cover-bg="https://static.tildacdn.com/tild3733-3863-4435-b039-333265613065/blob.jpg" data-content-cover-height="560px" data-content-cover-parallax="fixed"        style="background-image:url('');height:560px; "></div>

    <div class="t-cover__filter" style="height:560px;background-image: -moz-linear-gradient(top, rgba(0,0,0,0.80), rgba(0,0,0,0.70));background-image: -webkit-linear-gradient(top, rgba(0,0,0,0.80), rgba(0,0,0,0.70));background-image: -o-linear-gradient(top, rgba(0,0,0,0.80), rgba(0,0,0,0.70));background-image: -ms-linear-gradient(top, rgba(0,0,0,0.80), rgba(0,0,0,0.70));background-image: linear-gradient(top, rgba(0,0,0,0.80), rgba(0,0,0,0.70));filter: progid:DXImageTransform.Microsoft.gradient(startColorStr='#33000000', endColorstr='#4c000000');"></div>

  <div class="t-container">
        <div class="t-col t-col_10 t-prefix_1 t-align_center">
      <div class="t-cover__wrapper t-valign_middle" style="height:560px; position: relative;z-index:1;">
                <div class="t581">
                  <div data-hook-content="covercontent">
                    <div class="t581__wrapper t-align_center">
                      <div class="t581__title t-title t-title_sm t-margin_auto" style="" field="title">Got questions? <span style="font-weight: 300;">We'll find the answers.</span></div>                      <div class="t581__descr t-descr t-descr_xl t-margin_auto" style="max-width:600px;" field="descr">Contact us if you have any questions or simply want to chat about digital marketing. Coffee is on us!</div>                                            <div class="t581__buttons">
                        <div class="t581__buttons-wrapper t-margin_auto">
                                                                                      <svg class="t581__arrow-icon_mobile" style="fill:#ed4b3a;" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 35 70"><path d="M30.6 47.5c-.6-.5-1.6-.4-2.1.2L19 59.6V5.5c0-.8-.7-1.5-1.5-1.5S16 4.7 16 5.5v54.1L6.5 47.7c-.6-.6-1.5-.7-2.1-.2-.7.5-.8 1.5-.3 2.1l12.2 15.2c.3.4.7.6 1.2.6s.9-.2 1.2-.6l12.2-15.2c.5-.6.4-1.6-.3-2.1z"/></svg>
                                <svg class="t581__arrow-icon " style="fill:#ed4b3a; " xmlns="http://www.w3.org/2000/svg" viewBox="0 0 80 180"><path d="M54.1 108c-.5 0-.9-.2-1.2-.6-.5-.7-.3-1.6.4-2.1 1.5-1 9.5-5.5 14.6-8.3-17.4-.5-31.3-7.3-41.3-20C9.9 55.7 9.5 24.2 14.2 3.7c.2-.8 1-1.3 1.8-1.1.8.2 1.3 1 1.1 1.8-4.6 19.9-4.2 50.3 11.8 70.8 9.5 12.2 23 18.6 39.9 18.9h.3l-3.2-4c-1.4-1.7-2.7-3.3-4.1-5.1-.7-.9-1.5-1.9-2.3-2.9-.5-.6-.4-1.6.2-2.1.6-.5 1.6-.4 2.1.2 0 0 0 .1.1.1l6.4 7.9c.5.6.9 1.1 1.4 1.7 1.5 1.8 3.1 3.6 4.3 5.5 0 .1.1.1.1.2.1.2.1.3.2.5v.3c0 .2 0 .3-.1.5 0 .1-.1.1-.1.2-.1.2-.2.3-.3.4-.1.1-.2.1-.3.2 0 0-.1 0-.2.1-.9.4-16 8.6-18.2 10.1-.4 0-.7.1-1 .1z"/></svg>
                                                                                <a href="#GrowMyBusiness2" target="" class="t581__btn t-btn " style="color:#ffffff;background-color:#ed4b3a;border-radius:7px; -moz-border-radius:7px; -webkit-border-radius:7px;"><table style="width:100%; height:100%;"><tr><td>Step #1</td></tr></table></a>                                                  </div>
                      </div>
                                          </div>
                  </div>
                </div>
            </div>
        </div>
    </div>


</div>


</div>

</div>
<!--/allrecords-->


<link rel="stylesheet" href="https://cdn.rawgit.com/ttbagroup/ttbagroup.github.io/master/assets/tilda.css" rel="stylesheet" media="screen">
<script
  src="https://code.jquery.com/jquery-2.2.4.min.js"
  integrity="sha256-BbhdlvQf/xTY9gja0Dq3HiwQF8LaCRTXxZKRutelT44="
  crossorigin="anonymous"></script>
<script src="{{ site.assetsurl }}/tilda.js"></script>


<style>
@import url(https://fonts.googleapis.com/css?family=Open+Sans:300,400,500,600,700&subset=latin,cyrillic);@import url(https://fonts.googleapis.com/css?family=Roboto:300,400,500,600,700&subset=latin,cyrillic);.t-body{margin:0}#allrecords{-webkit-font-smoothing:antialiased;background-color:none}#allrecords a{color:#ff8562;text-decoration:none}#allrecords a[href^=tel]{color:inherit;text-decoration:none}#allrecords ol{padding-left:22px}#allrecords ul{padding-left:20px}@media print{body,html{min-width:1200px;max-width:1200px;padding:0;margin:0 auto;border:none}}.t-text{font-family:'Open Sans',serif;font-weight:300;color:#000}.t-text_xs{font-size:15px;line-height:1.55}.t-text_sm{font-size:18px;line-height:1.55}.t-text_md{font-size:20px;line-height:1.55}.t-text_lg{font-size:22px;line-height:1.55}.t-text_weight_plus{font-weight:400}.t-text-impact{font-family:'Open Sans',serif;font-weight:300;color:#000}.t-text-impact_xs{font-size:26px;line-height:1.5}.t-text-impact_sm{font-size:32px;line-height:1.35}.t-text-impact_md{font-size:38px;line-height:1.35}.t-text-impact_lg{font-size:42px;line-height:1.23}.t-name{font-family:'Roboto',sans-serif;font-weight:600;color:#000}.t-name_xs{font-size:16px;line-height:1.35}.t-name_sm{font-size:18px;line-height:1.35}.t-name_md{font-size:20px;line-height:1.35}.t-name_lg{font-size:22px;line-height:1.35}.t-name_xl{font-size:24px;line-height:1.35}.t-heading{font-family:'Roboto',sans-serif;font-weight:600;color:#000}.t-heading_xs{font-size:26px;line-height:1.23}.t-heading_sm{font-size:28px;line-height:1.17}.t-heading_md{font-size:30px;line-height:1.17}.t-heading_lg{font-size:32px;line-height:1.17}.t-title{font-family:'Roboto',sans-serif;font-weight:600;color:#000}.t-title_xxs{font-size:36px;line-height:1.23}.t-title_xs{font-size:42px;line-height:1.23}.t-title_sm{font-size:48px;line-height:1.23}.t-title_md{font-size:52px;line-height:1.23}.t-title_lg{font-size:64px;line-height:1.23}.t-title_xl{font-size:72px;line-height:1.17}.t-title_xxl{font-size:82px;line-height:1.17}.t-descr{font-family:'Roboto',sans-serif;font-weight:300;color:#000}.t-descr_xxs{font-size:14px;line-height:1.55}.t-descr_xs{font-size:16px;line-height:1.55}.t-descr_sm{font-size:18px;line-height:1.55}.t-descr_md{font-size:20px;line-height:1.55}.t-descr_lg{font-size:22px;line-height:1.55}.t-descr_xl{font-size:24px;line-height:1.5}.t-descr_xxl{font-size:26px;line-height:1.45}.t-descr_xxxl{font-size:30px;line-height:1.45;letter-spacing:.45}.t-uptitle{font-family:'Roboto',sans-serif;font-weight:600;color:#000;letter-spacing:2.5px}.t-uptitle_xs{font-size:12px}.t-uptitle_sm{font-size:14px}.t-uptitle_md{font-size:16px}.t-uptitle_lg{font-size:18px}.t-uptitle_xl{font-size:20px;letter-spacing:2px}.t-uptitle_xxl{font-size:22px;letter-spacing:2px}.t-uptitle_xxxl{font-size:24px;letter-spacing:2px}@media screen and (max-width:1200px){.t-text_xs{font-size:14px}.t-text_sm{font-size:16px}.t-text_md{font-size:18px}.t-text_lg{font-size:20px}.t-text-impact_md{font-size:30px}.t-descr_xxs{font-size:12px}.t-descr_xs{font-size:14px}.t-descr_sm{font-size:16px}.t-descr_md{font-size:18px}.t-descr_lg{font-size:20px}.t-descr_xl{font-size:22px}.t-descr_xxl{font-size:22px}.t-descr_xxxl{font-size:26px}.t-uptitle_md{font-size:14px}.t-uptitle_lg{font-size:16px}.t-uptitle_xl{font-size:18px}.t-uptitle_xxl{font-size:20px}.t-uptitle_xxxl{font-size:22px}.t-title_xxs{font-size:32px}.t-title_xs{font-size:38px}.t-title_sm{font-size:44px}.t-title_md{font-size:48px}.t-title_lg{font-size:60px}.t-title_xl{font-size:68px}.t-title_xxl{font-size:78px}.t-name_xs{font-size:14px}.t-name_sm{font-size:16px}.t-name_md{font-size:18px}.t-name_lg{font-size:20px}.t-name_xl{font-size:22px}.t-heading_xs{font-size:24px}.t-heading_sm{font-size:26px}.t-heading_md{font-size:28px}.t-heading_lg{font-size:30px}}@media screen and (max-width:640px){.t-text_xs{font-size:12px;line-height:1.45}.t-text_sm{font-size:14px;line-height:1.45}.t-text_md{font-size:16px;line-height:1.45}.t-text_lg{font-size:18px;line-height:1.45}.t-text-impact_sm{font-size:22px}.t-text-impact_md{font-size:26px}.t-text-impact_lg{font-size:28px}.t-descr_xs{font-size:12px;line-height:1.45}.t-descr_sm{font-size:14px;line-height:1.45}.t-descr_md{font-size:16px;line-height:1.45}.t-descr_lg{font-size:18px;line-height:1.45}.t-descr_xl{font-size:20px;line-height:1.4}.t-descr_xxl{font-size:20px}.t-descr_xxxl{font-size:22px}.t-uptitle_xs{font-size:10px}.t-uptitle_sm{font-size:10px}.t-uptitle_md{font-size:12px}.t-uptitle_lg{font-size:14px}.t-uptitle_xl{font-size:16px}.t-uptitle_xxl{font-size:18px}.t-uptitle_xxxl{font-size:20px}.t-title_xxs{font-size:28px}.t-title_xs{font-size:30px}.t-title_sm{font-size:30px}.t-title_md{font-size:30px}.t-title_lg{font-size:30px}.t-title_xl{font-size:32px}.t-title_xxl{font-size:36px}.t-name_xs{font-size:12px}.t-name_sm{font-size:14px}.t-name_md{font-size:16px}.t-name_lg{font-size:18px}.t-name_xl{font-size:20px}.t-heading_xs{font-size:22px}.t-heading_sm{font-size:24px}.t-heading_md{font-size:24px}.t-heading_lg{font-size:26px}}@media screen and (max-width:480px){.t-title_xl{font-size:30px}.t-title_xxl{font-size:30px}}.t-records{-webkit-font_smoothing:antialiased;background-color:none}.t-records a{color:#ff8562;text-decoration:none}.t-records a[href^=tel]{color:inherit;text-decoration:none}.t-records ol{padding-left:22px;margin-top:0;margin-bottom:10px}.t-records ul{padding-left:20px;margin-top:0;margin-bottom:10px}.t-cover{height:700px;width:100%;-webkit-background-size:cover;-moz-background-size:cover;-o-background-size:cover;background-size:cover;background-color:#000;background-repeat:no-repeat;background-position:center center;text-align:center;vertical-align:middle;position:relative;background-attachment:fixed;overflow:hidden}.t-cover__carrier{height:700px;width:100%;background-size:cover;-webkit-background-size:cover;-moz-background-size:cover;-o-background-size:cover;background-repeat:no-repeat;background-position:center center;text-align:center;vertical-align:middle;position:relative;background-attachment:fixed}.t-cover__carrier.loading{opacity:0}.t-cover__carrier[data-content-cover-bg=""].loading{opacity:1!important}.t-cover__carrier.loaded{opacity:1;transition:opacity 400ms}@media screen and (max-device-width:1024px){.t-cover{background-attachment:scroll}.t-cover__carrier{background-attachment:scroll}}@media print{.t-cover{background-attachment:scroll}.t-cover__carrier{background-attachment:scroll}}.t-cover__filter{height:700px;width:100%;position:absolute;top:0;left:0}.t-cover .t-container,.t-cover .t-container_100,.t-cover .t-container_10,.t-cover .t-container_8{position:absolute;top:0;left:0;bottom:0;right:0}.t-cover__wrapper{height:700px;display:table-cell;width:1200px}.t-cover__wrapper span.space{display:inline-block;height:100%;width:1px}@media screen and (max-width:640px){.t-cover{height:400px;background-attachment:fixed}.t-cover__carrier{background-attachment:scroll!important;background-size:cover;background-position:center center}.t-cover__filter{height:400px}.t-cover__wrapper{height:400px}}@-webkit-keyframes t-arrow-bottom{0%{-moz-transform:translateY(0);-ms-transform:translateY(0);-webkit-transform:translateY(0);-o-transform:translateY(0);transform:translateY(0)}50%{-moz-transform:translateY(-7px);-ms-transform:translateY(-7px);-webkit-transform:translateY(-7px);-o-transform:translateY(-7px);transform:translateY(-7px)}55%{-moz-transform:translateY(-7px);-ms-transform:translateY(-7px);-webkit-transform:translateY(-7px);-o-transform:translateY(-7px);transform:translateY(-7px)}100%{-moz-transform:translateY(0);-ms-transform:translateY(0);-webkit-transform:translateY(0);-o-transform:translateY(0);transform:translateY(0)}}@keyframes t-arrow-bottom{0%{-moz-transform:translateY(0);-ms-transform:translateY(0);-webkit-transform:translateY(0);-o-transform:translateY(0);transform:translateY(0)}50%{-moz-transform:translateY(-7px);-ms-transform:translateY(-7px);-webkit-transform:translateY(-7px);-o-transform:translateY(-7px);transform:translateY(-7px)}55%{-moz-transform:translateY(-7px);-ms-transform:translateY(-7px);-webkit-transform:translateY(-7px);-o-transform:translateY(-7px);transform:translateY(-7px)}100%{-moz-transform:translateY(0);-ms-transform:translateY(0);-webkit-transform:translateY(0);-o-transform:translateY(0);transform:translateY(0)}}.t-cover__arrow-wrapper_animated{animation:t-arrow-bottom 1.7s infinite ease}.t-cover__arrow{position:absolute;z-index:9;bottom:40px;right:0;left:0;text-align:center}.t-cover__arrow-wrapper{display:inline-block;-webkit-transition:all ease-in-out 0.2s;-moz-transition:all ease-in-out 0.2s;-o-transition:all ease-in-out 0.2s;transition:all ease-in-out 0.2s;cursor:pointer}.t-cover__arrow-wrapper:hover{opacity:.7}.t-cover__arrow-svg{fill:#fff}@media screen and (max-width:640px){.t-cover__arrow_mobile{-moz-transform:scale(.7);-ms-transform:scale(.7);-webkit-transform:scale(.7);-o-transform:scale(.7);transform:scale(.7)}.t-cover__arrow{bottom:14px}}.t-btn{display:inline-block;font-family:'Roboto',sans-serif;height:60px;border:0 none;font-size:16px;padding-left:60px;padding-right:60px;text-align:center;white-space:nowrap;vertical-align:middle;font-weight:700;background-image:none;cursor:pointer;-webkit-appearance:none;-webkit-user-select:none;-moz-user-select:none;-ms-user-select:none;-o-user-select:none;user-select:none;-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box}.t-btn td{vertical-align:middle}.t-btn_sending{opacity:.5}@media screen and (max-width:640px){.t-btn{white-space:normal;padding-left:30px;padding-right:30px}}.t-btn_sm{height:40px;font-size:14px;padding-left:30px;padding-right:30px}.t-btn_lg{height:60px;font-size:22px;padding-left:70px;padding-right:70px}.t-btn_xl{height:80px;font-size:26px;padding-left:80px;padding-right:80px}.t-btn_xxl{height:100px;font-size:30px;padding-left:90px;padding-right:90px}@media screen and (max-width:640px){.t-btn_lg{font-size:18px;padding-left:40px;padding-right:40px}.t-btn_xl{font-size:22px;padding-left:50px;padding-right:50px}.t-btn_xxl{font-size:26px;padding-left:60px;padding-right:60px}}.t-submit{font-family:'Roboto',sans-serif;text-align:center;height:60px;border:0 none;font-size:16px;padding-left:60px;padding-right:60px;-webkit-appearance:none;font-weight:700;white-space:nowrap;background-image:none;cursor:pointer;margin:0;-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box;outline:none}.t-submit_sending{opacity:.5}@media screen and (max-width:640px){.t-submit{white-space:normal;padding-left:30px;padding-right:30px}}.t-input{margin:0;font-family:'Roboto',sans-serif;font-size:100%;height:60px;padding:0 20px;font-size:16px;line-height:1.33;width:100%;border:0 none;-webkit-box-sizing:border-box;-moz-box-sizing:border-box;box-sizing:border-box;outline:none}.t-input::-moz-focus-inner{padding:0;border:0}.t-input_bbonly{outline:none;padding-left:0!important;padding-right:0!important;border-top:0!important;border-right:0!important;border-left:0!important;background-color:transparent!important;border-radius:0!important}.t-btntext{font-family:'Roboto',sans-serif;color:#000;font-size:20px;line-height:1.55;font-weight:700;text-decoration:none;cursor:pointer}.t-btntext_sm{font-size:16px}.t-btntext_lg{font-size:24px}.t-uppercase.t-btntext{font-size:16px}.t-uppercase.t-btntext_sm{font-size:14px}.t-uppercase.t-btntext_lg{font-size:20px}.t-btntext:after{content:"→";font-family:Arial,Helvetica,sans-serif}@media screen and (max-width:640px){.t-btntext_lg{font-size:20px}}@media screen and (max-width:1200px){.t-screenmin-1200px{display:none}}@media screen and (max-width:980px){.t-screenmin-980px{display:none}}@media screen and (max-width:640px){.t-screenmin-640px{display:none}}@media screen and (max-width:480px){.t-screenmin-480px{display:none}}@media screen and (max-width:320px){.t-screenmin-320px{display:none}}@media screen and (min-width:321px){.t-screenmax-320px{display:none}}@media screen and (min-width:481px){.t-screenmax-480px{display:none}}@media screen and (min-width:641px){.t-screenmax-640px{display:none}}@media screen and (min-width:981px){.t-screenmax-980px{display:none}}@media screen and (min-width:1201px){.t-screenmax-1200px{display:none}}.t-hidden{display:none}.t-opacity_50{filter:alpha(opacity=50);KHTMLOpacity:.5;MozOpacity:.5;opacity:.5}.t-opacity_70{filter:alpha(opacity=70);KHTMLOpacity:.7;MozOpacity:.7;opacity:.7}.t-uppercase{text-transform:uppercase}.t-align_center{text-align:center}.t-align_left{text-align:left}.t-align_right{text-align:right}.t-margin_auto{margin-left:auto;margin-right:auto}.t-valign_middle{vertical-align:middle}.t-valign_top{vertical-align:top}.t-valign_bottom{vertical-align:bottom}.t-margin_left_auto{margin-right:0;margin-left:auto}.yashare-style .b-share-btn__facebook,.yashare-style .b-share-btn__twitter,.yashare-style .b-share-btn__vkontakte{background-color:transparent!important}.yashare-style .b-share__link{-webkit-border-radius:0px!important;border-radius:0px!important}.yashare-style-black-white .b-share-btn__wrap{background-color:#000!important;padding:5px!important}.yashare-style-transp-white .b-share-btn__wrap{padding:5px!important}.yashare-style-transp-white .b-share-counter{color:#fff;font-weight:700}.yashare-style-white-black .b-share-btn__wrap{background-color:#fff!important;padding:5px!important}.yashare-style-white-black .b-share-icon{background-image:url(//static.tildacdn.com/img/b-share_counter_large_white.png)!important}.yashare-style-transp-black .b-share-btn__wrap{padding:5px!important}.yashare-style-transp-black .b-share-icon{background-image:url(//static.tildacdn.com/img/b-share_counter_large_white.png)!important}.yashare-style-transp-black .b-share-counter{color:#000;font-weight:700}.ya-share2 ul{padding-left:0px!important}.carousel{position:relative}.carousel ol{padding-left:0px!important}.carousel-inner{position:relative;width:100%;overflow:hidden}.carousel-inner>.item{position:relative;display:none;-webkit-transition:0.6s ease-in-out left;transition:0.6s ease-in-out left}.carousel-inner>.item>img,.carousel-inner>.item>a>img{display:block;height:auto;line-height:1}.carousel-inner .widthauto{width:auto;max-width:100%;vertical-align:middle}.carousel-inner>.active,.carousel-inner>.next,.carousel-inner>.prev{display:block}.carousel-inner>.active{left:0}.carousel-inner>.next,.carousel-inner>.prev{position:absolute;top:0;width:100%}.carousel-inner>.next{left:100%}.carousel-inner>.prev{left:-100%}.carousel-inner>.next.left,.carousel-inner>.prev.right{left:0}.carousel-inner>.active.left{left:-100%}.carousel-inner>.active.right{left:100%}.carousel-control{position:absolute;top:0;bottom:0;left:0;width:15%;opacity:.2;filter:alpha(opacity=20)}.carousel-control.right{right:0;left:auto}.carousel-control .carousel-control-left{position:absolute;top:48%;z-index:5;display:inline-block;left:20%;height:34px;width:21px;background:url(//static.tildacdn.com/img/aboutSliderControls.png) no-repeat}.carousel-control .carousel-control-left-white{position:absolute;top:48%;z-index:5;display:inline-block;left:20%;height:34px;width:21px;background:url(//static.tildacdn.com/img/aboutSliderControls_white.png) no-repeat}.carousel-control .carousel-control-right{position:absolute;top:48%;z-index:5;display:inline-block;right:20%;height:34px;width:21px;background:url(//static.tildacdn.com/img/aboutSliderControls.png) no-repeat;background-position:left bottom}.carousel-control .carousel-control-right-white{position:absolute;top:48%;z-index:5;display:inline-block;right:20%;height:34px;width:21px;background:url(//static.tildacdn.com/img/aboutSliderControls_white.png) no-repeat;background-position:left bottom}.carousel-indicators{position:absolute;bottom:10px;left:50%;z-index:15;width:60%;padding-left:0;margin-left:-30%;text-align:center;list-style:none}.carousel-indicators.dotsbottom{bottom:-60px}.carousel-indicators li{display:inline-block;width:10px;height:10px;margin:1px;margin-left:5px;margin-right:5px;text-indent:-999px;cursor:pointer;background-color:#000;border:none;border-radius:10px}.carousel-indicators .active{width:10px;height:10px;margin:0;margin-left:4px;margin-right:4px;border:1px solid #000;border-radius:10px;background-color:transparent}.carousel-indicators li.white{background-color:#fff}.carousel-indicators li.white.active{border:1px solid #fff;border-radius:10px;background-color:transparent}.carousel-caption-imgs h6{font-family:'Open Sans',serif;color:#000;font-weight:400;font-size:14px;line-height:28px;padding-top:28px;padding-bottom:0;text-align:center}.carousel-caption-imgs p{font-family:'Open Sans',serif;color:#000;font-size:14px;line-height:28px;padding-top:14px;padding-bottom:14px;text-align:center}.carousel-title{font-family:'Roboto',sans-serif;color:#000;font-size:18px;line-height:28px;padding-top:36px;padding-bottom:14px;text-align:center}.carousel-descr{font-family:'Open Sans',serif;color:#000;font-size:14px;line-height:28px;padding-top:14px;padding-bottom:14px;text-align:center}@media screen and (min-width:768px){.carousel-indicators{bottom:20px}}.clearfix:before,.clearfix:after{display:table;content:" "}.clearfix:after{clear:both}.center-block{display:block;margin-right:auto;margin-left:auto}@media screen and (max-width:960px){.carousel-control .carousel-control-left{left:10%}.carousel-control .carousel-control-left-white{left:10%}.carousel-control .carousel-control-right{right:10%}.carousel-control .carousel-control-right-white{right:10%}}.t-tildalabel{background-color:#000;color:#fff;width:100%;height:70px;font-family:Arial;font-size:14px}.t-tildalabel:hover .t-tildalabel__wrapper{opacity:1}.t-tildalabel_white{background-color:#fff;color:#000}.t-tildalabel_gray{background-color:#eee;color:#000}.t-tildalabel__wrapper{display:table;height:30px;width:270px;margin:0 auto;padding-top:20px;opacity:.4}.t-tildalabel__txtleft{display:table-cell;width:120px;height:30px;vertical-align:middle;text-align:right;padding-right:12px;font-weight:300;font-size:12px}.t-tildalabel__wrapimg{display:table-cell;width:30px;height:30px;vertical-align:middle}.t-tildalabel__img{width:30px;height:30px;vertical-align:middle}.t-tildalabel__txtright{display:table-cell;width:120px;height:30px;vertical-align:middle;padding-left:12px;font-weight:500;letter-spacing:2px}.t-tildalabel__link{color:#fff;text-decoration:none;vertical-align:middle}.t-tildalabel_white .t-tildalabel__link,.t-tildalabel_gray .t-tildalabel__link{color:#000}.t-carousel{position:relative}.t-carousel__inner{position:relative;overflow:hidden;margin:0 auto}.t-carousel__slides{position:relative}.t-carousel__inner>.t-carousel__item{position:relative;display:none;-webkit-transition:0 ease-in-out left;-moz-transition:0 ease-in-out left;-o-transition:0 ease-in-out left;transition:0 ease-in-out left}.t-carousel__inner>.t-carousel__item.t-carousel__animation_fast{-webkit-transition:.3s ease-in-out left;-moz-transition:.3s ease-in-out left;-o-transition:.3s ease-in-out left;transition:.3s ease-in-out left}.t-carousel__inner>.t-carousel__item.t-carousel__animation_slow{-webkit-transition:.6s ease-in-out left;-moz-transition:.6s ease-in-out left;-o-transition:.6s ease-in-out left;transition:.6s ease-in-out left}.t-carousel__item__wrapper{position:relative;margin:0 auto}.t-carousel__item__img{background-size:contain;background-repeat:no-repeat;background-position:center;position:absolute;top:0;right:0;bottom:0;left:0}.t-carousel_cover .t-carousel__item__img{background-size:cover}.t-carousel__inner>.active,.t-carousel__inner>.next,.t-carousel__inner>.prev{display:block}.t-carousel__inner>.active{left:0}.t-carousel__inner>.next,.t-carousel__inner>.prev{position:absolute;top:0;width:100%}.t-carousel__inner>.next{left:100%}.t-carousel__inner>.prev{left:-100%}.t-carousel__inner>.next.left,.t-carousel__inner>.prev.right{left:0}.t-carousel__inner>.active.left{left:-100%}.t-carousel__inner>.active.right{left:100%}.t-carousel__arrows__container{position:absolute;top:0;left:0;right:0;bottom:0;margin:0 auto;pointer-events:none;filter:progid:DXImageTransform.Microsoft.AlphaImageLoader(src='data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAQAAAC1HAwCAAAAC0lEQVR4nGP6zwAAAgcBApocMXEAAAAASUVORK5CYII=',sizingMethod='scale');background:none!important}.t-carousel__arrow_outsidesmall .t-carousel__arrow__wrapper_left{left:16px}.t-carousel__arrow_outsidesmall .t-carousel__arrow__wrapper_right{right:16px}.t-carousel__arrow_outsidemiddle .t-carousel__arrow__wrapper_left{left:20px}.t-carousel__arrow_outsidemiddle .t-carousel__arrow__wrapper_right{right:20px}.t-carousel__control{position:absolute;top:0;bottom:0;left:0;width:15%;-webkit-transition:all ease-in-out 0.3s;-moz-transition:all ease-in-out 0.3s;-o-transition:all ease-in-out 0.3s;transition:all ease-in-out 0.3s;pointer-events:auto}.t-carousel__control:hover{opacity:.6}.t-carousel__arrow{width:34px;height:34px;background:transparent;-moz-transform:rotate(45deg);-ms-transform:rotate(45deg);-webkit-transform:rotate(45deg);-o-transform:rotate(45deg);transform:rotate(45deg)}.t-carousel__arrow.t-carousel__arrow_small{width:20px;height:20px}.t-carousel__arrow.t-carousel__arrow_large{width:54px;height:54px}.t-carousel__arrow__wrapper{-moz-transform:translateY(-50%);-ms-transform:translateY(-50%);-webkit-transform:translateY(-50%);-o-transform:translateY(-50%);transform:translateY(-50%);position:absolute;top:50%}.t-carousel__arrow__wrapper_left{left:30px}.t-carousel__arrow__wrapper_right{right:30px}.t-carousel__arrow_right{border-top:3px solid;border-right:3px solid}.t-carousel__arrow_right.t-carousel__arrow_light{border-top:1px solid;border-right:1px solid}.t-carousel__arrow_right.t-carousel__arrow_bold{border-top:6px solid;border-right:6px solid}.t-carousel__arrow_left{border-left:3px solid;border-bottom:3px solid}.t-carousel__arrow_left.t-carousel__arrow_light{border-left:1px solid;border-bottom:1px solid}.t-carousel__arrow_left.t-carousel__arrow_bold{border-left:6px solid;border-bottom:6px solid}.t-carousel__control.right{right:0;left:auto}@media screen and (max-width:768px){.t-carousel__control .t-carousel__arrow{width:12px;height:12px}.t-carousel-control{width:10%}.t-carousel__arrow__left{left:15px}.t-carousel__arrow__right{right:15px}}.t-carousel__indicators.carousel-indicators{z-index:15;text-align:center;list-style:none;position:relative;padding-left:0!important;margin:0 auto;padding:20px 0;bottom:auto;left:auto}.t-carousel__indicators.t-carousel__indicators_light{padding:15px 0 18px}.t-carousel__indicators.t-carousel__indicators_bold{padding:24px 0 21px}.t-carousel__indicators .t-carousel__indicator{display:inline-block;width:8px;height:8px;margin:0 6px;text-indent:-999px;cursor:pointer;background-color:#222;border:none;border-radius:10px;opacity:.4;-webkit-transition:.2s ease-in-out opacity;-moz-transition:.2s ease-in-out opacity;-o-transition:.2s ease-in-out opacity;transition:.2s ease-in-out opacity}@media screen and (max-width:640px){.t-carousel__indicators.carousel-indicators,.t-carousel__indicators.t-carousel__indicators_light,.t-carousel__indicators.t-carousel__indicators_bold{padding:15px 0}}.t-carousel__indicators.t-carousel__indicators_light .t-carousel__indicator{width:4px;height:4px;margin:0 5px}.t-carousel__indicators.t-carousel__indicators_bold .t-carousel__indicator{width:10px;height:10px;margin:0 6px}.t-carousel__indicators .t-carousel__indicator:hover{opacity:.8}.t-carousel__indicators .t-carousel__indicator.active{opacity:1}.t-carousel__indicators.t-carousel__indicators_inside{position:absolute;bottom:0;left:0;right:0}.t-carousel__caption-inside{display:none}.t-carousel__caption_wrapper{border-top:1px solid #eee;padding:14px 0}.t-carousel__descr{margin-top:5px;color:#777}.t-mbfix{opacity:.01;-webkit-transform:translateX(0);-ms-transform:translateX(0);transform:translateX(0);position:fixed;width:100%;height:500px;background-color:white;top:0;left:0;z-index:10000;-webkit-transition:all 0.1s ease;transition:all 0.1s ease}.t-mbfix_hide{-webkit-transform:translateX(3000px);-ms-transform:translateX(3000px);transform:translateX(3000px)}.r_anim{-webkit-transition:opacity 0.5s;transition:opacity 0.5s}.r_hidden{opacity:0}.r_showed{opacity:1}img:not([src]){visibility:hidden}.t107{text-align:center}.t107__width{vertical-align:middle}.t107__widthauto{width:auto;max-width:100%;display:block;margin:0 auto}.t107__title{padding-top:28px;padding-bottom:28px;font-size:14px;line-height:28px}.t102__title{font-size:104px;color:#fff;margin:74px 0 54px 0;text-transform:uppercase}.t102__descr{color:#fff;padding:0 220px}@media screen and (max-width:1024px){.t102__title{font-size:70px;line-height:70px;margin-top:30px}.t102__descr{padding:0 120px}}@media screen and (max-width:640px){.t102__title{font-size:34px;line-height:38px;margin-top:30px}.t102__descr{padding:0 10px}}.t001__wrapper{padding-top:42px;padding-bottom:42px}.t001__uptitle{text-transform:uppercase;color:#fff;padding-bottom:60px;padding-top:30px}.t001__title{color:#fff;padding:24px 0 38px 0;letter-spacing:.5px}.t001__descr{color:#fff;padding:0 0 30px 0}.t001__descr_center{max-width:700px;margin:0 auto}.t001__descr_center a{color:#fff!important;font-weight:600}@media screen and (max-width:640px){.t001__title{padding-left:10px;padding-right:10px}.t001__uptitle{padding-left:10px;padding-right:10px}.t001__descr{padding-left:10px;padding-right:10px;font-size:14px;line-height:20px}}.t006{position:relative}.t006__line_top{width:100%;text-align:center;position:relative}.t006__line_top:after{content:'';position:absolute;top:50%;left:0;right:0;height:1px;background-color:#000}.t006__line_bottom{border-top:1px solid #000;width:100%;height:1px;text-align:center;margin-top:22px;padding-bottom:4px}.t006__uptitle{padding:10px 43px;background-color:#000;display:inline-block;color:#fff;font-weight:700;text-transform:uppercase;letter-spacing:2px;position:relative;z-index:1}.t006__text-impact{padding:40px 0 30px 0;text-align:center}.t006 .t-col_10{margin:0}@media screen and (max-width:640px){.t006 .t-col_10{margin:0;padding:0}.t006__text-impact{padding-left:0;padding-right:0}.t006__line_top{height:auto}}.t015__title{padding-top:8px;padding-bottom:3px}.t015__uptitle{text-transform:uppercase;padding-top:10px;padding-bottom:40px}.t015__descr{padding:41px 0 0 0}.t017__uptitle{padding-top:3px;padding-bottom:22px}.t017__title{padding-top:2px;padding-bottom:0}.t017__descr{padding-top:21px}.t021__line{width:100%;max-width:140px;margin-left:auto;margin-right:auto;height:1px;background-color:#000}.t021__text-impact{text-align:center;margin-top:44px;margin-bottom:54px}.t022__text{padding-top:8px;padding-bottom:6px}.t026__title{line-height:28px;font-size:14px;font-weight:700;text-transform:uppercase;padding-top:7px;padding-bottom:6px}.t026-descr{padding-top:1px}.t030__title{margin-bottom:15px}.t030__descr{margin-top:8px;padding-bottom:6px}.t032__wrapper{padding-top:42px;padding-bottom:42px}.t032__title{color:#fff;margin-bottom:50px}.t032__line{width:100%;height:1px;background-color:#fff}.t032__descr{color:#fff;margin-top:43px;padding:0 50px;margin-bottom:0}@media screen and (max-width:960px){.t032__line{max-width:160px;margin:0 auto}}@media screen and (max-width:640px){.t032 .t-cover__wrapper{display:block;width:100%}.t032__title{padding:0 10px}.t032__descr{padding:0 10px}}.t050__uptitle{padding-top:9px;padding-bottom:93px;text-transform:uppercase}.t050__descr{padding-top:50px;padding-bottom:9px}.t051__text{text-align:center}.t056__title{padding-top:8px;padding-bottom:9px}.t056__descr{font-size:18px;line-height:28px;letter-spacing:1px;padding-top:22px;padding-bottom:5px}.t059__text-impact{padding:1px 75px 10px 75px}@media screen and (max-width:640px){.t059__text-impact{padding-left:0;padding-right:0}}.t075__wrapperleft{padding-left:0;padding-right:0}.t075__wrappercenter{padding-left:20px;padding-right:20px}.t075__img{margin-bottom:14px;width:100px;height:100px}.t075__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}.t075__textclass1 .t075__title{font-size:24px;line-height:30px;margin-bottom:25px;margin-top:18px}.t075__textclass1{font-size:16px;line-height:25px}.t075__textclass2 .t075__title{font-size:18px;line-height:21px;margin-bottom:25px;margin-top:12px}.t075__textclass2{font-size:13px;line-height:20px}.t075__textclass3 .t075__title{font-size:30px;line-height:40px;margin-bottom:25px;margin-top:12px}.t075__textclass3{font-size:16px;line-height:25px}@media screen and (max-width:960px){.t075__textclass1,.t075__textclass2,.t075__textclass3{margin-bottom:45px}}.t082__img{margin-bottom:14px;float:right;margin-right:22px;width:100px;height:100px}.t082__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}.t082__title{margin-top:0;margin-bottom:25px}.t082__blockdescr{padding-right:150px;font-size:16px;line-height:25px}@media screen and (max-width:960px){.t082 .t082__col{width:100%;max-width:100%}.t082__blockdescr{padding-bottom:40px}}.t004{padding-top:8px;padding-bottom:6px}.t004__text-column-count_2{column-count:2;column-gap:40px;-moz-column-count:2;-moz-column-gap:40px;-webkit-column-count:2;-webkit-column-gap:40px}.t004__text-column-count_3{column-count:3;column-gap:40px;-moz-column-count:3;-moz-column-gap:40px;-webkit-column-count:3;-webkit-column-gap:40px}.t004__text-column-count_4{column-count:4;column-gap:40px;-moz-column-count:4;-moz-column-gap:40px;-webkit-column-count:4;-webkit-column-gap:40px}.t004__initial-letter:first-child::first-letter{font-size:100px;float:left;margin:-30px 20px -30px 0}.t004 table{border-collapse:collapse;font-size:1em;width:100%}.t004 table td,.t004 table th{padding:5px;border:1px solid #ddd;vertical-align:top}.t004 table thead td,.t004 table th{font-weight:700;border-bottom-color:#888}@media screen and (max-width:1200px){.t004__text-column-count_2,.t004__text-column-count_3,.t004__text-column-count_4{column-gap:20px;-moz-column-gap:20px;-webkit-column-gap:20px}}@media screen and (max-width:960px){.t004__text-column-count_2,.t004__text-column-count_3,.t004__text-column-count_4{column-count:1;column-gap:0;-moz-column-count:1;-moz-column-gap:0;-webkit-column-count:1;-webkit-column-gap:0}}@media screen and (max-width:640px){.t004 h1{font-size:28px;line-height:35px}}.t119__preface{font-size:30px;line-height:1.35;margin-top:-1px}@media screen and (max-width:640px){.t119__preface{font-size:22px}}.t120__title{padding-top:4px;padding-bottom:14px}.t120__descr{margin-top:-6px;padding-bottom:3px}.ok-klass{display:none!important}.t215 .t-row{clear:both}.t215__blockimg{height:560px;margin-bottom:20px}.t215__title{padding-bottom:14px}.t215__descr{font-size:14px;line-height:24px;padding-bottom:14px}.t215__textwrapper{margin-bottom:10px}@media screen and (max-width:1200px){.t215__blockimg{height:460px}}@media screen and (max-width:960px){.t215__blockimg{max-width:460px;height:460px}}@media screen and (max-width:320px){.t215__blockimg{height:320px}}.t214 .t-row{clear:both}.t214__blockimg{max-width:360px;height:360px;margin-bottom:20px}.t214__title{padding-bottom:14px}.t214__descr{font-size:14px;line-height:24px;padding-bottom:14px}.t214__textwrapper{margin-bottom:10px}@media screen and (max-width:1200px){.t214__blockimg{height:320px}}@media screen and (max-width:960px){.t214__blockimg{height:360px}}@media screen and (max-width:320px){.t214__blockimg{height:320px}}.t145__title{font-size:30px;line-height:34px;font-weight:700;padding-top:8px;padding-bottom:6px;margin-right:20px}.t145__line{margin-top:14px;margin-bottom:14px;border:0;border-top:3px solid #000;margin-right:20px}.t145__text{padding-top:4px;padding-bottom:6px;font-size:16px;line-height:25px;margin-right:20px}@media screen and (max-width:960px){.t145 .t145__col{margin-top:20px;margin-bottom:20px}}.t148__title{color:#fff;padding-top:28px;padding-bottom:28px;max-width:480px;width:100%;margin-left:50px;text-align:left;margin-bottom:40px}@media screen and (max-width:640px){.t148__title{width:90%;margin-left:20px;margin-bottom:20px}}.t153__title{color:#fff;padding-top:20px;padding-bottom:20px}.t153__uptitle{color:#fff;padding-bottom:30px;padding-top:0}.t153__descr{color:#fff;padding:10px 0 20px 0;letter-spacing:.7px;font-weight:400}.t153__descr_center{max-width:460px;margin:0 auto}@media screen and (max-width:640px){.t153__title{padding-left:10px;padding-right:10px}.t153__uptitle{padding-left:10px;padding-right:10px}.t153__descr{padding-left:10px;padding-right:10px}}.t158__text{font-size:28px;line-height:42px;text-align:center}@media screen and (max-width:640px){.t158__text{font-size:22px;line-height:34px}}.t160{text-align:center;padding-bottom:20px}.t160__img{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%;width:150px;max-width:150px;height:150px;padding-top:17px;padding-bottom:14px}.t160__title{text-align:center;padding-top:8px;padding-bottom:5px}.t160__descr{text-align:center;padding-top:0;padding-bottom:6px;letter-spacing:2px}.t160__text{padding-top:30px;padding-bottom:30px;font-size:22px;line-height:1.55}@media screen and (max-width:960px){.t160__wrapper{padding:0 20px}}@media screen and (max-width:640px){.t160__text{font-size:18px;line-height:1.45}}@media screen and (max-width:480px){.t160__text{font-size:16px;padding-left:10px;padding-right:10px}}.t164__wrapper{padding-top:42px;padding-bottom:42px}.t164__text{padding-top:8px;padding-bottom:6px;color:#fff}.t164__descr{padding-bottom:16px;margin-top:-3px;color:#fff}.t164__title{padding-bottom:12px;color:#fff}.t164__subtitle{font-size:14px;color:#fff;line-height:28px;margin-top:-12px;padding-bottom:14px}.t165 .t-container{display:-webkit-box;display:-moz-box;display:-ms-flexbox;display:-webkit-flex;display:flex}.t165__vmiddle{margin-top:auto;margin-bottom:auto}.t165__vtop{margin-bottom:auto}.t165__vbottom{margin-top:auto}.t165__left{text-align:left}.t165__center{text-align:center}.t165__right{text-align:right}.t165__textwrapper{padding-right:20px}.t165__uptitle{padding:0;margin:0;margin-bottom:14px}.t165__title{padding:0;margin:0;padding-bottom:28px}.t165__text{filter:alpha(opacity=85);KHTMLOpacity:.85;MozOpacity:.85;opacity:.85}.t165__img{float:right;width:100%}.t165__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}@media screen and (max-width:640px){.t165 .t-container{display:-webkit-block;display:block}.t165__img{float:none}.t165__col-top{margin-bottom:30px}}.t169__text{font-size:60px;line-height:90px;margin:0 100px}@media screen and (max-width:640px){.t169__text{font-size:28px;line-height:36px;margin:0 20px}}.t142__submit-overflowed{line-height:1.1!important}.t142__text{display:table-cell;vertical-align:middle;height:50px}.t142__wrapone{position:relative;right:50%;float:right}.t142__wraptwo{position:relative;z-index:1;right:-50%}.t142__submit{font-family:'Roboto',sans-serif;text-align:center;height:50px;line-height:50px;border:0 none;font-size:16px;padding-left:60px;padding-right:60px;-webkit-appearance:none;font-weight:700;background:none;cursor:pointer;box-sizing:content-box}.t142__submit_size_sm{height:40px;line-height:40px;font-size:14px;padding-left:30px;padding-right:30px}.t142__submit_size_lg{height:60px;line-height:60px;font-size:22px;padding-left:70px;padding-right:70px}.t142__submit_size_xl{height:80px;line-height:80px;font-size:26px;padding-left:80px;padding-right:80px}.t142__submit_size_xxl{height:100px;line-height:100px;font-size:30px;padding-left:90px;padding-right:90px}@media screen and (max-width:640px){.t142__submit{white-space:normal;padding-left:30px;padding-right:30px;margin-left:20px;margin-right:20px;-webkit-border-radius:0}.t142__submit_size_lg,.t142__submit_size_xl,.t142__submit_size_xxl{height:60px;line-height:60px;font-size:18px;padding-left:40px;padding-right:40px}.t142__submit_size_lg .t142__text,.t142__submit_size_xl .t142__text,.t142__submit_size_xxl .t142__text{height:60px}}.t175__widepadding{padding:60px}.t175__title{margin:0 auto}.t175__descr{padding-top:20px;margin:0 auto;opacity:.5}.t175__text{padding-top:20px;margin:0 auto}.t175__img{max-width:100%;margin:0 auto}@media screen and (max-width:960px){.t175__widepadding{padding:20px}.t175__img,.t175__text{margin-bottom:60px}}.t181{text-align:left}.t181__wrapper{padding-top:42px;padding-bottom:42px}.t181__title{color:#fff;padding:24px 0 38px 0;letter-spacing:1px}.t181__descr{color:#fff;padding:0 0 30px 0}.t181 .t-btn:nth-child(2){margin-left:10px}@media screen and (max-width:640px){.t181 .t-btn:nth-child(2){margin-left:0}.t181 .t-btn{margin:5px;margin-left:0}}.t182{text-align:center}.t182__wrapper{padding-top:42px;padding-bottom:42px}.t182__title{color:#fff;padding:24px 0 24px 0;letter-spacing:1px}.t182__descr{color:#fff;padding:15px 0 30px 0}.t182__buttons{margin-top:45px}.t182 .t-btn:nth-child(2){margin-left:10px}@media screen and (max-width:640px){.t182__title{font-size:30px;line-height:30px;padding-left:10px;padding-right:10px}.t182__descr{padding-left:10px;padding-right:10px;font-size:14px;line-height:20px}.t182 .t-btn{margin:7px 3px}.t182 .t-btn:nth-child(2){margin-left:3px}}.t183__wrapper{padding-top:42px;padding-bottom:42px}.t183__uptitle{color:#fff;padding-bottom:20px;padding-top:10px}.t183__title{color:#fff;padding:24px 0 24px 0;letter-spacing:1px}.t183__buttons{margin-top:45px}.t183 .t-btn:nth-child(2){margin-left:10px}@media screen and (max-width:640px){.t183__title{padding-left:10px;padding-right:10px}.t183__uptitle{padding-left:10px;padding-right:10px}.t183 .t-btn:nth-child(2){margin-left:5px}.t183 .t-btn{margin:5px}}.t142A__wrapone{position:relative;right:50%;float:right}.t142A__wraptwo{position:relative;z-index:1;right:-50%}.t142A__wraptwo td{vertical-align:middle}.t142A__marginleft20px{margin-left:20px}@media screen and (max-width:640px){.t142A{padding:0 20px}.t142A .t-btn{width:100%;margin-bottom:10px}.t142A__marginleft20px{margin-left:0}}.t185__butwrapper{text-align:right;margin-top:10px;margin-bottom:10px}@media screen and (max-width:980px){.t185__butwrapper{text-align:center;margin-top:20px;margin-bottom:20px}.t185{text-align:center}}.t188__wrapone{position:relative;right:50%;float:right}.t188__wraptwo{position:relative;z-index:1;right:-50%}.t188__sociallinkimg{display:inline-block;padding-left:5px;padding-right:5px}.t188__imgwrapper{background-size:contain;background-repeat:no-repeat;background-position:center}.t189{text-align:left}.t189__wrapper{padding-top:42px;padding-bottom:42px}.t189__title{font-size:26px;line-height:34px;color:#fff;padding:20px 0 20px 0;letter-spacing:1px}.t189__descr{color:#fff;padding:0 0 30px 0}.t189 .t-btn:nth-child(2){margin-left:10px}@media screen and (max-width:640px){.t189__title{font-size:26px;line-height:30px}.t189 .t-btn:nth-child(2){margin-left:0}.t189 .t-btn{margin:5px;margin-left:0}}.t191{padding-top:28px;padding-bottom:28px}.t191__line{height:1px;background-color:#000;border:none}.t192__title{padding-top:8px;padding-bottom:6px;text-align:center}.t192__text{padding-top:4px;padding-bottom:6px;text-align:center}.t192 hr{margin-top:14px;margin-bottom:14px;border:0;border-top:1px solid #000;opacity:.2}@media screen and (max-width:960px){.t192 .t192__col{margin-top:20px;margin-bottom:20px}}.t203__wrapper{display:table;padding-top:60px;padding-bottom:60px;margin-left:-60px;margin-right:-60px}.t203__textwrapper{display:block;text-align:left;background-color:#fff;padding-left:60px;padding-right:60px;padding-top:60px;padding-bottom:60px}.t203__title{padding-top:20px;padding-bottom:20px}.t203__text{padding-bottom:20px;padding-top:20px}@media screen and (max-width:720px){.t203__wrapper{padding-top:0;padding-bottom:0;margin-left:0;margin-right:0}.t203__textwrapper{margin:20px 0;padding:20px}}.t218__blocktable{width:100%;height:700px;margin:0;padding:0;border:0;border-spacing:0}.t218__blocktext{width:50%;height:100%;vertical-align:middle}.t218__blockimg{width:50%;height:100%;vertical-align:middle;-webkit-background-size:cover;-moz-background-size:cover;-o-background-size:cover;background-size:cover;background-repeat:no-repeat;background-position:center center;border:0;margin:0;padding:0}.t218__textwrapper{margin:10%}.t218__textfield{padding-top:20px}.t218__imgmobile{width:auto;max-width:100%;vertical-align:middle;margin:0}@media screen and (max-width:980px){.t218__blockimg{display:none}.t218__blockimgmobile{display:block!important;text-align:center;width:100%;padding:60px 0 0 0}}@media screen and (max-width:640px){.t218__descrfield{padding-top:50px;width:100%}.t218__textfield{padding-bottom:50px;width:100%}.t218__textwrapper{margin:20px}}.t222 img{width:100%;padding:0;margin:0}.t222__greyonhovercolor{-webkit-filter:grayscale(100%);-moz-filter:grayscale(100%);-ms-filter:grayscale(100%);-o-filter:grayscale(100%);filter:grayscale(100%);filter:gray}.t222__greyonhovercolor:hover{-webkit-filter:grayscale(0%);-moz-filter:grayscale(0%);-ms-filter:grayscale(0%);-o-filter:grayscale(0%);filter:grayscale(0%);filter:none}.t222__alphaonhover{opacity:.5}.t222__alphaonhover:hover{opacity:1}.t222 .t222__container{text-align:center}.t222 .t222__col_2{display:inline-block;float:none;margin-left:18px;margin-right:18px;padding:0;border:0;vertical-align:middle}.t222 .t222__col_3{display:inline-block;float:none;margin-left:10px;margin-right:10px;padding:0;border:0;vertical-align:middle}@media screen and (max-width:1200px){.t222 .t222__container{max-width:960px;margin-left:auto;margin-right:auto;padding:0}}@media screen and (max-width:960px){.t222 .t222__container{text-align:center}.t222 .t222__col_2{max-width:200px;margin-bottom:20px}.t222 .t222__col_3{max-width:160px;margin-bottom:20px}}@media screen and (max-width:640px){.t222 .t222__col_2{max-width:180px;margin-bottom:15px}.t222 .t222__col_3{max-width:240px;margin-bottom:20px}}@media screen and (max-width:480px){.t222 .t222__col_3{max-width:200px;margin-bottom:20px}}@media screen and (max-width:400px){.t222 .t222__col_2{max-width:140px;margin-bottom:10px}.t222 .t222__col_3{max-width:160px;margin-bottom:20px}}.t223__blocktext{padding-top:20px}.t223 iframe{display:block;border:0;padding:0}.t225__title{padding-top:8px;padding-bottom:3px}.t225__uptitle{text-transform:uppercase;padding-top:10px;padding-bottom:50px}.t225__descr{padding:41px 0 0 0}.t270__error-msg{text-align:center;display:none}.t270__error-msg-text{display:inline-block;margin:0 20px 35px 20px;padding:15px;color:red;border:1px solid red;font-size:14px;font-family:tfutura,Arial}.t250__text{text-align:center;margin-bottom:32px}.t250__link{text-align:center;text-decoration:none;display:block;width:110px;margin:0 auto;-webkit-transition:opacity ease-in-out 0.2s;-moz-transition:opacity ease-in-out 0.2s;-o-transition:opacity ease-in-out 0.2s;transition:opacity ease-in-out 0.2s}.t250__link__descr{font-size:12px;line-height:1.55;text-align:center}.t250__link:hover{opacity:.7}.t250__icon{width:28px;height:25px;margin:0 auto 12px;display:block}@media screen and (max-width:600px){.t250__text{margin-bottom:26px}.t250__img{width:24px;height:24px}}@media screen and (max-width:460px){.t250__text{margin-bottom:18px}.t250__img{width:18px;height:21px}}.t253{text-align:center}.t253__icon{color:#222;font-family:Georgia;font-size:70px;margin-bottom:0;line-height:1}.t253__text{margin-bottom:32px}@media screen and (max-width:600px){.t253__icon{font-size:36px}.t253__text{margin-bottom:28px}}@media screen and (max-width:480px){.t253__icon{font-size:30px;margin-bottom:0}.t253__text{margin-bottom:19px}}.t255__mainblock{margin:0 auto}.t255 .t-cover__wrapper span.space{height:60px}.t255__uptitle{color:#fff;text-transform:uppercase;margin-bottom:26px}.t255__title{letter-spacing:2px;color:#fff;margin:0 auto}.t255__userblock{position:absolute;bottom:70px;right:0;left:0}.t255__userblock-img{width:50px;height:50px;border-radius:100px;display:block;margin:0 auto 12px;background-size:cover;background-position:center;background-repeat:no-repeat}.t255__userblock-descr,.t255__userblock-date{color:#fff}@media screen and (max-width:660px){.t255__uptitle,.t255__title{padding-left:20px;padding-right:20px}.t255__title{padding-bottom:46px}.t255__userblock{bottom:20px;left:20px;right:20px}.t255__userblock-img{width:40px;height:40px}.t255__uptitle{margin-bottom:16px}}@media screen and (max-width:480px){.t255 .t-cover__wrapper span.space{height:0}}.t256__mainblock{margin:0 auto}.t256__video-container{z-index:190099;opacity:1;-webkit-transition:all ease-in-out .2s;-moz-transition:all ease-in-out .2s;-o-transition:all ease-in-out .2s;transition:all ease-in-out .2s;position:fixed;top:0;right:0;bottom:0;left:0}.t256__overflow{overflow:hidden}.t256__hidden{z-index:-1;opacity:0;-webkit-transition:all ease-in-out .2s;-moz-transition:all ease-in-out .2s;-o-transition:all ease-in-out .2s;transition:all ease-in-out .2s}.t256__video-bg{position:absolute;top:0;right:0;bottom:0;left:0}.t256__iframe{width:854px;height:480px;position:absolute;top:50%;margin-top:-240px;left:50%;margin-left:-427px;z-index:1}.t256__play-link{display:inline-block;margin-bottom:50px}.t256__play-icon{width:70px;height:70px;margin:0 auto;-webkit-transition:all ease-in-out .2s;-moz-transition:all ease-in-out .2s;-o-transition:all ease-in-out .2s;transition:all ease-in-out .2s;display:block;padding-top:100px}.t256__play-icon:hover{opacity:.8}.t256__title{color:#fff;margin-bottom:40px}.t256__descr{color:#fff}.t256__close{position:absolute;z-index:9999;right:0;top:0;background:#fff;width:30px;height:30px;border:5px solid #fff;-webkit-transition:all ease-in-out .2s;-moz-transition:all ease-in-out .2s;-o-transition:all ease-in-out .2s;transition:all ease-in-out .2s;opacity:1}.t256__close:hover{opacity:.8}.t256__close:before,.t256__close:after{content:'';position:absolute;height:1px;width:100%;top:50%;left:0;background:#222}.t256__close:before{-moz-transform:rotate(45deg);-ms-transform:rotate(45deg);-webkit-transform:rotate(45deg);-o-transform:rotate(45deg);transform:rotate(45deg)}.t256__close:after{-moz-transform:rotate(-45deg);-ms-transform:rotate(-45deg);-webkit-transform:rotate(-45deg);-o-transform:rotate(-45deg);transform:rotate(-45deg)}.t256__wrapper{padding:80px 0}@media screen and (max-height:480px){.t256__iframe{height:320px;width:540px;margin-top:-160px;margin-left:-270px}}@media screen and (max-width:854px){.t256__title{font-size:40px;margin-bottom:35px}.t256__play-link{margin-bottom:40px}.t256__iframe{height:320px;width:540px;margin-top:-160px;margin-left:-270px}.t256__wrapper{padding:50px 0}}@media screen and (max-width:640px){.t256__title,.t256__descr{padding:0 20px}.t256__wrapper{padding:30px 0}}@media screen and (max-width:540px){.t256__title{margin-bottom:22px}.t256__descr{font-size:14px}.t256__play-link{margin-bottom:25px}.t256__iframe{height:240px;width:100%;margin-top:-120px;margin-left:0;left:0}.t256__wrapper{padding:20px 0}}@media screen and (max-width:480px){.t256__title{margin-bottom:18px}.t256__descr{font-size:12px}.t256__play-link{margin-bottom:20px}}.t262__col{float:left;width:50%;height:100%}.t262__mainblock{height:700px}.t262__contentwrapper{display:table-cell;vertical-align:middle;padding:0 70px}.t262__contentbox{display:table;width:100%;color:#fff}.t262__title{margin-bottom:60px}@media screen and (max-width:900px){.t262__title{margin-bottom:40px;font-size:26px}.t262__mainblock,.t262__col,.t262__contentbox{height:460px!important}.t262__contentwrapper{display:table-cell;vertical-align:middle;padding:0 40px}}@media screen and (max-width:800px){.t262__title{font-size:21px;margin-bottom:30px}.t262__contentwrapper{padding:0 25px}.t262__mainblock,.t262__col,.t262__contentbox{height:390px!important}}@media screen and (max-width:700px){.t262__title{font-size:18px;margin-bottom:20px}.t262__mainblock,.t262__col,.t262__contentbox{height:320px!important}}@media screen and (max-width:600px){.t262__contentwrapper{padding:30px 20px}.t262__descr{font-size:12px}.t262__mainblock{height:auto!important}.t262__col,.t262__contentbox{float:none;width:100%;height:auto!important}.t262__map{height:300px!important}.t262__contentbox{height:auto!important}}.t269__mainblock{margin:0 auto}.t269__uptitle{color:#fff;position:absolute;top:80px;left:0;right:0}.t269__uptitle_mobile{display:none}.t269__title{color:#fff;margin-bottom:24px;padding-top:20px}.t269__descr{color:#fff;margin-bottom:44px}.t269__input-container{max-width:600px;margin:0 auto}.t269__blockinput{display:table-cell;vertical-align:middle;height:100%;width:100%;padding-right:20px}.t269__input{height:56px;outline:none}.t269__submit{height:56px;padding-left:40px;padding-right:40px}.t269__blockinput input{background-color:transparent;-webkit-appearance:none;border-radius:0}.t269__wrapper{display:table;-webkit-transition:all ease-in-out 0.2s;-moz-transition:all ease-in-out 0.2s;-o-transition:all ease-in-out 0.2s;transition:all ease-in-out 0.2s}.t269__blockinput.js-error-control-box .t269__input{border:1px solid red!important}.t269__blockinput-errors-text{color:#ff7;box-sizing:border-box;padding:0 10px 10px 10px;font-family:'Open Sans',serif}.t269__blockinput-errors-item{padding-top:10px;display:none;font-family:'Open Sans',serif}.t269__blockinput-errorbox{background:#f66 none repeat scroll 0 0;color:#ff7;padding:1px 10px;text-align:center;margin-bottom:20px;font-family:'Open Sans',serif;margin-top:20px}.t269__hint{color:#fff;margin-top:20px;max-width:600px;margin:20px auto 0}.t269__blockinput-success{text-align:center;color:#fff;padding:20px;font-family:'Open Sans',serif}.t269__success-message{color:#fff}.t269 .js-send-form-success .t269__wrapper{display:none}@media screen and (max-width:680px){.t269__blockinput{display:block;padding-right:0;width:100%}.t269__descr{margin-bottom:32px}.t269__uptitle_desktop{display:none}.t269__uptitle_mobile{display:block}.t269__uptitle{position:initial;top:40px;font-size:16px!important}.t269__mainwrapper{padding:0 20px}.t269__input-container{max-width:320px}.t269__input{width:100%;margin-bottom:18px;height:42px;font-size:14px;padding-left:14px}.t269__submit{width:100%;height:42px;font-size:14px}.t269__wrapper{display:block}}.t265__wrapper{padding:30px 20px 28px 55px;position:relative;text-align:left}.t265__icon{position:absolute;top:27px;left:20px}@media screen and (max-width:650px){.t265__wrapper{padding:20px 20px 16px 50px;margin:0 -20px}.t265__icon{top:16px;-moz-transform:scale(.8);-ms-transform:scale(.8);-webkit-transform:scale(.8);-o-transform:scale(.8);transform:scale(.8)}}.t186C__blockinput{display:block;vertical-align:middle;height:100%;padding-right:0;margin-bottom:25px}.t186C__blockinput textarea{padding-top:17px}.t186C__blocktitle{display:block;vertical-align:middle;height:100%;padding-right:0;padding-bottom:5px}.t186C__blockbutton{display:block;text-align:center;vertical-align:middle;height:100%;margin-bottom:10px}.t186C__nomargin .t186C__blocktitle{padding-bottom:0;margin-bottom:0}.t186C__nomargin .t186C__blockinput{margin-bottom:35px}.t186C__form-bottom-text{margin-top:30px;text-align:center}@media screen and (max-width:640px){.t186C__wrapper{display:block}.t186C__blockbutton{display:block;width:100%;padding-bottom:20px;text-align:center}.t186C__blockinput textarea{padding-top:5px}.t186C__blockinput{padding-right:0}.t186C .t-submit{width:100%}}.t186C__blockinput-errors{background:#f66 none repeat scroll 0 0}.js-error-control-box .t186C__input{border:1px solid red!important}.t186C__blockinput-errors-text{color:#ff7;box-sizing:border-box;padding:0 10px 10px 10px;font-family:'Open Sans',serif}.t186C__blockinput-errors-item{padding-top:10px;display:none;font-family:'Open Sans',serif}.t186C__blockinput-errorbox{background:#f66 none repeat scroll 0 0;color:#ff7;padding:10px;text-align:center;margin-bottom:20px;font-family:'Open Sans',serif}.t186C__blockinput-success{text-align:center;background:#FFF;color:#222;padding:20px;border:2px solid #2D2;margin-bottom:20px;font-family:'Open Sans',serif}.t278__mainwrapper{padding:0 20px}.t278__mainblock{margin:0 auto}.t278__mainblockleft{margin:0 0}.t278__mainblockright{margin:0 0 0 auto}.t278__title{color:#fff;margin-bottom:40px}.t278__descr{color:#fff;margin-bottom:50px}.t278__nomargin .t278__descr{margin-bottom:30px}.t278__text{color:#fff;margin-top:30px;margin-bottom:30px;opacity:.7}.t278__input-mainblock{margin:0 auto}.t278__wrapper{display:table;margin:0 auto}.t278__blockinput{display:inline-block;height:100%;width:100%;height:auto;margin-bottom:20px}.t278__blockinput textarea{padding-top:17px}.t278__input{height:56px;outline:none;background-color:transparent}.t278__blockbutton{display:inline-block;height:auto;width:100%}.t278 .t-submit{height:56px;padding:0 20px;-webkit-transition:all ease-in-out 0.2s;-moz-transition:all ease-in-out 0.2s;-o-transition:all ease-in-out 0.2s;transition:all ease-in-out 0.2s;width:100%}.t278 .t-submit:hover{opacity:.8}@media screen and (max-width:670px){.t278__title{margin-bottom:18px}.t278__descr{margin-bottom:30px}}@media screen and (max-width:500px){.t278__text{font-size:10px}.t278__blockinput{margin-bottom:15px}}.t278__blockinput-errors{background:#f66 none repeat scroll 0 0}.t278 .js-error-control-box .t278__input{border:1px solid red!important}.t278__blockinput-errors-text{color:#ff7;box-sizing:border-box;padding:0 10px 10px 10px;font-family:'Open Sans',serif}.t278__blockinput-errors-item{padding-top:10px;display:none;font-family:'Open Sans',serif}.t278__blockinput-errorbox{background:#f66 none repeat scroll 0 0;color:#ff7;padding:10px;text-align:center;margin-bottom:20px;font-family:'Open Sans',serif}.t278__blockinput-success{border:1px solid #fff;text-align:center;color:#fff;padding:20px;margin-bottom:20px}.t278__success-message{color:#fff}.t278 .js-send-form-success .t278__wrapper{display:none}.t328{padding:0 20px}.t-container.t328__container{position:relative;padding-top:20px;padding-bottom:20px}.t328__block{padding-right:40px}.t328__flipped .t328__block{padding-right:0;padding-left:40px}.t328__mainblock{margin:0 auto}.t328__line{position:absolute;width:2px;top:0;background:#eee;bottom:0;left:0;right:0;margin:0 auto}.t328__col{width:50%;text-align:right}.t328__flipped{float:right!important;text-align:left}.t328__circle{width:20px;height:20px;border-radius:100px;background:#eee;position:absolute;right:0;left:0;top:25px;margin:0 auto;border:2px solid #fff}.t328__img{width:100%;display:block;margin-bottom:14px;margin-left:auto}.t328__flipped .t328__img{margin-left:0}.t328__title{margin-bottom:6px}.t328__descr{color:#777;margin-top:10px;margin-bottom:5px}@media only screen and (max-width:640px){.t328__block{padding-right:30px}.t328__circle{width:12px;height:12px}.t328__flipped .t328__block{padding-left:30px}}@media only screen and (max-width:540px){.t328__block{padding-right:0;padding-left:20px}.t328__title{margin-bottom:0}.t328__descr{margin-top:5px}.t328__circle{width:10px;height:10px;top:22px;left:-2px;right:auto}.t328__col{float:right;text-align:left;width:100%}.t328__flipped .t328__block{padding-left:20px}.t328__line{right:auto;left:4px}.t328__img{margin-left:0}}.t330__wrapper{padding:40px 45px;background:#fff}.t330__title{margin-bottom:11px}.t330__descr{margin-bottom:24px}.t330__text{margin-top:20px}.t330__img{width:100%;display:block}.t330 .t-popup__container{background:transparent}@media screen and (max-width:640px){.t330__title{margin-bottom:6px}.t330__descr{margin-bottom:14px}.t330__wrapper{padding:20px}}.t330__blockinput{display:block;vertical-align:middle;height:100%;padding-right:0;margin-bottom:25px}.t330__blockinput textarea{padding-top:17px}.t330__blocktitle{display:block;vertical-align:middle;height:100%;padding-right:0;padding-bottom:5px}.t330__blockbutton{display:block;text-align:center;vertical-align:middle;height:100%;width:100%}.t330__submit,.t330__input{width:100%;height:54px;-webkit-appearance:none}@media screen and (max-width:640px){.t330__input-wrapper{display:block}.t330__blockbutton{display:block;padding-bottom:0;text-align:center}.t330__blockinput textarea{padding-top:5px}.t330__blockinput{padding-right:0;margin-bottom:20px}.t330__submit,.t330__input{height:46px;font-size:14px}.t330__input{padding:0 14px}}.t330__blockinput-errors{background:#f66 none repeat scroll 0 0}.js-error-control-box .t330__input{border:1px solid red!important}.t330__blockinput-errors-text{color:#ff7;box-sizing:border-box;padding:0 10px 10px 10px;font-family:'Open Sans',serif}.t330__blockinput-errors-item{padding-top:10px;display:none;font-family:'Open Sans',serif}.t330__blockinput-errorbox{background:#f66 none repeat scroll 0 0;color:#ff7;padding:10px;text-align:center;margin-bottom:20px;font-family:'Open Sans',serif}.t330__blockinput-success{text-align:center;background:#FFF;color:#222;padding:20px;border:2px solid #2D2;margin-bottom:20px;font-family:'Open Sans',serif}.t331__fullwidth .t331__video-carier,.t331__fullwidth .t331__youtube{height:100vh!important}.t331__fullwidth iframe{display:block}@media screen and (max-width:640px){.t331__fullwidth .t331__mainblock{padding:0}}.t333__wrapper{position:relative;text-align:left}.t333__uptitle{color:#fff;margin-bottom:20px}.t333__title{color:#fff}.t333__title-second{font-size:18px}.t333__descr{color:#fff;margin-top:20px}.t333__right-content{position:relative;padding:34px}.t333__bg{position:absolute;top:0;right:0;left:0;bottom:0;background:#eee}.t333__form-bottom-text{margin-top:20px}.t333__form,.t333__form-text,.t333__form-bottom-text{position:relative;z-index:1}.t333__blockinput{margin-bottom:20px}.t333__nomargin .t333__blockinput{margin-bottom:5px}.t333__nomargin .t333__blockbutton{margin-top:30px}.t333__nomargin .t333__form-text{margin-bottom:5px}.t333__input,.t333__submit{height:50px;padding:0 18px}.t333__submit{width:100%}.t333__textarea{padding-top:15px}.t333__form-text{margin-bottom:20px}.t333__blockinput-errors{background:#f66 none repeat scroll 0 0}.js-error-control-box .t333__input{border:1px solid red!important}.t333__blockinput-errors-text{color:#ff7;box-sizing:border-box;padding:0 10px 10px 10px;font-family:'Open Sans',serif}.t333__blockinput-errors-item{padding-top:10px;display:none;font-family:'Open Sans',serif}.t333__blockinput-errorbox{background:#f66 none repeat scroll 0 0;color:#ff7;padding:10px;text-align:center;margin-bottom:20px;font-family:'Open Sans',serif}.t333__blockinput-success{text-align:center;padding:20px;font-family:'Open Sans',serif}.t333 .js-send-form-success .t333__form-wrapper{display:none}@media screen and (max-width:960px){.t333__left-content{margin-bottom:35px}.t333__wrapper_witharrow{padding-bottom:70px}}@media screen and (max-width:640px){.t333__wrapper_witharrow{padding-bottom:20px}}.t334__table{display:table;width:100%;height:400px;vertical-align:middle;background-color:#000;position:relative;overflow:hidden}.t334__col{overflow:hidden}.t334__bg{background-position:center center;background-repeat:no-repeat;background-size:cover;position:absolute;top:0;right:0;bottom:0;left:0}.t334__cell:hover .t334__bg_animated{-moz-transform:scale(1.05);-ms-transform:scale(1.05);-webkit-transform:scale(1.05);-o-transform:scale(1.05);transform:scale(1.05)}.t334__overlay{position:absolute;top:0;right:0;bottom:0;left:0}.t334__show_hover .t334__overlay{opacity:0}.t334__cell:hover .t334__overlay{opacity:.8}.t334__show_hover .t334__cell:hover .t334__overlay{opacity:1}.t334__cell{display:table-cell;width:100%;height:100%}.t334__textwrapper{padding:20px 40px;position:relative}.t334__show_hover .t334__textwrapper{opacity:0}.t334__show_hover .t334__textwrapper.t334__textwrapper_animated{-moz-transform:translateY(20%);-ms-transform:translateY(20%);-webkit-transform:translateY(20%);-o-transform:translateY(20%);transform:translateY(20%)}.t334__show_hover .t334__cell:hover .t334__textwrapper{opacity:1}.t334__cell:hover .t334__textwrapper_animated{-moz-transform:translateY(0);-ms-transform:translateY(0);-webkit-transform:translateY(0);-o-transform:translateY(0);transform:translateY(0)}.t334__textwrapper__content{margin:30px auto;position:relative}.t334__text{color:#fff;margin-top:20px}.t334__title{color:#fff}.t334__title_small{font-size:28px;line-height:1.25}.t334__img{width:100%;max-width:70px}.t334__animation_fast{-webkit-transition:all ease-in-out .25s;-moz-transition:all ease-in-out .25s;-o-transition:all ease-in-out .25s;transition:all ease-in-out .25s}.t334__animation_slow{-webkit-transition:all ease-in-out .45s;-moz-transition:all ease-in-out .45s;-o-transition:all ease-in-out .45s;transition:all ease-in-out .45s}.t334__button-container{-webkit-transition:all ease-in-out .2s;-moz-transition:all ease-in-out .2s;-o-transition:all ease-in-out .2s;transition:all ease-in-out .2s;position:absolute;right:0;bottom:0;left:0;opacity:0}.t334__button-container_show{opacity:1}.t334__textwrapper__content{-webkit-transition:all ease-in-out .2s;-moz-transition:all ease-in-out .2s;-o-transition:all ease-in-out .2s;transition:all ease-in-out .2s}.t334__button-wrapper{display:inline-block;margin-top:40px}.t334__submit{text-align:center;height:50px;vertical-align:middle;display:table-cell;border:0 none;font-size:16px;padding-left:34px;padding-right:34px;-webkit-appearance:none;background:none}.t334__submit_middle{font-size:14px;height:44px;line-height:38px;padding-left:30px;padding-right:30px}.t334__submit_small{font-size:12px;height:40px;line-height:30px;padding-left:24px;padding-right:24px}.t334__button-bottom .t334__textwrapper{position:static}.t334__button-bottom .t334__button-container{left:40px;bottom:40px;right:40px;-moz-transform:translateY(30%);-ms-transform:translateY(30%);-webkit-transform:translateY(30%);-o-transform:translateY(30%);transform:translateY(30%)}.t334__button-bottom .t334__button-container.t334__button-container_show{left:40px;bottom:40px;right:40px;-moz-transform:translateY(0);-ms-transform:translateY(0);-webkit-transform:translateY(0);-o-transform:translateY(0);transform:translateY(0)}@media screen and (max-width:960px){.t334 .t334__col{margin-bottom:40px}}@media screen and (max-width:640px){.t334 .t334__table{height:350px}.t334__textwrapper{padding:20px 20px}.t334__button-bottom .t334__button-container{left:20px;right:20px;bottom:20px}.t334__title_small{font-size:21px}}.t335__table{display:table;width:100%;vertical-align:middle;background-color:#000;position:relative;overflow:hidden}.t335__col{overflow:hidden}.t335__bg{background-position:center center;background-repeat:no-repeat;background-size:cover;position:absolute;top:0;right:0;bottom:0;left:0}.t335__cell:hover .t335__bg_animated{-moz-transform:scale(1.05);-ms-transform:scale(1.05);-webkit-transform:scale(1.05);-o-transform:scale(1.05);transform:scale(1.05)}.t335__overlay{position:absolute;top:0;right:0;bottom:0;left:0}.t335__show_hover .t335__overlay{opacity:0}.t335__cell:hover .t335__overlay{opacity:.8}.t335__show_hover .t335__cell:hover .t335__overlay{opacity:1}.t335__cell{display:table-cell;width:100%;height:100%}.t335__textwrapper{padding:20px 40px;position:relative}.t335__show_hover .t335__textwrapper{opacity:0}.t335__show_hover .t335__textwrapper.t335__textwrapper_animated{-moz-transform:translateY(20%);-ms-transform:translateY(20%);-webkit-transform:translateY(20%);-o-transform:translateY(20%);transform:translateY(20%)}.t335__show_hover .t335__cell:hover .t335__textwrapper{opacity:1}.t335__cell:hover .t335__textwrapper_animated{-moz-transform:translateY(0);-ms-transform:translateY(0);-webkit-transform:translateY(0);-o-transform:translateY(0);transform:translateY(0)}.t335__textwrapper__content{margin:30px auto;position:relative}.t335__text{color:#fff;margin-top:20px}.t335__title{color:#fff}.t335__img{width:100%;max-width:70px}.t335__animation_fast{-webkit-transition:all ease-in-out .25s;-moz-transition:all ease-in-out .25s;-o-transition:all ease-in-out .25s;transition:all ease-in-out .25s}.t335__animation_slow{-webkit-transition:all ease-in-out .45s;-moz-transition:all ease-in-out .45s;-o-transition:all ease-in-out .45s;transition:all ease-in-out .45s}.t-cell_100 .t335__table{height:80vh}.t-cell_50 .t335__table{height:80vh}.t-cell_33 .t335__table{height:60vh}.t-cell_25 .t335__table{height:60vh}.t-cell_25 .t335__textwrapper{padding:20px}.t335__button-container{-webkit-transition:all ease-in-out .2s;-moz-transition:all ease-in-out .2s;-o-transition:all ease-in-out .2s;transition:all ease-in-out .2s;position:absolute;right:0;bottom:0;left:0;opacity:0}.t335__button-container_show{opacity:1}.t335__textwrapper__content{-webkit-transition:all ease-in-out .2s;-moz-transition:all ease-in-out .2s;-o-transition:all ease-in-out .2s;transition:all ease-in-out .2s}.t335__button-wrapper{display:inline-block;margin-top:40px}.t335__submit{text-align:center;height:50px;vertical-align:middle;display:table-cell;border:0 none;font-size:16px;padding-left:34px;padding-right:34px;-webkit-appearance:none;background:none}.t335__submit_middle{font-size:14px;height:44px;line-height:44px;padding-left:30px;padding-right:30px}.t335__submit_small{font-size:12px;height:40px;line-height:40px;padding-left:24px;padding-right:24px}.t335__button-bottom .t335__textwrapper{position:static}.t335__button-bottom .t335__button-container{left:40px;bottom:40px;right:40px;-moz-transform:translateY(30%);-ms-transform:translateY(30%);-webkit-transform:translateY(30%);-o-transform:translateY(30%);transform:translateY(30%)}.t-cell_25 .t335__button-bottom .t335__button-container{left:20px;bottom:30px;right:20px}.t-cell_25 .t335__textwrapper__content{margin-top:10px}.t335__button-bottom .t335__button-container.t335__button-container_show{-moz-transform:translateY(0);-ms-transform:translateY(0);-webkit-transform:translateY(0);-o-transform:translateY(0);transform:translateY(0)}@media screen and (max-width:960px){.t335__col.t-cell_25{width:50vw;float:left}}@media screen and (max-width:700px){.t335__col.t-cell_50,.t335__col.t-cell_33{width:100vw;display:block}.t335__col .t335__table{height:380px}.t335__textwrapper{padding:20px 20px}}@media screen and (max-width:500px){.t335__col.t-cell_25{width:100vw;display:block}}.t338__logo{margin-bottom:55px;max-width:280px;width:100%}.t338__title{color:#fff;margin-bottom:50px}.t338__descr{color:#fff;margin-bottom:63px}.t338__btn{border-radius:100px;font-size:14px;height:50px;padding-right:34px;padding-left:34px;color:#fff}.t358__fullwidth .t358__video-carier,.t358__fullwidth .t358__vimeo{height:100vh!important}.t358__fullwidth iframe{display:block}@media screen and (max-width:640px){.t358__fullwidth .t358__mainblock{padding:0}}.t372__line{width:80px;height:2px;background:#222;margin-bottom:14px}.t372__line-center{margin-left:auto;margin-right:auto}.t372__line-right{margin-left:auto;margin-right:0}.t387__img{width:100px;height:100px}.t387__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}.t387__title{margin-top:23px}.t387__descr{margin-top:20px}@media screen and (max-width:960px){.t387__col{margin-bottom:40px}}.t408__uptitle,.t408__title,.t408__descr{color:#fff}.t408__uptitle{margin-bottom:26px}.t408__img{width:100px;height:100px}.t408__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}.t408__textwrapper{box-sizing:border-box;margin:0 auto 70px;padding:0 20px}.t408__textwrapper .t408__descr{margin-top:26px}.t408__blockswrapper .t408__descr{margin-top:18px}.t408__blockswrapper .t408__title{margin-top:20px}.t408__buttonwrapper{margin-top:60px}.t408 .t-btn{font-size:14px;height:54px;border:1px solid #fff;padding:0 30px;color:#fff}.t408__wrapper{padding:50px 0;position:relative;z-index:2}.t408__blockswrapper:before,.t408__blockswrapper:after{content:"";display:table;clear:both}.t408__blockswrapper .t408__wrapper{padding:0}@media screen and (max-width:960px){.t408__col{margin-bottom:40px}.t408__col:last-child{margin-bottom:0}}.t410 .jx-image .jx-label{font-family:'Roboto',sans-serif;font-weight:300;font-size:14px;padding:.25em .6em}.t410__wrapper{position:relative}.t410 .juxtapose{width:100%!important}.t410 .jx-knightlab{display:none!important}.t412{text-align:center}.t412__img{margin-bottom:30px;width:100px;height:100px}.t412__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}.t412__title{margin-bottom:25px;padding:0 25px}.t412__descr{font-size:16px;line-height:25px;padding:0 25px;padding-bottom:3px;padding-top:1px}.t412__content{border:0 solid #000;padding:35px 0 48px 0;box-sizing:border-box}.t412__wrapper{box-sizing:content-box;width:100%;height:100%}.t412__btn{font-size:14px;height:54px;padding-left:30px;padding-right:30px;margin-top:40px}.t412__buttonwrapper{display:block}@media screen and (max-width:960px){.t412__col{max-width:100%;margin-bottom:40px;height:auto!important;border:none}}.t427 .t-col{position:relative}.t427__img{margin-bottom:30px;width:100px;height:100px}.t427__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}.t427__textwrapper{padding:0 20px;text-align:center}.t427__text{padding-top:15px}.t427__uptitle{padding-bottom:15px}.t427__arrow{max-width:160px;display:inline-block;position:absolute;top:0;left:-20px;-moz-transform:translate(-50%,0);-ms-transform:translate(-50%,0);-webkit-transform:translate(-50%,0);-o-transform:translate(-50%,0);transform:translate(-50%,0)}.t427__arrow img{width:100%}.t427__btn-wrapper{text-align:center}.t427__btn{margin-top:40px;font-size:14px;height:54px;padding:0 30px}@media screen and (max-width:1200px){.t427__arrow{left:-10px}}@media screen and (max-width:960px){.t427 .t-col{text-align:center}.t427__mobile-col-padding{box-sizing:border-box;padding-bottom:45px}.t427__arrow{position:static;-moz-transform:rotate(90deg);-ms-transform:rotate(90deg);-webkit-transform:rotate(90deg);-o-transform:rotate(90deg);transform:rotate(90deg);margin-bottom:45px}.t427__img{margin:0 0 15px 0}}.t428__col{vertical-align:top;position:relative;height:auto}.t428__col-wrapper{text-align:center;box-sizing:border-box;padding:0 25px}.t428__line{width:1px;background:#eee;position:absolute;top:0;bottom:0;left:-20px;-moz-transform:translate(-50%,0);-ms-transform:translate(-50%,0);-webkit-transform:translate(-50%,0);-o-transform:translate(-50%,0);transform:translate(-50%,0)}.t428__img{margin:0 auto 30px auto}.t428__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}.t428__title{padding-bottom:20px}.t428__uptitle{font-weight:800;padding-bottom:15px}@media screen and (max-width:1200px){.t428__line{left:-10px}}@media screen and (max-width:960px){.t428__col{padding:0 5% 0 5%;width:100%;height:auto!important;display:block}.t428__col-wrapper{padding:45px 0 45px 0}.t428__col-wrapper_fisrt{padding-top:0}.t428__line{-moz-transform:translate(0,0);-ms-transform:translate(0,0);-webkit-transform:translate(0,0);-o-transform:translate(0,0);transform:translate(0,0);width:90%!important;margin:0 5% 0 5%;left:0;height:1px}.t428__img{margin-bottom:35px}.t428__title,.t428__uptitle{padding-bottom:10px}}.t449.t449__beforeready{-moz-transform:translate(100%,-50%);-ms-transform:translate(100%,-50%);-webkit-transform:translate(100%,-50%);-o-transform:translate(100%,-50%);transform:translate(100%,-50%)}.t449.t449__flipped.t449__beforeready{-moz-transform:translate(-100%,-50%);-ms-transform:translate(-100%,-50%);-webkit-transform:translate(-100%,-50%);-o-transform:translate(-100%,-50%);transform:translate(-100%,-50%)}.t449{position:fixed;top:50%;right:0;-moz-transform:translate(0,-50%);-ms-transform:translate(0,-50%);-webkit-transform:translate(0,-50%);-o-transform:translate(0,-50%);transform:translate(0,-50%);-webkit-transition:transform ease-in-out .3s;-moz-transition:transform ease-in-out .3s;-o-transition:transform ease-in-out .3s;transition:transform ease-in-out .3s;z-index:100}.t449.t449__preview.t449__beforeready,.t449.t449__preview{position:relative;top:auto;-moz-transform:translate(0,0);-ms-transform:translate(0,0);-webkit-transform:translate(0,0);-o-transform:translate(0,0);transform:translate(0,0);margin-left:auto;width:52px}.t449.t449__flipped.t449__preview{margin-left:0}.t449.t449__flipped{left:0;right:auto}.t449 .ya-share2__title{display:none}.t449 .ya-share2__list_direction_vertical>.ya-share2__item{margin:0}.t449 .ya-share2__badge{border-radius:0}.t449 .ya-share2__link{padding:12px}.t449 .ya-share2__item_service_facebook .ya-share2__link{background-color:#3b5998}.t449 .ya-share2__item_service_vkontakte .ya-share2__link{background-color:#48729e}.t449 .ya-share2__item_service_odnoklassniki .ya-share2__link{background-color:#eb722e}.t449 .ya-share2__item_service_twitter .ya-share2__link{background-color:#00aced}.t449__transp-white .ya-share2__link{background-color:transparent!important}.t449__transp-black .ya-share2__link{background-color:transparent!important}.t449__white-black .ya-share2__link{background-color:#fff!important;border-bottom:1px solid rgba(0,0,0,.2)}.t449__white-black .ya-share2__item:last-child .ya-share2__link{border-bottom:0}.t449__black-white .ya-share2__link{background-color:#111!important;border-bottom:1px solid rgba(255,255,255,.2)}.t449__black-white .ya-share2__item:last-child .ya-share2__link{border-bottom:0}.t449 .ya-share2__container_size_m .ya-share2__icon{width:28px;height:28px}.t449 .ya-share2__list{margin-bottom:0}.t449__black-white .ya-share2__badge{background-color:#111!important}.t449__transp-white .ya-share2__badge{background-color:transparent!important}.t449__white-black .ya-share2__badge{background-color:#fff!important}.t449__white-black .ya-share2__container_size_m .ya-share2__item_service_facebook .ya-share2__icon{background-image:url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjMjIyIiB2aWV3Qm94PSIwIDAgMjggMjgiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTE1LjEgMjN2LTguMjFoMi43NzNsLjQxNS0zLjJIMTUuMVY5LjU0N2MwLS45MjcuMjYtMS41NTggMS41OTYtMS41NThsMS43MDQtLjAwMlY1LjEyNkEyMi43ODcgMjIuNzg3IDAgMCAwIDE1LjkxNyA1QzEzLjQ2IDUgMTEuNzggNi40OTIgMTEuNzggOS4yM3YyLjM2SDl2My4yaDIuNzhWMjNoMy4zMnoiIGZpbGwtcnVsZT0iZXZlbm9kZCIvPjwvc3ZnPg==)}.t449__white-black .ya-share2__container_size_m .ya-share2__item_service_vkontakte .ya-share2__icon{background-image:url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjMjIyIiB2aWV3Qm94PSIwIDAgMjggMjgiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTE0Ljg4MyAxOS4zOTZzLjMyNS0uMDM2LjQ5LS4yMThjLjE1NC0uMTY3LjE1LS40OC4xNS0uNDhzLS4wMjMtMS40NjguNjQ4LTEuNjg0Yy42Ni0uMjEzIDEuNTEgMS40MTggMi40MDggMi4wNDYuNjguNDc0IDEuMTk3LjM3IDEuMTk3LjM3bDIuNDA0LS4wMzRzMS4yNTYtLjA4LjY2LTEuMDg0Yy0uMDUtLjA4Mi0uMzQ4LS43NDMtMS43ODgtMi4xMDItMS41MDctMS40MjMtMS4zMDUtMS4xOTIuNTEtMy42NTMgMS4xMDYtMS40OTggMS41NDgtMi40MTIgMS40MS0yLjgwNC0uMTMyLS4zNzMtLjk0NS0uMjc1LS45NDUtLjI3NWwtMi43MDYuMDE3cy0uMi0uMDI4LS4zNS4wNjNjLS4xNDQuMDg4LS4yMzguMjk1LS4yMzguMjk1cy0uNDI4IDEuMTYtMSAyLjE0NmMtMS4yMDQgMi4wOC0xLjY4NiAyLjE5LTEuODgzIDIuMDYtLjQ2LS4zLS4zNDUtMS4yMS0uMzQ1LTEuODU1IDAtMi4wMTcuMy0yLjg1Ny0uNTg2LTMuMDc1LS4yOTUtLjA3Mi0uNTEyLS4xMi0xLjI2NC0uMTI4LS45NjYtLjAxLTEuNzgzLjAwMy0yLjI0Ni4yMzQtLjMwOC4xNTMtLjU0Ni40OTUtLjQuNTE0LjE3OC4wMjUuNTgzLjExLjc5OC40MS4yNzcuMzgyLjI2OCAxLjI0NC4yNjggMS4yNDRzLjE2IDIuMzczLS4zNzMgMi42NjhjLS4zNjUuMjAyLS44NjUtLjIxLTEuOTQtMi4wOTgtLjU1LS45NjctLjk2Ni0yLjAzNi0uOTY2LTIuMDM2cy0uMDgtLjItLjIyMy0uMzA2Yy0uMTczLS4xMy0uNDE2LS4xNy0uNDE2LS4xN2wtMi41Ny4wMTZzLS4zODguMDEtLjUzLjE4MmMtLjEyNS4xNTItLjAxLjQ2Ni0uMDEuNDY2czIuMDE0IDQuNzkgNC4yOTQgNy4yMDJjMi4wOSAyLjIxNCA0LjQ2NSAyLjA2OCA0LjQ2NSAyLjA2OGgxLjA3NnoiICBmaWxsLXJ1bGU9ImV2ZW5vZGQiLz48L3N2Zz4=)}.t449__white-black .ya-share2__container_size_m .ya-share2__item_service_twitter .ya-share2__icon{background-image:url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjMjIyIiB2aWV3Qm94PSIwIDAgMjggMjgiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTIzIDguNzNhNy4zOCA3LjM4IDAgMCAxLTIuMTIuNTgzIDMuNzA2IDMuNzA2IDAgMCAwIDEuNjIzLTIuMDQzIDcuMzk3IDcuMzk3IDAgMCAxLTIuMzQ2Ljg5NiAzLjY5MyAzLjY5MyAwIDAgMC02LjI5MyAzLjM2OCAxMC40ODUgMTAuNDg1IDAgMCAxLTcuNjEtMy44NThjLS4zMi41NDUtLjUgMS4xOC0uNSAxLjg1NiAwIDEuMjguNjUgMi40MSAxLjY0MiAzLjA3M2EzLjY4MyAzLjY4MyAwIDAgMS0xLjY3My0uNDYydi4wNDdjMCAxLjc4OCAxLjI3MyAzLjI4IDIuOTYyIDMuNjJhMy43MTggMy43MTggMCAwIDEtMS42NjcuMDYzIDMuNjk3IDMuNjk3IDAgMCAwIDMuNDUgMi41NjRBNy40MSA3LjQxIDAgMCAxIDUgMTkuOTY3YTEwLjQ1MyAxMC40NTMgMCAwIDAgNS42NiAxLjY1OGM2Ljc5NCAwIDEwLjUwOC01LjYyNiAxMC41MDgtMTAuNTA1IDAtLjE2LS4wMDMtLjMyLS4wMS0uNDc4QTcuNTA3IDcuNTA3IDAgMCAwIDIzIDguNzMyeiIgZmlsbC1ydWxlPSJldmVub2RkIi8+PC9zdmc+)}.t449__white-black .ya-share2__container_size_m .ya-share2__item_service_odnoklassniki .ya-share2__icon{background-image:url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz48IURPQ1RZUEUgc3ZnIFBVQkxJQyAiLS8vVzNDLy9EVEQgU1ZHIDEuMS8vRU4iICJodHRwOi8vd3d3LnczLm9yZy9HcmFwaGljcy9TVkcvMS4xL0RURC9zdmcxMS5kdGQiPjxzdmcgdmVyc2lvbj0iMS4xIiBpZD0iTGF5ZXJfMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgeD0iMHB4IiB5PSIwcHgiIHdpZHRoPSIxNTBweCIgaGVpZ2h0PSIxNTBweCIgdmlld0JveD0iMCAwIDE1MCAxNTAiIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDE1MCAxNTAiIHhtbDpzcGFjZT0icHJlc2VydmUiPjx0aXRsZT5TaGFwZTwvdGl0bGU+PGRlc2M+Q3JlYXRlZCB3aXRoIFNrZXRjaC48L2Rlc2M+PGcgaWQ9IldlbGNvbWUiPjxwYXRoIGlkPSJTaGFwZSIgZmlsbD0iIzIyMjIyMiIgZD0iTTc0Ljk5Nyw0Ni4wMTFjLTQuOTAzLDAuMDA2LTguODc1LDMuOTc5LTguODgzLDguODgzYzAsNC44OTQsMy45ODUsOC44NzksOC44ODMsOC44NzljNC45MDMtMC4wMDgsOC44NzUtMy45NzksOC44OC04Ljg3OUM4My44NzksNDkuOTg5LDc5LjksNDYuMDE3LDc0Ljk5Nyw0Ni4wMTFMNzQuOTk3LDQ2LjAxMXogTTc0Ljk5Nyw3Ni4zMzhjLTExLjgzOC0wLjAxLTIxLjQzNy05LjYwNi0yMS40NDgtMjEuNDQ0YzAuMDA4LTExLjg0Niw5LjYwNC0yMS40NDIsMjEuNDQ4LTIxLjQ1NWMxMS44NDUsMC4wMSwyMS40NTEsOS42MDksMjEuNDU2LDIxLjQ1NUM5Ni40MzgsNjYuNzM0LDg2LjgzOCw3Ni4zMyw3NC45OTcsNzYuMzM4TDc0Ljk5Nyw3Ni4zMzh6IE02Ni4zMiw5My44MzZjLTQuNDEyLTEuMDAyLTguNjI0LTIuNzQ4LTEyLjQ1NS01LjE1NGMtMi45MzktMS44NS0zLjgyMy01LjczNC0xLjk3My04LjY2OGMxLjg0OC0yLjk0MSw1LjcyOC0zLjgyMiw4LjY2Ni0xLjk3NWM4LjgzNCw1LjUyMywyMC4wNTIsNS41MjMsMjguODg2LDBjMS45MDEtMS4xOTUsNC4yOTctMS4yODcsNi4yODQtMC4yNDJjMS45ODQsMS4wNDksMy4yNiwzLjA3OCwzLjM0Miw1LjMyNGMwLjA4NywyLjI0LTEuMDI3LDQuMzYzLTIuOTMsNS41NjFjLTMuODM0LDIuNDA2LTguMDQ5LDQuMTQ4LTEyLjQ1Nyw1LjE1NGwxMS45OTQsMTJjMi40NTEsMi40NTcsMi40NDYsNi40MzYtMC4wMTEsOC44OTNjLTIuNDU2LDIuNDQ1LTYuNDM0LDIuNDQ1LTguODg2LTAuMDEybC0xMS43NzktMTEuNzg5bC0xMS43ODUsMTEuNzg5Yy0yLjQ1NSwyLjQ1Ny02LjQzNiwyLjQ1Ny04Ljg4OSwwYy0yLjQ1NC0yLjQ1NS0yLjQ1NC02LjQzNCwwLTguODkxTDY2LjMyLDkzLjgzNkw2Ni4zMiw5My44MzZ6Ii8+PC9nPjwvc3ZnPg==);background-size:30px 30px}.t449__transp-black .ya-share2__badge{background-color:transparent!important}.t449__transp-black .ya-share2__container_size_m .ya-share2__item_service_facebook .ya-share2__icon{background-image:url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjMjIyIiB2aWV3Qm94PSIwIDAgMjggMjgiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTE1LjEgMjN2LTguMjFoMi43NzNsLjQxNS0zLjJIMTUuMVY5LjU0N2MwLS45MjcuMjYtMS41NTggMS41OTYtMS41NThsMS43MDQtLjAwMlY1LjEyNkEyMi43ODcgMjIuNzg3IDAgMCAwIDE1LjkxNyA1QzEzLjQ2IDUgMTEuNzggNi40OTIgMTEuNzggOS4yM3YyLjM2SDl2My4yaDIuNzhWMjNoMy4zMnoiIGZpbGwtcnVsZT0iZXZlbm9kZCIvPjwvc3ZnPg==)}.t449__transp-black .ya-share2__container_size_m .ya-share2__item_service_vkontakte .ya-share2__icon{background-image:url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjMjIyIiB2aWV3Qm94PSIwIDAgMjggMjgiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTE0Ljg4MyAxOS4zOTZzLjMyNS0uMDM2LjQ5LS4yMThjLjE1NC0uMTY3LjE1LS40OC4xNS0uNDhzLS4wMjMtMS40NjguNjQ4LTEuNjg0Yy42Ni0uMjEzIDEuNTEgMS40MTggMi40MDggMi4wNDYuNjguNDc0IDEuMTk3LjM3IDEuMTk3LjM3bDIuNDA0LS4wMzRzMS4yNTYtLjA4LjY2LTEuMDg0Yy0uMDUtLjA4Mi0uMzQ4LS43NDMtMS43ODgtMi4xMDItMS41MDctMS40MjMtMS4zMDUtMS4xOTIuNTEtMy42NTMgMS4xMDYtMS40OTggMS41NDgtMi40MTIgMS40MS0yLjgwNC0uMTMyLS4zNzMtLjk0NS0uMjc1LS45NDUtLjI3NWwtMi43MDYuMDE3cy0uMi0uMDI4LS4zNS4wNjNjLS4xNDQuMDg4LS4yMzguMjk1LS4yMzguMjk1cy0uNDI4IDEuMTYtMSAyLjE0NmMtMS4yMDQgMi4wOC0xLjY4NiAyLjE5LTEuODgzIDIuMDYtLjQ2LS4zLS4zNDUtMS4yMS0uMzQ1LTEuODU1IDAtMi4wMTcuMy0yLjg1Ny0uNTg2LTMuMDc1LS4yOTUtLjA3Mi0uNTEyLS4xMi0xLjI2NC0uMTI4LS45NjYtLjAxLTEuNzgzLjAwMy0yLjI0Ni4yMzQtLjMwOC4xNTMtLjU0Ni40OTUtLjQuNTE0LjE3OC4wMjUuNTgzLjExLjc5OC40MS4yNzcuMzgyLjI2OCAxLjI0NC4yNjggMS4yNDRzLjE2IDIuMzczLS4zNzMgMi42NjhjLS4zNjUuMjAyLS44NjUtLjIxLTEuOTQtMi4wOTgtLjU1LS45NjctLjk2Ni0yLjAzNi0uOTY2LTIuMDM2cy0uMDgtLjItLjIyMy0uMzA2Yy0uMTczLS4xMy0uNDE2LS4xNy0uNDE2LS4xN2wtMi41Ny4wMTZzLS4zODguMDEtLjUzLjE4MmMtLjEyNS4xNTItLjAxLjQ2Ni0uMDEuNDY2czIuMDE0IDQuNzkgNC4yOTQgNy4yMDJjMi4wOSAyLjIxNCA0LjQ2NSAyLjA2OCA0LjQ2NSAyLjA2OGgxLjA3NnoiICBmaWxsLXJ1bGU9ImV2ZW5vZGQiLz48L3N2Zz4=)}.t449__transp-black .ya-share2__container_size_m .ya-share2__item_service_twitter .ya-share2__icon{background-image:url(data:image/svg+xml;base64,PHN2ZyBmaWxsPSIjMjIyIiB2aWV3Qm94PSIwIDAgMjggMjgiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI+PHBhdGggZD0iTTIzIDguNzNhNy4zOCA3LjM4IDAgMCAxLTIuMTIuNTgzIDMuNzA2IDMuNzA2IDAgMCAwIDEuNjIzLTIuMDQzIDcuMzk3IDcuMzk3IDAgMCAxLTIuMzQ2Ljg5NiAzLjY5MyAzLjY5MyAwIDAgMC02LjI5MyAzLjM2OCAxMC40ODUgMTAuNDg1IDAgMCAxLTcuNjEtMy44NThjLS4zMi41NDUtLjUgMS4xOC0uNSAxLjg1NiAwIDEuMjguNjUgMi40MSAxLjY0MiAzLjA3M2EzLjY4MyAzLjY4MyAwIDAgMS0xLjY3My0uNDYydi4wNDdjMCAxLjc4OCAxLjI3MyAzLjI4IDIuOTYyIDMuNjJhMy43MTggMy43MTggMCAwIDEtMS42NjcuMDYzIDMuNjk3IDMuNjk3IDAgMCAwIDMuNDUgMi41NjRBNy40MSA3LjQxIDAgMCAxIDUgMTkuOTY3YTEwLjQ1MyAxMC40NTMgMCAwIDAgNS42NiAxLjY1OGM2Ljc5NCAwIDEwLjUwOC01LjYyNiAxMC41MDgtMTAuNTA1IDAtLjE2LS4wMDMtLjMyLS4wMS0uNDc4QTcuNTA3IDcuNTA3IDAgMCAwIDIzIDguNzMyeiIgZmlsbC1ydWxlPSJldmVub2RkIi8+PC9zdmc+)}.t449__transp-black .ya-share2__container_size_m .ya-share2__item_service_odnoklassniki .ya-share2__icon{background-image:url(data:image/svg+xml;base64,PD94bWwgdmVyc2lvbj0iMS4wIiBlbmNvZGluZz0idXRmLTgiPz48IURPQ1RZUEUgc3ZnIFBVQkxJQyAiLS8vVzNDLy9EVEQgU1ZHIDEuMS8vRU4iICJodHRwOi8vd3d3LnczLm9yZy9HcmFwaGljcy9TVkcvMS4xL0RURC9zdmcxMS5kdGQiPjxzdmcgdmVyc2lvbj0iMS4xIiBpZD0iTGF5ZXJfMSIgeG1sbnM9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxuczp4bGluaz0iaHR0cDovL3d3dy53My5vcmcvMTk5OS94bGluayIgeD0iMHB4IiB5PSIwcHgiIHdpZHRoPSIxNTBweCIgaGVpZ2h0PSIxNTBweCIgdmlld0JveD0iMCAwIDE1MCAxNTAiIGVuYWJsZS1iYWNrZ3JvdW5kPSJuZXcgMCAwIDE1MCAxNTAiIHhtbDpzcGFjZT0icHJlc2VydmUiPjx0aXRsZT5TaGFwZTwvdGl0bGU+PGRlc2M+Q3JlYXRlZCB3aXRoIFNrZXRjaC48L2Rlc2M+PGcgaWQ9IldlbGNvbWUiPjxwYXRoIGlkPSJTaGFwZSIgZmlsbD0iIzIyMjIyMiIgZD0iTTc0Ljk5Nyw0Ni4wMTFjLTQuOTAzLDAuMDA2LTguODc1LDMuOTc5LTguODgzLDguODgzYzAsNC44OTQsMy45ODUsOC44NzksOC44ODMsOC44NzljNC45MDMtMC4wMDgsOC44NzUtMy45NzksOC44OC04Ljg3OUM4My44NzksNDkuOTg5LDc5LjksNDYuMDE3LDc0Ljk5Nyw0Ni4wMTFMNzQuOTk3LDQ2LjAxMXogTTc0Ljk5Nyw3Ni4zMzhjLTExLjgzOC0wLjAxLTIxLjQzNy05LjYwNi0yMS40NDgtMjEuNDQ0YzAuMDA4LTExLjg0Niw5LjYwNC0yMS40NDIsMjEuNDQ4LTIxLjQ1NWMxMS44NDUsMC4wMSwyMS40NTEsOS42MDksMjEuNDU2LDIxLjQ1NUM5Ni40MzgsNjYuNzM0LDg2LjgzOCw3Ni4zMyw3NC45OTcsNzYuMzM4TDc0Ljk5Nyw3Ni4zMzh6IE02Ni4zMiw5My44MzZjLTQuNDEyLTEuMDAyLTguNjI0LTIuNzQ4LTEyLjQ1NS01LjE1NGMtMi45MzktMS44NS0zLjgyMy01LjczNC0xLjk3My04LjY2OGMxLjg0OC0yLjk0MSw1LjcyOC0zLjgyMiw4LjY2Ni0xLjk3NWM4LjgzNCw1LjUyMywyMC4wNTIsNS41MjMsMjguODg2LDBjMS45MDEtMS4xOTUsNC4yOTctMS4yODcsNi4yODQtMC4yNDJjMS45ODQsMS4wNDksMy4yNiwzLjA3OCwzLjM0Miw1LjMyNGMwLjA4NywyLjI0LTEuMDI3LDQuMzYzLTIuOTMsNS41NjFjLTMuODM0LDIuNDA2LTguMDQ5LDQuMTQ4LTEyLjQ1Nyw1LjE1NGwxMS45OTQsMTJjMi40NTEsMi40NTcsMi40NDYsNi40MzYtMC4wMTEsOC44OTNjLTIuNDU2LDIuNDQ1LTYuNDM0LDIuNDQ1LTguODg2LTAuMDEybC0xMS43NzktMTEuNzg5bC0xMS43ODUsMTEuNzg5Yy0yLjQ1NSwyLjQ1Ny02LjQzNiwyLjQ1Ny04Ljg4OSwwYy0yLjQ1NC0yLjQ1NS0yLjQ1NC02LjQzNCwwLTguODkxTDY2LjMyLDkzLjgzNkw2Ni4zMiw5My44MzZ6Ii8+PC9nPjwvc3ZnPg==);background-size:30px 30px}@media screen and (max-width:640px){.t449{position:relative;top:auto;-moz-transform:translate(0,0);-ms-transform:translate(0,0);-webkit-transform:translate(0,0);-o-transform:translate(0,0);transform:translate(0,0)}.t449.t449__beforeready{-moz-transform:translate(0,0)!important;-ms-transform:translate(0,0)!important;-webkit-transform:translate(0,0)!important;-o-transform:translate(0,0)!important;transform:translate(0,0)!important}.t449 .ya-share2__list_direction_vertical>.ya-share2__item{display:inline-block}.t449 .ya-share2__link{border-bottom:0!important}.t449__wrapper{text-align:center;padding:30px 0}}.t493__flex-wrapper{display:flex}.t493 .t-section__topwrapper{margin-bottom:105px}.t493 .t-section__title{margin-bottom:40px}.t493 .t-section__descr{max-width:560px}.t493 .t-section__bottomwrapper{margin-top:105px}.t493__img{display:block;width:100%}.t493__box-img-mobile{display:none}.t493__tablewrapper{display:table;height:100%;width:100%}.t493__textwrapper{padding-left:30px}.t493__imgwrapper{width:65px}.t493__bgimg{width:65px;height:65px;max-width:100%;background-size:cover;background-repeat:no-repeat;background-position:center}.t493__iconimg{width:100%;max-width:100%;height:auto}.t493__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}.t493__heading{padding-bottom:15px}.t493__item_padding-top{padding-top:50px}@media screen and (max-width:960px){.t493__flex-wrapper{display:block}.t493__box-img-mobile{display:block;height:auto;margin-bottom:75px}.t493__box-img{display:none}.t493__img{max-width:100%;height:auto}.t493__imgwrapper{max-width:50px!important}.t493__bgimg{max-width:50px!important;max-height:50px!important}.t493__box-text{height:auto}.t493 .t-section__bottomwrapper{margin-top:45px}.t493 .t-section__topwrapper{margin-bottom:45px}.t493 .t-section__title{margin-bottom:20px}}.t498 .t-section__topwrapper{margin-bottom:105px}.t498 .t-section__title{margin-bottom:40px}.t498 .t-section__descr{max-width:560px}.t498 .t-section__bottomwrapper{margin-top:105px}.t498__col{vertical-align:top;position:relative;height:auto}.t498__col-wrapper{text-align:center;box-sizing:border-box;padding:0 25px}.t498__line{width:1px;background:#eee;position:absolute;top:0;bottom:0;left:-20px;-moz-transform:translate(-50%,0);-ms-transform:translate(-50%,0);-webkit-transform:translate(-50%,0);-o-transform:translate(-50%,0);transform:translate(-50%,0)}.t498__bgimg{width:100px;height:100px;max-width:100%;background-size:cover;background-repeat:no-repeat;background-position:center;margin-bottom:30px}.t498__img{margin-bottom:30px;width:100px;height:auto;max-width:100%}.t498__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}.t498__title{padding-bottom:20px}.t498__uptitle{padding-bottom:15px}@media screen and (max-width:1200px){.t498__line{left:-10px}}@media screen and (max-width:960px){.t498 .t-section__bottomwrapper{margin-top:45px}.t498 .t-section__topwrapper{margin-bottom:45px}.t498 .t-section__title{margin-bottom:20px}.t498__col{padding:0 5% 0 5%;width:100%;height:auto!important;display:block}.t498__col-wrapper{padding:45px 0 45px 0}.t498__col-wrapper_fisrt{padding-top:0}.t498__line{-moz-transform:translate(0,0);-ms-transform:translate(0,0);-webkit-transform:translate(0,0);-o-transform:translate(0,0);transform:translate(0,0);width:90%!important;margin:0 5% 0 5%;left:0;height:1px}.t498__title,.t498__uptitle{padding-bottom:10px}}.t500 .t-section__topwrapper{margin-bottom:105px}.t500 .t-section__title{margin-bottom:40px}.t500 .t-section__descr{max-width:560px}.t500 .t-section__bottomwrapper{margin-top:105px}.t500__item_padding-top{padding-top:45px}.t500__img{display:block;width:100%;box-sizing:border-box;padding:0 30px 0 30px}.t500__imgwrapper{width:45px}.t500__bgimg{width:45px;height:45px;max-width:100%;background-size:cover;background-repeat:no-repeat;background-position:center}.t500__iconimg{width:100%;max-width:100%;height:auto}.t500__img_circle{border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%}.t500__cell-left{padding-left:20px}.t500__cell-left .t500__textwrapper{padding-right:20px;text-align:right}.t500__cell-left .t500__item{float:right}.t500__cell-right{padding-right:20px}.t500__cell-right .t500__textwrapper{padding-left:20px;text-align:left}.t500__cell-right .t500__item{float:left}.t500 .t-name{padding-bottom:10px}.t500__iconwrapper_mobile{display:none}.t500__justfeatures{padding:0 50px 0 50px;vertical-align:top}@media screen and (max-width:960px){.t500 .t-container>.t-cell{padding:0 20px 0 20px;box-sizing:border-box;width:100%;display:block}.t500__cell-left{margin-bottom:45px}.t500__cell-right{margin-top:45px}.t500__cell-left .t500__textwrapper{padding-right:0;padding-left:20px;text-align:left}.t500__img{max-width:90%;margin:0 auto}.t500__imgwrapper{max-width:50px!important}.t500__bgimg{max-width:50px!important;max-height:50px!important}.t500__iconwrapper{display:none}.t500__iconwrapper_mobile{display:table-cell}.t500__item{float:none!important}.t500 .t-section__bottomwrapper{margin-top:45px}.t500 .t-section__topwrapper{margin-bottom:45px}.t500 .t-section__title{margin-bottom:20px}}.t513 .t-section__topwrapper{margin-bottom:90px}.t513 .t-section__title{margin-bottom:20px}.t513 .t-section__descr{max-width:560px}.t513 .t-section__bottomwrapper{margin-top:105px}.t513__row:after{content:'';display:block;height:0;clear:both}.t513__rightcol,.t513__leftcol{margin-top:45px;margin-bottom:45px}.t513__line{height:1px;background:#000;opacity:.1}.t513__bottommargin{margin-bottom:35px}.t513__personwrapper{display:table}.t513__persontextwrapper,.t513__personimgwrapper{display:table-cell;vertical-align:middle}.t513__img{width:50px;height:50px;margin-right:20px;border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%;background-position:center center;background-repeat:no-repeat;background-size:cover}@media screen and (max-width:960px){.t513 .t-section__bottomwrapper{margin-top:90px}.t513 .t-section__topwrapper{margin-bottom:75px}.t513 .t-section__title{margin-bottom:20px}.t513__rightcol{margin-top:0}.t513__leftcol{margin-bottom:20px}.t513__bottommargin{margin-bottom:20px}}.t529 .t-section__topwrapper{margin-bottom:90px}.t529 .t-section__title{margin-bottom:40px}.t529 .t-section__descr{max-width:560px}.t529 .t-section__bottomwrapper{margin-top:85px}.t529__separator{margin-bottom:60px}.t529__bubble{padding:35px;border-radius:10px;background-color:#fff}.t529__bubble-tail{width:0;height:0;margin-left:35px;border:12px solid;border-color:#fff transparent transparent #fff}.t529__name-wrapper{margin:10px 0 0 0}.t529__descr{color:#666}.t529__bgimg{width:50px;height:50px;border-radius:50%;-moz-border-radius:50%;-webkit-border-radius:50%;margin-left:10px;margin-right:10px;background-position:center center;background-repeat:no-repeat;background-size:cover}@media screen and (max-width:960px){.t529 .t-section__bottomwrapper{margin-top:20px}.t529 .t-section__topwrapper{margin-bottom:40px}.t529 .t-section__title{margin-bottom:20px}.t529__separator{margin-bottom:40px}.t529__col{margin-bottom:40px}}@media screen and (max-width:640px){.t529__bubble{padding:20px}}.t532 .t-section__topwrapper{margin-bottom:105px}.t532 .t-section__title{margin-bottom:40px}.t532 .t-section__descr{max-width:560px}.t532 .t-section__bottomwrapper{margin-top:105px}.t532__table{display:table;width:100%;height:450px;vertical-align:middle;background-color:#000;position:relative;overflow:hidden}.t532__col{overflow:hidden}.t532__bg{background-position:center center;background-repeat:no-repeat;background-size:cover;position:absolute;top:0;right:0;left:0;bottom:0}.t532__cell_hover .t532__bg_animated{-moz-transform:scale(1.05);-ms-transform:scale(1.05);-webkit-transform:scale(1.05);-o-transform:scale(1.05);transform:scale(1.05)}.t532__overlay{position:absolute;top:0;right:0;bottom:0;left:0}.t532__show_hover .t532__overlay{opacity:0}.t532__cell_hover .t532__overlay{opacity:.8}.t532__show_hover .t532__cell_hover .t532__overlay{opacity:1}.t532__cell{display:table-cell;width:100%;height:100%}.t532__textwrapper{padding:20px 40px;position:relative}.t532__show_hover .t532__textwrapper{opacity:0}.t532__show_hover .t532__textwrapper.t532__textwrapper_animated{-moz-transform:translateY(20%);-ms-transform:translateY(20%);-webkit-transform:translateY(20%);-o-transform:translateY(20%);transform:translateY(20%)}.t532__show_hover .t532__cell_hover .t532__textwrapper{opacity:1}.t532__show_hover .t532__cell_hover .t532__textwrapper.t532__textwrapper_animated{-moz-transform:translateY(0);-ms-transform:translateY(0);-webkit-transform:translateY(0);-o-transform:translateY(0);transform:translateY(0)}.t532__textwrapper__content{margin:20px auto;position:relative}.t532__text,.t532__title{color:#000}.t532__title_small{font-size:28px;line-height:1.25}.t532__animation_fast{-webkit-transition:all ease-in-out .25s;-moz-transition:all ease-in-out .25s;-o-transition:all ease-in-out .25s;transition:all ease-in-out .25s}.t532__animation_slow{-webkit-transition:all ease-in-out .45s;-moz-transition:all ease-in-out .45s;-o-transition:all ease-in-out .45s;transition:all ease-in-out .45s}.t532__textwrapper__content{-webkit-transition:all ease-in-out .2s;-moz-transition:all ease-in-out .2s;-o-transition:all ease-in-out .2s;transition:all ease-in-out .2s}.t532__separator{margin-bottom:40px}.t532__bottommargin_sm{margin-bottom:4px}.t532__bottommargin_lg{margin-bottom:18px}@media screen and (max-width:1200px){.t532__separator{margin-bottom:20px}}@media screen and (max-width:960px){.t532 .t-section__bottomwrapper{margin-top:45px}.t532 .t-section__topwrapper{margin-bottom:45px}.t532 .t-section__title{margin-bottom:20px}.t532__separator{display:none}.t532__container{font-size:0}.t532__col-mobstyle{width:50%;display:inline-block;vertical-align:top}.t532__itemwrapper{margin:0 auto 40px auto}.t532__itemwrapper_3{max-width:300px}.t532__itemwrapper_1,.t532__itemwrapper_2{max-width:460px}.t532__itemwrapper_4{max-width:220px}}@media screen and (max-width:640px){.t532__col-mobstyle:nth-child(odd){padding-left:40px}.t532__col-mobstyle:nth-child(even){padding-right:40px}}@media screen and (max-width:480px){.t532__col-mobstyle{width:100%;display:block}.t532__col-mobstyle:nth-child(odd){padding-left:20px}.t532__col-mobstyle:nth-child(even){padding-right:20px}}.t554__general-wrapper{position:relative}.t554__card-wrapper{position:absolute;left:0;right:0;top:0;margin:auto;max-width:1160px;z-index:1}.t554__card{position:absolute;background:white;min-height:300px;padding:60px;box-sizing:border-box;width:100%;top:60px}.t554__title{margin-bottom:30px}.t554 .t-sociallinks{margin-top:30px}.t554 .t-sociallinks__item{display:inline-block;margin:4px 1px 0}.t554__prefix_1{left:100px}.t554__prefix_2{left:200px}.t554__prefix_3{left:300px}.t554__prefix_4{left:400px}.t554__prefix_5{left:500px}.t554__prefix_6{left:600px}.t554__prefix_7{left:700px}.t554__prefix_8{left:800px}.t554__prefix_9{left:900px}.t554__prefix_10{left:1000px}.t554__prefix_11{left:1100px}.t554__prefix_12{left:1200px}@media screen and (max-width:1200px){.t554__card-wrapper{max-width:940px}.t554__prefix_1{left:80px}.t554__prefix_2{left:160px}.t554__prefix_3{left:240px}.t554__prefix_4{left:320px}.t554__prefix_5{left:400px}.t554__prefix_6{left:480px}.t554__prefix_7{left:560px}.t554__prefix_8{left:640px}.t554__prefix_9{left:720px}.t554__prefix_10{left:800px}.t554__prefix_11{left:880px}.t554__prefix_12{left:960px}}@media screen and (max-width:960px){.t554__card-wrapper,.t554__card{position:initial}.t554__card-wrapper{max-width:640px}.t554__card{width:100%;margin:0;padding:45px 20px;min-height:auto}.t554_map{height:50vh!important}.t554_map .t-map{max-height:100%}}@media screen and (max-width:640px){.t554__card-wrapper{max-width:100%}}.t581{text-align:center}.t581__wrapper{padding-top:42px;padding-bottom:42px}.t581__title{color:#fff;margin-bottom:25px}.t581__descr{color:#fff}.t581__buttons{margin-top:70px}.t581__buttons-wrapper{display:table;position:relative}.t581__arrow-icon{width:45px;position:absolute;left:-30px;transform:translateX(-100%);fill:#fff;top:0;bottom:0;margin:auto}.t581__arrow-icon_mobile{display:none}.t581__arrow-icon_right{right:-30px;transform:scaleX(-1);transform-origin:right;left:auto}.t581__btn-size_lg{height:70px;font-size:22px;padding-left:70px;padding-right:70px}.t581__btn-size_xl{height:80px;font-size:26px;padding-left:80px;padding-right:80px}.t581__btn-size_xxl{height:100px;font-size:30px;padding-left:90px;padding-right:90px}.t581__marginleft20px{margin-left:20px}@media screen and (max-width:960px){.t581__buttons{margin-top:30px}.t581__arrow-icon{display:none}.t581__arrow-icon_mobile{display:block;width:20px;margin:0 auto 20px;fill:#fff}}@media screen and (max-width:640px){.t581__marginleft20px{margin-left:0}.t581__btn,.t581__buttons-wrapper{margin-bottom:10px;width:100%}.t581__btn-size_lg,.t581__btn-size_xl,.t581__btn-size_xxl{height:60px;font-size:18px;padding-left:40px;padding-right:40px}}.t589 .t-section__topwrapper{margin-bottom:105px}.t589 .t-section__title{margin-bottom:40px}.t589 .t-section__descr{max-width:560px}.t589 .t-section__bottomwrapper{margin-top:105px}.t589__col{margin-top:0;margin-bottom:0}.t589__img{max-width:100%;margin:0 auto;display:block}.t589__title{margin-bottom:90px}.t589__text{margin-top:20px;opacity:.7}.t589__buttons{margin-top:60px}.t589__btn{margin-bottom:10px}.t589__marginright10px{margin-right:10px}@media screen and (max-width:960px){.t589 .t-section__bottomwrapper{margin-top:45px}.t589 .t-section__topwrapper{margin-bottom:60px}.t589 .t-section__title{margin-bottom:20px}.t589__col:first-child{margin-bottom:45px}.t589__textwrapper{text-align:center}.t589__buttons{margin-top:45px}.t589__title{margin-bottom:60px}}@media screen and (max-width:640px){.t589__marginright10px{margin-left:0}.t589__btn{width:100%}}
</style>


<script type="text/javascript">
function t142_checkSize(recid){var el=$("#rec"+recid).find(".t142__submit");if(el.length){var btnheight=el.height()+5;var textheight=el[0].scrollHeight;if(btnheight<textheight){var btntext=el.text();el.addClass("t142__submit-overflowed");el.html("<span class=\"t142__text\">"+btntext+"</span>")}}}
window.t256showvideo=function(recid){$(document).ready(function(){var el=$('#coverCarry'+recid);var videourl='';var youtubeid=$("#rec"+recid+" .t256__video-container").attr('data-content-popup-video-url-youtube');if(youtubeid>''){videourl='https://www.youtube.com/embed/'+youtubeid}
$("body").addClass("t256__overflow");$("#rec"+recid+" .t256__cover").addClass("t256__hidden");$("#rec"+recid+" .t256__video-container").removeClass("t256__hidden");$("#rec"+recid+" .t256__video-carier").html("<iframe id=\"youtubeiframe"+recid+"\" class=\"t256__iframe\" width=\"100%\" height=\"540\" src=\""+videourl+"?autoplay=1\" frameborder=\"0\" allowfullscreen></iframe><a class=\"t256__close-link\" href=\"javascript:t256hidevideo('"+recid+"');\"><div class=\"t256__close\"></div></a>")})}
window.t256hidevideo=function(recid){$(document).ready(function(){$("body").removeClass("t256__overflow");$("#rec"+recid+" .t256__cover").removeClass("t256__hidden");$("#rec"+recid+" .t256__video-container").addClass("t256__hidden");$("#rec"+recid+" .t256__video-carier").html("<div class=\"t256__video-bg2\"></div>")})}
function t262_appendGoogleMap(recid,key){var grecid=recid;if(typeof google==='object'&&typeof google.maps==='object'){t262_handleGoogleApiReady(grecid)}else{if(window.googleapiiscalled!==!0){var runfunc='window.t262_handleGoogleApiReady_'+grecid+' = function () { t262_handleGoogleApiReady("'+grecid+'") }';eval(runfunc);var script=document.createElement("script");script.type="text/javascript";script.src="//maps.google.com/maps/api/js?key="+jQuery.trim(key)+"&callback=t262_handleGoogleApiReady_"+grecid;document.body.appendChild(script);window.googleapiiscalled=!0}else{setTimeout(function(){t262_appendGoogleMap(grecid,key)},200)}}}
function t262_setMapHeight(recid){var el=$('#rec'+recid);var map=el.find('.t262__map');var textwrapper=el.find('.t262__col_text').height();map.css('height',textwrapper)}
function t262_handleGoogleApiReady(recid){$('#rec'+recid).find('.t262__map').each(function(index,Element){var el=$(Element);var arMarkers=window['arMapMarkers'+recid];window.isDragMap=$isMobile?!1:!0;var myLatLng=arMarkers.length>0?new google.maps.LatLng(parseFloat(arMarkers[0].lat),parseFloat(arMarkers[0].lng)):!1;var myOptions={zoom:parseInt(el.attr('data-map-zoom')),center:myLatLng,scrollwheel:!1,draggable:window.isDragMap,zoomControl:!0};var map=new google.maps.Map(Element,myOptions);var i,mrk,marker,markers=[],infowindow;var bounds=new google.maps.LatLngBounds();for(i in arMarkers){mrk=arMarkers[i];myLatLng=new google.maps.LatLng(parseFloat(mrk.lat),parseFloat(mrk.lng));marker=new google.maps.Marker({position:myLatLng,map:map,title:mrk.title});bounds.extend(myLatLng);if(mrk.descr>''){attachInfoMessage(marker,mrk.descr)}else{attachInfoMessage(marker,mrk.title)}
markers[markers.length]=marker;infowindow='';marker=''}
function attachInfoMessage(marker,descr){var infowindow=new google.maps.InfoWindow({content:$("<textarea/>").html(descr).text()});marker.addListener('click',function(){infowindow.open(marker.get('map'),marker)})}
if(arMarkers.length>1){map.fitBounds(bounds);if(map.getZoom()>parseInt(el.attr('data-map-zoom'))){map.setZoom(parseInt(el.attr('data-map-zoom')))}}
google.maps.event.addDomListener(window,"resize",function(){var center=map.getCenter();google.maps.event.trigger(map,"resize");map.setCenter(center)});if($isMobile){google.maps.event.addDomListener(window,"dblclick",function(){if(window.isDragMap){window.isDragMap=!1}else{window.isDragMap=!0}
map.setOptions({draggable:window.isDragMap})})}})}
function t262_appendYandexMap(recid,key){var yarecid=recid;if(typeof ymaps==='object'&&typeof ymaps.Map==='function'){t262_handleYandexApiReady(recid)}else{if(window.yandexmapsapiiscalled!==!0){var runfunc='window.t262_handleYandexApiReady_'+yarecid+' = function () { return t262_handleYandexApiReady("'+yarecid+'") }';eval(runfunc);var script=document.createElement("script");script.type="text/javascript";script.src="https://api-maps.yandex.ru/2.1/?lang=ru-RU&coordorder=latlong&onload=t262_handleYandexApiReady_"+yarecid;if(key>''){script.src=script.src+'&apikey='+key}
document.body.appendChild(script);window.yandexmapsapiiscalled=!0}else{setTimeout(function(){t262_appendYandexMap(yarecid,key)},200)}}}
function t262_handleYandexApiReady(recid){$('#rec'+recid).find('.t262__map').each(function(index,Element){var el=$(Element);var arMarkers=window['arMapMarkers'+recid];window.isDragMap=$isMobile?!1:!0;if(el.attr('data-map-style')!=''){var mapstyle=eval(el.attr('data-map-style'))}else{var mapstyle='[]'}
var myLatlng=arMarkers.length>0?[parseFloat(arMarkers[0].lat),parseFloat(arMarkers[0].lng)]:!1;var myStates={zoom:parseInt(el.attr('data-map-zoom')),center:myLatlng,scrollZoom:!1,controls:['typeSelector','zoomControl'],drag:window.isDragMap};var map=new ymaps.Map(Element,myStates),i,mrk,marker;var myGroup=new ymaps.GeoObjectCollection({});map.behaviors.disable('scrollZoom');for(i in arMarkers){mrk=arMarkers[i];myLatlng=[parseFloat(mrk.lat),parseFloat(mrk.lng)];myGroup.add(new ymaps.Placemark(myLatlng,{hintContent:mrk.title,balloonContent:mrk.descr>''?$("<textarea/>").html(mrk.descr).text():mrk.title}))}
map.geoObjects.add(myGroup);if(arMarkers.length>1){map.setBounds(myGroup.getBounds(),{checkZoomRange:!0})}
$(window).resize(function(){map.container.fitToViewport()});if($isMobile){$(window).dblclick(function(){if(window.isDragMap){window.isDragMap=!1}else{window.isDragMap=!0}
if(window.isDragMap){map.behaviors.enable('drag')}else{map.behaviors.disable('drag')}})}})}
function t330_showPopup(recid){var el=$('#rec'+recid),popup=el.find('.t-popup');popup.css('display','block');setTimeout(function(){popup.find('.t-popup__container').addClass('t-popup__container-animated');popup.addClass('t-popup_show')},50);$('body').addClass('t-body_popupshowed');el.find('.t-popup').click(function(e){if(e.target==this){t330_closePopup()}});el.find('.t-popup__close').click(function(e){t330_closePopup()});el.find('a[href*=#]').click(function(e){var url=$(this).attr('href');if(!url||url.substring(0,7)!='#price:'){t330_closePopup();if(!url||url.substring(0,7)=='#popup:'){setTimeout(function(){$('body').addClass('t-body_popupshowed')},300)}}});$(document).keydown(function(e){if(e.keyCode==27){t330_closePopup()}})}
function t330_closePopup(){$('body').removeClass('t-body_popupshowed');$('.t-popup').removeClass('t-popup_show');setTimeout(function(){$('.t-popup').not('.t-popup_show').css('display','none')},300)}
function t330_resizePopup(recid){var el=$("#rec"+recid),div=el.find(".t-popup__container").height(),win=$(window).height()-120,popup=el.find(".t-popup__container");if(div>win){popup.addClass('t-popup__container-static')}else{popup.removeClass('t-popup__container-static')}}
function t330_sendPopupEventToStatistics(popupname){var virtPage='/tilda/popup/';var virtTitle='Popup: ';if(popupname.substring(0,7)=='#popup:'){popupname=popupname.substring(7)}
virtPage+=popupname;virtTitle+=popupname;if(window.Tilda&&typeof Tilda.sendEventToStatistics=='function'){Tilda.sendEventToStatistics(virtPage,virtTitle,'',0)}else{if(ga){if(window.mainTracker!='tilda'){ga('send',{'hitType':'pageview','page':virtPage,'title':virtTitle})}}
if(window.mainMetrika>''&&window[window.mainMetrika]){window[window.mainMetrika].hit(virtPage,{title:virtTitle,referer:window.location.href})}}}
function t330_initPopup(recid){$('#rec'+recid).attr('data-animationappear','off');$('#rec'+recid).css('opacity','1');var el=$('#rec'+recid).find('.t-popup'),hook=el.attr('data-tooltip-hook'),analitics=el.attr('data-track-popup');if(hook!==''){var obj=$('a[href="'+hook+'"]');obj.click(function(e){t330_showPopup(recid);t330_resizePopup(recid);e.preventDefault();if(window.lazy=='y'){t_lazyload_update()}
if(analitics=='yes'){t330_sendPopupEventToStatistics(hook)}})}}
function t331_setHeight(recid){var el=$('#rec'+recid);var div=el.find(".t331__video-carier");var height=div.width()*0.5625;div.height(height);div.parent().height(height)}
function t331_initPopup(recid){$('#rec'+recid).attr('data-animationappear','off');$('#rec'+recid).css('opacity','1');var el=$('#rec'+recid).find('.t-popup'),hook=el.attr('data-tooltip-hook'),analitics=el.attr('data-track-popup');if(hook!==''){var obj=$('a[href="'+hook+'"]');obj.click(function(e){t331_showPopup(recid);t331_resizePopup(recid);e.preventDefault();if(analitics=='yes'){t331_sendPopupEventToStatistics(hook)}})}}
function t331_showPopup(recid){var el=$('#rec'+recid),popup=el.find('.t-popup');var youtubeid=el.find(".t331__youtube").attr('data-content-popup-video-url-youtube');var videourl='https://www.youtube.com/embed/'+youtubeid;el.find(".t331__video-carier").html("<iframe id=\"youtubeiframe"+recid+"\" class=\"t331__iframe\" width=\"100%\" height=\"100%\" src=\""+videourl+"?autoplay=1\" frameborder=\"0\" allowfullscreen></iframe>");popup.css('display','block');t331_setHeight(recid);setTimeout(function(){popup.find('.t-popup__container').addClass('t-popup__container-animated');popup.addClass('t-popup_show')},50);$('body').addClass('t-body_popupshowed');el.find('.t-popup').click(function(e){if(e.target==this){t331_popup_close(recid)}});el.find('.t-popup__close').click(function(e){t331_popup_close(recid)});$(document).keydown(function(e){if(e.keyCode==27){t331_popup_close(recid)}})}
function t331_popup_close(recid){$('body').removeClass('t-body_popupshowed');$('.t-popup').removeClass('t-popup_show');setTimeout(function(){$("#rec"+recid+" .t331__video-carier").html("");$('.t-popup').not('.t-popup_show').css('display','none')},300)}
function t331_resizePopup(recid){var el=$("#rec"+recid),div=el.find(".t-popup__container").height(),win=$(window).height(),popup=el.find(".t-popup__container");if(div>win){popup.addClass('t-popup__container-static')}else{popup.removeClass('t-popup__container-static')}}
function t331_sendPopupEventToStatistics(popupname){var virtPage='/tilda/popup/';var virtTitle='Popup: ';if(popupname.substring(0,7)=='#popup:'){popupname=popupname.substring(7)}
virtPage+=popupname;virtTitle+=popupname;if(ga){if(window.mainTracker!='tilda'){ga('send',{'hitType':'pageview','page':virtPage,'title':virtTitle})}}
if(window.mainMetrika>''&&window[window.mainMetrika]){window[window.mainMetrika].hit(virtPage,{title:virtTitle,referer:window.location.href})}}
var t334={};t334.initeffect=function(recid){$('#rec'+recid).find(".t334__cell").hover(function(){var sizer=$(this).find(".t334__button-container").height();$(this).find(".t334__textwrapper__content").css({'padding-bottom':(sizer+'px')});$(this).find(".t334__button-container").addClass("t334__button-container_show")},function(){$(this).find(".t334__textwrapper__content").css("padding-bottom","0");$(this).find(".t334__button-container").removeClass("t334__button-container_show")})};var t335={};t335.initeffect=function(recid){$('#rec'+recid).find(".t335__cell").hover(function(){var sizer=$(this).find(".t335__button-container").height();$(this).find(".t335__textwrapper__content").css({'padding-bottom':(sizer+'px')});$(this).find(".t335__button-container").addClass("t335__button-container_show")},function(){$(this).find(".t335__textwrapper__content").css("padding-bottom","0");$(this).find(".t335__button-container").removeClass("t335__button-container_show")})};function t358_setHeight(recid){var el=$('#rec'+recid);var div=el.find(".t358__video-carier");var height=div.width()*0.5625;div.height(height);div.parent().height(height)}
function t358_initPopup(recid){$('#rec'+recid).attr('data-animationappear','off');$('#rec'+recid).css('opacity','1');var el=$('#rec'+recid).find('.t-popup'),hook=el.attr('data-tooltip-hook'),analitics=el.attr('data-track-popup');if(hook!==''){var obj=$('a[href="'+hook+'"]');obj.click(function(e){t358_showPopup(recid);t358_resizePopup(recid);e.preventDefault();if(analitics=='yes'){t358_sendPopupEventToStatistics(hook)}})}}
function t358_showPopup(recid){var el=$('#rec'+recid),popup=el.find('.t-popup');var vimeoid=$("#rec"+recid+" .t358__vimeo").attr('data-content-popup-video-url-vimeo');var videourl='//player.vimeo.com/video/'+vimeoid;$("#rec"+recid+" .t358__video-carier").html("<iframe id=\"vimeoiframe"+recid+"\" class=\"t358__iframe\" width=\"100%\" height=\"100%\" src=\""+videourl+"?title=0&byline=0&portrait=0&badge=0&color=ffffff&autoplay=1\" frameborder=\"0\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>");popup.css('display','block');t358_setHeight(recid);setTimeout(function(){popup.find('.t-popup__container').addClass('t-popup__container-animated');popup.addClass('t-popup_show')},50);$('body').addClass('t-body_popupshowed');el.find('.t-popup').click(function(e){if(e.target==this){t358_popup_close(recid)}});el.find('.t-popup__close').click(function(e){t358_popup_close(recid)});$(document).keydown(function(e){if(e.keyCode==27){t358_popup_close(recid)}})}
function t358_popup_close(recid){$('body').removeClass('t-body_popupshowed');$('.t-popup').removeClass('t-popup_show');setTimeout(function(){$("#rec"+recid+" .t358__video-carier").html("");$('.t-popup').not('.t-popup_show').css('display','none')},300)}
function t358_resizePopup(recid){var el=$("#rec"+recid),div=el.find(".t-popup__container").height(),win=$(window).height(),popup=el.find(".t-popup__container");if(div>win){popup.addClass('t-popup__container-static')}else{popup.removeClass('t-popup__container-static')}}
function t358_sendPopupEventToStatistics(popupname){var virtPage='/tilda/popup/';var virtTitle='Popup: ';if(popupname.substring(0,7)=='#popup:'){popupname=popupname.substring(7)}
virtPage+=popupname;virtTitle+=popupname;if(ga){if(window.mainTracker!='tilda'){ga('send',{'hitType':'pageview','page':virtPage,'title':virtTitle})}}
if(window.mainMetrika>''&&window[window.mainMetrika]){window[window.mainMetrika].hit(virtPage,{title:virtTitle,referer:window.location.href})}}
function t410_init(recid){var el=$('#rec'+recid);var firstimgurl=el.find(".t410__wrapper").attr("data-juxtapose-imgurl-first");var firstimgdescr=el.find(".t410__wrapper").attr("data-juxtapose-imgdescr-first");var secondimgurl=el.find(".t410__wrapper").attr("data-juxtapose-imgurl-second");var secondimgdescr=el.find(".t410__wrapper").attr("data-juxtapose-imgdescr-second");new juxtapose.JXSlider('#t410-juxtapose__'+recid+'',[{src:firstimgurl,label:firstimgdescr},{src:secondimgurl,label:secondimgdescr}],{animate:!1,showLabels:!0,showCredits:!1,startingPosition:'50%',makeResponsive:!0})}
function t410_update(recid){var el=$('#rec'+recid)}
function t412_unifyHeights(recid){var el=$("#rec"+recid);el.find('.t412__descr').css('height',"auto");$('#rec'+recid+' .t412 .t-container').each(function(){var highestBox2=0;$('.t412__descr',this).each(function(){if($(this).height()>highestBox2)highestBox2=$(this).height()});if($(window).width()>=960&&$(this).is(':visible')){$('.t412__descr',this).css('height',highestBox2)}else{$('.t412__descr',this).css('height',"auto")}});el.find('.t412__title').css('height',"auto");$('#rec'+recid+' .t412 .t-container').each(function(){var highestBox3=0;$('.t412__title',this).each(function(){if($(this).height()>highestBox3)highestBox3=$(this).height()});if($(window).width()>=960&&$(this).is(':visible')){$('.t412__title',this).css('height',highestBox3)}else{$('.t412__title',this).css('height',"auto")}});el.find('.t412__wrapper').css('height',"auto");$('#rec'+recid+' .t412 .t-container').each(function(){var highestBox=0;$('.t412__wrapper',this).each(function(){if($(this).height()>highestBox)highestBox=$(this).height()});if($(window).width()>=960&&$(this).is(':visible')){$('.t412__wrapper',this).css('height',highestBox)}else{$('.t412__wrapper',this).css('height',"auto")}})}
t427_alignMiddle=function(recid){if($(window).width()>960){var t427__img=$('#rec'+recid+' .t427__img');var t427__arrow=$('#rec'+recid+' .t427__arrow');t427__arrow.css('top',(t427__img.height()-t427__arrow.height())/2)}};function t428_unifyHeights(recid){$('#rec'+recid+' .t428 .t-container').each(function(){var t428__highestBox=0;$('.t428__col',this).each(function(){var t428__curcol=$(this);var t428__curcolchild=t428__curcol.find('.t428__col-wrapper');if(t428__curcol.height()<t428__curcolchild.height())t428__curcol.height(t428__curcolchild.height());if(t428__curcol.height()>t428__highestBox)t428__highestBox=t428__curcol.height()});if($(window).width()>=960){$('.t428__col',this).css('height',t428__highestBox)}else{$('.t428__col',this).css('height',"auto")}})};function t449_appearMenu(recid){var window_width=$(window).width();if(window_width>980){$(".t449").each(function(){var el=$(this);var appearoffset=el.attr("data-appearoffset");var hideoffset=el.attr("data-hideoffset");if(appearoffset!=""){if(appearoffset.indexOf('vh')>-1){appearoffset=Math.floor((window.innerHeight*(parseInt(appearoffset)/100)))}
appearoffset=parseInt(appearoffset,10);if($(window).scrollTop()>=appearoffset){if(el.hasClass('t449__beforeready')){el.finish();el.removeClass("t449__beforeready")}}else{el.stop();el.addClass("t449__beforeready")}}
if(hideoffset!=""){if(hideoffset.indexOf('vh')>-1){hideoffset=Math.floor((window.innerHeight*(parseInt(hideoffset)/100)))}
hideoffset=parseInt(hideoffset,10);if($(window).scrollTop()+$(window).height()>=$(document).height()-hideoffset){if(!el.hasClass('t449__beforeready')){el.finish();el.addClass("t449__beforeready")}}else{if(appearoffset!=""){if($(window).scrollTop()>=appearoffset){el.stop();el.removeClass("t449__beforeready")}}else{el.stop();el.removeClass("t449__beforeready")}}}})}}
function t498_unifyHeights(recid){$('#rec'+recid+' .t498 .t-container').each(function(){var t498__highestBox=0;$('.t498__col',this).each(function(){var t498__curcol=$(this);var t498__curcolchild=t498__curcol.find('.t498__col-wrapper');if(t498__curcol.height()<t498__curcolchild.height())t498__curcol.height(t498__curcolchild.height());if(t498__curcol.height()>t498__highestBox)t498__highestBox=t498__curcol.height()});if($(window).width()>=960){$('.t498__col',this).css('height',t498__highestBox)}else{$('.t498__col',this).css('height',"auto")}})};function t532__emulateMobileHover(recid){var el=$('#rec'+recid),cell=el.find('.t532__cell');cell.hover(function(){$(this).addClass("t532__cell_hover")},function(){$(this).removeClass("t532__cell_hover")})}
function t532_setHeight(recid){var t532__el=$("#rec"+recid),t532__image=t532__el.find(".t532__bg:first"),t532__wrapper=t532__el.find(".t532__table:first"),t532__width=t532__image.attr("data-image-width"),t532__height=t532__image.attr("data-image-height"),t532__ratio=t532__height/t532__width;$("#rec"+recid+" .t532__table").css("height",t532__wrapper.innerWidth()*t532__ratio)}
</script>
