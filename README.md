# project-maven-race
![87-converted](https://cdn.javarush.com/images/article/c0b2cb6c-8d36-4ef0-84be-e2d4e6295ab4/512.webp)

Miniproject for JavaRush University.

##IDEA
Create executable JAR-file with JavaFX game based on JavaRush game engine. 

#Tasks:
1. Fork from https://github.com/vasylmalik/project-maven.git
2. Download to your local PC. Continue to edit pom.xml
3. Add dependencies:
  - org.apache.commons: commons-lang3: 3.12.0
  - org.openjfx: javafx-controls: 18.0.1
  - com.javarush: desktop-game-engine:1.0 
  - org.junit.jupiter: junit-jupiter-engine: 5.8.2 (with scope test)
4. Add plugins: 
  - add `com.javarush: desktop-game-engine:1.0` from lib/ to local repo
  - plugin for compile all dependencies (with scope compile) and put build in one folder
  - add `maven-jar-plugin`. Also configure this plugin for creating file MANIFEST.MF with `Class-Path`, `Main-Class`, `Rsrc-Main-Class`
  - `Class-Path` should contain all JAR-dependencies
  - `Main-Class` should contain `org.eclipse.jdt.internal.jarinjarloader.JarRsrcLoader` for launching JavaFX app
  - `Rsrc-Main-Class` should contain start class `com.javarush.games.racer.RacerGame`
5. 
