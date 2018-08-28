# think-testing
ThinkPHP 5 应用单元测试组件


修改自 firma/think-testing 

官方不更新单元测试，一直无法使用，这里直接 自己改了它。

https://packagist.org/packages/foxiswho/think-testing

只支持 php 7.1.x,php 7.2.x,php 7.3.x

注意：这里 只支持 `ThinkPHP5.1.22` 以上版本

# 步骤

先执行
```angular2html
composer require foxiswho/think-testing
```
等待拉取报如下错误
```SHELL
                                   
  [InvalidArgumentException]       
  Unable to install this library!  
                                   
```

修改以下路径文件
```shell
vendor/topthink/think-installer/src/ThinkTesting.php
```
找到`26`行,修改为如下，并保存
```SHELL
//if ('topthink/think-testing' !== $package->getPrettyName()) {
//            throw new \InvalidArgumentException('Unable to install this library!');
//        }
```

最后调用
```SHELL
composer require foxiswho/think-testing
```