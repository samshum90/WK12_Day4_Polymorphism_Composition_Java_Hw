# Polymorphism & Composition Homework - Quiz

# Polymorphism

1. What does the ___word___ 'polymorphism' mean?

polymorphism is the ablity of an object to take on many forms.

2. What does it mean when we apply polymorphism to OO design? Give a simple Java example.
Implementation of polymorphism in java is when we use the same method in different ways 

public class Animal{

   public void sound(){
      System.out.println("Animal is making a sound");   
   }
}

public class Dog extends Animal{

    public void sound(){
        System.out.println("Bark!");
    }
}

public class Cat extends Animal{

    public void sound(){
        System.out.println("Meow");
    }
}

The method sound is a common action to all the animal subclasses but how the action is performed is diffrent as each animal gives a different sound.

3. What can we use to implement polymorphism in Java?

An interface can be implemented on a class, this gives objects of the class the ability to be grouped together by the interface. Two elements are polymorphic with respect to a set of behaviors if they realize the same interfaces.

public class Book implements IBuy

Objects of the Book class would then be able to be bought with items which can also be bought but are not books. In this way, you could make a list of buyable items, chocolate, cups, clocks, etc.


4. How many 'forms' can an object take when using polymorphism? 

At least 2

5. Give an example of when you could use polymorphism.

Shop could use to group objects which you can buy or items you can read, sell anything that can perform the same action.




# Composition

6. What do we mean by 'composition' in reference to object-oriented programming?

It describes a class that references one or more objects of other classes in instance variables. This allows you to model a "has-a" association between objects. For example, a car has an engine and modern coffee machines often have an integrated grinder and a brewing unit.

7. When would you use composition? Provide a simple example in Java.
Composition is used in the place of inheritance for example, a car is not an engine; it has one. And a coffee machine has a grinder and a brewing unit, but it is none of them.
Person has a job:

public class Job {
    private String role;
    private int salary;
    
    public long getSalary() {
        return salary;
    } 
}

public class Person {

    private Job job;
   
    public Person(){
        this.job=new Job();
        job.setSalary(1000L);
    }
    public long getSalary() {
        return job.getSalary();
    }

}

8. What is/are the advantage(s) of using composition?
Reuse existing code
Design clean APIs
Change the implementation of a class used in a composition without adapting any external clients

9. When an object is destroyed, what happens to all the objects it is composed of?
If the composite object is destroyed, all the component parts must be destroyed.