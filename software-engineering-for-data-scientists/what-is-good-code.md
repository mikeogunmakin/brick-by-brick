# What is Good Code?

A number of ways to think about this: the best code could be the code that runs fastest. Or it
could be easiest to read. Another possible definition is that good code is easy to maintain.
That is, if the project changes, it should be easy to go back to the code and change it to
reflect the new requirements. The requirements for your code will change frequently
because of updates to the business problem you’re solving, new research directions, or
updates elsewhere in the codebase.

---
## Why Good Code Matters

Good code is especially important when your data science code integrates with a larger
system. This could be putting a machine learning model into production, writing packages
for wider distribution, or building tools for other data scientists. It’s most useful for larger
codebases that will be run repeatedly. As your project grows in size and complexity, the
value of good code will increase.  

Sometimes, the code you write will be a one-off, a prototype that needs to be hacked
together today for a demo tomorrow. And if you truly will run the code only once, then don’t
spend the time making it beautiful: just write code to do the job it’s needed for. But in my
experience, even the code you write for a one-off demo is almost always run again or reused
for another purpose. I encourage you to take the time to go back to your code after the
urgency has passed and tidy it up for future use.

---
## Technical Debt

**Technical debt** (often abbreviated as **tech debt**) is a commonly used term for deferred work resulting from
when code is written quickly instead of correctly.  

Tech debt can take the form of missing documentation,
poorly structured code, poorly named variables, or any other cut corners. These make the code harder to maintain or refactor, and it’s likely that you will spend more time in the future fixing bugs than you would
have spent writing the code well in the first place.  

That said, tech debt is often necessary because of
business deadlines and budgets. You don’t always have time to polish your code.

---
## How to Adapt to Changing Requirements

Writing code is not like building a bridge, where the design is thoroughly worked out, the
plans are fixed, and then construction happens.  

The one constant in writing code, for a data science project or anything else, is that you should expect things to change as you work on a project. These changes may be the result of your discoveries through your research
process, changing business requirements, or innovations that you want to include in the
project. Good code can be easily adapted to work well with these changes.  

This adaptability becomes more important as your codebase grows. With a single small
script, making changes is simple. But as the project grows and gets broken out into multiple
scripts or notebooks that depend on each other, it can become more complex and harder to
make changes. Good practices from the start will make it easier to modify the code in a
larger project.

five features of good code: simplicity, modularity, readability, performance, and robustness

---
## Simplicity

Complexity makes it hard to modify code when your requirements change. Complexity is anything related to the structure of a system that makes it hard to understand and modify a system.

accidental complexity is when you’re not sure which function within your code you need to change to achieve some action.

---
## Don't Repeat Yourself (DRY)

One of the most important principles in writing good code is that information should not be
repeated. All knowledge should have one single representation in code. If information is
repeated in multiple places, and that information needs updating because of changing
requirements, then one change means many updates. You would need to remember all the
places where this information needs to be updated. . This is hard to do and increases code
complexity. Additionally, duplication increases opportunities for bugs, and longer code
requires more time to read and understand.

There’s also an increase in mental effort when you see two pieces of code that are very
similar but not exact duplicates. It’s hard to tell if the two pieces of code are doing the same thing or something different.

abstract and generalise your code so that it’s not tied to a single project, but can handle slight variations and be reused in future projects.

Write code that is easy for others to reuse (e.g., well-structured functions, clear APIs). Provide good documentation so teammates know what exists and how to use it. Share utilities in common libraries/packages instead of hiding them in personal notebooks.

Avoid documentation duplication by writing comments that explain intent, assumptions, or context — not just re-stating the code.

---
## Avoid Verbose Code

aim to make your code concise but still readable.  To do this, avoid
doing things that make your code unnecessarily long-winded, such as writing your own
functions instead of using built-in functions or using unnecessary temporary variables. ou
should also avoid repetition, as described in the previous section.

Sometimes, you can make your code simpler by having fewer lines of code. This means
fewer opportunities for bugs and less code for someone else to read and understand. However, there’s often a trade-off between making your code shorter and making it less
readable

Of course, there are downsides to squeezing your code into fewer lines. If a lot is happening
on one line, it can be extremely hard for anyone else to understand what is going on. This
means it is harder for someone else to work on your code, and this could lead to more bugs.
If in doubt, I recommend that you keep your code readable even if it means you use a few
extra lines.

------------
## Modularity

Writing modular code is the art of breaking a big system into smaller components. Modular
code has several important advantages: it makes the code easier to read, it’s easier to
locate where a problem comes from, and it’s easier to reuse code in your next project. It’s
also easier to test code that is broken into smaller components.

You could just write one big script to do the whole thing, and this might be fine at the start of a small project. But larger projects need to be broken into smaller pieces. To do this, you’ll need to think as far ahead into the future of the project as possible and try to anticipate what the overall system will do and what might be sensible places to divide it up.

