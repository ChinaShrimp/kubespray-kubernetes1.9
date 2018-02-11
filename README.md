# kubespray？
kubespray-kubernetes1.9 是一个基于 [Kubespray](https://github.com/kubernetes-incubator/kubespray) 部署 Kubernetes1.9.0 的 Ansible 脚本。
# kubespray做了些什么？
本项目基于[kubespray](https://github.com/kubernetes-incubator/kubespray)
- 将国外网站镜像库迁移到阿里云镜像库，可以在国内加速安装Kubernetes1.9.0
- 修复了 kubespray 的若干Bug
- 基于CentOS7.2系统做了可用性和稳定性测试
# 使用方式
## Deploy Server
1. Make sure python 3.x is installed on deploy server;
2. `git clone https://github.com/ChinaShrimp/kubespray-kubernetes1.9.git`
3. `cd kubespray-kubernetes1.9` and run `pip install -r requirements.txt`
4. Modify inventory file `inventory/inventory.cfg` (It could be generated,
   support later)
5. Make sure deploy server could access other nodes using ssh keys
6. Run `ansible-playbook -b -v -i inventory/inventory.cfg prerequisition.yml`
7. If everything is fine, run following commands to install kubernetes:
  `ansible-playbook -i inventory/inventory.cfg cluster.yml -b -v`

# 联系我
Following is contact info for original author, thanks a lot for his nice support!
- Email：iamwanglibing@qq.com
- DEVOPS俱乐部QQ群：207721193

参考 
[Kubespray部署Kubernetes](https://www.wanglibing.com/2017/12/26/Kubespray部署Kubernetes/)

