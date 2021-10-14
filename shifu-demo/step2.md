在集群中安装***Shifu***

下载解压 `wget --no-check-certificate -O shifu-setup.tar.gz https://edgenesis.com/wp-content/uploads/2021/10/shifu-setup.tar.gz && tar -zxvf shifu-setup.tar.gz && cd shifu`{{execute}}

安装  `bash ./test/scripts/deviceshifu-install.sh apply`{{execute}}

获取集群所有Pods的状态 `kubectl get pods -A`{{execute}}

此时应该会看到`controller`运行:
```
kubectl get pods --all-namespaces
NAMESPACE            NAME                                                READY   STATUS    RESTARTS   AGE
crd-system           crd-controller-manager-7bc78896b9-sq72b             2/2     Running   0          28m
```