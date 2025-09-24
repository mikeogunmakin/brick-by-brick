**what is good code?**
a number of ways to think about this: the best code could be the code that runs fastest. Or it
could be easiest to read. Another possible definition is that good code is easy to maintain.
That is, if the project changes, it should be easy to go back to the code and change it to
reflect the new requirements. The requirements for your code will change frequently
because of updates to the business problem you’re solving, new research directions, or
updates elsewhere in the codebase.

Why good code matters? 
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

Technical debt (often abbreviated as tech debt) is a commonly used term for deferred work resulting from
when code is written quickly instead of correctly. Tech debt can take the form of missing documentation,
poorly structured code, poorly named variables, or any other cut corners. These make the code harder to maintain or refactor, and it’s likely that you will spend more time in the future fixing bugs than you would
have spent writing the code well in the first place. That said, tech debt is often necessary because of
business deadlines and budgets. You don’t always have time to polish your code.

How to Adapt to Changing Requirements?
Writing code is not like building a bridge, where the design is thoroughly worked out, the
plans are fixed, and then construction happens. The one constant in writing code, for a data
science project or anything else, is that you should expect things to change as you work on a
project. These changes may be the result of your discoveries through your research
process, changing business requirements, or innovations that you want to include in the
project. Good code can be easily adapted to work well with these changes.

This adaptability becomes more important as your codebase grows. With a single small
script, making changes is simple. But as the project grows and gets broken out into multiple
scripts or notebooks that depend on each other, it can become more complex and harder to
make changes. Good practices from the start will make it easier to modify the code in a
larger project.

















