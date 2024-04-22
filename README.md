# How many data your publisher program will send to the message broker in one run?  
_Publisher_ akan mengirimkan 5 data dalam sekali _run_. 

# The url of: “amqp://guest:guest@localhost:5672” is the same as in the subscriber program, what does it mean? 
Artinya kedua program tersebut akan saling terkoneksi degan amqp yang sama. Sehingga, _publisher_ dan _subscriber_ bisa saling berkomunikasi.