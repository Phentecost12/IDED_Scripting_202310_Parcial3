# IDED_Scripting_202310_Parcial3
 
Para la realizacion de esta entrega se realizaron varios cambios importantes: 

1). Se implemento el singleton en donde se pidio (Game Controller, Player Controllar, UI y Obstacle Spawner)

2). Para la implementacion del patron de observador, no se realizo una implementacion de interfaces y herencias donde se registran los observadores y el sujeto los actualiza cuando se realiza cierta accion, en cambio, se utilizo el sistema de acciones (Actions<>) que trae implementada el lenguaje de C#. Se decidio utilizarla ya que es una forma mas simple y limpia de implementar este patron y en su defecto se aplica el mismo concepto de registrar y de-registrar eventos/acciones. A parte se es mas organizado a la hora de interconectar todos los eventos para que funcionen de manera adecuada sin la necesidad de algun manager que controle los eventos.  

3). Para los pools se modifico la interfaz Ipool eliminando la implementacion destinada para la reintegracion de los elementos al pool. Se decidio implementar un pool que trabaje con el estado de los objetos, mas especificamente, si estan activos o no. A su vez, a estos se les implemento un c# y una interfaz. La parte mas importante es la interfaz ya que no solo posee las firmas para el reciclado del objeto sino que tambien le dan autonomia y lo desligan del pool mientras esta haciendo lo que tiene que hacer. Se decidio usar esta implementacion por ese mismo motivo y por que al usar un pool que en cierto modo nunca reincorpora por cuenta propia los elementos, se requiere una funcion externa que si lo haga, implementar un evento que sea llamado por el pool es inecesario sabiendo que el objeto solito puede reincorporarse al pool mediante su desactivacion. 

4). En el segundo enunciado se interpreto que lo pedido era interconectar las firmas ya implementadas en las clases que nos dio, de otro modo, no tiene sentido crear una nueva firma que no haga nada pero que se llame cada vez que suceda algo. 

5). Se presenta un pequeño bug a la hora de reiniciar el nivel, cuando vuelve a cargar la escena deja de funcionar la UI, especificamente la parte que muestra el tipo de municion que se tiene equipado, no cambia. El editor salta un error de Null Reference pero las referencias si esta. Ya que es un bug externo a la implementacion realizada y que no es algo critico para la ejecucion del programa, no se soluciono, en otra palabras, eso se daño solo, yo no toque eso. 

