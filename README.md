# ETP.MSR
Интеграционная шина МСР


    cd move-queue
    mvn celan install
    .../servicemix/client
    feature:install activemq-web-console

список слушателей:
- очередь queue1 в http://localhost:8181/activemqweb/queues.jsp
- REST POST http://localhost:8080/queue1
- файлы /tmp/queue_in/*

лог в .../servicemix/data/log/servicemix.log

по умолчанию xml запрос из слушателя перекладывается в queue.default
 
пример тела для роутинга в queue.test:

    <test/>
