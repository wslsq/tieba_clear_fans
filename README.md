# tieba_clear_fans
批量清理贴吧粉丝js

//在浏览器命令行允许
$('.btn_follow').each(function(){
  $.post('/i/commit', {'cmd':'add_black_list','portrait':$(this).attr('portrait'),'tbs':PageData.tbs,'ie':'utf-8'})
})
