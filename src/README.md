# Introduction
Making leds blink 

# Wiring

![traffic light](doc/img/scheme.png)

|flame sensor      |  Raspberry Pi  |
|------------------|----------------|
| Ground 		   | GND            |
| Vcc / + 		   | 5V             |
| DO 			   | GPIO 21        |

# How to build

Compile flame.go like this
```
go get github.com/stianeikeland/go-rpio
env GOOS=linux GOARCH=arm GOARM=6 go build flame.go
```
Copy the generated file to your Raspberry Pi device and execute it with this command

```
env RED_PIN=12 YELLOW_PIN=13 GREEN_PIN=18 ./flame
```

Happy blinking 