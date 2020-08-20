# 08/28: Memory and Pointers


## Basics

1. In your own words, explain what the stack is, and what kind of data goes in the stack.
2. In your own words, explain what the heap is, and what kind of data goes in the heap.
3. *Primitive datatypes* are `bool`, `char`, `short`, `int`, `long`, `float`, `double`. Do variables of primitive datatypes live in the stack or the heap?
4. *Object datatypes* are classes, such as `Car` and `Engine`. Do variables of object datatypes live in the stack or the heap?
5. Would a `String` live in the stack or the heap? Why?
6. In your own words, explain the difference between local variables and reference variables.

## Exploration

7. `null` is a special value in Java for reference variables that do not currently refer to anything. In the code from the video (below), 

    ```Java
    public class MemoryModel {

        static class Engine {
            String name = "Turbo";
        }

        static class Car {

            int id;
            int hp;
            Engine myEngine;

            public Car(int id) {
                this.id = id;
            }
        }

        public static void doMore() {
            System.out.println("doing more stuff...");
        }

        public static void doWork() {
            double weight = 120.30;
            doMore();
        }

        public static void main(String[] args) {
            int age;
            age = 12;
            age = 15;
            String name = "";

            Car myCar = new Car(0);
            myCar = new Car(1);
            myCar = new Car(2);

            Car my2Car = new Car(3);
            my2Car.hp = 120;

            Car my3Car = new Car(4);
            my3Car.hp = 1000;

            Engine bigEngine = new Engine();
            my3Car.myEngine = bigEngine;
        }

    }
    ```

## Challenge

1. FIXME Arrays
