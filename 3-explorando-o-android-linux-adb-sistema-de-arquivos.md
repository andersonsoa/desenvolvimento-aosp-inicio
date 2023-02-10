# 3. Explorando o Android/Linux - ADB, Sistema de Arquivos

### 3.1. Android Debug Bridge
---
```bash
adb
```
![image](https://user-images.githubusercontent.com/19675356/217964699-dcbb4c28-5364-4fbe-914c-81043597e1d1.png)


```bash
adb shell
```
![image](https://user-images.githubusercontent.com/19675356/217964739-0b32cf33-c435-4932-8e06-ac135461d65d.png)


### 3.2. O Sistema de Arquivos
---
```bash
ls
```
![image](https://user-images.githubusercontent.com/19675356/217964848-e82cee05-7441-4df0-8b51-fa690d230606.png)


```bash
ount | grep -E '/\ |vendor|system_ext|product|\ /data\ '
```
![image](https://user-images.githubusercontent.com/19675356/217965258-b3088291-6ab3-4789-a015-c713df34db45.png)


```bash
cd system
ls
```
![image](https://user-images.githubusercontent.com/19675356/217965662-82b32210-ccc6-4e6c-957b-ab868c60d239.png)


```bash
cd system/etc
ls
```
![image](https://user-images.githubusercontent.com/19675356/217965983-e593fcad-3461-4d79-ac1a-257d4cb3d756.png)


```bash
cd system/app
ls
```
![image](https://user-images.githubusercontent.com/19675356/217966047-5f2eba26-5cda-4162-a476-e6f013f635d5.png)


```bash
cd product/app
ls
```
![image](https://user-images.githubusercontent.com/19675356/217966120-5d2aa949-a174-49d3-bc15-c59178bd6214.png)


### 3.3. Quem sou eu?
---
```bash
whoami
```
![image](https://user-images.githubusercontent.com/19675356/217966202-dd3da33e-42fa-416e-bc5a-dbd64d71fa18.png)


```bash
cat /etc/passwd
```
![image](https://user-images.githubusercontent.com/19675356/217966264-f30e38b1-fbaa-4ad0-a4a4-e6ab439dcc89.png)


```bash
nano system/core/libcutils/include/private/android_filesystem_config.h 
```
```c
#define AID_SHELL 2000 /* adb and debug shell user */
```
![image](https://user-images.githubusercontent.com/19675356/217966630-4b3029cb-5298-4e5b-9d34-41b290698636.png)


```bash
id
```
![image](https://user-images.githubusercontent.com/19675356/217967026-fb4422a8-5976-4207-92ab-0821f68b2a8b.png)


```bash
nano system/core/libcutils/include/private/android_filesystem_config.h 
```
```c
/*
 * This file is consumed by build/tools/fs_config and is used
 * for generating various files. Anything #define AID_<name>
 * becomes the mapping for getpwnam/getpwuid, etc. The <name>
 * field is lowercased.
 * For example:
 * #define AID_FOO_BAR 6666 becomes a friendly name of "foo_bar"
 *
 * The above holds true with the exception of:
 *   mediacodec
 *   mediaex
 *   mediadrm
 * Whose friendly names do not match the #define statements.
 *
 * This file must only be used for platform (Google managed, and submitted through AOSP), AIDs.  3rd
 * party AIDs must be added via config.fs, which will place them in the corresponding partition's
 * passwd and group files.  There are ranges in this file reserved for AIDs for each 3rd party
 * partition, from which the system reads passwd and group files.
 */
```
![image](https://user-images.githubusercontent.com/19675356/217967860-cfb7bf20-45d7-489e-8e81-daa80010ea85.png)


### 3.4. I am Root
---
```bash

```


```bash

```


```bash

```


```bash

```
