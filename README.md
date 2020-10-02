# NOW: Pensions DevOps Engineer Test

### Instructions
You will be asked to complete a simple code test and to describe some pipelines, tools and methodologies around DevOps.

For tasks 1-2 you are free to choose Python 3.x or Java 11.

* Do not use any third party dependencies except PyTest for Python, and JUnit/Hamcrest for Java.
* If using Java, please use Java 11 and the included build.gradle
* Code should be covered with adequate tests
* Code should be readable and clean
* For task 3-5 please provide a example files that each tool would use and an explanation of alternative tools that you may use

### Task 1: 
Implement a function that takes three lists of strings as parameters. The first argument is a list of words that can be used as a subject in a sentence, the second – as a predicate, and the third – as an object. The function must return a string that contains all the sentences in the alphabetical order that can be constructed using the provided subjects, predicates and objects. (Note that the words in the list of subjects are not necessarily in the alphabetical order, and the same applies to the lists of predicates and objects.) Each sentence must be ended by ”.” and the sentences must be separated by ” ”. (Alphabetical order has usual and common meaning, but if you have doubts about it, see test cases below for examples.)

#### Indicative test cases (Python):

``` python 
assert generate_sentences(["Mark", "Mary"], ["hates", "loves"], ["apples", "bananas"])) == "Mark hates apples. Mark hates bananas. Mark loves apples. Mark loves bananas. Mary hates apples. Mary hates bananas. Mary loves apples. Mary loves bananas."
```

``` python
assert generate_sentences(["Vlad", "John"], ["drives"], ["car", "motorcycle", "bus"])) == "John drives bus. John drives car. John drives motorcycle. Vlad drives bus. Vlad drives car. Vlad drives motorcycle."
```

#### Indicative test cases (Java 11):

``` java
assertThat(generateSentences(List.of("Mark", "Mary"), List.of("hates", "loves"), List.of("apples", "bananas")), is("Mark loves apples. Mark loves bananas. Mary hates apples. Mary hates bananas. Mary loves apples. Mary loves bananas."));
```

``` java
assertThat(generateSentences(List.of("Vlad", "John"), List.of("drives"), List.of("car", "motorcycle", "bus")), is( "John drives bus. John drives car. John drives motorcycle. Vlad drives bus. Vlad drives car. Vlad drives motorcycle."));
```

### Task 2: 
Implement a class Airplane that keeps track of the following features of an airplane:

* consumption: an integer representing number of litres consumed per km of distance
* position (x, y): a pair of integers representing a position of the plane on a map. Can be a tuple if chosen language supports tuples (assume that the airplane can only be in one of the positions of the 1 km x 1 km grid)
* fuel level: a floating point number representing the current fuel level in litres

##### Implement the following methods:

* `constructor`: takes four integer parameters (in the specified sequence) `initX, initY, consumption and initial fuel level` where initX/initY represents initial location of the plane, cons represents the consumption (litre/km) and initial fuel level represents the initial fuel level.

* `goto`: takes two integer parameters X and Y representing the location where the plane needs to go to. If the airplane has enough fuel to travel there from its current location, the method moves it there, updates remaining fuel level, and returns True. Otherwise, the plain does not move and False is returned.

* `refuel`: takes one integer parameter indicating how many litres of fuel are added. No value returned.

Assume that the airplane travels in a direct line between two positions (X1, Y1) and
(X2, Y2). The distance between two locations is computed as the square root of ((X2 − X1)^2 + (Y 2 − Y 1)^2)

### Task 3:

We need a CI/CD pipeline that does the following:
* Git for version control
* A tool for a build service
* A tool to manage an audited and authorized deployment service

Please describe how you would chain these tools into a pipeline that can handle developers testing, developing, building and deploying their work.

### Task 4:
Describe tools you would use to ensure code quality metrics and test evidence during a build?

### Task 5:
Describe a configuration management tool and where you have used it in your role 

