# Principles of Software Construction <small>Objects, Design, and Concurrency</small>

## Overview

Software engineers today are less likely to design data structures and algorithms from scratch and more likely to build systems from library and framework components. In this course, students engage with concepts related to the construction of software systems at scale, building on their understanding of the basic building blocks of data structures, algorithms, program structures, and computer structures. The course covers technical topics in four areas: (1) concepts of design for complex systems, (2) object oriented programming, (3) static and dynamic analysis for programs, and (4) concurrent and distributed software. Student assignments involve engagement with complex software such as distributed massively multi-player game systems and frameworks for graphical user interaction.

After completing this course, students will:

- Be comfortable with object-oriented concepts and with programming in the Java or JavaScript language
- Have experience designing medium-scale systems with patterns
- Have experience testing and analyzing your software
- Understand principles of concurrency and distributed systems

See a more detailed list of [learning goals](https://cmu-17-214.github.io/f2024/learninggoals.html) describing what we want students to know or be able to do by the end of the semester. We evaluate whether learning goals have been achieved through assignments and exams.

### Coordinates

M/W 11:00 - 12:20 p.m. in [POS](https://www.cmu.edu/admission/sites/default/files/inline-files/Carnegie%20Mellon%20University%20Campus%20Map.pdf) A35

**[Jeremy Lacomis](https://jeremylacomis.com/)**, [TCS](https://www.cmu.edu/admission/sites/default/files/inline-files/Carnegie%20Mellon%20University%20Campus%20Map.pdf) 362, office hours: see calendar

**[Claire Le Goues](https://clairelegoues.com/)**, [TCS](https://www.cmu.edu/admission/sites/default/files/inline-files/Carnegie%20Mellon%20University%20Campus%20Map.pdf) 363, office hours: see calendar

Our TAs also provide an additional 15h of office hours each week; see details in the calendar.

The instructors have an open door policy: If the instructors' office doors are open and no-one else is meeting with us, we are happy to answer any course-related questions. Feel free to email us for appointments; we are also available over Zoom.

## <a name=calendar></a>Calendar

<iframe src="https://calendar.google.com/calendar/embed?src=c_2a6e790c6ae7fd610c0f21536ff9b4a7447f8d7e24cd18343d59f10af3297ed3%40group.calendar.google.com&ctz=America%2FNew_York" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>

## Schedule

The schedule below reflects our current plans, but will be updated throughout the semester.
<div id="schedule">
<table>
  <thead>
    <tr>
      <th>Date</th>
      <th>Topic</th>
      <th style="width: 30%">Reading assignments*</th>
    </tr>
  </thead>
  <tbody>
    <tr class="">
      <td>Mon, Aug 26</td>
      <!-- <td><a href="https://docs.google.com/presentation/d/1w53j54X7w8TOMeESE997axKLSGXoH3svhZMr9QY_YmQ/edit?usp=sharing">Introduction</a></td> -->
      <td>Intro, IDEs, Build Systems, CI, Libraries</td>
      <td></td>
    </tr>
    <tr class="">
      <td>Wed, Aug 28</td>
      <td>OO basics, Dynamic dispatch, Encapsulation</td>
      <td></td>
    </tr>
    <tr>
      <td>Fri, Aug 30</td>
      <!-- <td><span class="rec">Lab 1</span> <a href="https://github.com/CMU-17-214/s2024/blob/main/labs/lab01.md">Course Infrastructure Setup</a></td> -->
      <td><span class="rec">Lab 1</span> <a href="https://github.com/CMU-17-214/f2024/blob/main/labs/lab01.md">Course Infrastructure Setup</a></td>
      <td></td>
    </tr>
  </tbody>
  <tbody>
    <tr>
        <td>Mon, Sep 2</td>
        <td class="break">No Class, Labor Day</td>
        <td></td>
    </tr>
    <tr class="">
      <td>Wed, Sep 4</td>
      <td>OO Analysis and UML</td>
      <!-- <td>Required: <a -->
      <!-- href="https://cmu.primo.exlibrisgroup.com/permalink/01CMU_INST/1feg4j8/alma991019578256404436">Effective Java, Items 15 and 16</td> -->
      <td />
    </tr>
    <tr>
      <td>Fri, Sep 6</td>
      <td><span class="rec">Lab 2</span> Encapsulation</td>
      <td />
    </tr>
    <!-- <tr class=""> -->
    <!--   <td>Thu, Jan 25</td> -->
    <!--   <td><a href="https://docs.google.com/presentation/d/1t6OKuap0bjrd4ikglvhaYD6jOEubugm5oPjW7vWiybE/edit?usp=sharing">Specifications and Unit Testing, Exceptions</a></td> -->
    <!--   <td>Recommended: <a href="https://cmu.primo.exlibrisgroup.com/permalink/01CMU_INST/1feg4j8/alma991000042699704436">Java Precisely</a> (Ch 3, 4, 9, 10, 11); <a href="https://cmu.primo.exlibrisgroup.com/permalink/01CMU_INST/6lpsnm/alma991019576570404436">JavaScript: The Good Parts</a> (Ch. 3, 4, 9), <a href="https://www.typescriptlang.org/docs/handbook/intro.html">TypeScript Handbook</a> (Basics, Everyday Types, Object Types)</td> -->
    <!-- </tr> -->
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Sep 9</td>
      <!-- <td><span class="assignment"><span class="hw">HW 1 due</span> <a href="https://github.com/CMU-17-214/s2024/blob/main/assignments/hw1.md">Flash cards</a> (Intro to OO and Libraries)</td> -->
      <td><span class="assignment"><span class="hw">HW 1 due</span> <a href="https://github.com/CMU-17-214/f2024/blob/main/assignments/hw1.md">Flash cards (Intro to OO and Libraries)</a></td>
      <td />
    </tr>
    <tr class="">
      <td>Mon, Sep 9</td>
      <td>Responsibility Assignment</td>
      <td><a href="https://www.safaribooksonline.com/library/view/applying-uml-and/0131489062">UML and Patterns</a>, Ch. 9-11, 15-16</td>
    </tr>
    <tr class="">
      <td>Wed, Sep 11</td>
      <td>Inheritance and Delegation</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Sep 13</td>
      <td><span class="rec">Lab 3</span> Inheritance and Delegation</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr class="">
      <td>Mon, Sep 16</td>
      <td>Design Patterns</td>
      <td><a href="https://www.safaribooksonline.com/library/view/applying-uml-and/0131489062">UML and Patterns</a>, Ch. 17-18</td>
    </tr>
    <tr class="">
      <td>Wed, Sep 18</td>
      <td>Design Critique</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Sep 20</td>
      <td><span class="rec">Lab 4</span> Design and UML</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Sep 23</td>
      <td><span class="assignment"><span class="hw">HW 2a due</span> Santorini: Intro to Design</td>
      <td />
    </tr>
    <tr>
      <td>Mon, Sep 23</td>
      <td>Refactoring and Anti-patterns</td>
      <td />
    </tr>
    <tr class="midterm">
      <td>Wed, Sep 25</td>
      <td class="midterm">Midterm 1</a></td>
      <td />
    </tr>
    <tr class="">
      <td>Fri, Sep 27</td>
      <td><span class="rec">Lab 5</span> Refactoring and Anti-patterns</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Sep 30</td>
      <td><span class="assignment"><span class="hw">HW 2b due</span> Santorini: Peer Review</td>
      <td />
    </tr>
    <tr class="">
      <td>Mon, Sep 30</td>
      <td>Specifications and Unit Testing, Exceptions</td>
      <td />
    </tr>
    <tr class="">
      <td>Wed, Oct 2</td>
      <td>Test Case Design</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Oct 4</td>
      <td><span class="rec">Lab 6</span> Unit Testing</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Oct 7</td>
      <td>Refactoring for Testability</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Oct 9</td>
      <td><span class="assignment"><span class="hw">HW 3 due</span> Testing</span></td>
      <td />
    </tr>
    <tr>
      <td>Wed, Oct 9</td>
      <td>Introduction to concurrency</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Oct 11</td>
      <td><span class="rec">Lab 7</span> Test Doubles</td>
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Oct 14</td>
      <td class="break">No class, Fall Break</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Oct 16</td>
      <td class="break">No class, Fall Break</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Oct 18</td>
      <td class="break">No lab, Fall Break</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Oct 21</td>
      <td>Java Parallelism</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Oct 23</td>
      <td><span class="assignment"><span class="hw">HW 4 due</span> Refactoring</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Oct 23</td>
      <td>Web Apps and Concurrency</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Oct 25</td>
      <td><span class="rec">Lab 8</span> Java Parallelism</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Oct 28</td>
      <td>Concurrency and Asynchrony in TypeScript</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Oct 30</td>
      <td><span class="assignment"><span class="hw">HW 2c due</span> Santorini: Final design</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Oct 30</td>
      <td>Concurrency and Hazards</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Nov 1</td>
      <td><span class="rec">Lab 9</span> Concurrency and Promises</td>
      <td />
    </tr>
    <tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Nov 4</td>
      <td>GUIs</td>
      <td />
    </tr>
    <tr class="midterm">
      <td>Wed, Nov 6</td>
      <td>Midterm 2</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Nov 8</td>
      <td><span class="rec">Lab 10</span> ReactJS/Intro to GUIs</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Nov 11</td>
      <td><span class="assignment"><span class="hw">HW 5 due</span> Concurrency</td>
      <td />
    </tr>
    <tr>
      <td>Mon, Nov 11</td>
      <td>Libraries and Frameworks</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Nov 13</td>
      <td>API Design</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Nov 15</td>
      <td><span class="rec">Lab 11</span> Frameworks/Extensibility</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Nov 18</td>
      <td><span class="assignment"><span class="hw">HW 6a due</span> Santorini: User Interface</td>
      <td />
    </tr>
    <tr>
      <td>Mon, Nov 18</td>
      <td>API Design II</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Nov 20</td>
      <td>Design Case Study</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Nov 22</td>
      <td><span class="rec">Lab 12</span> TBD</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Nov 25</td>
      <td>DevOps</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Nov 27</td>
      <td class="break">No class, Thanksgiving Break</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Nov 29</td>
      <td class="break">No lab, Thanksgiving Break</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr>
      <td>Mon, Dec 2</td>
      <td>Designing for Larger Scale: Distributed Systems</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Dec 4</td>
      <td><span class="assignment"><span class="hw">HW 6b due</span> Santorini: God Cards</td>
      <td />
    </tr>
    <tr>
      <td>Wed, Dec 4</td>
      <td>Towards Software Engineering</td>
      <td />
    </tr>
    <tr>
      <td>Fri, Dec 6</td>
      <td><span class="rec">Lab 13</span> Design Pattern Review</td>
      <td />
    </tr>
  </tbody>
  <tbody>
    <tr class="midterm">
      <td>TBD</td>
      <td>Final exam</td>
      <td />
    </tr>
  </tbody>
</table>
</div>

## <a name="staff"></a>Staff

Instructors: [Jeremy Lacomis](https://jeremylacomis.com/) [jlacomis] and [Claire
Le Goues](https://clairelegoues.com) [clegoues]

TAs:
Connie (Wenjun) Zhou [wenjunz2],

Terry (Jielin) Li [jielinl],

Jeffrey Hanyun Li [jhl4],

Yikang Cheng [yikangc],

Eileen Gu [yingfan2],

John Crawshaw [vcrawsha],

Victor Crawshaw [jccrawsh],

Clement Ou [clemento],

Yibo Ma [yibom]

## <a name="syllabus"></a>Course Syllabus and Policies

### Prerequisites

- 15-122 or 15-211, or equivalent with instructor's permission
- The equivalent of 2 semester-long programming classes
  - Ability to write small programs in C (or Java, C#, or other imperative languages with pointers or references)
  - Ability to reason about programs using preconditions, postconditions, and invariants
  - Familiarity with a basic set of algorithms and data structures (linked lists, simple graph and sorting algorithms)

- 15-151 or 21-127, or equivalent with instructor's permission
  - Sound foundation of mathematical concepts; ability to reason formally

------

### Grading and Deadlines

Evaluation will be based on the following approximate percentages:

- 50% assignments
- 30% midterm exams and final exam
- 10% labs
- 10% participation and quizzes

This course does not have a fixed letter grade policy; i.e., the final letter grades will **not** be A=90-100%, B=80-90%, etc.

**Homework grading and regrading.** We try to be transparent in our rubrics in our assignments. Feel free to ask instructors or TAs clarification questions about the rubrics before the assignment is due. If you disagree with a grade, please submit a regrade request within 7 days on Gradescope. Regrade requests need a justification, explaining why our assessment is inconsistent with the rubric. Regrade requests without such justification will be closed.

Each student can *resubmit* any *one* assignment milestone and it will be regraded as if it was the first submission (see below).

**Participation and quizzes.** You should expect a quiz at the start of nearly every lecture and often additional in-class activities within the lecture. When a reading assignment is given, the quiz will typically touch on the content from the reading material. Otherwise (and sometimes in addition), the quiz centers around the content from the most recent lecture or two. A quiz will typically have 1-2 questions and is graded pass/fail.

**Labs.** Labs will be graded on a pass/fail basis during recitations. You will have a chance during recitation to improve your solution. See a description [here](https://github.com/CMU-17-214/f2024/blob/main/labs.md).

**Late work.** We understand that normal life events, including projects and exams in other courses and technical difficulties out of your control, can interfere with your ability to complete your work on time or attend lectures and recitations. Our philosophy is that our late work policy includes built-in flexibility but that the policy will be uniformly applied to all students in all circumstances. Exceptions to this policy will be made only with explicit accommodations, almost always involving a family or medical emergency with your academic advisor or the Dean of Student Affairs requesting the exception on your behalf.

<!-- We provide the following flexibility, no questions asked, no justification needed: -->

<!-- - For midterms and finals, we drop the worst of the three grades. -->
<!-- - For quizzes, we will drop up to four missed/failed solutions during the semester. -->
<!-- - For labs, we will drop up to four missed/failed solutions during the semester. -->
<!-- - For homework deadlines you have 5 free late days for the semester. You can exceed each deadline by up to three days (unless explicitly specified otherwise in the assignment, check carefully), for a penalty of 10% per day once you run out of free late days. Note that some homework assignments have multiple milestones with separate deadlines; there are typically around 9 homework deadlines in a semester – late days are assessed for each deadline independently. -->
<!-- - For a single homework deadline during the semester, you can redo and resubmit your work after it was graded. It will be regraded as if it was the first submission and you can regain all lost points. Each student can only do this once. We accept resubmissions until April 26th, 11:59pm. (While we do not recommend it, you can use this as arbitrary late days for a single deadline, receiving 0 points for missing the initial deadline and then resubmitting later). -->

<!-- Any work submitted beyond the flexibility provided by these mechanisms will receive feedback but no credit unless explicit accommodations were provided. -->

------

### Attendance and remote participation

This course, including recitations, is marked by the registrar as IPE ("delivered in-person, students are expected to be in the classroom during the course's scheduled meeting time"). We do not plan to make accommodations for remote attendance.

We strongly recommend attending lectures. We have regular in-class activities and quizzes that we expect you to complete in class. Attending recitations is required for grading labs.

In case of illness, quarantine, or other exceptional circumstances, we may be able to share recordings of lectures upon request on a case by case basis. Recordings may not be shared to protect the FERPA rights of all students in the classroom.

------

### Textbooks

This course will occasionally assign **mandatory readings**, from the two text books below. The CMU library has both physical and electronic copies of these books. You can access *all* of these books for free electronically through the CMU library.

- Larman, Craig. [*Applying UML and Patterns: An Introduction to Object-Oriented Analysis and Design and Iterative Development*](https://bookshop.org/books/applying-uml-and-patterns-an-introduction-to-object-oriented-analysis-and-design-and-iterative-development/9780131489066), 3rd Edition. Prentice Hall. ISBN 0-13-148906-2. [[CMU Library](https://cmu.primo.exlibrisgroup.com/permalink/01CMU_INST/6lpsnm/alma991019576227704436)] This book describes basics of object-oriented design, responsibility assignment, and some design patterns used in the course. We will use the third edition, which covers the course's topics in more details than earlier editions. We will assign select chapters.
- Bloch, Joshua. [*Effective Java*](https://bookshop.org/books/effective-java-9780134685991/9780134685991), Third Edition. Addison-Wesley, ISBN 978-0-13-468599-1. [[CMU Library](https://cmu.primo.exlibrisgroup.com/permalink/01CMU_INST/1feg4j8/alma991019578256404436)] This book covers many aspects of program design, not only those specific to Java. We will assign multiple chapters.

In addition, we list **several optional readings** that may be helpful with specific topics in the course. Especially if Java/Javascript is new to you, you might want to consider exploring additional books.

- Object-Oriented Design and Design Patterns
  - Alan Shalloway and James Trott. [*Design Patterns Explained: A New Perspective on Object-Oriented Design (2nd Ed.)*](https://bookshop.org/books/design-patterns-explained-a-new-perspective-on-object-oriented-design/9780321247148) [[CMU Library](https://cmu.primo.exlibrisgroup.com/permalink/01CMU_INST/1feg4j8/alma991019576375404436)]
  - Gamma et al. [*Design Patterns: Elements of Reusable Object-Oriented Software*](https://bookshop.org/books/design-patterns-elements-of-reusable-object-oriented-software/9780201633610). Addison Wesley. ISBN 0-201-63361-2 [[CMU Library](https://cmu.primo.exlibrisgroup.com/permalink/01CMU_INST/6lpsnm/alma991019576613104436)] (this is an excellent book, but more of a reference text than the *Design Patterns Explained* book. In addition, because it was the original patterns book, the examples are in C++ and Smalltalk, not Java)

- Java
  - *Note: Here are some popular textbook and online resources for learning Java.*
  - Sestoft. [*Java Precisely*](https://bookshop.org/books/java-precisely-third-edition/9780262529075). MIT Press, 2016. [[2nd edition in the CMU library](https://cmu.primo.exlibrisgroup.com/permalink/01CMU_INST/1feg4j8/alma991016506989704436)] (this is a very concise reference with many good examples; it assumes that you already know other programming languages)
  - [Introduction to Programming Using Java](http://math.hws.edu/javanotes/) (free online textbook)
  - [Blue Pelican Java](http://www.bluepelicanjava.com/) (free online textbook)

- Javascript/Typescript
  - Douglas Crockford. [JavaScript: The good parts](https://bookshop.org/books/javascript-the-good-parts-the-good-parts/9780596517748). O'Reilly, 2008. [[CMU library](https://cmu.primo.exlibrisgroup.com/permalink/01CMU_INST/6lpsnm/alma991019576570404436)]
  - Boris Cherny. [Programming Typescript: Making Your JavaScript Applications Scale](https://bookshop.org/books/programming-typescript-making-your-javascript-applications-scale/9781492037651). O'Reilly, 2019. [[CMU library](https://cmu.primo.exlibrisgroup.com/permalink/01CMU_INST/6lpsnm/alma991019642791104436)]

------

### Time management

This is a 12-unit course, and it is our intention to manage it so that you spend close to 12 hours a week on the course, on average. In general, 4 hours/week will be spent in class, 1 hour on labs, and 7 hours on assignments. Please feel free to give the course staff feedback on how much time the course is taking for you.

------

### Research to Improve the Course

<!--- The language in this paragraph is IRB-approved --->
For this class, we are conducting research on teaching and learning. This research will involve some student work. You will not be asked to do anything above and beyond the normal learning activities and assignments that are part of this course. You are free not to participate in this research, and your participation will have no influence on your grade for this course or your academic career at CMU. If you do not wish to participate, please send an email to Chad Hershock (<hershock@andrew.cmu.edu>). Participants will not receive any compensation. The data collected as part of this research will include student grades. All analyses of data from participants’ coursework will be conducted after the course is over and final grades are submitted. The Eberly Center may provide support on this research project regarding data analysis and interpretation. The Eberly Center for Teaching Excellence & Educational Innovation is located on the CMU-Pittsburgh Campus and its mission is to support the professional development of all CMU instructors regarding teaching and learning. To minimize the risk of breach of confidentiality, the Eberly Center will never have access to data from this course containing your personal identifiers. All data will be analyzed in de-identified form and presented in the aggregate, without any personal identifiers. If you have questions pertaining to your rights as a research participant, or to report concerns to this study, please contact Chad Hershock (<hershock@andrew.cmu.edu>).

------

### Collaboration policy and academic integrity

The usual policies apply, especially the University Policy on Academic Integrity. We expect that your work on assignments, projects, and exams will be your own work. The key guiding principle of academic honesty in this course is: *"You may not copy any part of a solution to a problem that was written by another student (in this or prior iterations of the class), or was developed together with another student, or was delegated to another person. You may not look at another student's solution, even if you have completed your own, nor may you knowingly give your solution to another student or leave your solution where another student can see it."* Note that this implies that you cannot publicly post your solutions on GitHub (e.g., as part of a portfolio during job applications). We also expect and respect honesty when communicating with the course staff.

Any violation of this policy is cheating. We use automated systems to detect software plagiarism. These automated systems are highly effective and, so far, have detected software plagiarism almost every semester. The minimum penalty for cheating will be a zero grade for the whole assignment. Cheating incidents will also be reported through University channels, with possible additional disciplinary action (see the University Policy on Academic Integrity).

For labs and homeworks you are allowed to use various tools and help available to professional programmers, such as online documentation, online tutorials and support forums like Stackoverflow, and AI assistants like Copilot and ChatGPT. You are allowed to post technical questions about aspects of the homework elsewhere, as long as you do not ask other humans to complete the work for you. Whenever you use external resources like this, you are still fully responsible for the correctness of your solution and complying with licenses. Note that content generation tools often create plausible-looking but incorrect answers, which will not receive credit.

When you use AI assistants in homework, some assignments may require you to briefly describe their use and your experience with the homework submission.

Here are some examples of behavior that are inappropriate:

- Copying (or retyping) files, parts of files (such as source code, written text, or unit tests), quiz solutions, or exam solutions from another person or source, either in draft or final form, even if the file permissions are incorrectly set to allow it. This behavior is still clearly inappropriate even if you make modifications (such as style changes or minor logic modifications) from the original source.
- Searching for or viewing a current or past student's homework solution.
- Allowing someone else to view or copy your code, written assignment, quiz, or exam, either in draft or final form.
- Writing, using, or submitting a program that attempts to alter or erase grading information or otherwise compromise security of course resources.
- Lying to course staff.
- Making your work publicly available in a way that other students (current or future) can access your solutions, even if others’ access is accidental or incidental to your goals.

Here are some examples of acceptable behaviors:

- Solve technical problems by searching for the error message with Google or on StackOverflow.
- Copying code snippets from tutorials or StackOverflow into your own code.
- Importing libraries as part of your implementation. Reading documentation and examples of libraries. Copying libraries or utility files into your repository (bad practice to avoid, but not consider cheating).
- Copying code from labs or reference solutions provided in recitations.
- Using GitHub Copilot while writing your solution.
- Using ChatGPT to write or help write justifications in homework assignments, while checking the correctness of the answer.
- Looking at other students' solutions when explicitly instructed by the course staff, for example, as part of peer grading for labs, quizzes, or homework.

There is no statute of limitations for violations of the collaboration policy; penalties may be assessed (and referred to the university disciplinary board) after you have completed the course, and some requirements of the collaboration policy (such as restrictions on you posting your solutions) extend beyond your completion of the course.

If you have any question about how this policy applies in a particular situation, ask the instructors or TAs for clarification.

------

### Audit Policy

If you desire to audit the course, our general requirement is that you complete homeworks to achieve at least 50% of the total homework grade. Solutions do not need to be fully complete, but we encourage you to attempt to do so. We additionally encourage you to attend lectures and complete labs, but you are not required to do so. You should not attend our midterm exams or final exam.

------

### Your health matters

When we say "your health matters" we mean exactly that: Your health matters. We don't intend to imply that other peoples' health does not matter, or that your health matters more or less than theirs. We know that CMU can be a stressful, risky environment, and *your* health is the health that is relevant in this conversation. Worries about Covid-19 and possible remote classes do not help.

**Please take care of yourself**. Do your best to maintain a healthy lifestyle this semester by eating well, exercising, avoiding drugs and alcohol, getting enough sleep and taking some time to relax. This will help you achieve your goals and cope with stress.

All of us benefit from support during times of struggle. You are not alone. There are many helpful resources available on campus and an important part of the college experience is learning how to ask for help. Asking for support sooner rather than later is often helpful.

If you or anyone you know experiences any academic stress, difficult life events, or feelings like anxiety or depression, we strongly encourage you to seek support. Counseling and Psychological Services (CaPS) is here to help: call 412-268-2922 and visit their website at <http://www.cmu.edu/counseling/>. Consider reaching out to a friend, faculty or family member you trust for help getting connected to the support that can help.

If you are worried about affording food or feeling insecure about food, there are resources on campus who can help. Email the CMU Food Pantry Coordinator to schedule an appointment: <cmu-pantry@andrew.cmu.edu>

**Respect for diversity.** It is our intent that students from all diverse backgrounds and perspectives be well served by this course, that students’ learning needs be addressed both in and out of class, and that the diversity that students bring to this class be viewed as a resource, strength and benefit. It is my intent to present materials and activities that are respectful of diversity: gender, sexuality, disability, age, socioeconomic status, ethnicity, race, and culture. Your suggestions are encouraged and appreciated. Please let us know ways to improve the effectiveness of the course for you personally or for other students or student groups.

**Accommodations for students with disabilities.** If you have a disability and have an accommodations letter from the Disability Resources office, we encourage you to discuss your accommodations and needs with us as early in the semester as possible. We will work with you to ensure that accommodations are provided as appropriate. If you suspect that you may have a disability and would benefit from accommodations but are not yet registered with the Office of Disability Resources, we encourage you to contact them at <access@andrew.cmu.edu>.

------

### Informal feedback on this course

We are planning many changes to this course in this semester and not everything will work out smoothly the first time. We’d like you to provide ongoing feedback on your experience in the course, so that we can take into account your experience and adapt our practices to make the course work for you.

Outside of the regular course meetings and Piazza, you can submit feedback about anything in the course per email to the instructors or ask TAs to forward them anonymously. We will read every message submitted and use your feedback to try to improve the way we are teaching.
