# Whiteboard advices

### First, Restate the Question:

Do you understand what they’re asking you to do? Prove it. Restate the question for them and seek affirmation. You might actually be surprised to find you don’t fully understand what they’re asking for — perhaps the question is similar, but not the same, as a practice problem you have completed in the past. Using the tried-and-true fizz-buzz example, you could restate the problem as follows:

“So I’d like to restate the problem to you to make sure I understand what you’re looking for. The sole parameter for my function will be an integer. The sole output of my function will be an incrementing array, starting from the number 1 and ending at the input number.
If a number is a multiple of 3, the output will instead be `fizz`. If a number is a multiple of 5, the output will instead be `buzz`. However, if the output is a multiple of both 3 and 5, the output will instead be `fizzbuzz`. Is my understanding correct?”
The interview should give you affirmation or, perhaps, your understanding is incorrect and they will help you understand. There is no situation in which restating the problem will hurt you — it shows you can articulate a problem and gives you time to think it through a bit while you discuss. Furthermore, starting the discussion this way will help quell some nerves that might otherwise manifest while trying to solve the actual challenge.

### Ask About Edge Cases:

It’s still not time to dive right into coding the solution. Think for a bit about the inputs and expected output and think about potential edge cases to the problem. Ask about them. In many cases, the interviewer hasn’t even thought about edge cases and will make something up. That’s great — it shows you’re analytical and will work hard to try to prevent bugs (which often crop up due to edge cases).

Let’s use the fizz-buzz example. After successfully restating the problem, a valid way to ask about edge cases would be as follows:

“Now that I confirmed my understanding of the problem, I’d like to ask about some potential edge cases. Is it possible that the input would be a type other than a number? If so, what should the function do? Can the input be 0 or negative? Again, if so, what should the function do?”


### Write Pseudocode and Ask If It Makes Sense

(Write Pseudocode and Check Your Logic)


Again, you don’t actually want to start writing code in an actual language. You’ll find yourself constrained by trying to remember the methods or other idiosyncrasies of the language rather than trying to come up with the correct logic. Instead, let your interviewer know you’re going to start by writing pseudocode and fill in the actual code later. (Coincidentally, this is a reasonable way to write actual code as well).

Here’s the kicker: you can ask if your pseudocode makes sense to the interviewer. It’s possible they will be the type that doesn’t want to “give you hints,” but it’s also possible they’ll be more interested in how you think and want to discuss your pseudocode with you. When I interview candidates, I’m more interested in the latter — rarely do we ever actually develop software in a vacuum.

In other words, in the worst case the interviewer will tell you to continue without actually offering feedback. In the best case, the interviewer might actually point out logical flaws in your pseudocode that will give you some serious benefit when transitioning to actual code.

Super bonus: If your pseudocode looks good but you end up having difficulty translating it to actual code, you have actually earned a lot of points by now! Sure, in some elite companies they won’t accept anything but functional code, but simply being able to reason through the pseudocode is sufficient for many great companies.

In keeping with our fizz-buzz example, let’s say we came up with the following pseudocode. We’ll ultimately be writing our code in javascript, but it hardly matters at this point.


### Bonus: Communicating Prior to the Interview

You should have a human resources or interview point of contact prior to the interview. Are you curious whether there will be a coding portion of the interview? Ask them! Furthermore, you can ask if there is anything in particular you should prepare. They very well might give you hints like specifying the language in which they’ll ask questions, the number of questions, the style of question (e.g., develop an algorithm vs. find the bug). They might tell you whether you’ll be sitting at a computer or standing at a whiteboard — very useful information you might be able to use to practice or, at the very least, mentally prepare.
