[GitHub Submodule](https://git-scm.com/book/ko/v2/Git-%EB%8F%84%EA%B5%AC-%EC%84%9C%EB%B8%8C%EB%AA%A8%EB%93%88)을 활용해 민감한 정보를 관리합니다.

빌드, 배포를 같은 환경에서 진행한다면, GitHub Actions의 [Checkout@v4](https://github.com/actions/checkout/tree/v4)를 활용할 수 있습니다. `submodule` 옵션을 확인하세요.

빌드 환경과 배포 환경을 분리하고자 한다면, 빌드를 외부 환경에서 진행한 뒤, 배포 환경에서 submodule 정보만을 가져와 아래 명령어를 통해 설정 정보를 주입할 수 있습니다. 빌드 환경에서 submodule 정보를 가져와 노출되지 않도록 주의하세요.

`java -jar {jar location} --spring.config.location=secret/application-prod.yml` (base directory: `submodule-example`)

---

useful commands
```git
git submodule add {repository} {directory}
git submodule update --remote
git push --recurse-submodules=check
git push --recurse-submodules=on-demand
```
