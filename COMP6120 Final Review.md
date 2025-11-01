# COMP6120 Final Review

## Software Engineering

**Software engineering** is the establishment and use of sound engineering principles in order to obtain economically software that is reliable and works efficiently on real machines. - Design Under Constraints

A **software development** process organizes activity into distinct phases (e.g. design, coding, testing, etc.). Processes can increase **efficiency**, but are often implemented poorly.

Effort estimation is based on historical information (models, experience). It is complicated by uncertainty, which stems from risk, which can be **managed**(identified, minimized).

A project **plan** (like milestones, deliverables) includes all of these considerations. Measuring progress is difficult.

### How to develop software?
- Discuss
- Code
- Test
- Debug
- Fix

### WaterFall Model
In the waterfall software development model, the following phases are carried out in **order**:
- System and sofware requirements
- Analysis
- Design
- Coding
- Testing
- Operation

### Agile
Plan - (Design - Develop - Test - Deploy - Review)*n - Launch

## User Story

### Basic Format
As a [role], I want [function]. so that [value].

### Core Elements
- Card (write in)
- Conversation (between developer and user or PM)
- Confirmation (tell that the user story has been achieved)

### INVEST Principle
- I - independent
- N - Negotiable
- V - Valuable
- E - Estimable
- S - Small
- T - Testable

## Measurement
Software metrics should be used **cautiously**, since they are often inadequately supported and thus lack validity.

Measurement is a fundamental activity but is influenced by human biases. It is rasy to **misinterpret** data or focus on what is easy to **measure**. Metrics can incentivize perverse behavior.

### Software Qualities
- Availability
- Consistency
- Documentation
- Ease of use
- Energy Efficiency
- Extensibility
- Functionality (e.g. data integrity)
- Installability
- Maintainability
- Performance
- Portability
- Privacy
- Scalability
- Security

### Streetlight Effect
observational bias (when people are searching for something, they only look where it is easiest)

Despite this, don't lose faith in measurement, just work to avoid the bias

### Software Metric Warning
- Most controversial
- Usually based on plausibility arguments (not rigorous validation)
- e.g., Cyclomatic Complexity was repeatedly refuted and is still used

### Software Metric Advice
- Use software metrics **carefully**
- Avoid claims about human factors and quality unless validated
- Calibrate metrics using your project history and the histories of other projects

## Inspection

In a code review, another developer examines your proposed change and explanation, offers feedback, and decides whether to accept it. Modern code reviews have significant tool support.

In a formal code inspection, a team of developers meets and examines existing code, following a process to understand it and spot issues.

Both of these static quality assurance approaches have **costs** and **benefits**.

Pair programming is a well-studied technique within Agile involving a driver and a navigator; **it increases development time but decreases defects.**

Code Inspection -> Examine whole program

Code Review -> Examine Each Change

### Social Issues: Inspection Incentives
Meetings should **not include management**

Do not use code reviews for HR evaluations

Responsibility for quality with authors, not reviewers

### Review Costs
Formal inspections are very **expensive**

Passaround review is distributed, asynchronous

### Pair Programming
- 2 workers work at 1 computer
- 1 'driver' who actively **types** at the computer or records a design;
- 1 'navigator' who **watches** the work of the driver and attentively **identifies** problems, **asks** clarifyingquestions and **makes** suggestions. Both are also continuous brainstorming partners.

## Requirements and Specifications
- Requirements articulate the relationship and interface between a desired **system** and its **environment**. This includes both what **is** (or is expected) and what should **be**.
- We distinguish between functional and quality (or non-functional) requirements. Both should be stated in **measurable** ways.
- Requirements can describe variables, inputs, and outputs, and assumptions between them.
- We distinguish between **informal** statements and verifiable requirements.

### System, Software and Assumptions
- System requirements: relationships between monitored and controlled variables
- Software requirements: relationship between inputs and outputs
- Domain properties and assumptions state relationships between those

### Functional Requirements
- Functional requirements describe what the machine should do ("get the right answer")
    - input, output
    - interface
    - response to events

