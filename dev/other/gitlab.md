# gitlab

## gitlab-ci

### Gitlab -> AWSの認証 (+ EKSのk8sまでの認証）

AWS Security Token Serviceで、一時的に認証情報を取得 (Gitlabアクセス用のロール)

kubectl 用のcontext取得できたら 後はjob作るのは可能

before_scriptに載せるでも、別のJobにするでも、対象のJobで一度きりでも、なんでもOK

参考: https://docs.gitlab.com/ee/ci/cloud_services/aws/
参考: https://oblcc.com/blog/configure-openid-connect-for-gitlab-and-aws/
参考: https://docs.gitlab.com/ee/user/clusters/agent/ci_cd_workflow.html


