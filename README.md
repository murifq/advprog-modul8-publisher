# How many data your publisher program will send to the message broker in one run?  
_Publisher_ akan mengirimkan 5 data dalam sekali _run_. 

# The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean? 
Artinya kedua program tersebut akan saling terkoneksi degan amqp yang sama. Sehingga, _publisher_ dan _subscriber_ bisa saling berkomunikasi.

# Runnign RabbitMQ as Message Broker
![img.png](images/RunningRabbitMQAsMssgBroker.png)

# Sending and Processing Event
![img.png](images/SendingAndProcessingEvent.png)
Daoat dilihat bahwa terjadi proses pengiriman data dari _publisher_ kepada _subscriber_ melalui _message broker_ RabbitMQ.

# Monitoring chart based on publisher.
![img.png](images/MonitoringChart.png)
Sebelumnya, saya jalankan `cargo run` pada Publisher sekali saja. Hanya terdapat satu puncak saja pada _message rates_. Lalu saya coba jalankan `cargo run` kedua kali pada Publisher, maka akan terdapat 2 puncak pada _message rates_. Maka dapat dilihat bahwa _message rates_ meningkat ketika dijalankan `cargo run` pada Publisher. Cara kerjanya adalah Publisher akan mengirimkan data kepada RabbitMQ, lalu RabbitMQ akan mengirimkan data kepada Subscriber.