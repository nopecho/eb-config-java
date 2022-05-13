

## eb 환경 구

프로젝트 루트에서 아래 명령어를 실행한다.
```
$ ./eb.sh
```

아래 명령어를 실행한다.
```
$ ./docker-eb.sh
```

AWS 키를 입력한다.
```
$ (access_key) : 
$ (secret_key) :
```

신규 애플리케이션을 생성 할지 기존 애플리케이션을 사용할지 숫자를 입력한다
```
Select an application to use
4) discovery
5) configuration
6) tptp
7) user-new-prod
8) signup
9) user-signup
10) user-signup-prod
11) login
12) iamport
13) toss
14) point
15) refund
16) notifier
17) bot
.
.
.
${x}) [ Create new Application ]
(default is ${x} ): 
```

aws 코드 커밋을 사용할건지 묻는다. N 을 입력한다.
```
Do you wish to continue with CodeCommit? (Y/n): 
```

환경 명을 입력한다.
```
Enter Environment Name
(default is xxx-dev) : 
```

DNS의 CNAME을 입력한다.
```
Enter DNS CNAME prefix
(default is xxx-dev): 
```

해당 EB의 로드 밸런서를 선택한다.
```
Select a load balancer type
1) classic
2) application
3) network
(default is 2): 
```

공유 로드밸런서를 사용할지 묻는다. n 을 입력한다.
```
Your account has one or more sharable load balancers. Would you like your new environment to use a shared load balancer? (y/N): 
```

EC2 스팟 환경을 사용하는지 묻는다. n 을 입력한다. 
```
Would you like to enable Spot Fleet requests for this environment? (y/N): 
```

기다리면 .extensions 폴더와 .elasticbeanstalk 폴더에 있는 config 파일을 바탕으로 eb 애플리케이션과 배포 환경이 구성된다.


---

## 개선점

- 쉘 스크립트를 통해 eb 애플리케이션 이름 설정과 환경 이름 설정을 제외한 모든 작업을 자동화 한다.
  - 대화식 쉘에 입력값을 어떻게 전달 할것인가?

  - 이름 설정도 지정된 네이밍 규칙으로 자동화?
- aws iam key를 외부화 한다.
	- 도커 내부에 환경변수를 어떻게 전달 할것인가?

[ElasticBeanstalk Docs](https://docs.aws.amazon.com/ko_kr/elasticbeanstalk/latest/dg/command-options-general.html)
