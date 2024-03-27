# Clash_Meta_Modified
实现Clash_Meta主页面在多任务列表隐藏，方便放在后台保活


在没有root上的安卓手加上想要实现代理常驻往往需要“加锁”，但是在清理后台的时候往往会在多任务界面不小心把代理工具给划掉，通过修改apk文件可以实现应用不在多任务界面显示



实现方法：在AndroidManifest.xml文件中“com.github.kr238.clash.MainActivity”下将android:launchMode="1"改为"android:launchMode=singleInstance"，并添加"android:excludeFromRecents="true"




使用方法：因为只有软件主页面设置了隐藏，所以要先切换到代理界面，然后进入多任务界面，将Clash_Meta上锁，然后再返回软件主界面，此时直接退回桌面，再打开多任务界面，便不会显示Clash_Meta，即使清后台也不会清掉（简而言之，只有在软件主页面时直接退回到桌面在多任务栏里才会隐藏，再此之前要先上锁）



演示效果：

https://github.com/Capitariat/Clash_Meta_Modified/assets/145332176/eb5bd0db-976e-4d15-af83-6b332f229b5c


如有侵权，联系删除

