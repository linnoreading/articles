> 文件被意外迁出，无法签入，用过多种方法，都无法删除或签入迁出，一直提示文件被用户删除。使用powershell强制删除文件。
https://blog.csdn.net/noreading/article/details/106197884
```ps
$url=""
$list=""
$id=""
$site=get-spsite $url
$web=$site.rootweb
$list=$web.getlistfromurl($list)
$item=$list.getitembyid($id)
#$item.delete()#无法删除
$item.file.delete()
#$item.delete()
```