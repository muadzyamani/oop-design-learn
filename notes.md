# Introduction

## Learn object-oriented design principles

- **Core Problem Addressed:** The tendency to jump straight into programming a new idea without a proper design phase.
- **Proposed Solution:** Start with a good design to avoid wasting time and going down the wrong path.
- **Course Focus:** The fundamentals of Object-Oriented Analysis and Design (OOAD), which is the process of planning a program _before_ writing a single line of code.
- **Benefits of Proper OO Design:** Enables the creation of applications that are:
  - Flexible
  - Maintainable
  - Extensible
- **Course Process:**
  1.  Introduce foundational concepts and terminology for object-oriented development.
  2.  Demonstrate a process to deconstruct an idea (e.g., something written "on the back of a napkin") into the right components to know exactly what code to write.
- **Tools Used:**
  - This is **not** a coding course.
  - The course will use basic components of the **Unified Modeling Language (UML)** to diagram visual models.
  - UML is a tool to articulate ideas and collaborate with others on a design.

## What you should know

- **Prerequisites:**
  - A basic understanding of programming fundamentals (variables, functions, loops, conditions).
  - Familiarity with object-oriented concepts like classes and objects is helpful but not required.
- **Target Audience:**
  1.  Developers currently using an OO language but who may not be using it to its full extent or are struggling to maintain a growing application.
  2.  Experienced programmers with a background in non-object-oriented languages (like C) who find it difficult to transition to an object-oriented mindset.
- **Course Philosophy:**
  - The focus is on the **object-oriented design process**, not on programming.
  - The tools are simple and accessible: pencil and paper, index cards, and whiteboards—not a code editor or IDE.
  - Object-oriented design is not a single formal process but a set of ideas and techniques to incorporate into your own workflow.
- **Learning Encouragement:**
  - The course includes several challenge problems.
  - It is strongly encouraged to actively think about the challenges and review the provided solutions to get the most out of the course.

---

# 1. Object-Oriented Fundamentals

## Object-oriented thinking

- **Comparison to Procedural Programming:**
  - **Procedural (e.g., C):** The program is a long series of operations, organized into functions. The goal is to get from Point A to Point B to complete a task.
    - **Analogy:** A recipe in a cookbook. It lists a sequence of steps to follow in order (mix ingredients, pour in pan, put in oven).
  - **Object-Oriented (OO):** Instead of a sequence of steps, the program is described in terms of its objects and what each one can do. The code is split into self-contained objects, each with its own data and logic.
    - **Analogy:** The objects in a kitchen. The mixer, the pan, and the oven are all objects with specific capabilities (the mixer can mix, the oven can bake).
- **Key Advantage of OO:** Code re-usability.
  - If you've already created objects like a `mixer` and an `oven` to make a cake, you can reuse them to make muffins. You would only need to define a new `muffin tray` object.
- **Programming Paradigm:**
  - Object-orientation is not a language itself, but a **programming paradigm**—a set of ideas supported by many languages.
  - Other paradigms exist (e.g., Logic programming like Prolog, Functional programming like Haskell) but are often used in specialized environments.
  - OO is the dominant paradigm for web, mobile, desktop, and game development.
- **Practical Application:**
  - Many modern languages (like Java) are multi-paradigm, allowing you to write in either a procedural or OO way.
  - For small, simple programs, an OO approach can feel "bloated" or overly complex.
  - The true value and power of object-orientation become apparent as projects grow in scale and require changes.

## Objects

