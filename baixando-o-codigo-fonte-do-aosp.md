## 1. Baixando o Código-Fonte do AOSP

### 1.3. Fazendo Download do AOSP
---

```bash
repo sync -c -j10
```
![image](https://user-images.githubusercontent.com/19675356/216489005-d1f40677-adb0-465e-b953-32e5b37e71e6.png)


```bash
nano /proc/cpuinfo
cat /proc/cpuinfo | grep processor | wc -l
nproc --all
```
![image](https://user-images.githubusercontent.com/19675356/216489275-826e184f-c1a4-458c-9154-6c2722b2142a.png)
![image](https://user-images.githubusercontent.com/19675356/216489420-a579fdd5-14ee-48e3-b5c6-099280b8a038.png)

### 1.4. Explorando o Código do AOSP
---

```bash
cd aosp
ls
```
![image](https://user-images.githubusercontent.com/19675356/216487519-395fa699-99f0-49ea-b5a0-c7393f4868a4.png)

```bash
find . | grep Integer.java
```
![image](https://user-images.githubusercontent.com/19675356/216488606-048dfd7f-e5e8-4fef-87e4-a5c730fe1b48.png)

### 1.5. Usando o Android Code Search
---
- packages/apps/Settings/res/values-pt/strings.xml
![image](https://user-images.githubusercontent.com/19675356/216485323-54095c83-8a14-459f-bc0a-936ed7e0b8cb.png)

- packages/apps/Settings/res/values-it/strings.xml
![image](https://user-images.githubusercontent.com/19675356/216485803-ec347ddb-5201-4383-8f3e-4a1d18971038.png)

- Ora ti mancano
![image](https://user-images.githubusercontent.com/19675356/216486013-3cc19488-5039-44c5-bacb-5e5123a6e021.png)

- frameworks/native/services/surfaceflinger/SurfaceFlinger.cpp
![image](https://user-images.githubusercontent.com/19675356/216486236-6d735a1c-c41a-4659-b481-47107fd9d598.png)
![image](https://user-images.githubusercontent.com/19675356/216486851-d22c0d86-df92-4944-9500-e17731c06079.png)
