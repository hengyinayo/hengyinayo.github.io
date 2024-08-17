---
layout: single
title: "InfluxDB + Grafana를 EC2 Instance 위에서 연동하기"
categories: [TSDB]
tag: [InfluxDB]
toc: true
---

# 1. InfluxDB 환경 설정

## 1-0. InfluxDB 설치
아래 링크를 따라서, 자신의 환경에 맞는 버전을 다운받으면 된다:  
[InfluxDB Documentation](https://docs.influxdata.com/influxdb/v2/install/)


## 1-1. Service with systemd

1. InfluxDB 시작 -   
    - Systemd로 설치 했을 경우:  
    `sudo service influxdb start`   
    `influxd` 

    - Binary로 설치 했을 경우:  
    `./influxdb2-2.7.8/usr/bin/influxd`


2. InfluxDB 서버 환경 체크 \
    `sudo service influxdb status`


# 2. AWS 포트 열어주기

1. EC2를 생성해준다

2. 보안 설정에서 아래 이미지처럼 설정을 해주어, 포트 8086을 열어준다.
![](/assets/images/InfluxDB/1.png)

3. `<퍼블릭 IPv4 주소>:8086`에 접속하면 InfluxDB 자체에서 제공하는 UI에 접속하는 것을 볼 수 있다.

> 추가 -  
> [탄력적 IP주소](/aws/탄력적-IP-주소/)


## 2-1. Grafana 설치

1. 아래 링크를 따라서 Grafana oss 버전을 설치해주자.  
[Grafana 설치](https://grafana.com/grafana/download)

2. 

Reference: \
[InfluxDB Documentation](https://docs.influxdata.com/influxdb/v2/install/)  
[Grafana Dicumentation](https://grafana.com/grafana/download)