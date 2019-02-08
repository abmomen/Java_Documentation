# JAVA Basics Documentation

### প্যাকেজ কি :
#### প্যাকেজ হচ্ছে একটা ফোল্ডারের মত যেখানে রিলেটেড ক্লাস গুলো আলাদা ভাবে রাখা যায় ,যে কোনো জাভা ক্লাস অবশ্যই একটি প্যাকেজ এক মধ্যে থাকবে। 
### বুলেট পয়েন্টঃ
     * একটা ক্লাস একটাই প্যাকেজের আন্ডারে থাকবে । 
     * প্যাকেজ স্টেটমেন্ট টি সবার উপরে লিখতে হবে ।
##### উদাহরনঃ 
```java
package certification;
class Course{
}
``` 
#### যে সব যায়গায় প্যাকেজ স্টেটমেন্ট লিখা যাবে না :
* সবার নিচে লিখা যাবে না,লিখলে কম্পাইল ইরর খাবে। 
##### যেমনঃ 
```java
class Course{
}
package certification;
```    
* ক্লাসের ভেতরে লিখা যাবে না। 
##### যেমনঃ 
```java
class Course{
    package certification;
}
```
* আর একটা ক্লাসে একের বেশী প্যাকেজ থাকতে পারবে না , যেটা আগেই বলছি।
##### যেমনঃ 
```java
// This code won't compile
package certification;
package anotherpackage;
class Course{
}
```
### IMPORT STATEMENT:
#### একই প্যাকেজের ক্লাস বা ইন্টারফেস ব্যাবহার করতে শুধু তাদের নাম দিয়েই ব্যাবহার করা যাবে কিন্তু অন্য প্যাকেজ এর ক্লাস ব্যবহার করতে হলে তাদের import করে নিতে হবে।
##### যেমনঃ 
```java
import packageName.anySubPackageName.ClassName;
```
* কোনো ক্লাসে একের ওধিক import স্টেটমেন্ট থাকতে পারে ।
* এটি প্যাকেজের পরে এবং ক্লাস লেখার আগে লিখতে হবে। 
* ক্লাসের ভেতরে লিখা যাবে না।
* ক্লাসের শেষেও লিখা যাবে না। 
#### আর যদি একটা প্যাকেজের সব গুলা ক্লাসকে ইম্পরট করতে চাই তাহলে নিচের মত করে লিখতে হবে।
```java
import packageName.*;
class ClassName{
}
```
#### যে সব ক্লাস এবং ইন্টারফেস কোন প্যাকেজের মধ্যে থাকে না (মানে ডিফল্ট প্যাকেজে থাকে) তাদের কে প্যাকেজের মধ্যে থাকা ক্লাস বা ইন্টারফেস গুলা এক্সেস করতে পারবে না , কিন্তু প্যাকেজের বাইরের ক্লাস বা ইন্টারফেস গুলা এক্সেস করতে পারবে এবং এর জন্য তাদের ইম্পরট করতে হবে না । 
### COMMENTS:
#### মাল্টিলাইন ও সিঙ্গেললাইন কমেন্ট ।
```java 
class MyClass{
    /*
     comments that span multiple 
     line of code.
    */
   
    /*
     *multiple line comment that
     *has * in every line.
     */
     
    // single line comment.
}
```
#### Some uncommon use of comment.
```java
String name= /* Harry */ "Momen";
System.out.println(name);
//Output:Momen
```
```java
String name= "/* Harry */ Momen";
System.out.println(name);
//Output:/* Harry */ Momen
```
```java
String name="This /* will not
                  */ Compile";
System.out.println(name);
//This code won't compile.
```
### Java Source Code file.
#### একটি সোর্স ফাইলের মধ্যে অনেক গুলো ক্লাস আথবা ইন্টারফেস থাকতে পারে ।যেমনঃ Content of java source file `Multiple1.java` 
```java
interface Printable{
    //...other details
}
interface Movable{
    //...other details
}
```
#### Content of Multiple2.java
```java
interface Printable{
    //...other details
}
class MyClass{
    //...other details
}
interface Movable{
    //...
}
class Car{
    //...other details.
}
```
#### কিন্তু একটি সোর্স ফাইলে একটিই পাবলিক ক্লাস থাকতে পারবে এবং পাবলিক ক্লাসটির নাম সোর্স ফাইলের নামের সাথে অবশ্যই মিলতে হবে।
#### যেমনঃ `Test.java`
```java 
public class Test{
    //other details
}
class B{
    //other details
}
interface C{
    //other details
}
```
#### আর একটি সোর্স ফাইলে কোনো পাবলিক ক্লাস না থাকলেও প্রোগ্রাম ঠিক ঠাক ভাবে রান করবে। 
### Access Modifiers:
#### জাভাতে চার ধরনের এক্সেস মোডিফায়ার আছে । 
* private
* protected
* default
* public
#### ক্লাস , ইন্টারফেস এবং ইন্টারফেসের মেম্বার (ভেরিয়েবল ও মেথড) গুলো `private` বা `protected` হতে পারে না।
* ক্লাসের মেম্বার গুলো যদি প্রাইভেট হয় তাহলে ওই মেম্বার গুলা অন্য কোথাও থেকে এক্সেস পাওয়া যাবে না শুধু মাত্র ক্লাসের ভেতরে থেকে এক্সেস পাওয়া যাবে । 
* যদি প্রটেক্টেড হয় তাহলে ওই ক্লাসের ভিতরে এবং একই প্যাকেজ বা ভিন্ন প্যাকেজ এর সাব ক্লাস থেকে এক্সেস পাওয়া যাবে ।
* ডিফল্ট এক্সেস মোডিফায়ার কে প্যাকেজ প্রাইভেট বলা হয় তার মানে ডিফল্ট ক্লাস মেথড অথবা ভেরিয়েবল গুলো একই প্যাকেজের মেম্বার গুলো এক্সেস পাবে , প্যাকেজের বাইরে থেকে পাওয়া যায় না । 
* পাবলিক গুলা সবাই পাবে । 

