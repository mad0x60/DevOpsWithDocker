# Exercise 1.3: Secret message
>Now that we've warmed up it's time to get inside a container while it's running!
>Image devopsdockeruh/simple-web-service:ubuntu will start a container that outputs logs into a file. Go inside the >container and use tail -f ./text.log to follow the logs. Every 10 seconds the clock will send you a "secret message".
>Submit the secret message and command(s) given as your answer.

```
$ docker run -d --name secret_msg devopsdockeruh/simple-web-service:ubuntu 
$ docker exec -it secret_msg bash
root@f1d5cb3f1628:/usr/src/app# tail -f /usr/src/app/text.log 
2022-03-29 12:18:55 +0000 UTC
2022-03-29 12:18:57 +0000 UTC
Secret message is: 'You can find the source code here: https://github.com/docker-hy'
```

**Secret message is: 'You can find the source code here: https://github.com/docker-hy'**