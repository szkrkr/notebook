# gitlab

## gitlab-ci

### Gitlab -> AWSの認証 (+ EKSのk8sまでの認証）

AWS Security Token Serviceで、一時的に認証情報を取得 (Gitlabアクセス用のロール)

kubectl 用のcontext取得できたら 後はjob作るのは可能

before_scriptに載せるでも、別のJobにするでも、対象のJobで一度きりでも、なんでもOK

参考: https://docs.gitlab.com/ee/ci/cloud_services/aws/
参考: https://oblcc.com/blog/configure-openid-connect-for-gitlab-and-aws/
参考: https://docs.gitlab.com/ee/user/clusters/agent/ci_cd_workflow.html


### multiline

https://gitlab.com/gitlab-org/gitlab-runner/-/issues/166

```
> mark will combine all to one. You can't have the multi lines scripts.
| can't identify the black slash and split everything. You can't write a command in multi-line.
- without other decorate, well, it hard to match both YAML format and Shell script syntax.
```


- sample 
```
- > command
  --option xxx
```
->
```
command --option xxx
```

