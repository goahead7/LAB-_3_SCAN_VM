# LAB-_3_SCAN_VM
Выбранные машинки:
# 1. HTB  <img width="1437" alt="Снимок экрана 2022-06-04 в 11 31 22" src="https://user-images.githubusercontent.com/63841835/171971389-21b1f282-f84c-476e-aebd-ce71f0fcce9e.png">
10.10.11.157
# 2. VulnHub
<img width="1387" alt="Снимок экрана 2022-06-04 в 11 33 04" src="https://user-images.githubusercontent.com/63841835/171971445-59e08439-7c21-4cdb-8dea-f866e3c0bbdb.png">
192.168.56.118

# 3. Metasplotable3
192.168.0.108

# 1.1 NMAP
nmap -sS -A -sC -sV -vv  
-sS: TCP SYN/с использованием системного вызова Connect()/ACK/Window/Maimon сканирования  
-A: Активировать функции определения ОС и версии, сканирование с использованием скриптов и трассировку  
-sC: эквивалентно опции --script=default  
-sV: Исследовать открытые порты для определения информации о службе/версии  
-vv: Увеличить уровень вербальности (можно задать больше, для увеличения эффективности)  

![image](https://user-images.githubusercontent.com/62139377/171991533-180cb0c9-0250-44b2-b772-4ed038a84397.png)
![image](https://user-images.githubusercontent.com/62139377/171991537-b32e1db2-3520-44bd-812d-9cf779212fe7.png)
![image](https://user-images.githubusercontent.com/62139377/171991544-b695cd99-c21b-4d6d-bf6d-3f2ce88b7ecf.png)  
nmap -sN -sU -F -sV -vv  
-sN: TCP Null сканирования, не устанавливаются никакие биты  
-sU: UDP сканирование  
-F: Быстрое сканирование - Сканирование ограниченного количества портов  
-sV: Исследовать открытые порты для определения информации о службе/версии   
-vv: Увеличить уровень вербальности (можно задать больше, для увеличения эффективности)  

![image](https://user-images.githubusercontent.com/62139377/171991578-bf894383-dfec-4133-8a04-8cb18f905940.png)
![image](https://user-images.githubusercontent.com/62139377/171991585-94823b7e-4811-43fb-ac15-62d1be66a11e.png)  
nmap -Pn -Pe -sS -O  
-PN: Расценивать все хосты как работающие -- пропустить обнаружение хостов  
-PE: Пингование с использованием ICMP эхо запросов, запросов временной метки и сетевой маски  
-sS: TCP SYN/с использованием системного вызова Connect()/ACK/Window/Maimon сканирования  
-O: Включить режим определения ОС. При включении этой опции Nmap посылает несколько TCP и UDP пакетов на хост, а полученные результаты сравниваются с данными из файла nmap-os-db  

![image](https://user-images.githubusercontent.com/62139377/171991608-9cb6fbcf-80da-466d-a874-51ccc6392b26.png)  
nmap -sV —script=vulners.nse  
vulners.nse: Для каждого доступного CPE скрипт выводит известные vulns (ссылки на соответствующую информацию) и соответствующие оценки CVSS.  

![image](https://user-images.githubusercontent.com/62139377/171991626-1fab6d8d-3232-49f8-9c0c-a1c1b64cf828.png)  
nmap —script=qscan.nse  
qscan.nse: Повторно исследует открытые и/или закрытые порты на хосте, чтобы получить серию значений времени обхода для каждого порта. Эти значения используются для группировки наборов портов, которые статистически отличаются от других групп.  

![image](https://user-images.githubusercontent.com/62139377/171991633-0441863a-dc53-4508-a11e-117eb912281e.png)

# 1.2 SN1PER
![2022-05-06 (25)](https://user-images.githubusercontent.com/56391887/171975335-f7d5dd43-a385-4c3e-85c2-ce399b25489b.png)
![2022-05-06 (26)](https://user-images.githubusercontent.com/56391887/171975353-3be1d9a5-1215-4e9f-b3a7-c89565f0b826.png)
![2022-05-06 (27)](https://user-images.githubusercontent.com/56391887/171975418-3c86f6bb-4fee-4376-86ec-4ff2763b0d89.png)
![2022-05-06 (31)](https://user-images.githubusercontent.com/56391887/171975428-4fe69452-00de-4a96-8aa7-3416dfcfe673.png)
![2022-05-06 (33)](https://user-images.githubusercontent.com/56391887/171975435-3494cb52-7d8f-4461-b156-b495b8225ac5.png)
![2022-05-06 (63)](https://user-images.githubusercontent.com/56391887/171975519-fce8024b-6e2d-4ffe-bca1-b767f968a9bc.png)  

# 1.3 NESSUS  
![image](https://user-images.githubusercontent.com/62139377/172029940-1b5011f3-7188-4f7d-a661-14cc44bd051a.png)
![image](https://user-images.githubusercontent.com/62139377/172029954-2117b4f7-cf8c-4196-b385-94e266091bda.png)
![image](https://user-images.githubusercontent.com/62139377/172029960-773a4422-71a2-4b2b-ae8c-c601f3f5b7be.png)
![image](https://user-images.githubusercontent.com/62139377/172029962-f77535cd-34f9-4a54-9bbf-311acaf2306b.png)  

# 1.4 OPENVAS 
<img width="916" alt="Снимок экрана 2022-06-05 в 10 39 21" src="https://user-images.githubusercontent.com/63841835/172030139-d4728b89-ec51-47d0-834a-89356f33725b.png">

# 1.5 NEXPOSE
<img width="1048" alt="Снимок экрана 2022-06-05 в 11 36 46" src="https://user-images.githubusercontent.com/63841835/172031207-31807c77-9200-41e2-b39a-068386bc861e.png">
<img width="985" alt="Снимок экрана 2022-06-05 в 11 38 49" src="https://user-images.githubusercontent.com/63841835/172031250-3bd7e7fc-ee26-4edc-a8ce-d0b36df5d676.png">
<img width="1020" alt="Снимок экрана 2022-06-05 в 11 39 29" src="https://user-images.githubusercontent.com/63841835/172031262-055e609f-d5aa-4287-856d-4176ab0b1153.png">


# 2.1 NMAP  
nmap -sS -A -sC -sV -vv  

![image](https://user-images.githubusercontent.com/62139377/171991643-9a59a983-3d2d-4b99-aa00-13b8fc90ef99.png)
![image](https://user-images.githubusercontent.com/62139377/171991657-4c51487e-36e8-41dc-a777-caed84e446fe.png)
![image](https://user-images.githubusercontent.com/62139377/171991662-0695252b-73b3-449d-8815-6702d9faecef.png)  
nmap -sN -sU -F -sV -vv  

![image](https://user-images.githubusercontent.com/62139377/171991688-24efd5c8-55ec-4392-8349-670366476097.png)  
nmap -Pn -Pe -sS -O  

![image](https://user-images.githubusercontent.com/62139377/171991699-beacc2fc-e6bb-4800-b173-e15656b6d6fc.png)  
nmap -sV —script=vulners.nse  

![image](https://user-images.githubusercontent.com/62139377/171991707-4cc436dd-700f-4576-b72a-95ef35f702cc.png)  
nmap —script=qscan.nse  

![image](https://user-images.githubusercontent.com/62139377/171991713-ce693916-7bd0-47c4-8bb0-93e07bcf154b.png)
# 2.2 SNIPER
![2022-05-14 (15)](https://user-images.githubusercontent.com/56391887/171976260-a08ff2b9-ea1e-4e45-bae8-e0c1226b3762.png)
![2022-05-14 (16)](https://user-images.githubusercontent.com/56391887/171976272-e7770e95-f404-49c1-b03c-72d946c0fe36.png)
![2022-05-14 (17)](https://user-images.githubusercontent.com/56391887/171976284-2ab8e78e-b604-43e5-9261-9fe93ac36f3b.png)
![2022-05-14 (18)](https://user-images.githubusercontent.com/56391887/171976310-8a842b92-029f-4671-a177-c81dd165c3fa.png)
![2022-05-14 (19)](https://user-images.githubusercontent.com/56391887/171976327-cece835a-1897-41c6-8276-5f326271224c.png)

# 2.3 NESSUS
![image](https://user-images.githubusercontent.com/62139377/172029995-63061ffd-5d24-4bfa-98a7-d3af4cab84b4.png)
![image](https://user-images.githubusercontent.com/62139377/172030001-b875b805-7fb1-4e50-bb4c-b989c3fee862.png)
![image](https://user-images.githubusercontent.com/62139377/172030010-c4f82c3b-a711-4e78-bdb8-840bf61a93b0.png)
![image](https://user-images.githubusercontent.com/62139377/172030026-2e896b7b-7936-48c7-b911-8ffdb8a602f6.png)  

# 2.4 OPENVAS 
<img width="916" alt="Снимок экрана 2022-06-05 в 10 39 21" src="https://user-images.githubusercontent.com/63841835/172030139-d4728b89-ec51-47d0-834a-89356f33725b.png">
# 2.5 NEXPOSE
-

# 3.1 NMAP. 
Проверяет, уязвим ли веб-сервер для обхода каталога, пытаясь получить /etc/passwd или \boot.ini.
<img width="533" alt="Снимок экрана 2022-06-05 в 12 30 16" src="https://user-images.githubusercontent.com/63841835/172032414-3f47e4e8-ac4c-4d4b-90dc-e3e5d297ef65.png">
<img width="508" alt="Снимок экрана 2022-06-05 в 12 30 54" src="https://user-images.githubusercontent.com/63841835/172032432-100cb8fa-aa77-42f8-8f63-1abc6c379248.png">
<img width="500" alt="Снимок экрана 2022-06-05 в 12 31 41" src="https://user-images.githubusercontent.com/63841835/172032451-e7cfe803-5b82-43f3-8d81-fb7ad63e9bdd.png">
<img width="602" alt="Снимок экрана 2022-06-05 в 12 35 15" src="https://user-images.githubusercontent.com/63841835/172032528-d326d0f3-838d-4821-bbae-be077be28887.png">
<img width="653" alt="Снимок экрана 2022-06-05 в 12 39 45" src="https://user-images.githubusercontent.com/63841835/172032671-5253739b-d420-4584-a004-f61f18db1681.png">

# 3.2 SN1PER
<img width="575" alt="Снимок экрана 2022-06-05 в 12 16 30" src="https://user-images.githubusercontent.com/63841835/172032108-3855964f-b00b-494a-a2f0-819b847c5003.png">
 <img width="752" alt="Снимок экрана 2022-06-05 в 12 17 50" src="https://user-images.githubusercontent.com/63841835/172032145-37aa72c5-3e85-46da-a2e4-1565f04452db.png">
<img width="761" alt="Снимок экрана 2022-06-05 в 12 18 27" src="https://user-images.githubusercontent.com/63841835/172032154-d1b0b94e-87bf-452f-ae2e-05370db8cd0c.png">
<img width="624" alt="Снимок экрана 2022-06-05 в 12 22 16" src="https://user-images.githubusercontent.com/63841835/172032233-9c11a9dc-5674-4ef5-b4eb-5bbb26a04d18.png">

# 3.3 NESSUS
<img width="766" alt="Снимок экрана 2022-06-05 в 12 24 13" src="https://user-images.githubusercontent.com/63841835/172032278-b8f65619-bee1-42c4-b4b2-a54878535687.png">

# 3.4 OPENVAS
<img width="908" alt="Снимок экрана 2022-06-05 в 12 24 44" src="https://user-images.githubusercontent.com/63841835/172032301-7c8c1eb7-59f3-4024-896f-b3d101878d78.png">

# 3.5 NEXPOSE
-


