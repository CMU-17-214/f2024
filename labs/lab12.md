# Lab 12: APIs

## Context
This lab will test your knowledge of good API design principles. For this lab you will identify and fix API design principle violations inside a repository containing 3 different APIs

## Deliverables
- [ ] Fix an API design principle violation in the DirManager package
- [ ] Fix an API design principle violation in the Library package
- [ ] Fix an API design principle violation in the Weather package

## Instructions
Clone the repository from: https://github.com/CMU-17-214/f24-lab12

Inside the repository you will find three different APIs: DirManager, Library, and Weather. For each of these, you should identify the flaw, update the code, and also update the documentation to match the code that you corrected. You will get full points for each of them if you are able to both identify and fix the flaws.

## API Design principles
Here is a list of general API design principles. Each of the violations we have included in this lab correspond to at least one of them.
![General API Design principles](resources/GPoAD.pdf)

## Hints
DirManager is an API designed for managing directories. The design of the `newDirectory` method in the `Manager` class has a flaw that should be identified and fixed. _For this specific flaw_ you do not need to worry about creating new objects, feel free to use them as if they already existed.

Library is an API designed for managing user accounts in a library system. The design of the `getBooks` method in the `LibraryAccount` API has a flaw.

Weather is an API designed for interacting with the weather at a specific location. In this case, the `setLengthScale` method has an API design flaw. You may also need to update the `getRainfall` method as well.