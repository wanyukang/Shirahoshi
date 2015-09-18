# Shirahoshi

苹果婊应用构建脚本，使你的苹果婊应用易于集成。


## 依赖环境
* Xcode Command Line Tools
* [xctool](https://github.com/facebook/xctool)
* [cupertino](https://github.com/nomad/cupertino)

## 如何使用

脚本通过接收一个参数来判定使用哪个配置集来执行构建。

~~~
./AppleWatchBuildScript dev
~~~

所以你必须在脚本中配上你自己工程的配置参数。

## 工作原理

由于苹果婊app加入，需要签名的target从一个变成三个，而且三个target还各自需要不一样的签名，xcodebuild提供的-target已经不适用了。

这个脚本的解决方案是，代替xcodebuild提供的flag，构建前自行替换掉project.pbxproj中签名相关的键值，构建时即可直接使用project.pbxproj中的签名配置。

#### 参考资料
[watchkit-command-line-builds](http://www.matrixprojects.net/p/watchkit-command-line-builds)

[kkbox-ios-jenkins](https://kkbox.codes/archives/2015/07/03/kkbox-ios-jenkins/)

[project.pbxproj，最熟悉的”陌生人”](http://www.olinone.com/?p=215)

##LICENSE
MIT