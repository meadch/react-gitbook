# Introducing React

What is React?

If you’ve gone through a stack or two at the Dojo, you already know that the first full-stack applications you build –- be it in Python, JavaScript or Ruby –- used server-side rendering. We just wrote some logic into our HTML templates and had our interpreter substitute code that the browser could read before sending it back as an HTTP response.

A little further down the line, you picked up some Ajax skills and started using JavaScript to make requests to the server. Out went those ugly page refreshes, and in came single-page applications for a much-improved user experience.

That presented us with a challenge: How should we organize our (front-end) JavaScript code to best figure out what HTML to spit out to the browser? Or, how should we generate UI?

That's all React is: a strategy for generating UI based on the current **state** of an application.