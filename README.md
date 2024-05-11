# Week 4 Exercises ☕🤖

![](./prog-at.png)

## 🌱 Exercise 1: KombuchaKing Inventory Manager 🍵 
Create a Maven project for managing the inventory of a kombucha brewery using the Gson library.

### Instructions:
1. Create a Maven project and add the Gson dependency to the `pom.xml` file. 📦

2. Create a `Kombucha` class with the following properties:
  - `private String name`: The name of the kombucha flavor. 🍓🍋
  - `private int quantity`: The quantity of the kombucha in stock. 🧮
  - `private double price`: The price of the kombucha per bottle. 💰

3. Implement getter and setter methods for the `name`, `quantity`, and `price` properties.

4. Create a constructor for the `Kombucha` class that accepts the `name`, `quantity`, and `price` as parameters.

5. Create a `KombuchaInventory` class with the following methods:
  - `public void addKombucha(Kombucha kombucha)`: Adds a kombucha object to the inventory `ArrayList`. 🍾
  - `public void removeKombucha(String name)`: Removes a kombucha from the inventory based on its name. ❌
  - `public Kombucha findKombucha(String name)`: Finds a kombucha in the inventory based on its name and returns it. 🔍
  - `public void printInventory()`: Prints the current inventory of kombuchas. 🖨️

6. In the `main` method, create an instance of `KombuchaInventory` and use a `Scanner` to interact with the user. Allow the user to add, remove, find, and print the inventory. 🖥️

7. Use Gson to serialize the `KombuchaInventory` object to a JSON file when the program exits. 💾

8. Write unit tests for the `Kombucha` and `KombuchaInventory` classes using JUnit. ✅

## 🤖 Exercise 2: RoboWarehouse 🚀
Implement a simulation of a robot-operated warehouse using the DataFaker library.

### Instructions:
1. Create a Maven project and add the DataFaker dependency to the `pom.xml` file. 📦

2. Create an interface called `RobotAction` with the following method:
  - `void performAction()`: Performs a specific action in the warehouse. 🏭

3. Create classes `PickingRobot` and `PackingRobot` that implement the `RobotAction` interface. Implement the `performAction()` method for each robot type. 🤖📦

4. Create a `Warehouse` class with an `ArrayList` to store the robots. Implement methods to add robots to the warehouse and to execute the `performAction()` method for each robot using a for loop. 🏭🔄

5. In the `main` method, create an instance of `Warehouse` and use DataFaker to generate random robot names and types. Add the robots to the warehouse. 🎲🤖

6. Implement a method in the `Warehouse` class to simulate a day's work by iterating over the robots and calling their `performAction()` method. 🌞💼

7. Use a `Scanner` to interact with the user and allow them to simulate multiple days or add more robots to the warehouse. 🖥️

8. Implement error handling using a custom `WarehouseException` class that extends `RuntimeException`. Throw the exception when the warehouse runs out of robots. 🚨

9. Write unit tests for the `PickingRobot`, `PackingRobot`, and `Warehouse` classes using JUnit. ✅

## ☕ Exercise 3: CoffeeMaker Unit Testing ☕
Write unit tests for a `CoffeeMaker` class that simulates the functionality of a coffee machine.

### Instructions:
1. Create a new class called `CoffeeMaker` with the following methods:
  - `public void brew(String coffeeType)`: Brews a cup of coffee of the specified type (e.g., "Espresso", "Cappuccino", "Latte"). ☕
  - `public void addWater(int amount)`: Adds water to the coffee maker's reservoir. 💧
  - `public void addCoffeeBeans(int amount)`: Adds coffee beans to the coffee maker's bean container. 🌱
  - `public int getWaterLevel()`: Returns the current water level in the reservoir. 💦
  - `public int getCoffeeBeansLevel()`: Returns the current level of coffee beans in the bean container. 🫘
  - `public String getLastBrewedCoffee()`: Returns the type of the last brewed coffee. ☕

2. Implement the methods in the `CoffeeMaker` class according to their descriptions. Use instance variables to keep track of the water level, coffee beans level, and the last brewed coffee type. 🔧

3. Create a new class called `CoffeeMakerTest` in the `src/test/java` directory of your project. 🧪

4. In the `CoffeeMakerTest` class, write the following unit tests using JUnit:
  - `Given_SufficientResources_When_Brew_Then_UpdatesLastBrewedCoffee()`: Test the `brew()` method by calling it with different coffee types and asserting that the last brewed coffee type is updated correctly. ☕✅
  - `Given_ValidAmount_When_AddWater_Then_UpdatesWaterLevel()`: Test the `addWater()` method by adding water to the reservoir and asserting that the water level is updated correctly. 💧✅
  - `Given_ValidAmount_When_AddCoffeeBeans_Then_UpdatesCoffeeBeansLevel()`: Test the `addCoffeeBeans()` method by adding coffee beans to the bean container and asserting that the coffee beans level is updated correctly. 🌱✅
  - `Given_WaterLevelSet_When_GetWaterLevel_Then_ReturnsCorrectLevel()`: Test the `getWaterLevel()` method by setting the water level and asserting that the retrieved water level matches the expected value. 💦✅
  - `Given_CoffeeBeansLevelSet_When_GetCoffeeBeansLevel_Then_ReturnsCorrectLevel()`: Test the `getCoffeeBeansLevel()` method by setting the coffee beans level and asserting that the retrieved coffee beans level matches the expected value. 🫘✅
  - `Given_BrewedCoffee_When_GetLastBrewedCoffee_Then_ReturnsLastBrewedCoffeeType()`: Test the `getLastBrewedCoffee()` method by brewing different types of coffee and asserting that the last brewed coffee type is returned correctly. ☕✅

5. Use the `@Before` annotation in JUnit to set up a new instance of the `CoffeeMaker` class before each test method. 🆕

6. Run the unit tests and ensure that all tests pass successfully. ✅

7. Add additional test cases to cover edge cases and potential error scenarios, such as trying to brew coffee without sufficient water or coffee beans. 🚨

8. Optionally, you can add methods to the `CoffeeMaker` class to simulate consuming water and coffee beans during the brewing process and update the unit tests accordingly. ⚙️

Remember to follow the **Given_Preconditions_When_StateUnderTest_Then_ExpectedBehavior** naming convention for your test methods. This convention helps in clearly expressing the purpose and expected behavior of each unit test. ✨

By practicing unit testing with the `CoffeeMaker` class, you'll gain hands-on experience in writing effective tests and ensuring the correctness of your code. ☕💪