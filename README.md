[GitHub Submodule](https://git-scm.com/book/ko/v2/Git-%EB%8F%84%EA%B5%AC-%EC%84%9C%EB%B8%8C%EB%AA%A8%EB%93%88)을 활용해 민감한 정보를 관리합니다

사용 시에는 GitHub Actions의 [Checkout@v4](https://github.com/actions/checkout/tree/v4)를 확인하고, `submodule` 옵션을 통해 내부 비밀 정보를 가져옵니다.

`java -jar {jar location} --spring.config.location=secret/application-prod.yml` (base directory: `submodule-example`)

Spring Boot을 빌드한 뒤, 위 명령어를 통해 외부 파일을 설정 파일로 지정할 수도 있습니다.

---

useful commands
```git
git submodule add {repository} {directory}
git submodule update --remote
git push --recurse-submodules=check
git push --recurse-submodules=on-demand
```
