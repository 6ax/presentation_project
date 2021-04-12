# Добро пожаловать
Данный проект является дополнением к моему резюме, целью которого является демонстрация уровня владения инструментами используемых в проекте.

## Задачи проекта:
_Первый этап:_

Используя подход [Iac](https://ru.wikipedia.org/wiki/%D0%98%D0%BD%D1%84%D1%80%D0%B0%D1%81%D1%82%D1%80%D1%83%D0%BA%D1%82%D1%83%D1%80%D0%B0_%D0%BA%D0%B0%D0%BA_%D0%BA%D0%BE%D0%B4), требуется полностью автоматизировать процесс создания в частном "облаке" [Proxmox Virtual Environment](https://www.proxmox.com/en/proxmox-ve) кластер виртуальных машин [Kubernetes](https://kubernetes.io/ru/docs/concepts/overview/what-is-kubernetes/), состоящий из одной "master node" и двух "worker node" со средой выполнения [containerd](https://github.com/containerd/containerd). Автоматизацию необходимо реализовать в виде [Jenkins](https://www.jenkins.io/) pipeline с использованием [Terraform](https://www.terraform.io/) и [Ansible](https://www.ansible.com/). Состояние ифраструктуры хранить в [SCM](https://git-scm.com/). Хранить и запускать [Jenkins](https://www.jenkins.io/) требуется  в виде [Docker](https://www.docker.com) контейнера на локальной машине администратора соображениям безопасности.

_Второй этап:_

Подготовить кластре [Kubernetes](https://kubernetes.io/ru/docs/concepts/overview/what-is-kubernetes/) к работе на bare matel используя для этого следующее ПО:
- [MetalLLB](https://metallb.universe.tf/) для  [LoadBalancer](https://kubernetes.io/docs/tasks/access-application-cluster/create-external-load-balancer/)
- [Nginx ingress controllers](https://kubernetes.github.io/ingress-nginx/) для [Ingress-controller](https://kubernetes.io/docs/concepts/services-networking/ingress-controllers/)

Мониторинг [Kubernetes](https://kubernetes.io/ru/docs/concepts/overview/what-is-kubernetes/) реализовать на базе связки [Prometheus](https://prometheus.io)+ [Grafana](https://grafana.com/) работающими в кластере при помощи: 
- [Prometheus-operator](https://github.com/prometheus-operator/prometheus-operator)
