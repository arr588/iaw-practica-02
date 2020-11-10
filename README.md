# iaw-practica-02

## Implantación de una aplicación web LAMP en Amazon Web Services (AWS)

1. Le damos a lanzar instancias y seleccionamos la última version de Ubuntu Server. Las opciones de procesador, detalles de la instancia y espacio de disco las dejamos por defecto:

    ![](https://github.com/arr588/iaw-practica-02/blob/main/img/1.png)

2. Abrimos los puertos SSH, HTTP y HTTPS:

    ![](https://github.com/arr588/iaw-practica-02/blob/main/img/2.png)

3. Generamos una clave de acceso. En mi caso al haber creado otra máquina ya tengo una generada que voy a usar ya que es para la misma práctica por comodidad:

    ![](https://github.com/arr588/iaw-practica-02/blob/main/img/3.png)

4. Para gestionar las instancias vamos a usar Visual Studio Code con la extensión de Remote-SSH:

    ![](https://github.com/arr588/iaw-practica-02/blob/main/img/4.png)

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
    ![Aplicación web](https://github.com/arr588/iaw-practica-02/blob/main/img/10.png)
    

    #### phpMyAdmin
    ![phpMyAdmin](https://github.com/arr588/iaw-practica-02/blob/main/img/9.png)

    #### Usuario de Adminer
    ![Adminer_usuario](https://github.com/arr588/iaw-practica-02/blob/main/img/7.png)

    #### Adminer
    ![Adminer](https://github.com/arr588/iaw-practica-02/blob/main/img/8.png)
