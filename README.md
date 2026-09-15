# IJA / Java Maze Game

Java 17 / JavaFX university team project implementing a Pac-Man-style maze game with file-based maps, moving ghosts, gameplay logging and replay support.

This repository is a fork of the original team repository and preserves the shared coursework implementation.

## Project overview

The player navigates a maze from the starting position to the target while avoiding ghosts. Maps are loaded from files, and game sessions can be saved to log files and replayed later.

The project is organized into separate `model`, `controller`, `view` and `interfaces` packages. The original coursework files are preserved in the `mazegame/` directory.

## Main features

- JavaFX graphical interface
- maze maps loaded from text files
- player movement and independently moving ghosts
- key and target game objects
- multiple lives and game-state handling
- gameplay logging to files
- loading and replaying previous game sessions
- Maven build configuration and Javadoc generation

## Project structure

```text
.
├── README.md
└── mazegame/
    ├── data/
    │   ├── maps/
    │   └── logs/
    ├── src/main/java/
    │   ├── controller/
    │   ├── interfaces/
    │   ├── model/
    │   ├── view/
    │   └── App.java
    ├── pom.xml
    ├── readme.txt
    └── requirements.pdf
```

The main application source is under `mazegame/src/main/java/`. `MapParser` reads map definitions from `data/maps`, while saved sessions in `data/logs` are parsed for replay functionality.

## Requirements

- JDK 17
- Maven
- JavaFX 17

## Build and run

Move to the Maven project directory:

```bash
cd mazegame
```

Compile the application:

```bash
mvn clean compile
```

Package it as a JAR:

```bash
mvn package
```

The original project instructions run the packaged application with a local JavaFX SDK:

```bash
java --module-path <path-to-javafx-sdk>/lib --add-modules javafx.controls,javafx.fxml -jar target/mazegame-1.0-SNAPSHOT.jar
```

Generate Javadoc with:

```bash
mvn javadoc:javadoc
```
