Here is the SportsTeam from the "Model 3 Things" activity.

```java
public class SportsTeam {

    String name;
    boolean isEsport;
    String nameOfSport;
    String location;

    public SportsTeam(String name, boolean isEsport, String nameOfSport, String location) {
        this.name = name;
        this.isEsport = isEsport;
        this.nameOfSport = nameOfSport;
        this.location = location;
    }

    public void printInfo () {
        System.out.println("Team Name: " + name);
        System.out.println("Name of Sport: " + nameOfSport);
        System.out.println("E-Sport: " + isEsport);
        System.out.println("Location: " + location);
    }
}
```
Here is the BaseballTeam which extends SportsTeam:

```java
public class BaseballTeam extends SportsTeam {

    String pitchersName;

    public BaseballTeam (String name, String location, String pitchersName) {
        super(name, false, "Baseball", location);
        //I know that Baseball is the sport and it's not an E-Sport
        //So I don't need to pass these values into the BaseballTeam constructor
        this.pitchersName = pitchersName;
        //Yes, I am aware that all MLB teams have more than just one pitcher
    }

    public void printInfo () {
        super.printInfo();
        System.out.println("Pitcher's Name: " + pitchersName);
    }
}
```
