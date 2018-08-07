Apache server with https on centos
=================

# 环境准备

    确保下列软件已安装
    
* [Vagrant](https://www.vagrantup.com/)
    * plugin: **vagrant-vbguest**
* [Virtual Box](https://www.virtualbox.org/)

# 域名设置

## 对象域名指向本地的Public IP
 
    例： www.sample.com -> 12.34.56.78

## 公网的ip通过设置NAT，实现下列端口转化

    12.34.56.78；80  -> 192.168.0.x：10080
    12.34.56.78；443 -> 192.168.0.x：10443
    * 上面的设置一般可以在路由器上设置

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
vagrant up
```

# 结果确认

访问下面url，你就可以在浏览器中访问你的网站了
    例： https://www.sample.com


# ------------------------
＞＞＞时间仓促，后面在详细补吧＜＜＜
