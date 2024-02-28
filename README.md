# Passos para instalacao do kong

## Instalando Kong via Helm
```shell
helm repo add kong https://charts.konghq.com
helm repo update
helm install kong/ingress --generate-name
```

## Checando PODs da instalacao do kong
```shell
kubectl get pods
```
![pods](/assets/pods.png)

## Checando SVC da instalacao do kong
```shell
kubectl get svc
```
![svcs](/assets/svcs.png)

## Instalacao do httpbin
```shell
kubectl apply -f ingress.yaml
```

### Testando o httpbin
```shell
curl http://<IP>/headers

```
![curl](/assets/curl.png)
