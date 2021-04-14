# MouseV0.1
move mouse with emulator first test

Steps for configuration
- sudo ./setup.sh (install libraries requeried)
- sudo reboot
- sudo ./updateMac.sh 
- sudo ./updateName.sh + <assign name for view bluetooth>
- cd MouseV0.1/server

CREATE SCREEN FOR THIS STEP THEN CONTINUE WITH 
- sudo ./btk_server.py (connect your device by bluetooth)

- cd MouseV0.1/mouse

- sudo ./mouse_emulate.py <ADD COORDINATES IN FORMAT OF 0 0 0 0>

Example:

"Usage: mouse_emulate [button_num dx dy dz]"

aqui ya va todo en español xD

[0 0 0 0]

El primer valor sera el boton a presionar del mouse, en este caso solo posee 3 botones
el mouse normal, clic izquierdo corresponde al valor 1 ,clic o scroll corresponde al valor 2 y el tercer clic que es el derecho corresponde al valor 3.


El segundo valor corresponde al movimiento en DX del mouse o en x que va de 0 a 256 bits, este se divide en dos:
de 0 a 127 el puntero se movera hacia la derecha
de 128 a 255 se movera hacia la izquierda

tener en cuenta que para mover a la izquierda 128 es el valor maximo a mover y 255 es igual a mover 1 bit 


El tercer valor corresponde a DY o y, se divide en dos:
de 0 a 127 va para abajo
de 128 a 255 va para arriba 

de igual manera tener en cuenta que para mover a la izquierda 128 es el valor maximo a mover y 255 es igual a mover 1 bit 

Ejemplos :

- sudo ./mouse_emulate.py 0 0 0 0 "no va hacer nada"
- sudo ./mouse_emulate.py 2 0 0 0 "mostrara el puntero en el medio de la pantalla"
(siempre la primera conexion sera en el centro de la pantalla, luego si se mueve , su nuevo punto cero sera el ultimo movimiento)
- sudo ./mouse_emulate.py 1 0 0 0 "clicleara en donde este el puntero"


EJEMPLO , HACIENDO UN CUADRO

- sudo ./mouse_emulate.py 0 0 0 0 "Activar/Desactivar"
- sudo ./mouse_emulate.py 2 0 0 0 "Ubicar puntero"
- sudo ./mouse_emulate.py 1 0 0 0 "hacer clic inicial"
- sudo ./mouse_emulate.py 1 127 0 0 "mantener clic + mover puntero hacia la derecha"
- sudo ./mouse_emulate.py 1 0 127 0 "mantener clic + mover puntero hacia abajo"
- sudo ./mouse_emulate.py 1 128 0 0 "mantener clic + mover puntero hacia la izquierda"
- sudo ./mouse_emulate.py 1 0 128 0 "mantener clic + mover puntero hacia la arriba"
- sudo ./mouse_emulate.py 0 0 0 0 "Desactivar/Activar"
- sudo ./mouse_emulate.py 0 128 0 0 "solamente mover hacia la izquierda"
- sudo ./mouse_emulate.py 2 0 0 0 "ubicar puntero"


copiar y pegar en terminal para hacer que se ejecute de un ave

sudo ./mouse_emulate.py 0 0 0 0
sudo ./mouse_emulate.py 2 0 0 0 
sudo ./mouse_emulate.py 1 0 0 0
sudo ./mouse_emulate.py 1 127 0 0
sudo ./mouse_emulate.py 1 0 127 0 
sudo ./mouse_emulate.py 1 128 0 0
sudo ./mouse_emulate.py 1 0 128 0
sudo ./mouse_emulate.py 0 0 0 0 
sudo ./mouse_emulate.py 0 128 0 0 
sudo ./mouse_emulate.py 2 0 0 0
sudo ./mouse_emulate.py 0 0 0 0



