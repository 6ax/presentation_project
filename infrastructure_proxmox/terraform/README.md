## Terraform

Для создания виртуальных машин в облаке Proxmox используем :

- [Proxmox ](https://registry.terraform.io/providers/Telmate/proxmox/latest) - провайдер Terraform

- [Cloud-init](https://cloud-images.ubuntu.com/focal/current/) - образ Ubuntu 20.04

_Описание содержимого:_

- main.tf - файл сборки terraform
- variables.tf - файл переменных terraform, конфигурация создаваемых виртуальных машин описана тут же
- cloud-init-configs - сожержит шаблон настроек cloud-init образа для создаваемых виртуальных машин из terraform
- destroy_infrastructure - содержит pipeline Jenkins для уничтожения созданной инфраструктуры