- Criteria
    - Completeness: All requirements are documented
    - Consistency: No conflicts between requirements
    - Precision: No ambiguity in requirements

### Quality Requirements
- Qualiy requirements specify not the functionality of the system, but the manner in which it delivers that functionality.
- Can be more critical than functional requirements
    - can work around missing functionality
    - low-quality system may be unusable

## DevOps and Team Communication
- DevOps is a culture and **set of practices** that bring together **development** and **operations** teams to build, test, and release software faster and more reliably
- Continuous Integration: Code changes are integrated and tested **automatically**
- Continuous Delivery: Changes are always ready to **release** (manual approval for production).
- Continuous Deployment: Changes go straight to **production** automatically.
- Software teams **communicate** more effectively by using **tools** (e.g., Slack, Jira, Github) to share updates, track work, and collaborate in real time.

### What is DevOps
DevOps is the **integration** and **automation** of the software development and information technology operations.

### DevOps Phases

Plan -> Create -> Verify -> Package -> Release -> Configure -> Monitor -> Plan -> ...

### CI / CD
- Continuous Integration (CI)
- Continuouts Deployment (CD)

### Big Bang Deployment
replace all instances with new version once a time

### Rolling Deployment
replace all instances with new version step by step

### Red/Black (Blue/Green) Deployment
keep two groups of instances, with one for old version and one for new version

### Canary Deployment
let a small part of users use new version first and monitor the metrics, then increase the ratio of new version if no issues.

## Testing
- Quality Assurance maintains desired product propeties through proces choices.
- Testing involves running the program and inspecting its results or behavior. It is the dominant approach to software quality assurance. There are numerous methods of testing, such as **unit testing, mutation testing, fuzing, performance testing, and A/B testing**.
- Testing is the most common dynamic technique for software quality assurance

### Unit Test
- Tests on small sections of a system, e.g., a single class
- Test data is chosen by developers based on their understanding
- Can be open or close box

### Mutation Testing
- Inject bugs in the program by mutating the source code
- Ideally: at least one test should fail on the mutated program (= catch bug)
- Mutation score = (mutants killed)/(total mutants)

### Test Oracles
The method to validate if the output is correct.

### Fuzzing Test
Give the program some random inputs and check whether the program failed or report any errors. The purpose is to test the robustness of the program.

### Performance Test
To check the performance of the program, trying to find out some performance disadvantage with some inputs.

common metric:
- latency
- throughput
- resources usage

Oracle: set proper threshold

### Profilling
- Finding bottlenecks in execution time and memory
- Flame graphs are a popular visualization of resource consumption by call stack

### Usability: A/B testing
Give two version program with an attribute set A or B, let the user use and check the performance to know which is better. Often used in GUI tests

### Code Converage
- Line coverage 
- Statement coverage
- Branch coverage
- Instruction coverage
- Basic-block coverage
- Edge coverage
- Path coverage

## Architecture: Microservices

- Monolithic architectures bundle all functionality together, while modular architectures divide systems into **independent** parts.
- Types of modularity include plug-in architectures, service-oriented architectures and **microservices**.
- **Microservices** bring benefits such as scalability and flexibility, but also introduce trade-offs like complexity and overhead.
- Following the principles of microservices helps maximize their benefits and avoid common pitfalls.



### Modularity
Plug-in architecture --> Service-oriented architectures --> Distributed micro-services (Modularity increase)

### Scaling
- Vertical scaling: increase resources of one server
- Horizonal scaling: increase the number of servers

### Sam Newman's principles of Microserices
- Domain Driven Modeling
- Culture of Automation
- Hide Implementation Details
- Decentralized Governance
- Deploy Independently
- Consumer First
- Isolate Failures

### Microservice challenges
- Too many choices
- Delay between investment and payback
- Complexities of distributed systems
- Monitoring is more complex
- More system states
- More points of failure
- Operational complexity
- Frequently adopted by breaking down a monolithic application

