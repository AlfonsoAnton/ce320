##Lecture 1

### The Pains Of Programming

- perfection is difficult
- the authority is not equal to the responsibility
- painstaking labour
- programming projects converge more slowly near the end
- product threatened with obsolescence even before completion (contrast this with civil engineering)
  where an engineer/team of engineers reserve a particular plot.
  
### Brooks' No Silver Bullet

- Brooks outlines two different types of complexity: Accidental and Essential Complexity
- Accidental complexity relates to problems which engineers create and can fix; for example, 
  the details of writing and optimizing assembly code or the delays caused by batch processing.
  Essential complexity is caused by the problem to be solved, and nothing can remove it; if
  users want a program to do 30 different things, then those 30 things are essential and the
  program must do those 30 different things.
- High level languages like Java and Python reduce the accidental complexity.
  

### Complexity of software entities

- No two parts are alike (above statement level)
- Contains a large amount of states which make describing, conceiving and testing hard
- As the size of a piece of software increases so does the interaction between it's parts and so too 
  does it's complexity

- Resulting problems from complexity

    - Difficulty of communication between team members
    - Unreliability as a byproduct of difficulty enumerating and understanding all possible states
      of a program.
    - complex functions are hard to use 
    - difficulty odf extending programs to new functions without creating side effects (think interfaces
      without default methods)
    - security vulnerabilities as a result of unanticipated states
    
### Solving Accidental Complexities

- High level languages
    - Enable a programmer to write programs that are more or less independent of a specific machine
    - More abstract: consitst of concecptual constructs like operations, data types sequences and communications
    - High level langiages provide all the constructs the programmer imagines in the abstract program

- Object Oriented Programming
    - Two concepts: Abstract Data Types [think of the collections interface] and Hierarchical Types (Classes)
    - Allow a higher order expression of design
    - By nature is an essential complexity

- Programming environments
    - Language specific smart editors [like VS Code anf IntelliJ] precompiles the code for syntax highlighting
      to help the programmer from making syntactic and semantic errors
    - IDEs use integrated databases [think IntelliJ MySQL integration] to keep track of details that must be recalled 
      accurately by the individual programmer. 

## Large scale software development is like a tar pit the more you fight the deeper you sink

### Problems in Large Scale Software Systems

- Software projects go off course due to lack of time more than any other reason
- "Good cooking takes time" - some tasks cannot be hurried without spoiling the result.
- Because programmers build with pure thought we expect few difficulties in implementation but the reality
  is that our ideas themselves are an essential complexity and therefore faulty which can cause bugs.
  
### The Mythical Man Month

- Estimating time for devleopmenmt work confuse two concept: effort and progress
- Although cost is proportional to the number of personnel and time, a 'Person-Month' is a dangerous myth
  as it implies persons and months are one and the same.
- The person month concept only works for independent tasks.
- Splitting up work for more people causes extra effort in communication
- "The fact that one woman makes a baby in 9 months does not imply that 9 women make a baby in 1 month!"

### Brooke's Law

- "Adding manpower to a late software project makes it later"

### Communication and organisation

- Teams need to communicate in as many ways as possible. Teams drift apart when making assumptions.
- The purpose of organisation is to reduce the amount of communication and coordination necessary.
- Project managers need to monitor objectives, product specs, schedule and budget but above all else
  to keep everybody going in the same direction. Their job is communication not decision making.

### Program Maintenance: Two steps forward, One step back

- Repair defects (fixing bugs), adding functionality, adapting to changes in the user environment or 
  configuration.
  
- Quite often maintaining an application is more costly than the initial development of it.

- More users = Higher maintenance cost as more users find bugs 

- Fixing bugs has the potential to break existing code, so regression testing is essential when new code
  is deployed.
  
- Committing to hotfixes and minor versions increases entropy (disorder) of the system and makes it brittler
  so there must be an effort to combat this otherwise software systems die by subsiding into unfixable chaos.

### System Integration

- System integration is hard.
- Many failures are due to the components that are meant to integrate are not specified.
- Do system debugs
- Write lots of debugging and test code.

### Schedule Slippage

- Day by day schedule slippage is hard to recognise
- Chronic schedule slippage kills morale. If you miss one deadline make sure you make the next one.
- According to Brooks it is good practise to have a schedule of milestones and dates for said milestones.
- Milestones are all or nothing
- Milestones should be concrete, specific, measurable and precisely defined.
- It is essential to accept status reports without panic: it encourages honest reporting.


### Programs and Documentation

- Documentation is essential for the user who may forget the purpose of the code but also maintenance 
  (so whoever touches the code understands what's going on) 
  
- Documentation for users should include test cases for all inputs (invalid, barely valid and valid)

- Brooks suggests self documenting programming techniques:
    - Documentation is more easily maintained if it is part of the program
    - One should use parts of the program which must be there anyway to carry as much of the documentation
      as possible such as variable names, functions and class names.
   

- Buy vs Build
    - Best to buy software as it is cheaper and delivery is immediate.

### Requirements and refinement and rapid prototyping

- The hardest part of building a software system is deciding precisely what to build (establishing the 
  detailed technical requirements, including interfaces to people, machines, and other software).
- Clients don't know what they want/need
- It is difficult for clients to specify completely, precisely and correctly the exact requirements of
  a product without having tried some early version of it so best to create a prototype for them.
  
### Incremental development: grow, not build, software

- software systems should endeavour to be grown incrementally 
- The initial systems should be first made to run even if it is functionally useless (just call dummy endpoints/data)
- Incremental development has a positive impact on moral
- There are always prototypes available since at every stage of the process, one always has a working sytem.