Writing modular code is an ongoing process, and it’s not something you’ll get completely
correct from the beginning, even if you have the best intentions. You should expect to
change your code as your project evolves.

---
## Readability

Readable code ensures long-term usability for both you and others. Following conventions, using clear names, removing unused code, and documenting early makes code simpler, less complex, and easier to maintain.

if you pay attention to making your code readable at the time of writing it, you will write code that is less complex and easier to maintain.

---
## Standards and Conventions

Coding standards have been developed to encourage consistency across everyone writing
Python code, and the aim is to make code feel familiar even when someone else has written
it.  This helps reduce the amount of effort it takes to read and edit code that you haven’t
written yourself.

Python is inherently very readable compared to many programming languages; sticking to a
coding standard will make it even easier to read. The main coding standard for Python is
PEP8 (Python Enhancement Proposal 8), established in 2001.



Linters such as Flake8 and Pylint highlight places where your code doesn’t conform with PEP8. Automatic formatters such as Black will update your code automatically to conform with coding standards. A linter is a tool that automatically checks your code for mistakes, inconsistencies, or style issues.

---
## Names

When writing code for data science, you’ll need to choose names at many points: names of
functions, variables, projects and even whole tools. Your choice of names affects how easy it
is to work on your code. If you choose names that are not descriptive or precise, you’ll need
to keep their true meaning in your head, which will increase your code’s cognitive load.

--
## Cleaning up
After testing your code, clean it by removing commented-out sections and unnecessary print() statements, as these make code confusing and lower project standards. Untidy code signals that poor quality is acceptable and may spread bad practices, a concept known as the Broken Window Theory.

To improve quality, you can refactor your code. Refactoring means restructuring it to be more efficient or reusable without changing its overall behaviour. Tests are essential in this process to confirm the code still works as intended.

---
## Documentation
Documentation makes code easier to understand and use, both for others and for your future self. It can range from inline comments and function docstrings to README files and full tutorials. Good documentation encourages others to use your code, but it must also be kept up to date—outdated documentation is worse than none, as it creates confusion and wastes time.

---
## Performance
Good code should be performant in both speed and memory usage. Choosing efficient data structures and algorithms helps avoid unnecessary slowdowns, and it’s important to identify which parts of code take the most time. Performance matters most in production, where code may run millions of times daily—small optimisations can save significant time and prevent your code from becoming a bottleneck in larger applications.

---
## Robustness
Good code should be robust, meaning it runs reliably from start to finish and handles unexpected inputs gracefully. Robustness is achieved through proper error handling, clear logging, and thorough testing to prevent failures and ensure reproducibility.

---
## Error and Logging
Robust code should behave predictably when given incorrect input. As a developer, you need to make an explicit decision on how your code should respond—either crash and raise an error, handle the issue gracefully with a clear alert or warning, or fail silently and continue execution. For example, if a CSV file loads with only half the expected rows, you must decide whether the program should stop with an error, process the available data with a warning, or proceed without notice. The key is to consciously choose a strategy for error handling rather than leaving behaviour undefined. If the error is handled, it can still be important to record that it has happened so that it doesn’t fail silently, if that’s not what you want to happen. This is one use case for logging.

---
## Testing

Testing is essential for writing robust and reliable code. There are two main types of testing: user testing, where a person manually interacts with the software to check if it behaves correctly, and automated testing, where code is used to verify expected behaviour.

Tests are important because code that works perfectly on one machine may fail on another, or even on the same machine in the future. This can happen due to changes in data, updates to libraries, or differences in Python versions across environments. Automated tests ensure that others can verify your code works correctly on their systems.

There are different kinds of automated tests. Unit tests focus on a single function, integration tests cover a group of functions working together, and end-to-end tests validate an entire project workflow. A practical approach to introducing testing in a large codebase with no existing tests is to add a test whenever something breaks, ensuring that the same error cannot occur again.

---
## Key Takeaways

Writing good code has several benefits. It makes your code easier for others to use, helps you quickly understand your own work when revisiting it after a long time, and allows your code to scale and integrate with larger systems. Well-written code also simplifies the process of adding new features that were not part of the original plan.

In summary, here are some ways to think about how to write good code:

_Simplicity:_
Your code should avoid repetition, unnecessary complexity, and unneeded lines of code.

_Modularity:_
Your code should be broken down into logical functions, with well-defined inputs and
outputs.

_Readability:_
Your code should follow the PEP8 standard for formatting, contain well-chosen names,
and be well documented.

_Performance:_
Your code should not take an unnecessarily long time to run or use up more resources
than are available.

_Robustness:_
Your code should be reproducible, raise useful error messages, and handle unexpected
inputs without failing











