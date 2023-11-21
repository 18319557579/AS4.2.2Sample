# 要改这么几个地方
1.项目最外层的实际文件名，例如TargetGather
2.将.git目录给删掉
3.settings.gradle中将项目名改为: TargetGather
4.string中app的名称修改为：TargetGather
5.app/build.gradle中的applicationId改为: com.example.targetgather
6.app中的资源包名修改，将AndroidManifest.xml中<Mainfest>的package该为：com.example.targetgather。如果目录结构没有因此改变的话，那就手动去改
7.一些杂七杂八的地方，例如androidTest, style

# Java模块要改
1.子模块在实际文件名
2.settings.gradle中子模块名称
3.app/build.gralde中引用的子模块名称
4.改资源包名。如果目录结构没有因此改变的话，那就手动去改

# Kt版本的不同点
0.先将gradle版本升到6.8.3，因为这是kotlin 1.9要求的最小gradle版本
1.在根build.gradle中引入kotlin的插件依赖
2.在app/build.gradle中引入kotlin插件，并引入ktx依赖
（将MainActivity、test、androidTest中的Java类转为Kotlin类）