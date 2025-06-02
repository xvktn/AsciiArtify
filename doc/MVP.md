# MVP: AsciiArtify CI/CD via ArgoCD

## Репозиторій
https://github.com/xvktn/go-demo-app

## Мета
Показати синхронізацію між Git-репозиторієм і Kubernetes-кластером за допомогою ArgoCD.

## Ключові етапи
1. ArgoCD налаштовано на моніторинг репозиторію `go-demo-app`.
2. При зміні файлу `values.yaml` в Helm-чарті застовується тип сервісу `LoadBalancer`.
3. Сервіс доступний через зовнішній IP.
4. Здійснено curl POST з зображенням — бекенд відповідає ASCII-артом.

## Демонстрація
https://www.youtube.com/watch?v=li1ozyyIP6c
