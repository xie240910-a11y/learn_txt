查看集群是否正常
	kubectl cluster-info

获取所有k8sNode的信息
	kubectl get nodes (- o wide 查看更详细的信息)

获取所有命名空间，包括pod
	kubectl get pods -A (- o wide 查看更详细的信息)

查看pod运行在哪
	kubectl get pod device-center2-0 -n lenovo04 -o wide

进入pod
	kubectl exec -it device-center2-0 -n lenovo04 -- /bin/bash 

查看集群组件状态
	kubectl get componentstatus
	
查看pod详细状态
	kubectl describe pod <pod-name> -A（所有命名空间） -n （指定命名空间） 不加默认default命名空间	

进入pod中
	kubectl exec -it <pod-name> -- /bin/bash
	kubectl exec -it <pod-name> -- sh

查看pod日志
	kubectl logs <pod-name> 需要加命名空间

查看实时日志
	kubectl logs -f <pod-name>
	
删除pod
	kubectl delete pod <pod-name>
	
创建/更新pod
	kubectl apply -f xxx.yaml

删除deployment
	kubectl delete deployment <name>
	
重启Deployment: pod
	kubectl rollout restart deployment <name> -n <namespace>
	
重启StatefulSet: pod
	kubectl rollout restart statefulset <name> -n <namespace>
	
拷贝k8s到本地文件
kubectl cp ./libNyxIODriver.so lenovo04/ice47-0:/opt/supcon/ice/shared
kubectl cp -n lenovo04 ice47-0:/opt/supcon/ice/bin/pacp.pacp ./pacp.pacp

查看 statefulset 根据命名空间
kubectl get statefulset -n lenovo07

打印statefulset的配置
kubectl get statefulset device-center7 -n lenovo07 -o yaml

修改statefulset配置
kubectl edit statefulset device-center7 -n lenovo07

// 重启k8s
kubectl delete pod device-center-0 -n macchi-5
kubectl delete pod device-center7-0 -n lenovo07

获取k8s服务
kubectl get svc -n supcon-1

查看当前集群环境
kubectl config get-contexts

切换集群环境
kubectl config use-context macchi-admin@macchi