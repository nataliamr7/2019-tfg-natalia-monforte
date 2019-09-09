# 2019-tfg-natalia-monforte
### Week 1
I've dedicated this first week to familiarize myself with JavaScript. I've followed the tutorial provided by this [webpage] to learn the language and I've made the examples proposed by the [webpage].

[webpage]: http://w3schools.com

Besides, I've started working with Kibotics. Especially, I've focused on the Pibot follows-lines. The aim of this exercise is to achive the Pibot follows a black line. In order to do this, the results obtained by the infrared sensors of the robot will be analysed to know where is the black line.

The following values are obtained from the reading of the infrared sensors:




Using the following functions you must achieve the purpose of the exercise:




Finally, this is my code to solve the exercise:

from pibot.pibot import PiBot
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