## Defect Reporting and Triage
- A software defect report includes information and communications related to addressing a software issue
- Defect reports have many **components**
- Defect reports are ssubject to triage based on severity and priority information
- Defect reports have a lifecycle that is complicated and non-linear with multiple possible resolutions.

### Defect Report Lifecycle
The defect report lifecycle consists of a number of possible stages and actions including: reporting, confirmation, triage, assignment, resolution, and verification.

    - Not every defect report follows the same path.
    - The overall process is **not linear**.

The status of a defect report tracks its position in the lifecycle("new", "resolved", etc.)

### Triage
- Triage is the assignment of degrees of urgency to wounds or illnesses to decide the order of treatment of a large number of patients or casualties.
- There are always more defects reports than resources available to address them.
- Cost-benifit analysis
    - How expensive is it to fix this bug?
    - How expensive is it to not fix this bug?


### Severity
Severity is the degree of impact that a defect has on the development or operation of a component or system. In another word, **the cost of not fixing it**.

### Priority
Defect Priority indicates the importance or urgency of fixing a defect

### Possible Resolutions
Bugzilla resolution options:
- Fixed
- Invalid
- Won't fix
- Duplicate
- Worksforme (cannot reproduce)
- Moved
- Not a bug
- Not out bug
- Insufficient data

## Debugging as Hypothesis Testing
Delta debugging is an automated debugging approach that finds a minimal interesting subset of a given set. It is very efficient.

Delta debugging is based on divide-and-conquer and relies heavily on critical assumptions(monotonicity, unambiguity, and consistency).

It can be used to find which code changes cause a bug, to minimize failure-inducing inputs, and even to find harmful thread schedules.

### Delta Debugging (Interface)
- Given
    - A set C = ${c^1, ..., c^n}$ (of changes)
    - A function Interesting: a (sub)set of changes --> Yes or No
    - We know: Interesting(C) = Yes, Interesting({}) = No
    - We require: Interesting is monotonic, unambiguous and consistent (more on these later)

- The delta debugging algorithm returns a minimal "Interesting" subset M of C:
    - Interesting(M) = Yes
    - For all m in M, Interesting(M\\{m}) = No

- Algorithm Candidate
~~~
    DD(${c_1, ..., c_n}$) = 
        if n == 1 then return {$c_1$}
        let P1 = {$c_1, ..., c_{n/2}$}
        let P2 = {$c_{(n/2)+1}, ..., c_n$}
        if Interesting(P1) == Yes
            return DD(P1)
        else return DD(P2)
~~~

### Useful Assumptions
- Any subset of changes may be Interesting
    -   not just singleton subsets of size 1
- Interesting is Monotonic:
    - Interesting(X) --> Interesting(X u {C})
- Interesting is Unambiguous:
    - Interesting(X) & Interesting(Y) --> Interesting(X and Y)
- Interesting is Consistent:
    - Interesting(X) = Yes or Interesting(X) = No (Sometimes = Unknown)

## Open Source

### Background: laws and open source
- Copyright protects creative, intellectual and artistic works - including software
- Alternative: public domain (nobody may claim exclusive property rights)
- Trademark protects the name and logo of a product
- OSS is generally copyrighted, with copyright retained by contributors or assigned to entity that maintains it.
- Copyright holder can grant a license for use, placing restrictions on how it can be used.

### Copyleft vs. Permissive
- Copyleft protects the commons by having all linked code under same license, transitively requiring more sharing
- Permissive licenses encourage adoption by permitting this practice

### MIT License
- Simple, commercial-friendly license
- Must retain copyright credit
- software is provided as is
- Authors are not liable for software
- No other restrictions

### Apache License
- Similar to MIT License
- Not copyleft
- Not required to distribute source code
- Does not grant permission to use project's trademark
- Does not require modifications to use the same license

### BSD License
- No liability and provided as is
- Copyright statemnt must be included in source and binary
- The copyright holder does not endorse any etensions without explicit written consent

### Copyright vs. Intellectual Property (IP)
- IP and Patents cover an idea for solving a problem
- Copyrights cover particular expressions of some work
- Exceptions for trivial works and ideas