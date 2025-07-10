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
