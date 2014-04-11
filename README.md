# Typechecking tests for Compilers

Historically, [Rick Ord's 131](http://cseweb.ucsd.edu/~ricko/CSE131/) has let the students keep a shared collection of compiler tests. More tests and more contributors means:

* Better coverage
* <del>Lazy</del> overworked TAs might use some for the autograder
* Better grades for everyone

Sounds like a plan?

If you're in someone else's class, make sure to ask if it's ok before you share. Even if it's not, read [How it works](#how-it-works) and then [skip down](#hermits) to see how you can use this for yourself.

# How it works

The TAs' autograder feeds your project broken source files and makes sure it prints what it's supposed to. You can use your own to do the same.

This repository format is compatible with [Yuno](https://github.com/bulatb/yuno) and with [SOtest](https://bitbucket.org/elliottslaughter/cse131-sotest/wiki/Home), both written for 131. A basic test case has two parts: the source file `testname.rc` with code to be compiled, and the answer file `testname.ans.out` with the expected output.

A minimal Compilers repo, organized by phase and check, would look like this:

    this-repo/
        phase1/
            check1/
                first.rc
                first.ans.out
            check2a/
                (etc)
        phase2/
            (etc)

But in a class so large, you'll sometimes want to do things like:

* Run just your own tests
* Figure out whose tests are broken
* Make it obvious when someone edits one of yours

For that, each group should pick one partner's ACS account and keep their tests in folders with that name. If you want your group to be contactable, like for getting @mentioned on GitHub, add your GitHub usernames or other contact info to `authors/<acs name>.txt`. Keep in mind your info will be public—no emails if you don't want spam.

A nice Compilers repo looks like this:

    this-repo/
        phase1/
            check1/
                bbochkar/
                    bitwise-ops.rc
                    bitwise-ops.ans.out
                jpink/
                    float-ops.rc
                    float-ops.ans.out
                (etc)
            check2a/
                eslaught/
                    plusplus.rc
                    plusplus.ans.out
                minusminus.rc         # Someone didn't make a folder for
                minusminus.ans.out    # their group - that's ok too.
        phase2/
            check10/
                bbochkar/
                    (etc)
        (etc)
        authors/
            bbochkar.txt
            eslaught.txt
            jpink.txt

And an authors file:

    $ cat authors/jpink.txt
    Jesse Pinkman - jpinkman at ieng6 - github.com/SCIENCE_BITCH
    Walter White - walt.h.white at vamanos - github.com/goddamnright
