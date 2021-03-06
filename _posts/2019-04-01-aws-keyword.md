---
title: "AWS 기본 단어 정리"
date: 2019-04-01 22:10:30 +0000
categories: aws
---
AWS를 배우면서 기본적으로 알아둬야 할 단어들을 정리해두는 포스트.

AWS : Amazon Web Services. Xen 가상화 기술을 이용하여 아마존에서 제공하는 IT 인프라 서비스.

IDC

HVM : 하드웨어 가상화

Full Virtualization : 전가상화. CPU 차원에서 지원하는 가상화 기술. 게스트 운영체제 수정없이 바로 실행할 수 있다.

Paravirtualization : 반가상화. Xen이라는 소프트웨어 하이퍼바이저 기술을 사용한 가상화. 전가상화보다 훨씬 빠르며 호스트와 거의 동일한 성능을 낸다. OS(커널)을 수정해야 하므로 Linux같은 오픈소스를 사용한다.

Region : 리전. AWS의 모든 서비스가 위치하고 있는 물리적인 장소.

AZ : Availability Zone. 가용 영역. 리전안에 설치 되어 있는 데이터센터(IDC)들을 말한다.

Availability : 가용성. 서버, 네트워크, 프로그램 등이 정상적으로 사용가능한지 나타내는 정도. 비슷한 의미로 가동률이 있다.

EC2 : Elastic Compute Cloud. AWS에서 가장 기본적으로 널리 쓰이는 인프라로 인터넷에 연결된 가상서버를 제공하는 서비스이다.

EBS : Elastic Block Store. EC2 인스턴스에 장착하여 사용할 수 있는 가상 저장 장치.

Security Group : EC2 인스턴스에 적용하는 방화벽 설정.

Elastic IP : EC2 인스턴스에 제공하는 고정된 공인 IP.

AMI : Amazon Machine Images. EC2 인스턴스를 생성할때 쓰이는 기본 파일.

CloudWatch : AWS의 리소스 상태를 모니터링 하는 서비스.

S3 : Simple Storage Service. HTTP 프로토콜로 작동하는 인터넷 스토리지 서비스.

CloudFront : AWS에서 제공하는 CDN 서비스.

CDN : Content Delivery Network. 오리진을 대신하여 엔드유저의 요청에 가까운 물리적 위치 및 네트워크에서 응답하여 서버의 트래픽 부하와 응답속도를 개선하는 서비스.

RDS

DynamoDB

ElastiCache

IAM

Route 53

ELB

Auto Scaling

VPC

Glacier

CloudFormation

Elastic Beanstalk

OpsWorks

CloudSearch

SNS

SES

SQS
