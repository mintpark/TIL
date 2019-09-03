## SSH key 등록
비밀번호 없이 git push 하려면, 해당 repository에 내 pc의 public key를 등록해야 한다. 이때
1. 내 pc에 public key가 있나?
2. 어떻게 등록하나?

이 두 가지를 확인하고 실행하려면
1. ~/.ssh 디렉토리에서 id_rsa, id_rsa.pub가 있는지 확인한다.

1.1 없다면 생성한다.
```github
$ ssh-keygen
# github 공홈에서는 옵션이 많이 붙지만 우선 이걸로 충분한 것 같다.
```

2. push 할 repository > Settings > Deploy keys 에 add new key 한다.
```github
$ cat id_rsa
# 결과물을 복사해서 'Allow write access'에 체크한 뒤 키를 추가하면 된다.
# key를 다른 이름으로 생성했더라도, repository에 추가할 때는 id_rsa라는 prefix로 추가해줘야 한다.
```
### git tag
특정 commit을 기억하고 싶을 때(릴리즈 버전 기록, 코드 복구...) 사용.
태그는 따로 푸시해야 리모트에 저장된다 : git push --tags 
