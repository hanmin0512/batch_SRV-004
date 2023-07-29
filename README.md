# batch_SRV-004
## [SRV-004]
- 불필요한 SMTP 서비스 실행 검사


## 취약점 검사 실험 및 실험환경
- OS : Windows Server 2016
- batch file
- service : SMTP

## 기준 
- 불필요한 SMTP서비스가 비활성화되어 있는 경우 양호 

## 배치파일 로직
- net start 로 불필요한 서비스 구동중인지 확인
- 확인 목록 IIS Admin, World Wide Web, Simple Mail Transfer Protocol, SMTP 등 ...

## 검사 결과
- ![0](https://github.com/hanmin0512/batch_SRV-004/assets/37041208/9fd3dcb1-ddec-4390-bf94-c47f09a85885)

## 대응 방안 (사용하지 않은 서비스 중단)
- services SMTP
- ![1](https://github.com/hanmin0512/batch_SRV-004/assets/37041208/1ca74a05-bd57-4680-bc9d-faf371951c12)

- services IIS Admin
- ![2](https://github.com/hanmin0512/batch_SRV-004/assets/37041208/7bac48b5-e31b-4266-bc6c-910c1c0ed1dd)

- services World Wide Web
- ![3](https://github.com/hanmin0512/batch_SRV-004/assets/37041208/85016264-a6af-4b1f-9370-e2e3ba270ac9)

## 대응 후 검사 결과
- ![4](https://github.com/hanmin0512/batch_SRV-004/assets/37041208/40ba1c06-a823-41a8-b5d9-4234afad21da)

