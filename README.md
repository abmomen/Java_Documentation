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



