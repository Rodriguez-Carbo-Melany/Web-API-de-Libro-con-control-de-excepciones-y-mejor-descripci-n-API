# Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API
A la tarea ya presentada se le creo:
- una carpeta llamada exception
  
   ![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/4106f138-0ea5-4518-abce-618f79e9c6e5)  

- su respectiva clase que en esta ocasion se llamaria LibroException

    ![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/030cb8b0-ee4a-4231-8d2b-5cee17f0f946)

Este código es una clase en Java que define una excepción personalizada llamada LibroException en una aplicación Spring Boot. 

![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/e65cd592-3f63-43f3-b76d-3e09852a54b3)

se utilizo:

@ResponseStatus(HttpStatus.NOT_FOUND): Esta anotación indica que cuando se lanza esta excepción, Spring automáticamente responderá con un estado HTTP 404 (Not Found). Es una forma de vincular una excepción específica a un código de estado HTTP.

public class LibroException extends RuntimeException: Define la clase LibroException que extiende RuntimeException. Esto significa que LibroException es una excepción no verificada (unchecked exception), lo que implica que no es obligatorio manejarla o declararla.

public LibroException(String mensaje): Es el constructor de la clase, que recibe un mensaje de error como parámetro y lo pasa al constructor de la clase padre (RuntimeException) para que pueda ser accesible a través de los métodos de la excepción estándar.

luego se modifico la clase del controller 

![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/2c513a7a-36fd-4048-8358-4751f48ac915)

especificamente en el id 

![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/f18676ca-4a6b-4e4d-8b6c-89ae7a175f6a)

Este método maneja las solicitudes GET en la ruta / seguida de un ID (por ejemplo, /1).

Utiliza libroService para buscar un libro por su ID.

Si se encuentra el libro, devuelve el libro con un estado HTTP 200 (OK).

![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/ddde8fdf-6842-4cf6-83b5-4846ad262a0e)

Si no se encuentra el libro, lanza una excepción LibroException con un mensaje de error y un mensaje personalizado que en este caso es "No se encontro el libro con el ID:"

![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/e5d8cf5a-2f8d-486d-86e2-2f0fb3608549)

- y al momento de crear un libro

 ![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/746202ef-29ff-402f-b34c-884289d7df31)

 Utiliza libroService para agregar un nuevo libro.
 
Devuelve una respuesta con un estado HTTP 201 (CREATED) y un mensaje de éxito.

![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/e8a0653c-c5f7-4024-b4c5-5befa8a72f55)

- y como respuesta en el navegador se muestra:

    ![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/e63d835d-d148-4c7c-9b25-7c2d5167359f)  
- el mensaje de que no se encontro el libro 
  
     ![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/d1d0c70a-475e-4c10-bf6c-862952c88c4c)   

- y el mensaje libro creado 
  
    ![image](https://github.com/Rodriguez-Carbo-Melany/Web-API-de-Libro-con-control-de-excepciones-y-mejor-descripci-n-API/assets/170265718/ac48ba91-d315-4283-afdd-b798fafbdeae)






