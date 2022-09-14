`Error1 : `  adservice imagepullbackerror <br />
`Solution1: ` Open adservice file and change image version from anyone from https://console.cloud.google.com/gcr/images/google-samples/GLOBAL/microservices-demo/adservice?tag=v0.3.1 and redeploy this file and after pod running successfully.

`Error2: ` cartservice pod in crashoffimage status <br />
`Solution2: ` As check log of cartservice pod depended on redis pod. So need to start redis pod first.

`Error3: ` redis-cart pod in pending state <br />
`Solution3: ` Need to change NodeSelector to qa-cluster-worker and deploy.

<b>Assignment- Part-C</b> <br />

`Error4: ` UI getting 500 Error <br />
`Solution4: ` check log and find frontend going to connect with wrong port of currencyservice. So Go to frontend file and change env currencyservice port from 8000 to 7000

`Error5: ` Click on any product getting 500 error <br />
`Solution5: ` As checked replicaset of recommendationservice it use undefine service account. So change with default SA.

`Error6: ` When we click on place Order it will give 500 error <br />
`Solution6: ` As describe checkoutservice service can not find any endpoint. So check checkoutservice file and found selector name change from <b>check-outservice</b> to <b> checkoutservice. </b>

`Error7: ` After resolve checkout service getting same 500 error on paymentservice. <br />
`Solution7: ` For that we need to open paymentservice file and change target port from 50052 to 50051.

`Error8: ` In loadgeneration pod we are getting failed all request. <br />
`Solution8: ` As this single pod on different namespace that's why it don't communicate with other service. So Need to comment or change namespace in loadgenerator from qa to default.
