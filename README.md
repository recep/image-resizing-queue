# RabbitMQ Example-GO
This repo is an example of an image resize queue. Resizes all photos to 500x500.  
### Set up a RabbitMQ instance with Docker  
```
docker run -it --rm --name rabbitmq -p 5672:5672 -p 15672:15672 rabbitmq:3-management
```
### RUN  
```
go run ./producer/main.go
```
```
go run ./consumer/main.go
```
**Side of Producer**  
![gproject-1](https://user-images.githubusercontent.com/10357501/103801815-4e421180-505f-11eb-8724-8ba7950be884.png)  
**Side of Consumer**  
![gproject-2](https://user-images.githubusercontent.com/10357501/103801958-7e89b000-505f-11eb-8bec-ec2029a98229.png)  
**After Resizing**  
You can see them in new images folder
```
├── consumer
│   ├── main.go
│   └── new-images
│       ├── 15582.png
│       ├── 25850.png
│       └── 88566.png
├── go.mod
├── go.sum
├── producer
│   ├── main.go
│   └── test-images
│       ├── go2.png
│       ├── go3.png
│       └── go4.png
└── README.md
```

