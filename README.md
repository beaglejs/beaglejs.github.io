BeagleJS Website
================

개발환경에서 도커를 통하여 확인하는 방법

```sh
docker run -itd --rm -v .\docs:/usr/share/nginx/html -p 8080:80 --name beaglejs nginx
```
