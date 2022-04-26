emacs-gradle-mode
=================

Minor mode for emacs to run gradle from emacs and not have to go to a terminal!

# Installation #

Installation on doom emacs 
```lisp
(package! gradle-mode
  :recipe (:host github :repo "caishuyao/emacs-gradle-mode"))
```


Or you can just dump `gradle-mode.el` in your load path somewhere.

After installation, you can configure this mode to always be on with:

```lisp
(require 'gradle-mode)

(gradle-mode 1)
```

Or just

    M-x gradle-mode

when you are ready to use it.

## Keybindings ##
Keybindings for doom emacs

* `SPC c g b`
  - run `gradle build`
* `SPC c g t`
  - run `gradle test`
* `SPC c g s`
  - run `gradle test -Dsingle.test="user-supplied"`
  - User supplies test to run from prompt
* `SPC c g d b`
  - run `gradle build --daemon`
* `SPC c g d t`
  - run `gradle test --daemon`
* `SPC c g d s`
  - run `gradle -Dsingle.test="user-supplied" --daemon`
  - User supplies test to run from prompt
* `SPC c g d`
  - run `gradle "user-supplied" --daemon`
  - User supplies tasks to run from prompt
* `SPC c g r`
  - run `gradle "user-supplied"`
  - User supplies tasks to run from prompt

The prefix `d` runs the command with gradle's daemon, or creates one
if it is not already present.



