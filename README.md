# 使用说明
1. 将文件夹放入到你的项目中,框架文件夹覆盖
2. 参照admin.shop.com/Admin/Controller/EditorController.class.php文件,拷贝放置到你的项目中
3. 视图模板中你仍旧需要自行导入Ueditor所需要的js文件,还有要做的初始化仍旧要做,比如像我这样:

>     <js href='__UE__/ueditor.config.js'/>
>     <js href='__UE__/ueditor.all.min.js'/>
>     <js href='__UE__/lang/zh-cn/zh-cn.js'/>
>     <script type="text/javascript">
>           var ue = UE.getEditor('editor',{serverUrl: '{:U('Editor/ueditor')}'});
>     </script>

目前支持:
1. ueditor的单文件上传(支持本地和七牛)
2. ueditor的多文件上传(支持本地和七牛)
3. 在线图片列表功能(支持七牛)
4. 图片上传后得到的是绝对路径,如果是本地上传,会自动拼接当前域名前缀,可以外链.