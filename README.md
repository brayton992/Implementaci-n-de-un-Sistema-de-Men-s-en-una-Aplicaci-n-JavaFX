# Implementaci-n-de-un-Sistema-de-Men-s-en-una-Aplicaci-n-JavaFX

## EXPLICACION DEL CODIGO

Este código implementa una interfaz gráfica en JavaFX con una barra de menú que contiene menús y elementos de menú organizados y con acciones definidas. La utilización de BorderPane facilita la organización estructurada de los componentes en la ventana de la aplicación.

```java
import javafx.application.Application;
import javafx.scene.Scene;
import javafx.scene.control.Menu;
import javafx.scene.control.MenuBar;
import javafx.scene.control.MenuItem;
import javafx.scene.layout.BorderPane;
import javafx.stage.Stage;

public class GUIJavaFX extends Application {

    @Override
    public void start(Stage primaryStage) {
        // Crear la barra de menú
        MenuBar menuBar = new MenuBar();

        // Crear el menú "Archivo"
        Menu archivoMenu = new Menu("Archivo");
        MenuItem nuevoItem = new MenuItem("Nuevo");
        MenuItem abrirItem = new MenuItem("Abrir");
        MenuItem guardarItem = new MenuItem("Guardar");
        MenuItem salirItem = new MenuItem("Salir");
        archivoMenu.getItems().addAll(nuevoItem, abrirItem, guardarItem, salirItem);

        // Crear el menú "Editar"
        Menu editarMenu = new Menu("Editar");
        MenuItem cortarItem = new MenuItem("Cortar");
        MenuItem copiarItem = new MenuItem("Copiar");
        MenuItem pegarItem = new MenuItem("Pegar");
        editarMenu.getItems().addAll(cortarItem, copiarItem, pegarItem);

        // Crear el menú "Ayuda"
        Menu ayudaMenu = new Menu("Ayuda");
        MenuItem acercaDeItem = new MenuItem("Acerca de");
        ayudaMenu.getItems().add(acercaDeItem);

        // Agregar los menús a la barra de menú
        menuBar.getMenus().addAll(archivoMenu, editarMenu, ayudaMenu);

        // Crear el contenedor principal
        BorderPane root = new BorderPane();
        root.setTop(menuBar);

        // Crear la escena y el stage
        Scene scene = new Scene(root, 600, 400);
        primaryStage.setTitle("GUI JavaFX");
        primaryStage.setScene(scene);
        primaryStage.show();

        // Agregar acciones a los items de menú
        nuevoItem.setOnAction(e -> System.out.println("Nuevo archivo"));
        abrirItem.setOnAction(e -> System.out.println("Abrir archivo"));
        guardarItem.setOnAction(e -> System.out.println("Guardar archivo"));
        salirItem.setOnAction(e -> primaryStage.close());
        cortarItem.setOnAction(e -> System.out.println("Cortar"));
        copiarItem.setOnAction(e -> System.out.println("Copiar"));
        pegarItem.setOnAction(e -> System.out.println("Pegar"));
        acercaDeItem.setOnAction(e -> System.out.println("Acerca de"));
    }

    public static void main(String[] args) {
        launch(args);
    }
}
```

   
## Practica de interface 

## Imagen de ejemplo de la tarea
![image](https://github.com/brayton992/Implementaci-n-de-un-Sistema-de-Men-s-en-una-Aplicaci-n-JavaFX/assets/142423609/699b043d-c593-4f8a-b0e1-50c080bdde32)



##MenuBar:

Descripción: Una barra de menú principal.
Función: Actúa como contenedor para los menús de la aplicación, ubicada en la parte superior de la ventana.
##Menus:

Descripción: Menús principales como "Archivo", "Editar" y "Ayuda".
Función: Agrupan opciones relacionadas bajo un mismo encabezado, organizando las acciones disponibles para el usuario.
##MenuItems:

Descripción: Elementos de menú dentro de cada menú principal.
Función: Representan acciones específicas que el usuario puede seleccionar, como "Nuevo", "Abrir" y "Guardar" en el menú "Archivo".
##Separadores:

Descripción: Uso de SeparatorMenuItem para organizar los elementos del menú.
Función: Divide lógicamente las opciones del menú en secciones, mejorando la claridad visual y la organización.
##Acciones:

Descripción: Definir acciones para cada elemento de menú.
Función: Manejar las interacciones del usuario, como imprimir mensajes en la consola cuando se selecciona una opción.
##Layout:

Descripción: Uso de un BorderPane para organizar la interfaz.
Función: Coloca la barra de menú en la parte superior de la ventana, permitiendo una disposición clara y estructurada de los componentes de la interfaz.
