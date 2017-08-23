
<!DOCTYPE HTML>
<html>

<head>
  <meta charset="utf-8" />
  <meta name="author" content="http://www.softwhy.com/" />
  <title>点击弹出窗口效果-蚂蚁部落</title>
  <style type="text/css">
    body,
    h2 {
      margin: 0;
      padding: 0;
    }
/*遮罩层*/
    #faqbg {
      background-color: #666666;
      position: absolute;
      z-index: 99;
      left: 0;
      top: 0;
      display: none;
      width: 100%;
      height: 1000px;
      opacity: 0.5;
      filter: alpha(opacity=50);
      -moz-opacity: 0.5;
    }
/*被弹出的窗口*/
    #faqdiv {
      position: absolute;
      width: 400px;
      left: 50%;
      top: 50%;
      margin-left: -200px;
      height: auto;
      z-index: 100;
      background-color: #fff;
      border: 1px #8FA4F5 solid;
      padding: 1px;
    }

    #faqdiv h2 {
      height: 25px;
      font-size: 14px;
      background-color: #8FA4F5;
      position: relative;
      padding-left: 10px;
      line-height: 25px;
    }

    #faqdiv h2 a {
      position: absolute;
      right: 5px;
      font-size: 12px;
      color: #FF0000
    }
  </style>
  <script type="text/javascript" src="http://www.softwhy.com/mytest/jQuery/jquery-1.8.3.js"></script>
  <script type="text/javascript">
    $(function() {
      $(".but").click(function() {
        $("#faqbg").css({
          display: "block",
          height: $(document).height()
        });
        $("#faqdiv").css("top", "100px");
        $("#faqdiv").css("display", "block");
      });
      $(".close").click(function() {
        $("#faqbg").css("display", "none");
        $("#faqdiv").css("display", "none");
      })
    })
  </script>
</head>

<body>
  <div id="faqbg"></div>
  <div id="faqdiv" style="display:none">
    <h2>信息窗口<a href="#" class="close">关闭</a></h2>
    <div class="form">这里是提示信息！！</div>
  </div>
  <p align="center">
    <input value="点击弹出窗口" class="but" type="button" />
  </p>
</body>

</html>
