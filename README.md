# Sublime 安装Package control失败以及安装成功后点击Package Control: Install Package报错的问题解决办法

## 1. 手动安装Package Control
打开`Sublime`，在`Perferences`中选择`Browse Packages`，这时就会自动打开一个`Packages`文件夹，将本项目中的`Package Control`文件夹整个拷贝到该文件夹下即可。

重启`Sublime`后，在`Perferences`中就可以看到`Package Settings`和`Package Control`两个菜单项了。

## 2. 上面安装`Package Control`成功后，`control + command + P`打开安装插件输入框，输入`Install Package`， 点击`Package Control: Install Package`没有反应或者报`There are no packages available for installation`这样的错误。

这是因为`Sublime`下载插件的时候会使用到一个文件`channel_v3.json`，并且这个文件是联网下载的，由于**原因下载失败的话就会报错了。在`Sublime`的`Perferences`中选择`Package Settings` -> `Package Control` -> `Settings-User` 会打开一个新的文件，在这个文件中配置我们自己的`channel_v3.json`(将本项目中的channel_v3.json文件保存到一个本地目录)路径就可以了：

```
{
	"bootstrapped": true,
	"installed_packages":
	[
		"Package Control"
	],
	"channels": [
        "/Users/SupperMen/Desktop/MyProjects/PHPTester/Configs/channel_v3.json"
    ]
}

```
