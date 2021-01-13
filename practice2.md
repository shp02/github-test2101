# [2일차] VMware에 우분투 설치 및 이더리움 설치

## 1. VMware 설치
VMware workstation 16 player 설치

## 2. 우분투 가상머신 생성

## 3. 이더리움 설치 및 프라이빗 네트워크 연결
* 이더리움 설치
```
$ sudo apt-get install software-properties-common
$ sudo add-apt-repository -y ppa:ethereum/ethereum
$ sudo apt-get update
$ sudo apt-get install ethereum
```
* 최초 블럭생성 설정파일 생성
<!--image-->
![설정파일](https://user-images.githubusercontent.com/77226745/104475658-b31ede00-5602-11eb-83a7-76bbaa0c166d.PNG)
#### - 오류발생
 ```
 Fatal: Failed to write genesis block: unsupported fork ordering: eip150Block not enabled, but eip155Block enabled at 0
 ```
#### - 오류해결(eip150Block 추가)
![설정파일 변경](https://user-images.githubusercontent.com/77226745/104475695-c0d46380-5602-11eb-8cd3-4cc7cc16927c.PNG)
* 프라이빗 네트워크 연결
<!--image-->
![네트워크연결](https://user-images.githubusercontent.com/77226745/104475722-c631ae00-5602-11eb-9d47-16e1b29c8dfa.PNG)

## 4. 기타
* 오류 github에 업로드 오류
#### - branch명이 master에서 main으로 변경되었는데 인지하지 못함
```
git pull origin main
git push origin main
```
