
https://git-scm.com/book/ko/v2/Git-%EB%8F%84%EA%B5%AC-%EC%84%9C%EB%B8%8C%EB%AA%A8%EB%93%88

`git submodule add {repository} {directory}`

`git submodule update --remote`

`git push --recurse-submodules=check` : submodule 변경사항이 없는지 확인 및 push

`git push --recurse-submodules=on-demand` : submodule 변경사항이 있으면 함께 push

`java -jar {jar location} --spring.config.location=secret/application-prod.yml` (base directory: `submodule-example`)
