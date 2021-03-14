


Then add/commit/push to gitlab

```

```
git commit -m "Put some message about this push here"
```

## Push your changes to gitlab, and merge to dev branch
```
git push --set-upstream origin feature/[Your branch name]
```

### Validate your changes have been triggered by gitlab-ci in
[propitix-scm] (https://gitlab.com/propitix/microservices/frontend-propitix)

### Check the image have been pushed to
[Google Container Registry] (https://console.cloud.google.com/gcr/images/non-prod-pdz/EU/frontend-propitix?project=non-prod-pdz&authuser=1&gcrImageListsize=30) (Depending on the environment. Either non-prod or prod)

## pulling the image
```
docker pull eu.gcr.io/$environment/frontend-propitix:$tag-version
```

## Running (You can do this step without the pulling the above as it will put down if not found locally)
To run the container:
```
$ docker run -d eu.gcr.io/$environment/frontend-propitix:$tag-version
```

Default web root:
```
/usr/share/nginx/html
```

## If you require permissions to GCP, or Gitlab resources, please talk to dare@propitix.com
