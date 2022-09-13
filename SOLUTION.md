`Error1 : `  adservice imagepullbackerror <br />
`Solution1: ` Open adservice file and change image version from anyone from https://console.cloud.google.com/gcr/images/google-samples/GLOBAL/microservices-demo/adservice?tag=v0.3.1 and redeploy this file and after pod running successfully.

`Error2: ` cartservice pod in crashoffimage status <br />
`Solution2: ` As check log of cartservice pod depended on redis pod. So need to start redis pod first.

`Error3: ` redis-cart pod in pending state <br />
`Solution3: ` Need to change NodeSelector to qa-cluster-worker and deploy.
