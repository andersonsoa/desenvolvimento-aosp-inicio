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
![image](https://user-images.githubusercontent.com/19675356/217676231-fd7bd16e-41d2-48ed-bf3b-6784b1538e40.png)


```bash
ls -lh out/target/product/emulator_x86_64/system-qemu.img 
```
![image](https://user-images.githubusercontent.com/19675356/217676386-418597af-1391-492f-ba28-100b5bfdab33.png)


### 2.4. Executando o Emulador
---
```bash
emulator &
```
![image](https://user-images.githubusercontent.com/19675356/217678511-fef4aa99-7455-4369-ac9b-ce7fa394654e.png)


### 2.5. Modificando o Código-Fonte I - Settings
---
```bash
nano packages/apps/Settings/res/values/strings.xml
```
![image](https://user-images.githubusercontent.com/19675356/217679016-c289ed50-2fb3-4312-8df4-8126e52420e7.png)


```bash
m
```
![image](https://user-images.githubusercontent.com/19675356/217682390-3aaaa8dd-1133-46c9-a353-83362ef5fa58.png)


```bash
emulator
```
![image](https://user-images.githubusercontent.com/19675356/217682801-6618c2f6-6dd4-4e67-b197-8acbb9671ec9.png)


```bash
cd packages/apps/Settings
git status
```
![image](https://user-images.githubusercontent.com/19675356/217682890-446faa55-c1ef-4546-b89a-693996564b58.png)


```bash
git reset --hard HEAD
git status
croot
```
![image](https://user-images.githubusercontent.com/19675356/217683087-4478dde8-4fc9-4eab-80f1-dba0e6da1db6.png)


### 2.6. Modificando o Código-Fonte II - Screenshot Watermark
---

- Sem modificação
```bash
adb shell "
su root sendevent /dev/input/event1 1 114 1
su root sendevent /dev/input/event1 1 116 1
su root sendevent /dev/input/event1 0 0 0
sleep 1
su root sendevent /dev/input/event1 1 114 0
su root sendevent /dev/input/event1 1 116 0
su root sendevent /dev/input/event1 0 0 0"
```
![image](https://user-images.githubusercontent.com/19675356/217688931-bf33ef1c-5094-4667-a0aa-2d9884f6803f.png)

```bash
gedit frameworks/native/services/surfaceflinger/SurfaceFlinger.cpp
```
![image](https://user-images.githubusercontent.com/19675356/217686464-7fc488b3-f740-45eb-bb63-8dff0da12ed3.png)

- Com modificação
```bash
adb shell "
su root sendevent /dev/input/event1 1 114 1
su root sendevent /dev/input/event1 1 116 1
su root sendevent /dev/input/event1 0 0 0
sleep 1
su root sendevent /dev/input/event1 1 114 0
su root sendevent /dev/input/event1 1 116 0
su root sendevent /dev/input/event1 0 0 0"
```
![image](https://user-images.githubusercontent.com/19675356/217688977-7413516d-15a7-48de-b76a-3e7060d51763.png)



```bash

```


```bash

```


```bash

```


```bash

```
