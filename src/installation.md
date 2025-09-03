# Installation and setup

## Clojure CLI & Emacs

Add the following packages to your NixOS configuration file (residing usually in `/etc/nixos/configuration.nix`):

```nix
clojure
emacs
git
git-credential-oauth
```

## Prelude

Check if you have an Emacs configuration file or directory and, if so, rename it (as we will use the Prelude configuration):

```bash
mv ~/.emacs ~/.emacs-backup
mv ~/.emacs.d ~/.emacs.d-backup
```

Clone the Prelude configuration as your Emacs configuration directory (this is why we installed `git` in the previous section):

```bash
git clone https://github.com/bbatsov/prelude.git ~/.emacs.d
```

Copy the modules sample:

```bash
cp ~/.emacs.d/sample/prelude-modules ~/.emacs.d/
```

Activate the Clojure module by removing the `;;` from the line containing `(require 'prelude-clojure)`.
The section will look as follows:

```elisp
;;; Programming languages support
;;
;; Modules for a few very common programming languages
;; are enabled by default.

(require 'prelude-c)
(require 'prelude-clojure)
;; (require 'prelude-coffee)
;; (require 'prelude-common-lisp)
```

Open Emacs to trigger the installation of all packages required by Prelude.
This may take up to a minute, depending on your connection speed.
The setup process will have ended when your minibuffer displays the message *Prelude is ready to do thy bidding, master ...*

If Emacs displays a lot of warnings in a separate buffer at the lower half of the window, you can mute them by inserting the following in `~/.emacs.d/init.el`:

```elisp
;; Do not display warnings
(setq warning-minimum-level :error)
```
