# 2019-tfg-natalia-monforte
### Week 1
I've dedicated this first week to familiarize myself with JavaScript. I've followed the tutorial provided by this [webpage] to learn the language and I've made the examples proposed by the [webpage].

[webpage]: http://w3schools.com

Besides, I've started working with Kibotics. Especially, I've focused on the Pibot follows-lines. The aim of this exercise is to achive the Pibot follows a black line. In order to do this, the results obtained by the infrared sensors of the robot will be analysed to know where is the black line.

<img width="357" alt="sigue_lineas" src="https://user-images.githubusercontent.com/52928749/64567522-bc39d400-d358-11e9-83c1-490c9455182f.PNG">

The following values are obtained from the reading of the infrared sensors:
<img width="407" alt="IR_pibot" src="https://user-images.githubusercontent.com/52928749/64567526-bcd26a80-d358-11e9-97fa-884aa32283bc.PNG">

Using the following functions you must achieve the purpose of the exercise:
<img width="456" alt="funciones_pibot" src="https://user-images.githubusercontent.com/52928749/64567525-bcd26a80-d358-11e9-9a69-45a9b4004d70.PNG">
<img width="455" alt="funcion_parar_pibot" src="https://user-images.githubusercontent.com/52928749/64567524-bc39d400-d358-11e9-925c-455a1a8cfc75.PNG">

Finally, this is my code to solve the exercise:
```
from pibot.pibot 
import PiBot
import time

if __name__ == "__main__":

    robot = PiBot()   
    robot.quienSoy() 
    while True:
        ir = robot.leerIRSigueLineas()
       
        if ir == 0:
            robot.avanzar(0.1)
            time.sleep(0.01)
            robot.parar()
        elif ir == 1:
            robot.girarIzquierda(0.4)
            time.sleep(0.01)
            robot.parar()
        elif ir == 2:
            robot.girarDerecha(0.4)
            time.sleep(0.01)
            robot.parar()
        else:
            robot.retroceder(0.1)
            time.sleep(0.01)
            robot.parar()
 ```

