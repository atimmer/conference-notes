# Continuous Integration at a Distribution Level

Shepherding 30K Ubuntu packages to never break

Martin Pitt


It takes 2 day to complete the test suite of the unity package for Ubuntu.

They used Jenkins at first but switched to a micro-services architecture. They start with a proposed-migration, it get's handled using an AMQP server with RabbitMQ. Workers take out of the Queue and execute the tests. Then they put the logs and artifacts in a Swift object store. Then they can read these in a result browser.