- **Core Concept:** Object-oriented programming makes thinking about code similar to thinking about the real world.
- **The Three Characteristics of an Object:**
  1.  **Identity:** Every object is unique and has its own existence, separate from all other objects. (e.g., two similar mugs are still two separate, individual objects).
  2.  **Attributes:** Properties that describe the object's current state.
      - Some attributes are constant (e.g., a mug's color and size).
      - Other attributes can change (e.g., a mug can be full or empty).
      - _Note:_ The terms attributes, properties, characteristics, states, fields, and variables are often used interchangeably. This course will primarily use **attributes**.
  3.  **Behaviors:** The things an object can do.
      - Behaviors are specific to the type of object (e.g., a cellphone can ring and text, but a mug cannot).
- **Objects Beyond the Physical:**
  - Objects are not just tangible things. They can be non-tangible concepts like a `date`, a `timer`, or a `bank account`.
  - A `bank account` is a good example:
    - **Identity:** Your account is separate from everyone else's.
    - **Attributes:** Account number, balance.
    - **Behaviors:** You can deposit to it and withdraw from it.
- **Identifying Potential Objects:**
  - A simple test is to see if the concept is a **noun**. Nouns can be things, people, places, or ideas.
  - Ask yourself: Can you put the word "the" in front of it?
    - Works: "the mug", "the person", "the bank account", "the event". These are good candidates for objects.
    - Doesn't work: "the ringing", "the texting". These are **verbs** that describe behaviors, not the objects themselves.
  - When structuring an OO program, the focus tends to be on the **nouns first**.

## Classes

- **Definition:** A **class** is the template, definition, or detailed description of what an object will be. It is the "cookie cutter," not the "cookie" itself.
- **Relationship between Classes and Objects:**
  - The class must be created first.
  - You use a single class to create many objects of that type.
  - The process of creating an object from a class is called **instantiation**. Each created object is an **instance** of that class.
- **The Three Components of a Class:**
  1.  **Name:** The type of object the class defines (e.g., `RoundCookie`).
  2.  **Attributes:** The data fields that describe the object (e.g., `weight`, `color`, `hasIcing`). The class defines _what_ attributes an object will have, but not their specific values.
  3.  **Behaviors:** The things an object can do. In code, these are called **methods**.
- **Methods vs. Functions:**
  - A **method** is essentially a function, but with the key difference that it is defined as part of a class.
  - Because a method belongs to an object, it can only access and modify the data (attributes) known to that specific object.
- **Example: `RoundCookie` Class**
  - A class diagram can be used to sketch a class with its name, attributes, and behaviors.
  - From the `RoundCookie` class, you can instantiate multiple cookie objects.
  - Each object (instance) has its own identity and its own data. One cookie object can have its `color` attribute set to "red" while another's is "brown".
  - Calling a method on one instance (e.g., `decorate()` on Olivia's cookie to add blue icing) only affects that specific instance's attributes. It does not change any other cookie objects.
- **Predefined Classes:**
  - Most OO languages come with a collection of built-in classes so you don't have to redefine common things like strings, dates, and arrays.
  - These collections are called **frameworks** or **libraries**.
  - Examples: Java Class Library, .NET Framework (for C#), C++ Standard Library, Python Standard Library.

## Abstraction

- **A-P-I-E Acronym:** A mnemonic for the four fundamental concepts of object-oriented programming: **A**bstraction, **P**olymorphism, **I**nheritance, and **E**ncapsulation.
- **Definition:** Abstraction means focusing on the **essential qualities** of something rather than a specific example, while automatically discarding what is unimportant or irrelevant for a given context.
- **Analogy (The idea of a "person"):**
  - When you hear the word "person," you understand the general concept without needing specific details like name, height, or gender.
  - Your mental model of a "person" includes relevant attributes (name, height) but excludes irrelevant ones (flavor, icing).
- **Relationship to Classes:** Creating a class is an act of abstraction. You create one `Person` class to represent the _idea_ of a person, not separate classes for every individual person.
- **Context is Key:** Abstraction is always relative to the needs of the application.
  - You must ask: "What should a `Person` class look like _for this application_?"
  - If your application doesn't need to track a person's height, then the `height` attribute is irrelevant and should be omitted from the class, even if all real-world people have a height.

## Encapsulation

- **Definition:** Encapsulation is the bundling of an object's attributes (data) and the methods that operate on that data into a single unit (the class). It's about keeping elements together and protecting them.
- **Core Principles:**
  1.  **Restrict Access:** An object should hide its internal data. Other parts of the application should not be able to directly change an object's attributes.
  2.  **Provide Public Methods:** Access to the data should be controlled through public methods.
- **Analogy (The Cookie Jar):**
  - The `CookieJar` class has an attribute for the `numberOfCookies`.
  - Direct access to this attribute is restricted. You can't just reach in and change the number.
  - To get a cookie, you must use a public method like `requestCookie()`.
- **Reasons for Encapsulation:**
  - **Data Integrity:** Prevents the data from being set to an invalid state (e.g., setting `numberOfCookies` to -1).
  - **Control:** Allows the class to control how its data is modified (e.g., limiting the number of cookies you can take).
- **"Black Boxing":**
  - This concept means closing off the inner workings of an object and only revealing specific, necessary inputs and outputs (the public methods).
  - You don't need to know _how_ the `requestCookie()` method works internally to be able to use it.
  - **Benefit:** This allows the internal implementation of a class to change without affecting other parts of the application that use it. If the `CookieJar` changes from tracking a single number to tracking three separate cookie types, the `requestCookie()` method can be updated internally, but the rest of the application still calls it in the same way.
- **Reduces Dependencies:** Encapsulation prevents a change in one place from causing a "domino effect" of required changes throughout the application, leading to more maintainable and robust code.
- **General Rule:** Encapsulate as much as possible.

## Inheritance

- **Definition:** Inheritance allows a new class to be based on an existing class, receiving (inheriting) all of its attributes and methods without having to rewrite them.
- **Primary Benefit:** Code reuse.
- **Terminology:**
  - **Superclass (or Parent/Base Class):** The existing class that is being inherited _from_.
  - **Subclass (or Child/Derived Class):** The new class that _inherits_ from the superclass.
- **Example (Bakery Characters):**
  - Instead of creating separate `Customer` and `Employee` classes with duplicate attributes (name, phone number, email), a common `Person` superclass is created.
  - The `Person` class contains the common attributes (`name`, `phone`, `email`) and methods (`updateContactInfo`).
  - `Customer` and `Employee` become subclasses of `Person`. They automatically get all of `Person`'s attributes and methods.
  - Unique attributes (e.g., `customerID` for `Customer`) and methods (e.g., `getPromoted` for `Employee`) are then added to the specific subclasses.
- **Class Diagram Notation:** An arrow is drawn from the subclass pointing to the superclass to show the inheritance relationship.
- **Maintenance Benefit:** A change made in the superclass automatically applies to all of its subclasses. Adding an `email` attribute to the `Person` class means the `Customer`, `Employee`, and `Courier` subclasses all get the `email` attribute instantly.
- **Single vs. Multiple Inheritance:**
  - **Multiple Inheritance:** A subclass inherits from more than one superclass. Supported by languages like C++ and Python, but can become complex.
  - **Single Inheritance:** A subclass can only inherit from one superclass. This is more common and is enforced by languages like Java, C#, Swift, and Ruby. This course focuses on single inheritance.

## Polymorphism

- **Definition:** A complex-sounding word that simply means "having many forms."
- **Two Main Forms:**

  1.  **Dynamic (or Run-time) Polymorphism:**

      - **Concept:** Allows different types of objects to be accessed through the same interface, even if they implement the methods in different ways.
      - **Analogy (Coffee Makers):**
        - A `BasicCoffeeMaker` and a `FrenchPress` are different classes.
        - Both have a `brew()` method with the same inputs (coffee, water) and output (a cup of coffee).
        - The internal process of how they brew is completely different.
      - **Benefit:** Code can work with any "coffee maker" object, as long as it has the required `brew()` method, without needing to know its specific type.
      - **Implementation:** This is often achieved through:
        - **Method Overriding:** A subclass provides its own implementation of a method inherited from its superclass.
        - Abstract Classes
        - Interfaces

  2.  **Static (or Compile-time) Polymorphism:**
      - **Concept:** Achieved through **Method Overloading**.
      - **Method Overloading Definition:** Implementing multiple methods within the _same class_ that have the _same name_ but a _different set of input parameters_ (either a different number or different types of parameters).
      - **Analogy (French Press):**
        - `brew(coffee, water)` -> returns a cup of coffee.
        - `brew(tea_leaves, water)` -> returns a cup of tea.
      - The program automatically calls the correct version of the `brew` method based on the arguments you provide.

## Analysis, design, and programming

- **The Three Core Activities of Software Development:**
  1.  **Analysis:** Understanding the problem. Answers the question, "What do you need to do?"
  2.  **Design:** Planning the solution. Answers the question, "How are you going to do it?"
  3.  **Programming:** Building the solution.
- **Course Focus:** This course focuses on **Analysis and Design**, which encompasses everything that should happen _before_ writing a single line of code.
- **The Deliverable:** The output of the analysis and design process is a **conceptual design**. This is not code, but a plan that a programmer or team can use to build the software. It can consist of:
  - Diagrams
  - Sketches on a whiteboard
  - Written descriptions
- **A Typical Five-Step OOAD Process:**
  1.  **Gather Requirements:** Figure out what the application needs to do and flesh out the problem you're trying to solve.
  2.  **Describe the Application:** Build a narrative in plain, conversational language explaining how people will use the application.
  3.  **Identify Important Objects:** This is the starting point for identifying the actual classes needed in the program.
  4.  **Describe Interactions:** Formally describe the interactions between objects, understanding each object's responsibilities and the behaviors they need to have.
  5.  **Create a Class Diagram:** This is the main output of the process. It's a visual representation of the classes and is where object-oriented principles like inheritance and polymorphism come into play.

## Unified modeling language (UML)

- **What is UML?**
  - Stands for **Unified Modeling Language**.
  - It is **not** a programming language. It is a **graphical notation** for drawing diagrams to visualize object-oriented systems.
- **Basic Class Diagram Structure:**
  - A simple graphical representation of a class.
  - It has three sections:
    1.  **Top:** Name of the class.
    2.  **Middle:** Attributes (or fields).
    3.  **Bottom:** Behaviors (or methods).
- **Philosophy of Using UML:**
  - UML is a **tool**, not the goal itself. Knowing more UML doesn't necessarily make you a better developer.
  - Knowing a little UML can be more useful than knowing a lot, as it prevents an over-emphasis on the diagrams themselves.
  - Diagrams should be a **quick, useful communication tool**—a "support system for your brain."
- **Diagramming Tools:**
  - **Initial Stages:** Paper or a whiteboard are highly recommended.
  - **Mature Projects:** Electronic tools are useful for sharing among team members. These tools range from simple drawing applications to advanced ones that can generate code from diagrams.
- **Types of UML Diagrams:**
  - UML includes over a dozen types of structural and behavioral diagrams.
  - This course will only use a few common types, including **Class Diagrams** and **Use Case Diagrams**.
- **Resources:**
  - **Finding Tools:** The Wikipedia page "List of Unified Modeling Language tools" is the single best source for finding and comparing UML software.
  - **Deeper Learning:** The book **"UML Distilled" by Martin Fowler** is highly recommended as a short, practical guide for what most developers would ever need to know.

## Chapter Quiz

**Question 1 of 20**
What is the difference between object-oriented programming and procedural programming?

- Procedural programming can use looping and branching, but object-oriented programming cannot.
- Procedural programming uses subroutines, but object-oriented programming does not allow them.
- **Procedural programming specifies a sequence of tasks, but object-oriented programming describes the properties of tools or items.**
  > _Feedback: Correct. In object-oriented programming, there are some elements of procedural programming in the description of objects._
- Procedural programming specifies a sequence of calculations, but object-oriented programming involves more logic.

**Question 2 of 20**
How does dynamic polymorphism differ from static polymorphism?

- It uses inheritance instead of abstraction.
- **It uses overriding instead of overloading.**
  > _Feedback: Correct._
- Dynamic polymorphism creates a unique instance.
- It uses abstraction instead of inheritance.
- It uses overloading instead of overriding.

**Question 3 of 20**
What is overriding a method?

- Removing an inherited method from a subclass.
- Adding a subclass method to a superclass.
- Changing the name of a method.
- **Creating a unique version of an inherited method.**
  > _Feedback: Correct._

**Question 4 of 20**
How are analysis and design different?

- **Analysis describes a problem; design describes a solution.**
  > _Feedback: Correct._
- Analysis constructs; design dissects.
- Analysis considers abstractions; design considers data.
- Analysis describes a solution; design implements a solution.

**Question 5 of 20**
What is the term for a visual representation of the classes in an application?

- whiteboard sketch
- CRC card
- use case
- **class diagram**
  > _Feedback: Correct._

**Question 6 of 20**
In addition to attributes and methods, what does a UML class diagram contain?

- **the class name**
  > _Feedback: Correct._
- all objects created from the class
- the superclass of the subclass
- any inherited behavior

**Question 7 of 20**
How do object behaviors and attributes differ?

- Attributes apply only to a specified object, but behaviors apply to other linked objects.
- Behaviors are vector quantities, but attributes are scalars.
- **Attributes describe a state, but behaviors describe actions.**
  > _Feedback: Correct._
- Behaviors describe dynamic properties, but attributes are static.

**Question 8 of 20**
You are designing a traffic simulation program. What is a possible attribute that you could use for a car object?

- opening the door
- accelerating
- cleaning
- **gas mileage**
  > _Feedback: Correct._

**Question 9 of 20**
Shonzu has gathered the requirements for a new solution, described the application he is going to build, and identified the main objects in the solution. What should he do next?

- **Describe object interactions.**
  > _Feedback: Correct. This will be essential for understanding behaviors._
- Start writing code.
- Build class diagrams.
- Build CRC cards.

**Question 10 of 20**
What is the purpose of encapsulation?

- **to protect an object from unwanted changes**
  > _Feedback: Correct._
- to eliminate redundant properties
- to separate attributes from behaviors
- to organize attributes and behaviors in a hierarchical fashion

**Question 11 of 20**
In addition to attributes and behaviors, which quality must a class possess?

- a data type
- a state
- a sex or color
- **a name**
  > _Feedback: Correct._

**Question 12 of 20**
In the following class diagram, what does `lower()` represent?

<pre>
TRIPOD
- height
- width
- angle
+ raise()
+ lower()
+ point()
+ fold()
</pre>

- an attribute
- an abstraction
- **a behavior**
  > _Feedback: Correct. Behaviors come at the end of a class diagram, and contain room for arguments._
- a name

**Question 13 of 20**
What is a benefit of using a programming language that has a large library?

- A large library tracks the state of individual objects within a program.
- A large library allows many programmers to work simultaneously.
- **Many classes are already defined and can be used without have to re-define them.**
  > _Feedback: Correct._
- Objects are contained in the library, so they won't have to be created if the library is referenced.

**Question 14 of 20**
In the following class diagram, what does `height` represent?

<pre>
TRIPOD
- height
- width
- angle
+ raise()
+ lower()
+ point()
+ fold()
</pre>

- an aggregation
- a title
- **an attribute**
  > _Feedback: Correct. Attributes are generally nouns, and are placed just below the title._
- a behavior

**Question 15 of 20**
We're using abstraction when we define a(n) **\_**.

- attribute
- object
- behavior
- **class**
  > _Feedback: Correct._

**Question 16 of 20**
Focusing on the idea of a person instead of an individual is an example of what fundamental idea in object-oriented programming?

- inheritance
- **abstraction**
  > _Feedback: Correct._
- encapsulation
- polymorphism

**Question 17 of 20**
Steve is able to turn on and adjust his television even though he does not know how it works internally. This exemplifies which principle of object-oriented programming?

- abstraction
- polymorphism
- inheritance
- **encapsulation**
  > _Feedback: Correct._

**Question 18 of 20**
Why is inheritance used when creating a new class?

- **to avoid redefining attributes and behaviors**
  > _Feedback: Correct._
- to conserve memory
- to protect attributes from unwanted changes
- to delegate coding responsibilities more efficiently

**Question 19 of 20**
If an attribute is added to a superclass, what happens to all of the objects of the subclass?

- Each subclass object must request the additional attribute.
- Nothing happens to the subclass objects.
- **Each subclass object automatically receives the additional attribute.**
  > _Feedback: Correct._
- Only newly created subclass objects will receive the new attribute.

**Question 20 of 20**
Static polymorphism uses method **\_**.

- abstraction
- overriding
- **overloading**
  > _Feedback: Correct._
- inheritance

---

# 2. Requirements

## Defining requirements

*   **Core Purpose:** The first step in any design process is to gather requirements to understand what the application needs to do and what problem it's solving.
*   **Functional Requirements:**
    *   **Definition:** These describe what the application *must do*; its necessary features and capabilities.
    *   **Phrasing:** Often start with "The system must..."
    *   **Example (Space Microwave):**
        *   The system must heat food.
        *   The system must allow the user to set a time.
        *   The system must notify the user when food is ready.
*   **Non-functional Requirements:**
    *   **Definition:** These place constraints on *how* the application should function. They describe the required characteristics or "-ilities" (maintainability, reliability, usability, etc.).
    *   **Phrasing:** Often describe how the system "should be."
    *   **Examples:**
        *   Compliance with regulations (e.g., for banking or healthcare data).
        *   Performance (e.g., response time, number of simultaneous users).
        *   Support (e.g., what happens if there's an issue at 2 a.m.).
        *   Security.
*   **Common Mistakes and Best Practices:**
    *   **Understand the "Why":** Don't just accept a list of requirements from a client. Take the time to understand *why* they want something to ensure you are building what they truly need.
    *   **Avoid Implementation Details:** Requirements should be about *what* the system does, not *how* it does it. Avoid object-oriented terms like "class," "object," or "inheritance" at this stage.
    *   **Focus on Minimum Viable Product (MVP):** On the first pass, capture the absolute minimum set of requirements—the bare necessities. Avoid "nice to have" or "dream" features.
    *   **Be Specific, but Not Exhaustive:** Write things down clearly. However, it's okay if the first pass isn't perfect; requirements can be updated later. The initial goal is to get something on paper.

## FURPS+ requirements

*   **Purpose:** FURPS+ is a model and acronym used as a checklist to classify and consider key software quality attributes when defining requirements.
*   **FURPS Categories:**
    *   **F - Functionality:** The core features and capabilities of the application.
    *   **U - Usability:** How easy and intuitive the application is to use (e.g., visual design, documentation).
    *   **R - Reliability:** Acceptable downtime, predictability of failures, and system recovery.
    *   **P - Performance:** Response time, throughput, and limits on system resources.
    *   **S - Supportability:** How easily the application can be tested, extended, serviced, installed, and configured.
*   **The "+" Extension:**
    *   **Design:** Constraints on how the software must be built (e.g., must use a specific database).
    *   **Implementation:** Constraints on the development process (e.g., must be written in a certain language or follow specific standards).
    *   **Interface:** Requirements for interfacing with external systems (not the user interface).
    *   **Physical:** Constraints related to the hardware where the application will be deployed.
*   **Usage Notes:**
    *   FURPS+ is a **prompt** to help you think about key areas. Not all categories will be relevant to every project.
    *   It is acceptable to mark categories as "Not Applicable" or "To Be Determined."
*   **Further Reading:**
    *   *Software Requirements* by Karl Wiegers.
    *   *Mastering the Requirements Process* by Suzanne and James Robertson.

## Challenge: Jukebox requirements

*   **Scenario:** Design a jukebox for astronauts on a moon shuttle.
*   **Core Functional Rules:**
    1.  The jukebox is free to use.
    2.  A user can select an album and then choose individual songs from it to be played.
    3.  To prevent one person from dominating, if an astronaut adds more than three songs in a row to the queue, another astronaut who wants to play a song can jump ahead in line.
*   **Task:**
    *   Write a set of requirements for the jukebox.
    *   Aim for at least **three functional** and **three non-functional** requirements.
*   **Hints:**
    *   Use the FURPS+ model to inspire ideas for requirements.
    *   The problem is intentionally vague to encourage the process of thinking through and discovering requirements. There is no single correct answer.

## Solution: Jukebox requirements

*   **Approach:** The solution uses the FURPS model as a guide to generate requirements.
*   **Example Functional Requirements (F):**
    *   The system must maintain a music library of albums and songs.
    *   The system must allow users to browse albums and songs.
    *   The system must allow users to select *individual* songs (preventing playing full albums).
    *   The system must maintain a queue of songs to play.
    *   The system must play music.
    *   The system must allow the user to sort by artist. (Note: Phrased to be implementation-agnostic, not "must have a button to sort").
    *   The system must identify individual users and track their plays. (Note: Also implementation-agnostic; doesn't specify *how* to identify them).
*   **Example Non-functional Requirements (URPS):**
    *   **Usability:** The system should be intuitive to use in zero-gravity (e.g., have large buttons or voice commands).
    *   **Reliability:** The system should be available 24/7.
    *   **Performance:** The system should be low-power to avoid impacting other critical spacecraft systems.
    *   **Supportability:** The system should have an updatable music library.
*   **Key Takeaway:** The provided requirements are not a complete set but a starting point. The goal of the exercise is to get comfortable with the process of thinking about and writing down requirements.

## Chapter Quiz

**Question 1 of 5**
What is the first step in defining requirements for an application?

*   **determining what the application must have and do**
    > _Feedback: Correct_
*   creating a superclass for all of the objects in the application
*   choosing which classes should be used to create the objects
*   selecting the group of test users

**Question 2 of 5**
Which is a valid nonfunctional requirement?

*   The system should execute a wash cycle in under 20 minutes.
*   **The system should be updated annually.**
    > _Feedback: Correct_
*   The system should automatically register new users.
*   The system should display 2048 x 2048 images.

**Question 3 of 5**
A requirement that all onscreen text must be at least 20-point font size is an example of which FURPS quality?

*   functionality
*   **usability**
    > _Feedback: Correct_
*   performance
*   reliability

**Question 4 of 5**
In which category does extensibility of an application reside?

*   functionality
*   usability
*   **supportability**
    > _Feedback: Correct_
*   reliability

**Question 5 of 5**
Atul is working on an application that must communicate with a scientific instrument and a data archiving system. Into which category would these requirements fall in the FURPS+ model?

*   design
*   physical requirements
*   implementation
*   **interface**
    > _Feedback: Correct. Communication with other devices is a common need._

---
