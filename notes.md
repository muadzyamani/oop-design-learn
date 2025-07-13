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

# 3. Use Cases and User Stories

## Use cases

*   **Purpose:** To shift focus from system-centric requirements to the user's perspective, describing how a user accomplishes a specific goal.
*   **Three Essential Components:**
    1.  **Title:** A short, active verb phrase describing the goal (e.g., "Heat Meal," "Heat Delayed Meal").
    2.  **Primary Actor:** The entity (human or external system) that interacts with the application to achieve the goal.
    3.  **Execution Flow (Scenario):** The steps needed to accomplish the goal, written in plain, non-technical language.
*   **Formatting the Scenario:**
    *   Can be a **single paragraph** describing the successful flow of events.
    *   Can be a **numbered list** of individual steps.
    *   The goal is readability and clarity, not strict formatting.
*   **Handling Alternate Flows:**
    *   Use cases typically describe the "sunny day" or successful scenario.
    *   **Extensions** or alternative steps can be added to describe what happens when things go wrong (e.g., system can't identify a meal package).
*   **Fully Dressed Use Cases:**
    *   A more formal version that includes additional fields like preconditions, post-conditions, secondary actors, and stakeholders.
    *   **Caution:** This level of formality can slow down progress and is often unnecessary for smaller projects. Casual, readable use cases are often better than incomplete formal templates.
*   **Best Practices:**
    *   Don't spend more than a few days on use cases in any project iteration.
    *   It's okay to make assumptions and evolve use cases later.
    *   **Recommended Reading:** *Writing Effective Use Cases* by Alistair Cockburn.

## Identifying the actors

*   **Definition:** An actor is anything that lives outside your application but interacts with it to accomplish a goal.
*   **Types of Actors:**
    *   **Human Actors:** Represented by stick figures. Can be specific roles (Mission Commander, Pilot) or more general (Player, User).
    *   **External Systems:** Other computer systems or organizations the application needs to interact with. Represented by a box, often with `<<actor>>` written inside.
*   **Brainstorming Actors:**
    *   Think about different job titles or departments that might use the system.
    *   Ask if the application needs to interact with other systems.
*   **Primary vs. Secondary Actors:**
    *   **Primary Actor:** The one who *initiates* the use case.
    *   **Secondary Actor:** Other actors involved in the use case, often in a monitoring or reactive role.
*   **Focus on Goals, Not Just Roles:**
    *   The same person can be a different actor at different times, depending on their goal.
    *   It may be more useful to define actors by their goal in a specific scenario (e.g., "the Cook," "the Monitor") rather than just their job title.

## Identifying the scenarios

*   **Goal-Oriented:** A use case scenario should describe a goal an actor can accomplish in a **single encounter**.
    *   **Good Examples:** "Cook Meal," "Generate Reports." These are user-focused goals with multiple steps.
    *   **Too Small:** "Turn on microwave." This is a step within a larger goal, not a goal itself.
    *   **Too Broad:** "Feed entire crew." This involves multiple encounters.
*   **Writing Style:**
    *   Use an **active voice** (e.g., "Astronaut inserts meal package" instead of "The system is provided with the meal package by the astronaut").
    *   Omit needless words and details.
    *   **Avoid technical implementation details** like protocol names (HTTPS, JSON) or programming concepts. "System sends pager message" is sufficient.
    *   **Avoid describing the user interface** (UI). Do not use words like "screen," "click," or "button." Focus on the user's *intention*.
*   **Discovering Missed Use Cases:** Ask questions to prompt new goals or actors:
    *   Who performs system administration (starting/stopping, backups, updates)?
    *   Who manages users and security?
    *   What happens if the system fails, and who reacts to it?
    *   Is anyone looking at performance metrics or system activity logs?

## Diagramming use cases

*   **Purpose:** A UML Use Case Diagram shows the relationships between multiple actors and multiple use cases at a high level.
*   **Key Elements:**
    *   **System Boundary:** A box drawn around all the use cases to represent the application itself.
    *   **Actors:** Stick figures (for humans) or boxes (for external systems) placed outside the system boundary. Primary actors are often on the left, secondary on the right.
    *   **Use Cases:** Ellipses with the use case title inside.
    *   **Association Lines:** Simple lines connecting an actor to a use case they are involved with. These lines do not have arrows and do not imply sequence.
*   **Important Notes:**
    *   This diagram is **not a substitute** for written use cases; they are complementary.
    *   It is a simple overview and communication tool, not a detailed flow diagram. It can be useful for finding missing pieces of the overall picture.

## User stories

*   **Definition:** A short, simple description of a feature told from the perspective of the user. It focuses on their goal and the reason for it.
*   **Format:** User stories are typically one or two sentences written on index cards, following this template:
    > **As a** `<type of user>`, **I want** `<some goal>` **so that** `<some reason or benefit>`.
*   **Example:** "As an astronaut, I want to heat up my food so that I can eat a warm meal."
*   **Key Differences from Use Cases:**
    *   **Purpose:** A user story is a **placeholder for a conversation**—a reminder to discuss a feature. A use case is a **record of a conversation** that has already happened, detailing the steps.
    *   **Length & Detail:** User stories are very short and concise. Use cases can be much longer and more detailed.
*   **Best Practices:**
    *   Focus on user intent; do not include UI descriptions or technical details.
    *   Avoid detailing alternate paths or exceptions.
    *   Keep them short and sweet.
*   **Relationship to Other Artifacts:** User stories, use cases, and functional requirements are all different tools. A project might use a combination of them, but not necessarily all three.
*   **Recommended Reading:** *User Stories Applied for Agile Software Development* by Mike Cohn.

## Challenge: Jukebox use cases

*   **Scenario:** Extend the previous jukebox design challenge.
*   **Task:** Write at least two use cases and two user stories for the space jukebox.
*   **Goal:** Practice creating these artifacts, with the format and level of detail left up to you.

## Solution: Jukebox use cases

*   **Example Use Case 1: Play a Song**
    *   **Actor:** User
    *   **Scenario (Paragraph):** The system identifies the user. The user browses albums, selects an album, browses songs, and selects a song. The jukebox plays the selected song.
*   **Example Use Case 2: Select Multiple Songs**
    *   **Actor:** User
    *   **Scenario (Numbered List):**
        1. System identifies user.
        2. User browses and selects a song.
        3. System begins playing the song.
        4. User continues browsing and selects a second song.
        5. System adds the second song to a **play queue**.
        6. System plays the second song after the first song finishes.
    *   *Note: This use case introduces the new concept of a "play queue."*
*   **Example User Stories:**
    *   "As a user, I want my song to be added to the front of the long play queue so that I don't have to wait hours to hear it."
    *   "As a user, I want to be identified without having to touch anything so I can use my hands to do other things."
    *   "As a user, I want to sort and browse songs by artist so that I can listen to every song by ABBA."
    *   "As the spaceship's commander, I want the ability to cancel other users' selections so I don't have to listen to disco all the way to the moon."
*   **Key Takeaway:** The process of writing user stories and use cases is valuable because it can help uncover new requirements (like the need for a "commander" or "administrator" role).

## Chapter Quiz

**Question 1 of 12**
When creating a use case diagram, what can you do to show each self-contained use case?

*   draw a box around each case
*   create a diagram for each use case
*   **draw an ellipse around each use case**
    > _Feedback: Correct_
*   connect the use cases with lines, not arrows

**Question 2 of 12**
What is wrong with the following scenario description. "The pedals were used to control speed and direction."

*   **It is passive and focuses on means instead of intent.**
    > _Feedback: Correct. There should be an actor with a clear goal or intent._
*   It does not explain how the pedals work.
*   It is too short and lacks detail.
*   It does not provide a desired speed and direction.

**Question 3 of 12**
What is the function of a use case diagram?

*   It shows the relationship between use cases.
*   It minimizes the number of actors required.
*   **It connects actors to use cases.**
    > _Feedback: Correct_
*   It identifies duplicative or unnecessary use cases.

**Question 4 of 12**
Why are arrows and numbers not found in use case diagrams?

*   Arrows and numbers are optional features of use case diagrams.
*   **Sequence and direction are not critical at this stage.**
    > _Feedback: Correct. Listing features and their connectivity is the function of a use case diagram._
*   The use of arrows and numbers would conflict with the scenario definitions.
*   Sequence and direction are not important in object-oriented programming.

**Question 5 of 12**
What is typically written on index cards, and describes a small scenario from a user perspective?

*   use case diagram
*   UML diagram
*   use case
*   **user story**
    > _Feedback: Correct_

**Question 6 of 12**
User stories are _____ than use cases.

*   more detailed and structured
*   **shorter and less detailed**
    > _Feedback: Correct_
*   longer and less formal
*   more anecdotal and personal

**Question 7 of 12**
Marge is working on a short and simple project involving inventory maintenance. Why should she write short use cases?

*   They are a minimum for project definition, but full use cases would be better.
*   They are really window dressing that will satisfy project administrators.
*   They are useful for documenting effort and billing for work on the project.
*   **They help identify problems but do not create the confusing work of full use cases.**
    > _Feedback: Correct. Casual use cases can be very helpful, but the use cases should be more fully developed for larger projects._

**Question 8 of 12**
Which sentence is most appropriate for a use case scenario?

*   Contrast and brightness are set by the user to achieve the most pleasing levels for indoor viewing.
*   **User adjusts contrast and brightness controls.**
    > _Feedback: Correct_
*   The users are prompted to employ an iterative algorithm for contrast and brightness adjustment.
*   Most users start by adjusting brightness to see the image better, and then adjust contrast, and then adjust brightness again, and so on.

**Question 9 of 12**
What is the role of the primary actor in a use case?

*   to decide if the scenario was a success
*   **to interact with the application to achieve the goal**
    > _Feedback: Correct_
*   to determine how many scenarios to create from the use case
*   to see if the use case can be used with multiple actors

**Question 10 of 12**
When are fully fleshed out cases most appropriate?

*   for time-limited projects
*   for single-user projects
*   **for large, complex projects**
    > _Feedback: Correct_
*   for simple, small projects

**Question 11 of 12**
You are creating a use case for an application that controls the dispensing of gasoline at a pump. Who is the primary actor in this scenario?

*   the company that supplies the gasoline
*   **the customer who uses the pump**
    > _Feedback: Correct_
*   the owner of the gas station who bought the pump
*   the designer of the application

**Question 12 of 12**
What distinguishes primary actors?

*   outcome evaluation
*   task termination
*   **application initiation**
    > _Feedback: Correct_
*   information routing

---

# 4. Domain Modeling

## Identifying the objects

*   **Purpose:** To create a conceptual model by identifying the most important objects in the application and their relationships. This step transitions from analysis (what to do) to design (how to do it).
*   **Technique: Noun Identification**
    1.  Go through use cases, user stories, and other written requirements.
    2.  Highlight or list all of the **nouns**.
    3.  Initially, don't analyze or judge the words. The goal is to gather a raw list of potential objects.
*   **Refining the List:**
    *   **Remove Duplicates:** Combine nouns that refer to the same concept (e.g., "it" referring to "asteroid").
    *   **Identify Attributes:** Some nouns might actually be attributes of other objects (e.g., "offscreen" could be an attribute of an "area" class). Remove these from the object list for now.
    *   **Questionable Objects:** If you are unsure whether a noun should be an object or an attribute (e.g., "direction"), it's better to **keep it** for now. It's easier to remove it later than to add it back in.
    *   **Remove "System":** Avoid making "system" an object. This often leads to a procedural mindset where one central object controls everything.
*   **Result:** A preliminary list of potential objects, which forms the beginning of a conceptual model. These can be represented as simple boxes with names.

## Identifying class relationships

*   **Purpose:** To indicate the main relationships or associations between the identified objects in the conceptual model.
*   **Technique:**
    1.  Draw lines between objects that have a relationship or interaction.
    2.  Refer back to use cases and user stories if the relationships aren't immediately obvious.
*   **Describing Relationships (Optional but useful):**
    *   Add a short, active verb phrase to the line to describe the relationship (e.g., "Spaceship *fires* Missile," "Player *steers* Asteroid").
*   **Describing Multiplicity (Optional):**
    *   Use UML notation to indicate how many objects are involved in a relationship (e.g., one-to-one, one-to-many `1..*`).
    *   Only add this detail if it's interesting or important enough to show on the diagram.
*   **Benefit:** Detailing these relationships makes it easier to understand which objects interact with each other, which helps in identifying necessary behaviors.

## Identifying class responsibilities

*   **Purpose:** To determine the responsibilities (behaviors) of each conceptual object, which helps solidify which ones will become actual classes.
*   **Technique: Verb Identification**
    1.  Go back to the use cases and user stories.
    2.  Pick out all the **verbs and verb phrases**. This will generate a starting list of potential responsibilities.
    3.  This list will need refinement (combining, splitting, or removing responsibilities).
*   **Assigning Responsibilities:**
    *   **Core Principle:** An object should be responsible for itself. It should manage its own state and perform its own actions.
    *   **Example:** The `Player` initiates the action of steering, but the `Asteroid` object should have the responsibility to actually move itself and change its own state. The `Player` *tells* the `Asteroid` what to do; it doesn't do it for the `Asteroid`.
*   **The "God Object" Anti-Pattern:**
    *   Avoid giving too much knowledge or too many responsibilities to a single object (like a `Player` or `System` object). This is a common mistake that leads to procedural-style code.
    *   Seeing phrases like "System spawns spaceship" should be interpreted as "some part of the system spawns the spaceship." The responsibility should be distributed.
    *   A central "master" object that controls everything else is a sign of a poor design. Distribute responsibilities among objects to make the application more maintainable.

## CRC cards

*   **Definition:** CRC stands for **C**lass, **R**esponsibility, **C**ollaboration. CRC cards are a simple, physical tool for object-oriented design.
*   **Format:**
    *   Drawn on index cards.
    *   **Class:** The name of the class is at the top.
    *   **Responsibilities:** A list of what the class needs to do, occupying the left two-thirds of the card.
    *   **Collaborators:** A list of other classes it interacts with, on the right-hand side.
*   **Process:**
    1.  Use the nouns from your requirements to identify potential classes and create a card for each.
    2.  Use the verbs to identify responsibilities and list them on the appropriate card.
    3.  As you work, identify which other classes are needed to fulfill a responsibility and list them as collaborators.
*   **Benefits of Physical Cards:**
    *   **Simplicity:** Easy to create, discuss, and throw away if you change your mind.
    *   **Collaboration:** Spreading them out on a table encourages discussion and helps in discovering natural collaborations as you physically group related cards.
    *   **Constraint:** If you need more than one card for a single class, it's a strong sign that the class has too much responsibility and may need to be redesigned.
*   **End Goal:** Whether you use CRC cards or a conceptual diagram, this phase should end with a clear understanding of the initial set of classes, their core responsibilities, and their relationships.

## Challenge: Jukebox conceptual model

*   **Scenario:** Extend the previous jukebox design challenge.
*   **Task:** Create a conceptual model for the space jukebox.
    1.  Identify nouns and verb phrases from the use cases/user stories to find potential objects and responsibilities.
    2.  Determine where responsibilities should reside and the relationships between objects.
*   **Format:** The solution can be a conceptual model diagram (boxes and lines), a stack of CRC cards, or a hybrid approach.

## Solution: Jukebox conceptual model

*   **Step 1: Identify Nouns (Potential Objects)**
    *   From the use cases and user stories, a list of nouns is gathered: `system`, `user`, `library`, `album`, `list`, `song`, `queue`, `commander`, `ability`, `selection`, `disco`, `moon`.
    *   **Cleanup:**
        *   Remove `system` (to avoid a god object).
        *   Remove irrelevant nouns like `disco` and `moon`.
        *   Remove `ability` (it's a behavior, not an object).
        *   Combine duplicates (`selection` is covered by `song`; `list` is covered by `album`).
        *   Rename `commander` to the more generic `admin`.
    *   **Final Object List:** `User`, `Library`, `Album`, `Song`, `Queue`, `Admin`.

*   **Step 2: Identify Verbs (Potential Responsibilities)**
    *   From the same sources, verb phrases are gathered: `identifies user`, `browses library`, `selects an album`, `plays a selected song`, `add song to queue`, `cancel other user selections`, etc.

*   **Step 3: Assign Responsibilities and Define Relationships**
    *   A hybrid model of CRC cards on a whiteboard with lines for relationships is used.
    *   **Library:**
        *   *Responsibility:* `display albums`
        *   *Relationship:* `User` *browses* `Library`; `Library` *contains* `Album`s.
    *   **Album:**
        *   *Responsibility:* `display songs`, `select song`
    *   **Song:**
        *   *Responsibility:* `play song`
    *   **Queue:**
        *   *Responsibilities:* `add song`, `get next song`, `remove song`, `identify user`.
    *   **Key Design Decision:** The responsibility to `identify user` is placed in the `Queue` object. Why? Because the `Queue` is the object that *cares about* the user's identity in order to reorder songs correctly. This avoids creating a central `System` object for this task.

## Chapter Quiz

**Question 1 of 10**
How can one avoid assigning too many responsibilities to a single object?

*   Create two system-like objects.
*   Reduce the overall number of responsibilities.
*   Assign the most responsibility to the system.
*   **Require objects to take care of themselves to a greater extent.**
    > _Feedback: Correct_

**Question 2 of 10**
What common problem should new programmers avoid when designing a program?

*   **creating a god object**
    > _Feedback: Correct_
*   distributing responsibilities among different classes
*   assigning properties to objects
*   looking for verbs to identify potential class responsibilities

**Question 3 of 10**
In addition to responsibilities, which should be listed on CRC cards?

*   parents
*   **interacting classes**
    > _Feedback: Correct_
*   attributes
*   subclasses

**Question 4 of 10**
Which design tool contains the same information as a conceptual object diagram?

*   user stories
*   an object list
*   use cases
*   **CRC cards**
    > _Feedback: Correct_

**Question 5 of 10**
After analysis and use cases are completed, what is the first step in the design phase of a project?

*   deciding how to program the application
*   creating user stories
*   **creating a conceptual model**
    > _Feedback: Correct_
*   defining the requirements

**Question 6 of 10**
When is there a relationship between two objects?

*   when two objects are instantiated from the same class
*   **when one object depends on or affects the other object**
    > _Feedback: Correct_
*   when one object replaces the other object
*   when the objects are very similar in attributes

**Question 7 of 10**
When diagramming relationships between objects, what is the UML notation that represents one or more objects?

*   **1…\***
    > _Feedback: Correct_
*   0->1
*   ---1
*   1…1

**Question 8 of 10**
How can you identify candidates for objects?

*   by listing all of the verbs in the user stories
*   by listing all of the scenarios
*   by listing all of the actors in the use cases
*   **by listing all of the nouns in the user stories**
    > _Feedback: Correct. Objects are nouns; they are things._

**Question 9 of 10**
In the following CRC card, what does `card` represent?
```
Wallet
receive                        cash
receive                        card
withdraw                     cash
withdraw                     card
```
*   a case
*   **a collaborator**
    > _Feedback: Correct. The wallet interacts with the card and cash supplies._
*   a responsibility
*   an attribute
    > _Feedback: Incorrect. CRC cards do not necessarily contain attributes._

**Question 10 of 10**
Which words in the following list are candidates for objects: trumpet, clean, enrage, leaf, tree, collapse, active, or lively?

*   leaf and tree
*   **trumpet, leaf, and tree**
    > _Feedback: Correct_
*   clean, active, and lively
*   clean, collapse, and enrage

---

# 5. Class Diagrams

## Creating class diagrams: Attributes

*   **Purpose:** To create a formal UML class diagram to visually represent the classes identified in the conceptual model.
*   **Class Naming:**
    *   Use the singular form (e.g., `Asteroid`, not `Asteroids`).
    *   Use an uppercase first letter (PascalCase or UpperCamelCase).
*   **Attribute Naming:**
    *   Use a consistent naming convention, like camelCase (e.g., `shieldStrength`, `callSign`).
*   **Defining Attributes:**
    *   **Name:** The name of the attribute.
    *   **Data Type (Optional):** You can suggest a data type by adding a colon after the name (e.g., `callSign: String`). Don't get hung up on the exact type (e.g., 16-bit vs. 32-bit integer); the general type is sufficient for the design phase.
    *   **Default Value (Optional):** You can specify a default value using an equals sign after the data type (e.g., `shieldActive: Boolean = true`).
*   **Abstraction is Key:** At this stage, you don't need to decide on every implementation detail. For example, a `position` attribute could be a custom `Coordinate` class, two separate `x` and `y` attributes, or a tuple. The diagram just needs to convey the concept.

## Creating class diagrams: Behaviors

*   **Purpose:** To add behaviors (methods) to the class diagram, based on the responsibilities identified in the conceptual model or CRC cards.
*   **Method Naming:**
    *   Use camelCase.
    *   Name them as short verb phrases (e.g., `reduceShield`, `getShieldStrength`).
    *   It's common practice to use "get" and "set" prefixes for methods that retrieve or modify attributes.
*   **Defining Methods:**
    *   **Parameters:** List any input parameters inside parentheses `()`.
    *   **Return Type (Optional):** Indicate the return type with a colon after the parentheses (e.g., `getShieldStrength(): Integer`).
*   **Visibility (Encapsulation):**
    *   Use plus (`+`) for **public** members (accessible by other objects).
    *   Use minus (`-`) for **private** members (only accessible from within the class itself).
    *   **Rule:** Leave as many attributes and methods private as possible. Only make something public if another object absolutely needs to use it.
*   **Focus on Behavior, Not Just Data:**
    *   A common mistake is to jump to creating classes by only listing their attributes (data). This is the wrong initial focus.
    *   If you find your classes have lots of attributes but few behaviors, you are likely thinking of them as simple data structures, not objects. Revisit the responsibilities.
    *   The focus should be on **what objects do**, not just what they are.

## Converting class diagrams into code

*   **Purpose:** To show how the high-level concepts in a UML class diagram can be translated into various object-oriented programming languages, despite differences in syntax.
*   **Example: `Spaceship` Class**
    *   **UML:**
        *   Attributes: `+ callSign: String`, `- shieldStrength: Integer`
        *   Methods: `+ fireMissile(): String`, `+ reduceShield(amount: Integer)`
    *   **Java/C#:** Use `public class Spaceship` with curly braces. Keywords `public` and `private` control visibility. Instance variables are declared inside the class.
    *   **Swift:** Also uses curly braces but has different syntax for variable declaration (`var callSign: String`).
    *   **Python:** Uses indentation instead of curly braces. Instance variables are typically declared inside a special `__init__` method. Python relies on naming conventions (e.g., an underscore prefix `_shieldStrength`) to indicate a variable should be treated as private.
    *   **Ruby:** Also uses indentation. The `@` symbol indicates an instance variable.
*   **Key Takeaway:** While syntax varies, the core concepts of classes, attributes, methods, and visibility are consistent across most OO languages.

## Instantiating classes

*   **Concept:** A class is a blueprint. To use it, you must **instantiate** it to create an object (an instance of the class).
*   **Instantiation Keyword:** Many languages (Java, C#, C++, Ruby) use the keyword `new`. Others (Python, Swift) do not.
*   **The Constructor:**
    *   A special method that is automatically called when an object is instantiated.
    *   Its purpose is to initialize the object and set its initial state.
    *   In many languages (Java, C#), the constructor has the same name as the class and has no return type.
    *   Using a constructor ensures an object is created in a valid, meaningful state, rather than relying on potentially problematic default values (like `null` or `0`).
    *   In UML, a constructor is represented as a method with the same name as the class.

## Class with multiple constructors

*   **Method Overloading:** Most languages allow a class to have multiple methods with the same name, as long as they have a different set of input parameters. This is called **overloading**.
*   **Multiple Constructors:** You can apply overloading to constructors to provide different ways of instantiating an object.
    *   **Example:** One `Spaceship()` constructor with no parameters (a "default constructor") that creates a "nameless ship," and a second `Spaceship(name: String)` constructor that takes a name as input.
*   **Benefit:** Gives flexibility in how objects are created and is crucial for ensuring complex objects are not created in an invalid state.
*   **Destructors:**
    *   The opposite of a constructor; a method that gets called when an object is destroyed.
    *   Used to release resources the object might be holding (e.g., closing a file or a database connection).
    *   Languages with garbage collection often use a "finalizer" instead, but the concept is the same.

## Static attributes and methods

*   **Instance Variables:** Each object (instance) gets its own separate copy of an instance variable. Changing it in one object does not affect others.
*   **Static Variables (or Class/Shared Variables):**
    *   There is only **one copy** of a static variable, which is **shared** across all objects of that class.
    *   If one object changes the static variable, the change is visible to all other objects of that class.
    *   This is useful for values that should be the same for all instances, like a game's `difficulty` setting.
    *   It is *not* a global variable; it is still encapsulated within the class.
*   **Static Methods:**
    *   Like static variables, there is only one copy of a static method, belonging to the class itself, not to any particular instance.
    *   They can only access static variables, not instance variables.
*   **Accessing Static Members:** Static members are accessed using the **class name**, not an instance name (e.g., `Spaceship.toughness`, not `myShip.toughness`).
*   **UML Notation:** Static members (attributes and methods) are typically denoted with an **underline**.

## Challenge: Jukebox class diagrams

*   **Scenario:** Extend the jukebox design challenge.
*   **Task:** Create a UML class diagram based on the previously created conceptual model.
*   **Goal:**
    *   Think about the attributes and methods each class needs to accomplish its responsibilities.
    *   Make assumptions where necessary.
    *   This is an open-ended challenge with many possible solutions.

## Solution: Jukebox class diagrams

*   **Approach:** Convert the conceptual model objects (`Song`, `Album`, `Library`, `Queue`, `User`, `Admin`) into formal class diagrams.
*   **`Song` Class:**
    *   Attributes: `- title: String`, `- artist: String`. (Private)
    *   Methods: `+ getTitle(): String`, `+ getArtist(): String`, `+ play()`.
*   **`Album` Class:**
    *   Attributes: `- title: String`, `- songs: Song[1..*]`. (A collection of one or more Song objects).
    *   Methods: `+ getTitles(): String[]`, `+ getSong(title: String): Song`.
*   **`Library` Class:**
    *   Similar to the `Album` class, but it contains a collection of `Album` objects instead of `Song` objects.
*   **`Queue` Class:**
    *   A collection of songs, but with different responsibilities than an `Album`.
    *   Methods: `+ addSong(song: Song, userId: String)`, `+ getNextSong(): Song`, `+ removeSong(song: Song)`.
*   **`User` and `Admin` Classes:**
    *   `User` class is given an `id` attribute and a `getId()` method.
    *   The `addSong` method in the `Queue` class is updated to take the user's ID as a parameter. This fulfills the queue's responsibility to "identify the user" without needing a separate method for it.
    *   The `Admin` class is given an `id` and methods like `createNewUser()` and `manageQueue()`.
*   **Key Takeaway:** This is just one of many possible ways to design the system. The process involves making logical assumptions to translate high-level responsibilities into concrete attributes and methods.

## Chapter Quiz

**Question 1 of 22**
In which language is the following class specification written?
```python
class Dog():
      def __init__(self):
#instance variables
      self.breed=""
       self.weight=50
#methods
```
*   C#
*   **Python**
    > _Feedback: Correct. Python does not use curly braces nor terminal semicolons._
*   Swift
*   Ruby

**Question 2 of 22**
Instantiating a class in many languages looks similar to that in C++, `DinnerPlate *myPlate = new DinnerPlate()`. What is the main difference between Python and Swift for achieving the same goal?

*   the use of colons
*   the absence of =
*   the use of terminal semicolons
*   **the absence of the word new**
    > _Feedback: Correct. Swift uses `let`, but neither Swift nor Python use `new`._

**Question 3 of 22**
A class Dog has the following constructors:
```java
public Dog() 
public Dog(String breed)
public Dog(int weight)
```
How would you instantiate a Dog with the weight set in Java?

*   `Dog Dog = new Dog(Fido)`
*   **`Dog Fido = new Dog(63);`**
    > _Feedback: Correct. The dog's weight is set to 63._
*   `Dog Fido = new Dog(Mutt);`
*   `Dog Fido = Dog(63);`

**Question 4 of 22**
Which languages require the use of static to declare class-wide variables or methods?

*   **Java and C#**
    > _Feedback: Correct. The word `static` can be confusing, because it implies that there is only one instance._
*   Ruby and Swift
*   Python and C++
*   all of these answers

**Question 5 of 22**
Which class diagram correctly specifies data types and default values?

*   ```
    Asteroid
    size, Integer: 5
    position, Coordinate:(0.5,0.5,0.6)
    velocity, Coordinate:(1,0,0)
    ```
*   ```
    Asteroid
    size: Integer: 5
    position: Coordinate:(0.5,0.5,0.6)
    velocity: Coordinate:(1,0,0)
    ```
*   ```
    Asteroid
    size, Integer, 5
    position, Coordinate,(0.5,0.5,0.6)
    velocity, Coordinate,(1,0,0)
    ```
*   **```
    Asteroid
    size: Integer=5
    position: Coordinate=(0.5,0.5,0.6)
    velocity: Coordinate=(1,0,0)
    ```**
    > _Feedback: Correct. It helps to have standard syntax even in UML, as it makes later jobs easier._

**Question 6 of 22**
Which is the function of a finalizer or destructor?

*   to delete a variable name
*   to hold space, even after an object is no longer being used
*   to reset an attribute value
*   **to relinquish resources that are no longer needed**
    > _Feedback: Correct_

**Question 7 of 22**
How would you declare a class variable in Ruby named maxScore?

*   **`@@maxScore`**
    > _Feedback: Correct_
*   `public maxScore`
*   `public static maxScore`
*   `@maxScore`
    > _Feedback: Incorrect_

**Question 8 of 22**
A class diagram contains the following behavior specifications. Which data type is returned by the `accelerate()` behavior?
```
move(Direction)
accelerate(Acceleration): Velocity
setPosition(Coordinate)
explodePieces(Integer)
```
*   **Velocity**
    > _Feedback: Correct. The return data type is indicated after the colon._
*   Integer
*   Acceleration
*   Coordinate

**Question 9 of 22**
A class diagram contains the following behavior specifications. The `explodePieces()` behavior breaks up an object into a number of pieces. What is the data type for that number? The answer will take the place of the '???'.
```
move(Direction)
accelerate(Acceleration): Velocity
setPosition(Coordinate)
explodePieces(???)
```
*   Acceleration
*   Direction
    > _Feedback: Incorrect. This is the data type for the `move()` argument._
*   **Integer**
    > _Feedback: Correct. An argument is contained within parentheses._
*   Coordinate

**Question 10 of 22**
For which case would the use of a static attribute be appropriate?

*   the color of each house in a small neighborhood
*   **the weather conditions for each house in a small neighborhood**
    > _Feedback: Correct_
*   the number of people in each house in a small neighborhood
*   the lot size for each house in a small neighborhood

**Question 11 of 22**
In which language would you find the following declaration of an instance variable?
```swift
private var _size: Int
```
*   Java
*   Python
*   C#
*   **Swift**
    > _Feedback: Correct. The use of `var` is unique._

**Question 12 of 22**
What other terminology is used for variables that are declared static?

*   unchanging
    > _Feedback: Incorrect. It is a variable, so it can change._
*   **class or shared**
    > _Feedback: Correct. Class or shared will imply that there is one variable used across the whole class._
*   discrete or stepped
*   permanent

**Question 13 of 22**
What does the value (0.5,0.5,0.5) indicate in the class diagram specification `position: Coordinate = (0.5,0.5,0.5)`?

*   a prohibited value of the position attribute
*   the size of the position array
*   an increment of the position attribute value
*   **a default value of the position attribute**
    > _Feedback: Correct_

**Question 14 of 22**
In a UML class diagram, how would you write an attribute called "name" that is a String data type and has a default value of Jane?

*   `String Jane = name`
    > _Feedback: Incorrect_
*   `String Jane as name`
*   `Jane: String = name`
*   **`name: String = "Jane"`**
    > _Feedback: Correct_

**Question 15 of 22**
In the class diagram specification `setSize(Integer):Integer`, to what do the integer specifications refer?

*   the name of the attribute to be evaluated or set
*   the amount of memory to be reserved for storage
*   **the data types for the argument, and return of the function setSize**
    > _Feedback: Correct_
*   the default values for the function setSize

**Question 16 of 22**
Which line of Java code declares a public method called getName that accepts no arguments and returns a String value?

*   **`public String getName()`**
    > _Feedback: Correct_
*   `private String getName()`
*   `public getName(void)`
*   `public void getName(String)`

**Question 17 of 22**
Which line of Java code will instantiate a new object named Student from the Person class?

*   `new Student = Person(Person)`
*   `Student Person = new Person()`
    > _Feedback: Incorrect_
*   `new Person = Person(Student)`
*   **`Person Student = new Person()`**
    > _Feedback: Correct_

**Question 18 of 22**
Which is the purpose of a constructor?

*   **to initialize attribute values**
    > _Feedback: Correct_
*   to test all behaviors associated with a class
*   to reserve memory
*   to link attributes into shared storage

**Question 19 of 22**
The class Person has the following constructors:
```java
public Person()
public Person(String name)
public Person(int age)
```
Which one will be called when a new person is created with the following command?
```java
Person Steve = new Person(39)
```
*   **`Person(int age)`**
    > _Feedback: Correct_
*   `Person(String name)`
*   `Person()`
*   all of the constructors will be called

**Question 20 of 22**
Which restrictions apply to the use of static methods?

*   They cannot act on static variables, but only instance variables.
*   They cannot change the values of any variables.
*   They can only act on global variables.
*   **They cannot act on instance variables, but only static variables.**
    > _Feedback: Correct. Static methods can be applied to class-wide variables._

**Question 21 of 22**
What does it mean if a class attribute is private?

*   It can be accessed from other classes.
*   The attribute cannot be changed.
*   **It can only be accessed from within the class.**
    > _Feedback: Correct_
*   The attribute is only visible to the programmer that created it.

**Question 22 of 22**
How do you declare a private variable in Python?

*   **Python does not have private or public variables.**
    > _Feedback: Correct_
*   Use a minus sign before the variable name.
*   Use a leading underscore in the variable name.
    > _Feedback: Incorrect_
*   All variables are private in Python.

---

# 6. Inheritance and Composition

## Identifying inheritance situations

*   **Definition:** Inheritance allows a subclass (or child class) to inherit the attributes and methods of a superclass (or parent class), enabling code reuse and easier maintenance.
*   **The "is a" Test:** The easiest way to identify an inheritance relationship is to use the phrase "is a" (or "is a kind of" / "is a type of").
    *   **Valid:** "A `Starfighter` is a `Spaceship`." "A `CargoShuttle` is a type of `Spaceship`." This suggests `Starfighter` and `CargoShuttle` can be subclasses of a `Spaceship` superclass.
    *   **Invalid:** "A `CargoShuttle` is a `Starfighter`" (no). "Cargo is a `CargoShuttle`" (no). This indicates a different relationship, likely a "has a" relationship.
*   **Process:**
    1.  Look for classes with common attributes and methods.
    2.  Extract these common elements into a new, more general superclass.
    3.  The original classes become subclasses that inherit from the new superclass.
*   **UML Notation:** Inheritance is shown with a solid line and a large, open, wedge-shaped arrow pointing from the subclass to the superclass.
*   **Method Overriding:** A subclass can provide its own unique implementation for a method that it inherited from its superclass.
*   **Caution:** New developers often over-emphasize inheritance. Don't force it; inheritance opportunities usually announce themselves naturally.

## Using inheritance

*   **Purpose:** To show how the concept of inheritance is implemented with slightly different syntax across various programming languages.
*   **Language Syntax for Inheritance:**
    *   **Java:** `class CargoShuttle extends Spaceship`
    *   **C# / C++ / Swift:** `class CargoShuttle : Spaceship`
    *   **Python:** `class CargoShuttle(Spaceship):`
    *   **Ruby:** `class CargoShuttle < Spaceship`
*   **Calling Superclass Methods:** It's common for a subclass to need to call a method from its parent.
    *   Most languages use the keyword `super` (e.g., `super.setShield()`).
    *   .NET languages (like C#) use the keyword `base`.
    *   C++ requires the explicit name of the superclass because it allows for multiple inheritance.

## Abstract and concrete classes

*   **Abstract Class:**
    *   A class that exists only to be inherited from; it **cannot be instantiated** on its own.
    *   It must contain at least one **abstract method**—a method that is declared but not implemented. The implementation is left to the subclasses.
    *   It can also contain fully implemented methods that are shared by all subclasses.
    *   **UML Notation:** The names of abstract classes and abstract methods are written in *italics*.
*   **Concrete Class:**
    *   A class that can be instantiated.
    *   A subclass that inherits from an abstract class and implements all of its abstract methods is a concrete class.
*   **Keywords:**
    *   Some languages (Java, C#) use keywords like `abstract` to enforce these rules.
    *   The keyword `final` can be used to declare a class as concrete and prevent it from being inherited from.
    *   The main benefit of these keywords is to clearly communicate the intended use of a class to other programmers.

## Interfaces

*   **Definition:** An interface is a programming structure that declares a set of method signatures but contains **no implementation**. It's a "contract" that a class can agree to fulfill.
*   **Purpose:** An interface defines a **capability**. A class that *implements* an interface promises to provide the actual code for all the methods defined in that interface.
*   **Interface vs. Abstract Class:**
    *   An **abstract class** defines a *type* (an "is a" relationship). `CargoShuttle` is a `Spaceship`.
    *   An **interface** defines a *capability*. An `Asteroid` is not a `Spaceship`, but both can be `Movable` and `Drawable`.
    *   A class can only inherit from one superclass, but it can **implement multiple interfaces**.
*   **UML Notation:**
    *   An interface is shown in a box with an `<<interface>>` tag.
    *   A class implementing an interface is connected with a **dashed line** and a large, open, wedge-shaped arrow.
*   **Best Practice:** "Program to an interface, not to an implementation." This promotes flexibility and is often a more future-friendly approach than inheritance.

## Aggregation

*   **Definition:** A type of object relationship where one object is built from or contains other objects. It is known as a **"has a"** or **"uses a"** relationship.
*   **Key Characteristic:** The contained objects have **independent lifetimes**. If the container object is destroyed, the objects it contains are not destroyed.
*   **Example:** A `Fleet` *has many* `Spaceship`s. If the `Fleet` is disbanded, the individual `Spaceship`s continue to exist.
*   **UML Notation:** A solid line with an **unfilled diamond** on the side of the container object.
*   Multiplicity can be used to show how many objects are contained (e.g., `*` for zero to many).

## Composition

*   **Definition:** A stricter form of aggregation that implies **ownership**. It is a "is composed of" or **"owns a"** relationship.
*   **Key Characteristic:** The contained objects' lifetimes are **dependent** on the owner object. If the owning object is destroyed, the contained objects are destroyed with it.
*   **Example:** A `Spaceship` *is composed of* an `Engine` and a `Shield`. If the `Spaceship` is destroyed, its `Engine` and `Shield` are also destroyed.
*   **UML Notation:** A solid line with a **filled-in diamond** on the side of the owning object.
*   **Importance:** Composition is often worth showing in a diagram because it implies the owner is responsible for the creation and destruction of its parts (in its constructor and destructor).

## Challenge: Jukebox class relationships

*   **Scenario:** The final extension of the jukebox design challenge.
*   **Task:** Identify the relationships (inheritance, interfaces, aggregation, composition) between the existing jukebox classes and modify the class diagrams to reflect them.
*   **Goal:** This may require adding/removing attributes and methods or even creating new classes.

## Solution: Jukebox class relationships

*   **Inheritance:**
    *   An `Admin` **is a** type of `User` with extra permissions.
    *   **Action:** Create a `User` superclass. The `Admin` class becomes a subclass and inherits the `id` attribute and `getId()` method from `User`. This avoids code duplication.
*   **Rejected Inheritance:**
    *   They considered making `Library` and `Album` inherit from a common `Collection` class because they share similar "collection" behaviors.
    *   **Decision:** They rejected this idea because it was an over-abstraction that added unnecessary complexity without providing significant benefit. This highlights that inheritance shouldn't be forced.
*   **Aggregation:**
    *   A `Library` **has** one or more `Album`s. (Aggregation)
    *   An `Album` **has** one or more `Song`s. (Aggregation)
    *   A `Queue` **has** zero or more `Song`s. (Aggregation)
*   **Final Result:** The final class diagram incorporates these relationships, providing a solid, well-designed starting point for implementation. It is understood that this design may still evolve as coding begins.

## Chapter Quiz

**Question 1 of 16**
Which relationship is a good candidate for superclass and subclass?

*   **utensil-fork**
    > _Feedback: Correct_
*   tires-truck
*   rock-stone
*   toes-feet

**Question 2 of 16**
What does this line of Java code declare?
```java
public class Apple extends Fruit {
```
*   that Fruit is an abstract class
*   a new class Fruit that is a child class of Apple
*   **a new class Apple that is inherited from the class Fruit**
    > _Feedback: Correct_
*   that the Apple constructor should be used to create a Fruit object

**Question 3 of 16**
Why is the syntax for inheritance in C++ different from most other languages?

*   **because a class can inherit from multiple levels in C++**
    > _Feedback: Correct_
*   because of sibling extensions in C++
*   because of the abbreviated syntax priority in C++
*   because C++ makes use of colons and semicolons instead of arrows and periods

**Question 4 of 16**
Which line of code will define a C# abstract class named School?

*   `@@School {`
*   `abstract School {`
*   `class School {`
*   **`abstract class School {`**
    > _Feedback: Correct_

**Question 5 of 16**
Which concept of object-oriented programming is displayed by using the "is a kind of" comparison between 2 classes?

*   **inheritance**
    > _Feedback: Correct_
*   abstraction
*   encapsulation
*   polymorphism

**Question 6 of 16**
A concrete class has no _____.

*   parents
*   attributes
*   methods
*   **children**
    > _Feedback: Correct_

**Question 7 of 16**
Why would you create an abstract class, if it can have no real instances?

*   **to avoid redundant coding in child classes**
    > _Feedback: Correct_
*   to prevent unwanted method implementation
*   to reserve memory for an unspecified class type
*   to explore a hypothetical class

**Question 8 of 16**
An aggregation is a _____.

*   group of methods
*   **collection of objects**
    > _Feedback: Correct_
*   class of resources
*   list of children

**Question 9 of 16**
What form of aggregation implies ownership, and that the lifetime of an object is dependent on another object's existence?

*   dependence
*   inheritance
*   **composition**
    > _Feedback: Correct_
*   abstraction

**Question 10 of 16**
How are the contents of a composition different from those of an aggregation?

*   **If a composition dies, the contents die.**
    > _Feedback: Correct_
*   An aggregation contains only abstract classes.
*   An aggregation consists of interfaces only.
*   The contents of a composition are all siblings.

**Question 11 of 16**
In Java, how would you define an interface named Box that contains two methods named Open and Close that don't accept or return any variables?
```java
interface Box {
    void Open();
    void Close();
```
*   **Correct**
*   ```java
    class interface Box {
        void Open();
        void Close();
    ```
*   ```java
    class Box implements interface {
        void Open();
        void Close();
    ```
*   ```java
    class Box {
        void Open();
        void Close();
    ```

**Question 12 of 16**
What do most languages have in common for referring to a method defined in the parent class?

*   the use of : in the method name
*   **the use of super in the prefix to the method name**
    > _Feedback: Correct. The word `super` is used for the common need for code within a subclass, to call a method that was originally defined in the super class._
*   specification of the parent class name in the method name
*   specification of the instance name

**Question 13 of 16**
Why should you use abstract and final in class definitions?

*   to allow instantiation
*   to allow inheritance
*   **to better communicate intentions**
    > _Feedback: Correct. Their use makes the code easier to read and maintain._
*   to define methods

**Question 14 of 16**
When is an interface used instead of an abstract class?

*   when multiple constructors are used
*   **when you need to describe the capabilities of a class**
    > _Feedback: Correct_
*   when parents are shared
*   when multiple subclasses exist

**Question 15 of 16**
Which relationship between classes is referred to as a "has a" relationship?

*   **aggregation**
    > _Feedback: Correct_
*   inheritance
*   many-to-many
*   one-to-many

**Question 16 of 16**
Which representation is correct UML for the interface Edible?

*   ```
    Edible <interface>
    beEaten()
    ```
*   ```
    <<interface>>
    Edible
    beEaten()
    ```
    > _Feedback: Correct. We represent an interface using a box that looks similar to a class, and include a tag with double angle quotes to indicate an interface._
*   ```
    Edible
    beEaten()
    ```
*   ```
    interface
    Edible
    ```

---

# 7. Software Development

## OOP support in different languages

*   **Purpose:** To highlight the differences in how common object-oriented languages implement core OOP concepts. The underlying design principles remain the same regardless of the language.
*   **Inheritance:**
    *   **Single Inheritance:** Most languages (Java, C#, Swift) only allow a class to inherit from one superclass.
    *   **Multiple Inheritance:** C++ and Python allow a class to inherit from more than one superclass.
    *   **Mixins (Ruby):** A feature that allows combining objects, which can be seen as a form of composition.
    *   **Prototypes (JavaScript):** JavaScript is less formal and doesn't use classes. It uses prototypes, allowing for more dynamic objects where properties can be added or removed at runtime.
*   **Typing:**
    *   **Statically Typed (most compiled languages):** The data type of all variables must be specified by the developer at compile time.
    *   **Dynamically Typed (most scripting languages like Python, Ruby, JS):** The type of a variable does not need to be specified. This allows for faster, more flexible development but can make bug-tracking more difficult.
*   **Interfaces:**
    *   Not supported in languages that are dynamically typed (Python, Ruby, JS) or that allow multiple inheritance (C++).
    *   In these languages, a similar concept can be implemented using an abstract class with only abstract methods.
*   **Language Variations:**
    *   Many variations exist that combine features, like **Jython** (Python on the Java platform) and **TypeScript** (a statically-typed version of JavaScript).

## General development principles

*   **SOLID Principles:** A set of five interrelated principles to make software more understandable, flexible, and maintainable.
    *   **Single Responsibility Principle:** A class should have only one primary responsibility, one reason to exist. This warns against creating "God objects" that do too many unrelated things. Big classes should be split into smaller, more focused ones.
*   **DRY (Don't Repeat Yourself):**
    *   Avoid copying and pasting large sections of code. If a mistake is found, it will have to be fixed in every copied location.
    *   This principle also applies to documentation, diagrams, and database schemas. There should be a single source of truth.
*   **YAGNI (You Ain't Gonna Need It):**
    *   Avoid over-engineering and adding features or hooks for every possible future scenario.
    *   Abstracting too much leads to code bloat, more testing, and more debugging for features that may never be used.
*   **Code Smells:**
    *   These are indicators of potential problems in code. The code might compile and work, but something "doesn't pass the sniff test" (e.g., duplicated code, God objects, unnecessary complexity).
    *   **Static analysis tools** can plug into an IDE to automatically detect some of these code smells.

## Software testing

*   **Importance of Testing:**
    *   It's not enough to test that the software meets requirements. You must also test for unexpected user behavior.
    *   Users may misunderstand instructions, make typos, or maliciously try to break the application.
*   **Usability Considerations:**
    *   Software should be intuitive and provide clear guidance.
    *   **Example:** If a phone number input field requires dashes, but the user enters only numbers, the application should handle it gracefully and provide helpful error messages, not just reject the input.
*   **Automated Testing:**
    *   Manually testing every scenario repeatedly is tedious and impractical.
    *   **Automated unit tests and system tests** are invaluable. They can be run repeatedly to ensure that changes and new features haven't broken existing functionality.
*   **Refactoring and Regression:**
    *   **Refactoring** (improving the internal structure of code without changing its external behavior) is a natural part of software maintenance.
    *   A common problem is that refactoring can introduce **regressions**—bugs in features that previously worked.
    *   A well-established automated testing system is crucial for catching regressions before they reach the user.

## Design patterns

*   **Definition:** Common, repeatable, and proven solutions for solving recurring software design problems. They are templates or best practices, not exact lines of code.
*   **Purpose:** To help structure code in a smart, flexible, maintainable, and extensible way, reducing the need for major refactoring later.
*   **Example Scenarios:**
    *   **Problem:** The game hard-codes which enemy ships appear. Adding new types is difficult.
    *   **Pattern:** The **Factory Method** pattern could provide a structured way to instantiate different types of objects based on context (like the current level).
    *   **Problem:** A "rewind" feature is requested to restore the game to a previous state.
    *   **Pattern:** The **Memento** pattern outlines a proven approach for saving and restoring an object's state.
*   **"Gang of Four" (GoF) Book:**
    *   The seminal book *Design Patterns* by four authors introduced 23 design patterns, organized into three groups:
        1.  **Creational Patterns:** Focus on object instantiation, providing flexibility in how objects are created (e.g., Factory Method).
        2.  **Structural Patterns:** Describe how classes are designed using concepts like inheritance and composition to add functionality.
        3.  **Behavioral Patterns:** Concerned with communication between objects (e.g., Memento).
*   **Recommended Reading:** *Design Patterns* (GoF) and *Head First Design Patterns*.

## Chapter Quiz

**Question 1 of 8**
You have developed an application with three classes of objects. One of the classes has 50 subclasses. What would style critics call this class?

*   a bloat class
*   **a god object**
    > _Feedback: Correct. God objects do a lot of things that are not related to each other, and you should consider breaking up the class into two or more classes._
*   a parent
*   a super object

**Question 2 of 8**
Which group of design patterns describes how inheritance and aggregation can be used to provide additional functionality?

*   **structural**
    > _Feedback: Correct_
*   creational
*   behavioral
*   defining

**Question 3 of 8**
Why should one use a design pattern when possible?

*   It will enable the use of shared code.
*   **It will likely result in code that is more easily extensible and maintainable.**
    > _Feedback: Correct_
*   It will result in a more compact product.
*   It will speed initial development.

**Question 4 of 8**
How does dynamic typing hinder troubleshooting?

*   The dynamic variables can only assume limited values.
*   Storage is fixed for dynamic variables.
*   **It can be difficult to identify variables that are incorrectly typed.**
    > _Feedback: Correct_
*   Static variables are more flexible than dynamic variables.

**Question 5 of 8**
What is an example of a code smell?

*   not using enough abstraction
*   strong documentation
*   distributing work among many classes
*   **duplicate code**
    > _Feedback: Correct_

**Question 6 of 8**
Why is code duplication so insidious?

*   The duplication uses unnecessary space.
*   Duplication can cause intellectual property concerns.
*   **One has to maintain all the duplicates.**
    > _Feedback: Correct_
*   Duplication is easy to hide.

**Question 7 of 8**
What is a good way to help users navigate a software application?

*   creating a chat room so users can communicate with each other
*   **providing proper error messages and prompts**
    > _Feedback: Correct_
*   asking the user to enter redundant information
*   making sure that the application is secure

**Question 8 of 8**
Which language is compiled and is statically typed?

*   Python
*   Ruby
*   JavaScript
*   **C++**
    > _Feedback: Correct_
