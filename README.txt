项目总览			作者：施尧

项目名称：LNMP集群架构一键搭建
简单说明：搭建总共需至少7台机器，我们分别命名为：
		nginx,m01
		web 01,web02
		db01,nfs
		backup
		集群架构图可见“集群架构总览.jpg”
项目步骤：
集群搭建顺序为: 
backup --> nfs --> web01 --> db01 --> web02 --> m01 --> nginx
其中包含的服务为：
rsync --> nfs+sersync --> nginx(html+proxy)+php --> mysql --> nginx(html)+php --> ansible(ssh) --> nginx(LB)
项目结果：
使用脚本一键搭建完成后，整个集群的就成型了。配置本地解析/etc/hosts之后可测试访问相应网页：wucyu.com，显示wordpress界面即搭建成功。

团队成员：施尧，武春雨，马国龙
项目启动时间：2019年5月8号