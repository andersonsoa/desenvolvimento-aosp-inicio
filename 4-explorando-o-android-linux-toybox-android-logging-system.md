# 4. Explorando o Android/Linux - Toybox, Android Logging System


### 4.1. Toybox
---
```bash
cd /system/bin/ 
ls -al
```
![image](https://user-images.githubusercontent.com/19675356/217972647-5a96dc8b-fa51-47dd-99e2-834a638a755e.png)


```bash
ls -al | grep toybox | wc -l  
```
![image](https://user-images.githubusercontent.com/19675356/217972803-bb8ffaad-ffa5-4c34-a3cf-c663cfa2aad8.png)

```bash
toybox
```
![image](https://user-images.githubusercontent.com/19675356/217973007-e67e275c-f5b2-41e9-9124-1315317916c8.png)


- Codigo fonte do Toybox


![image](https://user-images.githubusercontent.com/19675356/217973314-5ce3744f-132e-44b1-8a0b-4804d5e1e62c.png)

- Codio de exemplo de Toybox em C

![image](https://user-images.githubusercontent.com/19675356/217974912-fcd13018-4be9-4637-b9c6-770cdd767fd7.png)


### 4.2. Logs do Kernel: dmesg
---
```bash
su 
dmesg
```
![image](https://user-images.githubusercontent.com/19675356/217975447-6f3895b6-d9e9-4945-86f3-1f415e325dab.png)

```bash
dmesg -T
```
![image](https://user-images.githubusercontent.com/19675356/217975622-3e5e710d-54ff-46d8-8c86-26bf73c66143.png)


```bash
dmesg -T -w
```
![image](https://user-images.githubusercontent.com/19675356/217975962-d7681fca-7f09-4b1f-9a9b-9f0ac6bfb9cf.png)

```bash
echo "planet: Omicron Persei 8" > /dev/kmsg 
dmesg -T
```
![image](https://user-images.githubusercontent.com/19675356/217976337-5b3a7037-6f86-4aa5-89b3-6cde3bce4dae.png)


```bash
cat /dev/kmsg  
```
![image](https://user-images.githubusercontent.com/19675356/217976587-e5f1afcb-464d-4d2a-9b83-61be6b35938a.png)


### 4.3. Logs do Android: Android Logging System
---

```bash
logcat
```
![image](https://user-images.githubusercontent.com/19675356/217976901-52c88a7c-9a4c-48be-bf83-ba05dc0a7908.png)


```bash
adb logcat
```
![image](https://user-images.githubusercontent.com/19675356/217977099-88138924-0eea-4f63-b325-68c064e72f0b.png)


```bash
logcat -s PhotoView:d 
```
![image](https://user-images.githubusercontent.com/19675356/217977743-44824528-2dad-403b-a18a-7a7450dfd88e.png)


```bash
logcat -s Zygote

```
![image](https://user-images.githubusercontent.com/19675356/217977899-252449f7-1052-4c9b-af03-b10fdc1cc6d7.png)

```bash
logcat -s *:I
```
![image](https://user-images.githubusercontent.com/19675356/217978099-3668a6a9-c67d-4f5a-a5e2-c4b1d62de356.png)


```bash
logcat -s Zygote:I  
```
![image](https://user-images.githubusercontent.com/19675356/217978320-5df68e1e-2cd0-4bf1-b72b-94bf030a78b6.png)


```bash
logcat -b events 
```
![image](https://user-images.githubusercontent.com/19675356/217978556-b94a463f-f0e7-4ee3-b117-d3ded2a7372b.png)


```bash
logcat -h
```
![image](https://user-images.githubusercontent.com/19675356/217978679-16238137-4b2c-40a5-8f79-79387e8c12ad.png)


```bash
log -p I -t "book" "To the 8th Dimension and Back Again" 
logcat
```
![image](https://user-images.githubusercontent.com/19675356/217979067-c4aeeea7-35a9-4cd0-a94f-d321dc65a6eb.png)


```bash
ls -al /dev/socket/logd*
```
![image](https://user-images.githubusercontent.com/19675356/217979332-3fc3afc7-765d-4586-9c66-915c7bc2bf34.png)


```bash
echo -n 'getLogSize 0\0EXIT\0' | nc -U /dev/socket/logd    
```
![image](https://user-images.githubusercontent.com/19675356/217979651-3d64d99f-84f5-415d-9ae1-4a40cbcd569e.png)

```bash
logcat -g
```
![image](https://user-images.githubusercontent.com/19675356/217979763-d970162f-016c-4c98-a721-7450c81a6dbe.png)

