---
layout: post
title: CentOS/RHEL 7.1 & 6.7 安装 PHP 5.6
---

PHP 5.6.12 是 PHP 5 最新的版本，应该也是最后一个版本了吧，毕竟 PHP 7 RC1 已出，等到十月份就是正式版本发布了。

PHP 5.6 新增特性：

- constant scalar expressions
- variadic functions
- argument unpacking
- exponentiation operator
- support for large(>2GiB) file uploads
- SSL/TLS improvements including peer verification by default
- a new command line debugger called phpdbg

&nbsp;  

```bash
任何时候，使用 yum 之前先运行 yum update
任何时候，使用 yum 之前先运行 yum update
任何时候，使用 yum 之前先运行 yum update
```

重要的事情说三遍！  
<br/>

## 准备

安装 PHP 5.6 之前需要先添加 Webtatic EL 的 yum 仓库信息:  
CentOS/RHEL 7.x:  

```bash
rpm -Uvh https://dl.fedoraproject.org/pub/epel/epel-release-latest-7.noarch.rpm
rpm -Uvh https://mirror.webtatic.com/yum/el7/webtatic-release.rpm
```
CentOS/RHEL 6.x:  

```bash
rpm -Uvh https://mirror.webtatic.com/yum/el6/latest.rpm
```
<br/>

## 安装

然后开始安装 PHP 5.6:  

```bash
yum install php56w
```
<br/>

## 错误

```
错误：php56w-common conflicts with php-common-5.xxx.x86_64
```
如果出现类似上面的错误信息时，说明 yum 已经安装了 php。这时候需要升级替换原来版本的 php：

```bash
yum install yum-plugin-replace
yum replace php-common --replace-with=php56w-common
```
然后再次运行安装命令即可：

```bash
yum install php56w
```

Enjoy!