### Encapsulation: 
#### কোন একটি ক্লাসের ভেরিয়েবল গুলোকে প্রাইভেট করে তাদের এক্সেস রেস্ট্রিক্ট করা কেই এঙ্ক্যাপ্সুলেশান বলে . 
#### যেমন: 
```java
public class Student{
    private Integer id;
    private String name;
    //....constructors
    //....getters and setters
}
```
এখন এই ক্যাপস্যুলের মধ্যে রাখা ভেরিয়েবল গুলা যদি ব্যবহার করতে হয় তাহলে আমাদের কিছু পাবলিক মেথড লাগবে যার মাধ্যেমে আমরা এই ভেরিয়েবল গুলোকে মোডিফাই করতে পারব , যাদের কে সেটার ও গেটার মেথড বলে । 
#### যেমন :
```java
public class Student{
    private Integer id;
    private String name;
//..constructors
//..setter methods
    public void setId(Integer id){
        this.id=id;
    }
    public void setName(String name){
        this.name=name;
    }
//..getter methods
    public Integer getId(){
        return id;
    }
    public String getName(){
        return name;
    }
}  
```
আমরা এখানে ভ্যালু সেট করার সময় শুধু ভ্যালুটা নিয়ে কোন মোডিফাই না করেই সেট করে দিয়েছি , আপনি চাইলে মেথড গুলোর মধ্যে ইচ্ছা মত চেকিং বসাতে পারেন অথবা যোগ, বিয়োগ, গুন, ভাগ করে নিতে পারেন । আপনার এই ক্লাসটি যারা ব্যবহার করবে তারা জানতেও পারবে না আপনি ভিতরে কি করেছেন,  এর মাধ্যমে আমরা আসলে ইমপ্লিমেন্টেশান হাইড করে রাখছি । 
### Inheritance :
#### মনে করেন আপনার বাবা আপনার জন্য একটা বিশাল বাড়ি বানায় রাখছেন , তখন আপনি কি করবেন ? আপনি বাড়ি করার টেনশান বাদ্দিয়া আপনার বাবার বাড়ি টাই ব্যাবহার করার ট্রাই করবেন আর আপনি আপনার টাকা দিয়ে অন্য কিছু করবেন । তো ইনহেরিটেন্স ব্যাপারটা এমনি । 
মনে করেন কেও একজন একটা Calculator ক্লাস বানায় রাখছে নিচের মত অথবা আপনিই বানাইছেন । 
```java
public class Calculator{
    public Integer add(Integer a, Integer b){
        return a+b;
    }
    public Integer sub(Integer a, Integer b){
        return a-b;
    }
    public Integer mul(Integer a, Integer b){
        return a*b;
    }
    public Integer div(Integer a, Integer b){
        return a/b;
    }

}
```
এখন আপনি অন্য একটা কাজ করছেন যেখানে ক্যালকুলেটর টি দরকার আপনি কি আবার এই কাজ করবেন ? না দরকার নেই আপনি উপরের ক্লাসটিই ব্যবহার করতে পারেন । আপনাকে শুধু আপনার ক্লাসের সাথে উপরের ক্লাসটি এক্সটেন্ড করে নিতে হবে , তাহলে আপনি উপরের ক্লাসের সব গুলো মেথডই (যে মেথড গুলো পুব্লিক ও প্রটেক্টেড) পেয়ে যাবেন । 
#### যেমন : 
```java 
class myCalculator extends Calculator{} 
```
এমন হতে পারে যে আপনার প্যারেন্ট ক্লাসের কোন একটা মেথড এর ইমপ্লিমেন্টেশান ভালো লাগে নাই তাহলে আপনি সেটা নিজের মত করে ওভাররাইড করে নিতে পারেন । যেমন :
```java
class myCalculator extends Calculator{
    @Override
    public Integer add(Integer a, Integer b){
        if(a>0 && b>0)
        int sum=a+b;
        return sum;
    }
}
```
এ ছাড়াও ইন্টারফেস গুলোও ইনহেরিট করতে পারে । যেমন :
```java 
interface A{
    public void doSomethong();
}
interface B extends A{}
```
#### জাভাতে মাল্টিপল ইনহেরিটেন্স সাপোর্ট করে না । তার মানে আপনি একসাথে দুই বা ততোধিক ক্লাস কে এক্সটেন্ড করতে পারেন না ।
কেনো এমন টি করা যায় না নিচে বলছি । ধরুন নিচের মত আপনার দুইটি ক্লাস আছে যেখানে একই ধরনের দুইটি মেথড আছে । 
```java 
class A{
    void sayHello(){
        System.out.println("Hello World");
    }
} 

class B{
    void sayHello(){
        System.out.println("Hello World");
    }
} 
```
এখন ধরেন আরেকটি ক্লাস যেটি এই দুইটি ক্লাসকেই এক্সটেন্ড করছে নিচের মত। 
```java 
//not allowed in java
class C extends A ,B{}
```
এখন আপনি ক্লাস ছি এর একটি অবজেক্ট বানিয়ে sayHello() মেথডটি কল করলেন তাহলে কি হবে? জেভিএম আসলে কনফিউশান এ পড়ে যাবে যে কোন ক্লাসের মেথড টি কল করব ? এই প্রব্লেম থেকে বাচার জন্য জাভা মাল্টিপল ইনহেরিটেন্স সাপোর্ট করে না । 

তবে আপনি একটি ক্লাসের মধ্যে যত খুশি তত গুলা ইন্টারফেস কে ইম্পিপেন্ট করতে পারেন । যেমন :
```java
interface A{}
interface B{}
class C implements A,B{} 
```

### Polymorphism:
#### পলিমরফিজম কে বাংলায় বলা যায় বহু রুপিতা 
যেমন একটি হরিণ ও প্রাণী , ঘোড়াও প্রাণী , মানুষ ও প্রাণী সুতরাং এখানে প্রাণী বিভিন্ন রূপ ধারণ করছে এই আচরণ কেই জাভাতে পলিমরফিজম বলে । যেমন :
```java
interface Vegetarian{}
class Animal{}
class Deer extends Animal implements Vegetarian{} 
```
উপরের উদাহরণে ডেয়ার ক্লাসটি নিচের চারটি IS-A রিলেশান দেখাতে পারে । 
* Deer IS-A Animal
* Deer IS-A Vegetarian
* Deer IS-A Deer
* Deer IS-A Object 
জাভার যে কোন অবজেক্ট যা দুইটার বেশি IS-A রিলেশান পাস করবে তাদের পলিমরফিক অবজেক্ট বলে ।  


