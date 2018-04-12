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

Хост для REST задается через параметр rest.hos

Файл забирается или с FTP, доступ к которому настаивается через параметры ftp.url, ftp.user, ftp.password, или с локальной папки, задаваемой параметром file.url

XSD для валидации задается через параметр validator.url, XSD для примера с валидацией move.queue/examples/test.xsd

move.queue/examples/1.xml - xml, который проходит валидацию по xsd и xpath и уходит в queue.test
move.queue/examples/2.xml - xml, который проходит валидацию по xsd, но не проходит по xpath и уходит в queue.default
move.queue/examples/3.xml - xml, который не проходит валидацию по xsd, соответственно выбрасывается Exception, Exception обрабатывается в блоке <onException> и уходит в queue1.bk