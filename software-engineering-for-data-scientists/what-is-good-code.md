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











