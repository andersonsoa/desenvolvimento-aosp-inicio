# 2. Compilando, Executando e Modificando o Android

### 2.1. Instalando os Pacotes Necessários
---
```bash
sudo apt install vim git git-core python3 python-is-python3 python-mako openjdk-8-jdk android-tools-adb bc bison build-essential curl flex g++-multilib gcc-multilib gnupg gperf imagemagick lib32ncurses-dev lib32readline-dev lib32z1-dev liblz4-tool libncurses5-dev libsdl1.2-dev libssl-dev libxml2 libxml2-utils lzop pngcrush rsync schedtool squashfs-tools xsltproc yasm zip zlib1g-dev libtinfo5 libncurses5 zip libc6-dev-i386 lib32ncurses5-dev x11proto-core-dev libx11-dev libgl1-mesa-dev screen unzip fontconfig kpartx libcurl4 mplayer pigz pbzip2
```

### 2.2. Configurando o Ambiente
---
```bash
cd /media/arquivos/aosp
source build/envsetup
```
![image](https://user-images.githubusercontent.com/19675356/217396196-46d5a03b-322e-4102-89ef-2066c1bc3c9a.png)


```bash
croot
```
![image](https://user-images.githubusercontent.com/19675356/217396397-d1f342c0-f420-4e9b-8329-5920ed7992fa.png)


```bash
lunch
```
![image](https://user-images.githubusercontent.com/19675356/217396600-a45c9801-13e4-457c-a58f-7b41ffaf3b7b.png)


```bash
lunch sdk_phone_x86_64-userdebug
```
![image](https://user-images.githubusercontent.com/19675356/217396772-f3b38b9e-fe23-40fd-a023-36dfa1fbc6ab.png)


```bash
export
```
![image](https://user-images.githubusercontent.com/19675356/217396955-674aa3fd-e012-45e7-af08-b88e08eb3cd0.png)


```bash
export | grep "ANDROID_\|TARGET_\|PATH"
```
![image](https://user-images.githubusercontent.com/19675356/217397023-3e1b2958-4044-450e-9586-4694375f5a75.png)


```bash
export | grep "ANDROID_HOST_OUT"
```
![image](https://user-images.githubusercontent.com/19675356/217397163-e2a0c06b-26a8-4470-9ef6-1407abead0c1.png)


```bash
export | grep "ANDROID_JAVA_HOME"
```
![image](https://user-images.githubusercontent.com/19675356/217397443-d7a3ad69-36fa-4058-becd-32664675d333.png)


### 2.3. Compilando o Android
---
```bash
m
```


```bash

```


```bash

```


```bash

```


```bash

```


```bash

```


```bash

```
