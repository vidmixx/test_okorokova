# test_okorokova

1 Проверить статус файервола sudo firewall-cmd --state

![image](https://github.com/user-attachments/assets/2eb6a4fd-772f-4e68-9a88-2ed803429eba)

2 Установка wget, curl, git и tar sudo yum install -y wget curl git tar

![image](https://github.com/user-attachments/assets/2ea70da5-64a5-4bf5-ad59-d76f92c91205)

3 Установка Chrony sudo yum install -y chrony

![image](https://github.com/user-attachments/assets/4ff1a9ff-20e3-4f8e-9315-f1be737b7db3)

3.1 Включение и запуск службы sudo systemctl enable chronyd sudo systemctl start chronyd

![image](https://github.com/user-attachments/assets/d249baaf-f7a2-44a6-983c-f7e2a60a9453)

4.Проверка статуса SELinux getenforce

![image](https://github.com/user-attachments/assets/a10056c9-6a3c-4b22-8ab5-7476197f1a10)

4.1 Если выводится "Enforcing", отключаем SELinux: sudo setenforce 0 sudo sed -i 's/^SELINUX=.*/SELINUX=disabled/g' /etc/selinux/config

![image](https://github.com/user-attachments/assets/e8731c03-3410-4061-8b9c-b824460303a5)

Скачивание версии 3.3.0 wget https://github.com/prometheus/prometheus/releases/download/v3.3.0/prometheus-3.3.0.linux-amd64.tar.gz

![image](https://github.com/user-attachments/assets/e2c5deeb-ef7b-46ab-bffc-289cfbe855af)


Создание директорий sudo mkdir -p /etc/prometheus /var/lib/prometheus
image

7.Распаковка архива tar -zxf prometheus-*.linux-amd64.tar.gz

image

Переход в папку cd prometheus-*.linux-amd64

Проверка текущего пути pwd

10.Копирование бинарных файлов sudo cp prometheus promtool /usr/local/bin/

10.1 Копирование конфигурационного файла sudo cp prometheus.yml /etc/prometheus/

image

Выход из директории и удаление временных файлов cd .. && rm -rf prometheus-.linux-amd64/ && rm -f prometheus-.linux-amd64.tar.gz
12.Проверка текущего пути pwd

![image](https://github.com/user-attachments/assets/46e32b6b-d6a2-4c56-9e18-d5bab1b0a491)


Просмотр содержимого текущей директории ls -l

![image](https://github.com/user-attachments/assets/54c5ac80-7765-423e-842f-75db27c758ac)

