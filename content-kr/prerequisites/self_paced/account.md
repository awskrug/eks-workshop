---
title: "AWS 계정 만들기"
chapter: false
weight: 1
---

{{% notice warning %}}
실습을 진행할 계정은 새 IAM 역할을 만들고 다른 IAM 권한을 지정할 권한이 있어야합니다.
{{% /notice %}}

1. 관리자 접근 권한을 가진 AWS 계정이 없다면 : [지금 여기를 클릭해서 계정을 만드세요.](https://aws.amazon.com/getting-started/)

1. AWS 계정이 있다면, AWS 계정에 대해 관리자 접근 권한을 가진 IAM 사용자로 다음의 단계를 확인하세요 : 
[워크샵에서 사용하기 위한 새로운 IAM 사용자 만들기](https://console.aws.amazon.com/iam/home?#/users$new)

1. 사용자 정보를 입력하세요 :
![Create User](/images/iam-1-create-user.png)

1. 관리자 접근 IAM 권한을 부여합니다 :
![Attach Policy](/images/iam-2-attach-policy.png)

1. `Create user` 버튼을 클릭하여 IAM 유저를 생성합니다 :
![Confirm User](/images/iam-3-create-user.png)

1. 로그인 URL을 저장 또는 메모해두세요 :
![Login URL](/images/iam-4-save-url.png)
