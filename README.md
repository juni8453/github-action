#### Deploy 실패
- dial tcp 3.39.195.248:22: i/o timeout 에러 발생
- 시도) AWS_HOST_DNS 가 잘못된 것 같아서 다시 수정
- 결과) 배포 성공 !

- EC2 인스턴스를 새로 생성했는데 docker 를 깜빡하고 설치하지 않았음
- 시도) AWS EC2 인스턴스에 다시 docker 설정
- 결과) 배포 성공 !

- yml 파일 분리 (실패)
- 최근까지 사용하던 파일 설정하는 방법은 dedicated 되었음.
- 새로운 방법으로 설정파일 설정 완료
- 로컬 개발환경에서는 dev 파일을 사용한다.
- 배포 환경에서는 deploy 파일을 사용한다.
  - 이떄 ENV, ENTRYPOINT 를 사용해 환경변수를 셋팅한다.

- non-JS module files deprecated. 에러 발생
- 왜 에러가 발생한지 잘 모르겠다. 