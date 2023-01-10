# project-maven-race
![game GUI](https://cdn.javarush.com/images/article/c0b2cb6c-8d36-4ef0-84be-e2d4e6295ab4/512.webp)

Miniproject for JavaRush University.

## IDEA
Create executable JAR-file with JavaFX game based on JavaRush game engine. 

## JAVA 18 is required.

# Tasks:
1. Fork from https://github.com/vasylmalik/project-maven.git
2. Download to your local PC. Continue to edit **pom.xml**
3. Add dependencies:
  - org.apache.commons: commons-lang3: 3.12.0
  - org.openjfx: javafx-controls: 18.0.1
  - com.javarush: desktop-game-engine:1.0 
  - org.junit.jupiter: junit-jupiter-engine: 5.8.2 (with scope **test**)
4. Add plugins: 
  - add `com.javarush: desktop-game-engine:1.0` from **lib/** to local repo
  - plugin for compile all dependencies (with scope **compile**) and put build in one folder
  - add `maven-jar-plugin`. Also configure this plugin for creating file MANIFEST.MF with `Class-Path`, `Main-Class`, `Rsrc-Main-Class`
  - `Class-Path` should contain all JAR-dependencies
  - `Main-Class` should contain `org.eclipse.jdt.internal.jarinjarloader.JarRsrcLoader` for launching JavaFX app
  - `Rsrc-Main-Class` should contain start class `com.javarush.games.racer.RacerGame`
5. Configure plugin `maven-surefire-plugin` should skip StrangeTest, other tests should be executed.
6. Add resources for helping maven-jar-plugin add all JARs into folder **lib/**
7. Push all changes to your GitHub repo.

## How to start the game
1. Build with command `mvn clean install`
2. Start the game `mvn javafx:run` OR `<java18 home path> -jar <path to your file>/project-maven-1.0.jar`
Example: `C:\Users\leo12\.jdks\openjdk-18.100.21.42\bin\java.exe" -jar "C:\temp\project-maven-1.0.jar`

# Have fun!

P.S. also you can wrap your far-JAR-file into EXE with https://launch4j.sourceforge.net 
