﻿# Wenprise WeChatPay Payment Gateway For WooCommerce #
Contributors: iwillhappy1314
Donate link: https://www.wpzhiku.com/
Tags: Alipay, WooCommerce, woocommerce, payment, payment gateway, gateway, 微信, 微信支付, Wechat payment gateway, Wechat gateway, credit card, pay, online payment, shop, e-commerce, ecommerce
Requires PHP: 5.6.0
Requires at least: 4.7
Tested up to: 5.5
WC requires at least: 3.5
WC tested up to: 4.4
Stable tag: 1.0.15
License: GPL-2.0+

Wechat payment gateway for WooCommerce, WooCommerce 微信免费全功能支付网关。

## Description ##
**功能更全面的 WooCommerce 免费微信支付网关**，企业版，需要微信企业认证才可以使用。支持功能如下：

* 支持所有 WooCommerce 产品类型
* PC 端扫描二维码支付
* 移动端浏览器 H5 调起微信支付
* 微信端公众号支付，需要安装微信登录插件，设置 open_id
* 在 WooCommerce 订单中直接通过微信退款，退款原路返回
* 货币不是人民币时，可以设置一个固定汇率

支付宝支付网关：
[Wenprise Alipay Payment Gateway For WooCommerce](https://wordpress.org/plugins/wenprise-alipay-checkout-for-woocommerce/)


### Support 技术支持 ###

Email: amos@wpcio.com

## Installation ##

1. 上传插件到`/wp-content/plugins/` 目录，或在 WordPress 安装插件界面搜索 "Wenprise WeChatPay Gateway For WooCommerce"，点击安装。
2. 在插件管理菜单激活插件

## Upgrade Notice ##

更新之前，请先备份数据库。


## Frequently Asked Questions ##


### 无法在微信公众号中支付？在微信中支付，提示「微信支付配置错误」？ ###

在微信公众号中，需要获取 open_id 才能使用此插件进行支付，如果您的网站已经实现了微信公众号授权登录，请参考下一个问题中的代码进行兼容。


### 怎么兼容其他微信登录插件？ ###
如果已经使用了其他微信登录插件，可以通过`wprs_wc_wechat_open_id` 这个 Filter 来修改支付插件使用的 open_id，修改下面代码中获取 open_id 的代码为对应登录插件中的代码即可。
```php
    add_filter('wprs_wc_wechat_open_id', function(){
        $open_id = '';
        return $open_id;
    });
```

## Screenshots ##
* Setting
* payment

## Changelog ##

### 1.0.15 ###
* 移动端浏览器支付增加跳转中间页，解决某些情况下无法验证支付状态的问题。

### 1.0.14 ###
* 更新 readme

### 1.0.13 ###
* 小错误修复

### 1.0.12 ###
* 优化订单号显示方式
* 添加订单号前缀设置选项
* 微信登录启用设置问题修复

### 1.0.10 ###
* Wechat auth bugfix

### 1.0.9 ###
* 添加微信登录失败时的提示信息

### 1.0.8 ###
* Bugfix

### 1.0.6 ###
* Bugfix

### 1.0.4 ###
* 修复某些情况下图标不显示的问题

### 1.0.3 ###
* 初次发布
* 降低 PHP 版本需求

### 1.0 ###
* 初次发布
