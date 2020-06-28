# Frontend Architecture

## Goal

There is a lot of mistakes that we see in the projects, but still we repeat them,
falling and falling again in these issues. These patterns initially look harmless, but when
the project grows and requirements evolve, those small and harmless decisions will follow
you until the end.

This repository will be a reference point to avoid these mistakes and help to write better
code each day.

For the examples, I'll use React for familiarity, but they can be applied to any project.

## Topics

1. Functions should do only one thing. Functions should be short.
Bigger functions are not better. When I see a big function during a code review, sometimes I
assume it's doing weird, hard or hacky stuff and I tend to leave them for the end of the review. This
should not be the case. I think here is where the rest of the problems tend to appear.

I think this is one of the hardest to follow, but one of the most fundamentals. At least, try to worry
about your functions. Think always about this and try to reduce it as much as possible (by creating other
functions of course).

2. Forms:
2.1. Map your data before sending it.
A lot of times (and here is where the trap is...), forms have a lot of fields that are almost exactly as the
API. So you can have a function that takes the values from the forms and automatically you send them to the API,
but what if the API contract changes? Here is where the trap is, and that is: changing the names in the form.

Your form is one thing and the service it consumes is another thing. Any of them should worry about the other one.
How to solve this? by using a function that transforms the form data into the service input.

3. Boundaries


## Resources

- Clean Code https://www.amazon.com/-/es/Robert-C-Martin/dp/0132350882

