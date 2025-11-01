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



