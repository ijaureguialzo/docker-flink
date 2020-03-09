[Panel de control](http://localhost:8081)

```

docker-compose up -d

docker run -it --rm --network=flink_demonet --name=ncs subfuzion/netcat -vl 9000

docker cp flink_jobmanager_1:/opt/flink/examples/streaming/SocketWindowWordCount.jar .

flink run SocketWindowWordCount.jar 

--hostname ncs --port 9000

docker-compose logs -f taskmanager


docker-compose exec jobmanager /bin/bash

```
