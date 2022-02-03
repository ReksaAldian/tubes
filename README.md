# TUGAS BESAR
# **Modul 4 Practicum Report**

### By : Reksa Aldian Rahmandy Putra dan Fiandio Adhi Pradana
----

LXC yang kita perlukan adalah :

* 6 LXC ubuntu 20.04 PHP 7.4
* 2 LXC debian 10 PHP 5.6
* 1 LXC debian 10 mariadb server

![1](https://user-images.githubusercontent.com/95138486/152285371-02fef174-1b52-442b-bbaf-9878c77dbc84.png)

install open ![1 (LXC-LS)]
ssh server di semua lxc
```
apt install openssh-server
```

nano /etc/hosts

![2](https://user-images.githubusercontent.com/95138486/152290841-ea01d0c0-8282-436d-aa7e-7137333a467f.png)

  
```
Ci 

```

lalu kita buat Ansible codeiginiter dengan nama install-ci.yml yang berisi domain container yang kita gunakan

![4 ci](https://user-images.githubusercontent.com/95138486/152291182-075c4e88-b202-41cd-b91f-db0fdbb1cd1f.png)


Buat direktori handlers, tasks dan templates

app/handlers

![app 1](https://user-images.githubusercontent.com/95138486/152291357-aa55febd-c045-454c-a310-f5e3e9ef125e.png)

app/tasks

![app 2](https://user-images.githubusercontent.com/95138486/152291427-8e365950-836a-4fab-83f9-f15139791e86.png)

app/templates

![app 3](https://user-images.githubusercontent.com/95138486/152291668-01dd6168-8385-455f-88e4-798e777c1960.png)


Hasil Ansible Ci

![Ansible ci](https://user-images.githubusercontent.com/95138486/152292768-118d33f3-7e29-4e62-bbff-19268948c19c.png)


lalu kita akses http://kelompok11.fpsas/app


![39 (HASIL CI)](https://user-images.githubusercontent.com/95138486/152293100-35db17b9-f4df-4c00-8eba-6d65dd0ee4c4.png)



```
Laravel
```
Set domain pada Laravel dengan membuat install-laravel.yml
![4 (INSTALL LARAVEL)](https://user-images.githubusercontent.com/95138486/152293261-a2800155-8fa6-4718-8eaf-e52a5577423b.png)


php handlers

![12 (CD PHP HANDLERS MAINYML)](https://user-images.githubusercontent.com/95138486/152293319-be8f11c5-96c8-4e61-917a-c2dbdc5fcff2.png)



php tasks

![11 (CD PHP TASKS MAINYML)](https://user-images.githubusercontent.com/95138486/152293490-8ca6242a-3d3e-4c87-b99f-bb0123f4adb8.png)



laravel handlers

![17 (CD LV HANDLERS NANO MAINYML)](https://user-images.githubusercontent.com/95138486/152293639-9ec9326d-04c9-4c26-8102-c37dc364358d.png)


laravel tasks

![13 (CD LV TASKS MAINYML)](https://user-images.githubusercontent.com/95138486/152293644-b819b53a-ba6a-49de-b338-d0696edd08ab.png)


![14 (CD LV TASKS MAINYML2)](https://user-images.githubusercontent.com/95138486/152293667-357a5301-478f-47be-b4c5-27bd10b82de1.png)


laravel env.templates

![15 (CD LV TEMPLATE ENV TEMPLATE)](https://user-images.githubusercontent.com/95138486/152293818-ff2a0a4f-d718-435d-a285-0070765521b5.png)


laravel .conf

![16 (CD LV NANO LV CONF)](https://user-images.githubusercontent.com/95138486/152293833-ba676df6-e094-4226-b059-a2ff58bee9dd.png)


laravel www.conf

![45 (NANO WWW CONF)](https://user-images.githubusercontent.com/95138486/152294212-18c9413a-ef92-4373-8684-be332b538a39.png)


ansible laravel

![46 (ANSIBLE PLAYBOOK LARAVEL)](https://user-images.githubusercontent.com/95138486/152294234-32d2391d-22c8-451e-8525-c5b5f75da2df.png)

![47 (ANSIBLE PLAYBOOK LARAVEL2)](https://user-images.githubusercontent.com/95138486/152295141-83647e35-8d80-4df0-8bad-a6f27f0abde0.png)



lalu kita akses laravel nya http://kelompok11.fpas/ 

![38 (HASIL LARAVEL)](https://user-images.githubusercontent.com/95138486/152294343-7887b7e0-752d-49d0-afe1-56b2c25df014.png)


```
Yii
```
install-yi.yml

![6 (INSTALL YII)](https://user-images.githubusercontent.com/95138486/152295501-85f8c759-7a7f-4876-9635-0970d81eb5fd.png)


yii handlers

![30 (YII HANDLERS NANO MAINYML)](https://user-images.githubusercontent.com/95138486/152295526-e4d4185b-c40c-4981-a6c2-58ab0f4de116.png)


yii tasks

![28 (YII TASKS NANOMAINYML2)](https://user-images.githubusercontent.com/95138486/152295534-d93cf3d3-02e1-4c61-b40d-48453527959e.png)

yii. conf

![29 (YII TEMPLATES NANO YIICONF)](https://user-images.githubusercontent.com/95138486/152295549-3ba53b64-10f9-49e5-83b9-1ef4a040f5fc.png)

Hasil Ansible yii

![48 (ANSIBLE PLAYBOOK YII)](https://user-images.githubusercontent.com/95138486/152297124-c41b5c83-fffe-4c5d-b60b-0e030436f2b1.png)


![49 (ANSIBLE PLAYBOOK YII2)](https://user-images.githubusercontent.com/95138486/152297433-9f47143e-cff1-4d01-8a35-0a23d406fe3d.png)



lalu kita jalankan yii http://kelompok09.fpas/product

![40 (HASIL YIII)](https://user-images.githubusercontent.com/95138486/152296243-f1d2cd12-7c0c-4e6c-ba50-acfbdcff57e3.png)


```
lxc database
```
insttal-mariadb.yml

![7 (INSTALL MARIADB)](https://user-images.githubusercontent.com/95138486/152296293-9d1b10c4-8458-4e8f-b0ae-1f633265c203.png)

db handlers

![21 (DB HANDLERS NANO MAINYML)](https://user-images.githubusercontent.com/95138486/152296329-580c5b73-38cc-4c61-a3de-0536c9142662.png)

db tasks

![18 (CD DB TASKS MAINYML)](https://user-images.githubusercontent.com/95138486/152296388-94877ed7-98e5-4500-a786-39f9acee6428.png)

![19 (CD DB TASKS MAINYML2)](https://user-images.githubusercontent.com/95138486/152296461-c919ecfa-399d-4be2-a771-f24e7780b952.png)


db templates my.cnf

![20 (CD DB TEMPLATES MYCNF)](https://user-images.githubusercontent.com/95138486/152296568-7df2b373-50f9-41de-ae35-5a7b268e21a7.png)

Hasil Ansible Ci


![50 (ANSIBLE PLAYBOOK MARIADB)](https://user-images.githubusercontent.com/95138486/152297823-21d2f753-1692-465e-91a2-980853299f3c.png)


```
set host utama
```
nano /etc/hosts

![37 (NANO ETC HOSTS)](https://user-images.githubusercontent.com/95138486/152296649-bc5936db-f077-41ab-b28a-441cdb099dc9.png)


```
Host Grouping
```
lakukan grouping pada host untuk memfokuskan lxc sesuai yang diperlukan

![2 (NANO HOSTS ANSIBLE)](https://user-images.githubusercontent.com/95138486/152296712-e48ca130-b1f6-44ad-a2c5-41540ea5f274.png)





