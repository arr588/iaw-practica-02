# iaw-practica-02

## Implantación de una aplicación web LAMP en Amazon Web Services (AWS)

1. Le damos a lanzar instancias y seleccionamos la última version de Ubuntu Server. Las opciones de procesador, detalles de la instancia y espacio de disco las dejamos por defecto:

    ![](https://raw.githubusercontent.com/arr588/iaw-practica-02/main/img/1.png?token=ALTEBMQ7TWJAQBFV7AIKJYS7WPEII)

2. Abrimos los puertos SSH, HTTP y HTTPS:

    ![](https://raw.githubusercontent.com/arr588/iaw-practica-02/main/img/2.png?token=ALTEBMQ2ANT5Y4ZUBYJU5WK7U3CBQ)

3. Generamos una clave de acceso. En mi caso al haber creado otra máquina ya tengo una generada que voy a usar ya que es para la misma práctica por comodidad:

    ![](https://raw.githubusercontent.com/arr588/iaw-practica-02/main/img/3.png?token=ALTEBMVSKDAHNXXHFFHZHXS7U3CIQ)

4. Para gestionar las instancias vamos a usar Visual Studio Code con la extensión de Remote-SSH:

    ![](https://raw.githubusercontent.com/arr588/iaw-practica-02/main/img/4.png?token=ALTEBMVINME634R3B5NXYIS7U3CO4)

5. Modificamos el archivo de configuración de la extensión para poder conectarnos a la instancia con los datos de la misma:

    ```
    Host prac02
        HostName 34.227.65.211
        User ubuntu
        IdentityFile "C:\Users\djale\Desktop\Claves\clave_prac01.pem"
    ```

6. Una vez dentro de la instancia podemos arrastrar el script y el archivo de configuración para la instalación automática de la pila LAMP con la aplicación web. Una vez los archivos
dentro ejecutamos los siguientes comandos para instalarlo:

    `sudo chmod +x install_lamp.sh`

    `sudo ./install_lamp.sh`

7. Una vez instalado todo ya podremos acceder desde la IP de la instancia a la aplicación web y a las distintas herramientas:

    #### Aplicación web
    ![Aplicación web](https://raw.githubusercontent.com/arr588/iaw-practica-02/main/img/10.png?token=ALTEBMSRUGOGBVBCOMKWQRK7U3DY4 "Aplicación web")
    

    #### phpMyAdmin
    ![phpMyAdmin](https://raw.githubusercontent.com/arr588/iaw-practica-02/main/img/9.png?token=ALTEBMWL3TEF6ZC2OKQHM5S7U3EBK "phpMyAdmin")

    #### Usuario de Adminer
    ![Adminer_usuario](https://raw.githubusercontent.com/arr588/iaw-practica-02/main/img/7.png?token=ALTEBMVWB6HU5AKDORKXGO27U3EFQ "Adminer_usuario")

    #### Adminer
    ![Adminer](https://raw.githubusercontent.com/arr588/iaw-practica-02/main/img/8.png?token=ALTEBMVTQK3ZKKHUVIUUEJC7U3EHE "Adminer")
