# tieba_clear_fans
批量清理贴吧垃圾粉丝js

打开贴吧粉丝页面http://tieba.baidu.com/i/i/fans

//在浏览器控制台运行（ctrl+shift+i）

//运行一次清理一页
```
let clearSuccess = 0;
$('.btn_follow').each(function(){
  $.post('/i/commit', {'cmd':'add_black_list','portrait':$(this).attr('portrait'),'tbs':PageData.tbs,'ie':'utf-8'}, function(){
    clearSuccess += 1
    if (clearSuccess == $('.btn_follow').length){
      window.location.reload();
    }
  })
})

```
