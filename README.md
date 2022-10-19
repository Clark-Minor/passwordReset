<!-- START doctoc generated TOC please keep comment here to allow auto update -->
<!-- DON'T EDIT THIS SECTION, INSTEAD RE-RUN doctoc TO UPDATE -->
**Table of Contents**  *generated with [DocToc](https://github.com/thlorenz/doctoc)*

- [Title](#title)
- [Question](#question)
- [Flag](#flag)
- [Author](#author)
- [Difficulty](#difficulty)
- [Walkthrough](#walkthrough)
- [Hint](#hint)
- [Points](#points)

<!-- END doctoc generated TOC please keep comment here to allow auto update -->

# Password Reset
## AUTHOR:
Clark Minor, UCLA

## DESCRIPTION:
Andy forgot his BookFace login again. He has been sent a link to reset his password. A 5-digit verification code was sent to his cell phone, but unfortunately, he lost that too. Can you help Andy retrieve his password?

### HINTS:
1. Using a scripting language -- especially one with an easy-to-understand *requests* library -- might be helpful for automating verification code guesses.

### HINT PENALTY:
12

### DIFFICULTY LEVEL:
MEDIUM

### POINT ASSIGNMENT:
40

# SOLUTION:
flag{zuck_it_suckerberg}

## WALKTHROUGH:

The problem can be solved using the script bruteforce.py in this folder (you may have to adjust the target url). I created bruteforce.py by googling "brute force a login with python". Here are the articles I read:

- https://coderinaero.wordpress.com/2014/12/08/brute-force-a-website-login-in-python/
- http://mechanize.readthedocs.io/en/latest/browser_api.html#the-response
- http://jmduke.com/posts/a-gentle-introduction-to-itertools/
- https://docs.python.org/2/library/itertools.html

**Note:** Installing the dependencies for these libraries was pretty annoying. You may have to spend some time troubleshooting


The inspiration for this problem came from a real vulnerability in FaceBook's beta login page. Anand Prakash, the whitehat who found the vulnerability, was awarded a $15,000 bug bounty for finding it. He showed a solution to the problem using BurpSuite. Here are some references for his solution:

- https://medium.freecodecamp.org/responsible-disclosure-how-i-could-have-hacked-all-facebook-accounts-f47c0252ae4d
- https://www.youtube.com/watch?v=U3Of-jF1nWo
- https://www.youtube.com/watch?v=25cazx5D_vw
