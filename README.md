# tieba_clear_fans
批量清理贴吧垃圾粉丝js

打开贴吧粉丝页面http://tieba.baidu.com/i/i/fans

//在浏览器控制台运行
```
$('.btn_follow').each(function(){
  $.post('/i/commit', {'cmd':'add_black_list','portrait':$(this).attr('portrait'),'tbs':PageData.tbs,'ie':'utf-8'}, function(){
    window.location.reload();
  })
})
```
