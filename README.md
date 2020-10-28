# todo-manifest

Using argoCD to speed up git operation

Using master branch for staging development
```
argocd app create todo-app-stage \
--repo <repo-url> \
--path "." \
--dest-server https://kubernetes.default.svc \
--revision master \
--dest-namespace todo-app-stage
```

Using prod branch for production development
```
argocd app create todo-app-prod \
--repo https://<repo-url> \
--path "." \
--dest-server https://kubernetes.default.svc \
--revision prod \
--dest-namespace todo-app-prod
```