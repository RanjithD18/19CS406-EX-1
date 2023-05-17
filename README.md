# 19CS406-EX-1 STUDY OF SOCKET PROGRAMMING WITH CLIENT-SERVER MODEL

DATE :

AIM :


ALGORITHM :




PROGRAM :
Client:
~~~
import socket
s=socket.socket()
s.bind(('localhost',8080))
s.listen(5)
c,addr=s.accept()
while True:
	i=input("ENter a data:")
	c.send(i.encode())
	ack=c.recv(1024).decode()
	if ack:
		print(ack)
		continue
	else:
		c.close()
		break
~~~
Server:
~~~
import socket
s=socket.socket()
s.connect(('localhost',8080))
while True:
	print(s.recv(1024).decode())
	s.send("Recieved".encode())
~~~
OUTPUT:
![](https://github.com/RanjithD18/19CS406-EX-1/blob/main/Screenshot%20from%202023-05-17%2021-07-00.png)



RESULT:

