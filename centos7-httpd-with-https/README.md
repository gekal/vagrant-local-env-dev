Apache server with https on centos
=================

# 本机环境

    确保下列软件已安装
    
* [Vagrant](https://www.vagrantup.com/)
    * plugin: **vagrant-vbguest** （vagrant plugin install vagrant-vbguest）
* [Virtual Box](https://www.virtualbox.org/)

# 域名设置

## 对象域名指向本地的Public IP
 
    例： www.sample.com -> 12.34.56.78

* 域名解析服务下添加下面的记录

|记录类型|主机记录|解析线路(isp)|记录值|
|---|---|---|---|
|A|www|默认|12.34.56.78|


## 公网的ip通过设置NAT，实现下列端口转化

    12.34.56.78：80  -> 192.168.0.x：10080
    12.34.56.78：443 -> 192.168.0.x：10443

* 路由器上做如下配置

|服务类型|外部端口|内部IP|内部端口|协议类型|
|---|---|---|---|---|
|http|80|192.168.0.x|10080|TCP|
|https|443|192.168.0.x|10443|TCP|

# Vgrantfile修改

    修改下面的代码片中的owner_mail和domain_name的值

```ruby
    ansible.extra_vars = {
      ansible_ssh_user: "vagrant",
      owner_mail: "name@mail.com",
      domain_name: "www.excale.com"
    }
```

# 启动虚拟机

下载git的代码，并cd到[（root.dir）/vagrant-local-env-dev/centos7-httpd-with-https],在命令行下执行下面命令启动虚拟机

```ruby
# 启动
vagrant up
# 重启
vagrant reload
# 关机
vagrant halt
# 删除
vagrant destroy
```

# 结果确认

访问下面url，你就可以在浏览器中访问你的网站了

    例： https://www.sample.com
