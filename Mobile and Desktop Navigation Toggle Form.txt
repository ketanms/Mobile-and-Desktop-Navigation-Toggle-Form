Header.php

<script type="text/javascript">
        jQuery(document).ready( function () {
            SideNavi.init({
                container : '#sideNavi',
                item : '.side-navi-item',
                data : '.side-navi-data',
                tab : '.side-navi-tab',
                active : '.active',
                close: '.close-btn'
            });
        });
</script>


<?php if(wp_is_mobile()) {?>
<div id="sideNavi">
              <div class="side-navi-item item1"><div class="sendquerycolor">Contact Us</div></div>
              
              <div class="side-navi-data">
                <div class="side-navi-tab">
                    <div class="close-btn"><i class="fa fa-times-circle-o close-icn" aria-hidden="true"></i></div>
                    <div><?php echo do_shortcode('[contact-form-7 id="19251" title="Newsletter sign up"]'); ?></div>
                </div>
                
              </div>
</div>
<?php } ?>


Style.css
----------------

#sideNavi{
    display:none; 
}

#sideNavi, .side-navi-item, .side-navi-data {
    margin: 0;
    padding: 0;
}
#sideNavi {
    position: fixed;
    right: 50px;
    top: 25%;
    z-index: 999;
}
.side-navi-item {
    background-color: #ff8601;
    border-radius: 5px 5px 0 0;
    color: #fff;
    cursor: pointer;
    display: inline-block;
    font-size: 14px;
    font-weight: 600;
    height: 50px;
    position: absolute;
    transform: rotate(-90deg);
    transform-origin: left top 0;
    width: 100px;
    border: 1px solid #3d828f;
    border-bottom: none;
}
.side-navi-item.item1 {
    left: 20px;
    top: 165px;
}
.sendquerycolor a {
    color: #fff;
}
.side-navi-item.active {
    background-color: #ff8601;
    color: #fff;
    left: 20px;
}
.side-navi-item > div {
    padding-top: 6px;
    text-align: center;
}
.side-navi-data {
    background-color: #e5e5e5;
    height: 350px;
    left: 50px;
    position: absolute;
    top: -90px;
    width: 300px;
}
.side-navi-tab {
    display: none;
}
.side-navi-tab.active {
    display: inline-block;
}
.side-navi-tab > div {
    padding: 10px;
}
.side-navi-data .close-btn i {
    cursor: pointer;
    float: right;
    font-size: 30px;
    margin: 5px 15px 0 0;
}
#sideNavi input.form-control,#sideNavi textarea.form-control {
    margin-bottom: 0px;
    width: 100%;
}
#sideNavi form{
    margin: 18px 5px 0 5px;
}
#sideNavi .newsletter-button {
    background-color: #ff8601;
    border: medium none;
    color: #fff;
    display: block;
    font-size: 16px;
    font-weight: 600;
    margin: 0 auto 0;
    padding: 5px 0;
    text-align: center;
    width: 40%;
    border-radius: 0;
    float: left;
}
#sideNavi div.wpcf7-validation-errors {
    border: 2px solid #f7e700;
    background: #e5e5e5;
    margin-top: 14px;
    font-size: 10px;
}
#sideNavi .wpcf7-not-valid {
    border: 1px solid red;
}
#sideNavi span.wpcf7-not-valid-tip {
    display: none;
}
#sideNavi textarea.form-control {
    height: 35px;
}
#sideNavi div.wpcf7-response-output {
    margin: 14px 0;
    padding: 5px 5px;
    font-size: 11px;
} 






----------------------------------------------------------------------------------------------
Desktop:

Footer.php

<div class="footer-form-wrapper">
	<div class="footer-header">Contact Us</div>
	<div class="footer-content"><?php echo do_shortcode('[contact-form-7 id="19251" title="Newsletter sign up"]'); ?></div>
	<div class="footer-close" style="display: none;"></div>
</div>

<script>
jQuery(document).ready(function($) {
$('.footer-header').click(function() {
        $('.footer-form-wrapper').toggleClass('active');
        $('.footer-close').toggleClass('active');
    });
    $('.footer-close').click(function() {
        $('.footer-form-wrapper').toggleClass('active');
        $('.footer-close').toggleClass('active');
    });
    });
 </script>   


Style.css
-------------------------------------------------
 .footer-header {
    background: #ff8601;
    border-top-left-radius: 5px;
    border-top-right-radius: 5px;
    color: #ffffff;
    cursor: pointer;
    display: block;
    font-size: 18px;
    font-weight: bold;
    margin-top: -10px;
    padding: 10px 5px;
    text-align: center;
    width: 100%;
    border: 2px solid #3d828f;
    border-bottom: none;
    box-shadow: 0 0 7px #000;
}
.footer-content {
    height: 0;
    overflow: hidden;
    padding: 0;
    transition: height 2s ease 0s;
}
.footer-form-wrapper {
    background: #3d828f none repeat scroll 0 0;
    bottom: 0;
    position: fixed;
    right: 205px;
    width: 250px;
    z-index: 9999;
}
.footer-content .wpcf7-form > p {
    text-align: center;
}
.footer-content .wpcf7-captchac {
    float: left;
}
.footer-content .btn-primary {
    background-color: #dadada;
    border-color: #dadada;
    color: #24828d;
    font-weight: bold;
}
.footer-form-wrapper.active .footer-content {
    height: auto;
    padding: 20px;
    transition: height 1s ease 0s;
}
.footer-close {
    color: #ffffff;
    cursor: pointer;
    font-weight: bolder;
    padding: 5px 10px;
    position: absolute;
    right: 10px;
    top: 0;
}
.footer-form-wrapper.active .footer-close {
    background: rgba(0, 0, 0, 0) url("images/sprit-image.png") no-repeat scroll 1px 4px;
    display: block !important;
    height: 20px;
    width: 26px;
}

.footer-content form input.form-control {
    margin-bottom: 15px;
    width: 100%;
}