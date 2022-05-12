
### elastic beanstalk 배포 환경 설정 레포.

배포 환경 구축시

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

N 을 입력한다.
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
