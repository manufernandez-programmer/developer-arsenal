# Developer Arsenal

A practical developer encyclopedia and quick-reference manual for everyday development tools.

---

This arsenal is divided into two:

⚡ QUICK MODE

Need to remember something?
Find it, grab the command, and keep working.

🎓 LEARNING MODE

Don't understand something?
See a real example, break it down, understand what happened, then return to Quick Mode.

---

<a id="map"></a>

## 🗺️ Map

| Topic | ⚡ Quick Mode | 🎓 Learning Mode |
| --- | --- | --- |
| Fundamentals | — | [Command anatomy, shortcuts, exit codes](#learning-fundamentals) |
| Terminal | [Commands](#quick-terminal) | [Examples and effects](#learning-terminal) |
| Python | [Run and compile](#quick-python) | [First program and syntax](#learning-python) |
| Git & GitHub | [Reference](#quick-git) | [Local history to a reviewed PR](#learning-git) |
| Nano | [Shortcuts](#quick-nano) | [Editing walkthrough](#learning-nano) |
| Fish | [Sessions and functions](#quick-fish) | [Define and save a function](#learning-fish) |
| Utilities | [Inspect tabs](#quick-utilities) | [Review an indentation conversion](#learning-utilities) |

## Before copying a command

This is a reference, not a script to run from top to bottom. Names such as
`file`, `path`, `command` and `URL` are placeholders. Replace them deliberately;
quote paths with spaces, for example `cat "my notes.txt"`. With GNU file tools,
`--` ends option parsing: `rm -- "-draft.txt"` treats the name as a filename.

Examples target Linux with GNU utilities, Bash and current Fish. Fish function
syntax is labeled separately; it is not Bash syntax. Wayland clipboard examples
need `wl-clipboard` and an accessible compositor. Use `python --version`,
`git --version`, `fish --version` or `nano --version` to check your own tools.
Reading the manual requires no installation; install only tools you choose to use.

**Know the effect:** `rm` deletes; `cp` and `mv` can overwrite; `>` truncates an
existing destination before the command runs; `git push` publishes history.
Inspect paths and changes first. Work on disposable copies while learning, and
never pipe private files or logs to the clipboard without checking their contents.

<a id="quick-mode"></a>

## ⚡ Quick Mode

<a id="quick-terminal"></a>

### 💻 TERMINAL

[🧭 Navigation](#quick-terminal-navigation) · [📄 Files & Directories](#quick-terminal-files-directories) · [🔎 Search](#quick-terminal-search) · [📋 Clipboard](#quick-terminal-clipboard) · [🔀 Redirection & Pipes](#quick-terminal-redirection-pipes) · [⚙️ Options](#quick-terminal-options) · [🔣 Symbols & Sequences](#quick-terminal-symbols-sequences)

<a id="quick-terminal-navigation"></a>

#### 🧭 NAVIGATION

`pwd` → Show the current directory

`cd path` → Move to another directory

`cd ..` → Move to the parent directory

`ls` → List files and directories

---

<a id="quick-terminal-files-directories"></a>

#### 📄 FILES & DIRECTORIES

`cat file` → Display the entire contents of a file

`nano file` → Open or create a file for editing

`less file` → View a file without editing it

`mkdir directory` → Create a directory

`mkdir -p path/directory` → Create a directory path, including missing
parent directories

`cp source destination` → Copy a file; may overwrite the destination

`mv source destination` → Move or rename a file; may overwrite the destination

`rm file` → Delete a file directly, without using the trash

`rm -r directory` → Delete a directory tree; inspect the target first

`.bak` → Common suffix used to identify a backup copy

##### 🔒 Backup

`cp -i -- source destination.bak` → Copy with a prompt before overwriting

Choose a new backup name. Declining the prompt does not create a fresh backup.

---

<a id="quick-terminal-search"></a>

#### 🔎 SEARCH

`grep pattern file` → Search for a pattern inside a file

`grep -n pattern file` → Show matching lines with line numbers

`grep -P '\t' file` → Search for TAB characters (requires PCRE support)

`grep -Fn -- "literal.text" file` → Search for literal text with line numbers

---

<a id="quick-terminal-clipboard"></a>

#### 📋 CLIPBOARD

`wl-copy` → Copy data to the Wayland clipboard

`cat file | wl-copy` → Copy an entire file to the clipboard

`command | wl-copy` → Copy a command's standard output

`command 2>&1 | wl-copy` → Copy both standard output and errors

---

<a id="quick-terminal-redirection-pipes"></a>

#### 🔀 REDIRECTION & PIPES

`command1 | command2` → Send the output of one command to another

`command > file` → Write standard output; creates or truncates the file

`command1 && command2` → Run the second command only if the first
succeeds

`command 2>&1` → Merge error output with standard output

---

<a id="quick-terminal-options"></a>

#### ⚙️ OPTIONS

`mkdir -p` → Create missing parent directories

`rm -r` → Remove directories recursively

`grep -n` → Show line numbers for matches

`grep -P` → Interpret the pattern as a Perl-compatible regular
expression

---

<a id="quick-terminal-symbols-sequences"></a>

#### 🔣 SYMBOLS & SEQUENCES

`/` → Separate parts of a path

`~` → Home directory

`.` → Current directory

`..` → Parent directory

`|` → Pipe output into another command

`>` → Redirect output; creates or truncates the destination

`&&` → Continue only if the previous command succeeds

`2>&1` → Merge standard error into standard output

`\t` → TAB escape notation when the receiving tool interprets it

`\` → Continue a command on the next line

<a id="quick-python"></a>

### 🐍 PYTHON

[▶️ Running Programs](#quick-python-running-programs) · [🔍 Syntax Checking](#quick-python-syntax-checking)

<a id="quick-python-running-programs"></a>

#### ▶️ RUNNING PROGRAMS

`python script.py` → Run a Python program

`python script.py argument` → Run a Python program with a command-line
argument

---

<a id="quick-python-syntax-checking"></a>

#### 🔍 SYNTAX CHECKING

`python -m py_compile script.py` → Check Python syntax without running
the program; normally writes bytecode under `__pycache__/`

<a id="quick-git"></a>

### 🧬 GIT & GITHUB

[📦 Repository](#quick-git-repository) · [🔎 Status](#quick-git-status) · [🔄 Fetch & Pull](#quick-git-fetch-pull) · [📥 Staging](#quick-git-staging) · [💾 Commits](#quick-git-commits) · [🌿 Branches](#quick-git-branches) · [🪪 Identity](#quick-git-identity) · [🙈 .gitignore](#quick-git-gitignore) · [🌎 Remotes](#quick-git-remotes) · [🚀 Push](#quick-git-push) · [🐙 GitHub CLI](#quick-git-github-cli)

<a id="quick-git-repository"></a>

#### 📦 REPOSITORY

`git init` → Initialize a Git repository in the current directory

---

<a id="quick-git-status"></a>

#### 🔎 STATUS

`git status` → Show working tree/staging state and, when configured, branch
comparison with the locally stored upstream reference; does not contact GitHub

---

<a id="quick-git-fetch-pull"></a>

#### 🔄 FETCH & PULL

`git fetch` → Download remote history and refresh remote-tracking references;
remote selection follows configuration

`git fetch origin` → Fetch explicitly from `origin`; with standard tracking
configuration, updates `origin/main` without moving local `main` or its files

`git pull --ff-only` → Fetch, then advance the current branch to its upstream
only if no divergent history needs integrating; can update working files

**Fast-forward:** move a branch to a descendant commit without a merge commit.
A clean working tree and a fresh remote reference answer different questions.
See [the stale-reference example](#learning-git-fetch-pull).

---

<a id="quick-git-staging"></a>

#### 📥 STAGING

`git add file` → Add a file to the staging area

`git add .` → Stage additions, modifications and deletions under the current
directory (subject to ignore rules for untracked files)

---

<a id="quick-git-commits"></a>

#### 💾 COMMITS

`git commit -m "message"` → Create a commit with a message

---

<a id="quick-git-branches"></a>

#### 🌿 BRANCHES

`git branch -m main` → Rename the current local branch to `main`

`git switch -c docs-improvement` → Create and switch to a work branch

`git diff` → Inspect unstaged changes

`git diff --cached` → Inspect staged changes before committing

---

<a id="quick-git-identity"></a>

#### 🪪 IDENTITY

`git config --global user.name "Your Name"` → Set your global Git author
name for all repositories unless overridden locally

`git config --global user.email "you@example.com"` → Set your global Git
author email for all repositories unless overridden locally

---

<a id="quick-git-gitignore"></a>

#### 🙈 .GITIGNORE

`.gitignore` → Define patterns for untracked files Git should ignore; does not
untrack existing files or erase history

`*.bak` → Ignore files ending in `.bak`

`directory/` → Ignore a directory

---

<a id="quick-git-remotes"></a>

#### 🌎 REMOTES

`git remote add origin URL` → Add a remote repository named `origin`

`git remote -v` → Show configured remotes and their URLs

---

<a id="quick-git-push"></a>

#### 🚀 PUSH

`git push -u origin main` → Push `main` to `origin` and set its upstream
branch

`git push` → Push according to remote, upstream and `push.default` settings

---

<a id="quick-git-github-cli"></a>

#### 🐙 GITHUB CLI

`gh --version` → Show the installed GitHub CLI version

`gh auth login` → Authenticate GitHub CLI; changes stored credentials

<a id="quick-nano"></a>

### ✏️ NANO

These are traditional bindings. Nano 8+ also supports `Ctrl + F` for forward
search. Custom bindings or modernbindings mode can differ; `Ctrl + G` opens
help with traditional bindings. Check the shortcut bar in your own session.

[🧭 Navigation](#quick-nano-navigation) · [✏️ Editing](#quick-nano-editing) · [💾 Save & Exit](#quick-nano-save-exit)

<a id="quick-nano-navigation"></a>

#### 🧭 NAVIGATION

`Ctrl + W` → Search for text

`Alt + W` → Find the next occurrence

`Alt + G` → Go to a specific line and column

---

<a id="quick-nano-editing"></a>

#### ✏️ EDITING

`Ctrl + K` → Cut the current line or selected text

`Ctrl + U` → Paste the last cut text

`Alt + A` → Start or end text selection

`Alt + U` → Undo

`Alt + E` → Redo

`Ctrl + \` → Search and replace

---

<a id="quick-nano-save-exit"></a>

#### 💾 SAVE & EXIT

`Ctrl + O` → Write the current buffer to a file

`Enter` → Confirm the filename when saving

`Ctrl + X` → Exit Nano

`Ctrl + C` → Cancel the current action when applicable

<a id="quick-fish"></a>

### 🐟 FISH

[🖥️ Sessions](#quick-fish-sessions) · [🔎 Command Lookup](#quick-fish-command-lookup) · [⚙️ Functions](#quick-fish-functions)

<a id="quick-fish-sessions"></a>

#### 🖥️ SESSIONS

`exit` → Exit the current Fish shell session

---

<a id="quick-fish-command-lookup"></a>

#### 🔎 COMMAND LOOKUP

`type name` → Inspect how Fish resolves a command name without invoking it

`type -t name` → Print its category: `function`, `builtin` or `file` (executable)

`type -a name` → Show all matching definitions, including shadowed commands

Fish aliases are functions; `type -t` does not report a separate `alias` category.
See [examples and limits](#learning-fish-command-lookup).

---

<a id="quick-fish-functions"></a>

#### ⚙️ FUNCTIONS

`function name` → Start defining a function

`end` → End the function definition

`funcsave name` → Write a defined function to Fish configuration for future
sessions; can replace a saved function with that name

<a id="quick-utilities"></a>

### 🧰 UTILITIES

[🧹 Indentation Cleanup](#quick-utilities-indentation-cleanup)

<a id="quick-utilities-indentation-cleanup"></a>

#### 🧹 INDENTATION CLEANUP

`grep -nP '\t' file.py` → Locate TAB characters (GNU grep with PCRE)

`expand -i -t 4 -- file.py` → Preview conversion of leading tabs on standard output

Do not automatically replace a source file. Even leading whitespace can be data
inside a multiline string, and Make recipes may require tabs. See the
[review-first conversion example](#learning-utilities-indentation-cleanup).

[Back to the map](#map)

<a id="learning-mode"></a>

## 🎓 Learning Mode

Never used one of these tools before, or found something in Quick Mode
that you don't understand?

This section explains the same core material from the ground up with
concrete examples.

When useful, examples answer five questions:

1.  What do I want to do?
2.  What do I type?
3.  What might the terminal return?
4.  What does each part mean?
5.  What just happened?

<a id="learning-fundamentals"></a>

### 🧠 FUNDAMENTALS

[🧩 Command Anatomy](#learning-fundamentals-command-anatomy) · [⌨️ Shortcuts](#learning-fundamentals-shortcuts) · [🚦 Exit Codes](#learning-fundamentals-exit-codes)

<a id="learning-fundamentals-command-anatomy"></a>

#### 🧩 COMMAND ANATOMY

A common command-line pattern looks like this:

command -option argument

##### 🧩 Visual Breakdown

```text
command -option argument
│       │       │
│       │       └── Argument → What the command receives or acts on
│       └────────── Option → Changes how the command behaves
└────────────────── Command → The program or instruction being executed
```

##### Command

A command tells the system which program or instruction you want to
execute.

`pwd`

Here, `pwd` is the command. It prints the path of the current working
directory.

##### Option

An option modifies how a command behaves.

`grep -n error file.txt`

##### 🧩 Visual Breakdown

```text
grep -n error file.txt
│    │  │     │
│    │  │     └── File to search
│    │  └──────── Pattern to search for
│    └─────────── Option: show line numbers
└──────────────── Command
```

Options belong to the command that interprets them. The same option can
mean different things for different commands.

##### Argument

An argument provides information to a command.

`cp source.txt backup.txt`

##### 🧩 Visual Breakdown

```text
cp source.txt backup.txt
│  │          │
│  │          └── Destination argument
│  └───────────── Source argument
└──────────────── Command
```

Arguments can tell a command what to work with, what to search for,
where to operate, or other data it needs.

---

<a id="learning-fundamentals-shortcuts"></a>

#### ⌨️ SHORTCUTS

A shortcut is a key combination interpreted by the program you are
currently using.

For example, inside Nano:

`Ctrl + O`

This starts Nano's Write Out action.

You did not type a shell command. You triggered an action inside Nano.

Shortcuts are context-dependent: the same key combination can behave
differently in different programs.

---

<a id="learning-fundamentals-exit-codes"></a>

#### 🚦 EXIT CODES

Programs return an exit status when they finish.

`0` usually means successful completion.

A non-zero value means something else happened, but the exact meaning
depends on the program.

For example:

`grep -nP '\t' script.py`

If `grep` finds a match, it exits with:

`0`

If it finds no selected lines, it exits with:

`1`

That does not necessarily mean the computer exploded. It means `grep`
did not find what you asked it to find.

Some useful codes encountered in real workflows:

`0` → Successful completion

`1` → Program-specific non-zero result; for `grep`, no selected lines

`127` → Common shell status for command not found

`2` → For GNU grep, an error (for example, an unreadable file)

`128` → Seen when Git terminates with a fatal error; the message
explains the actual cause

`130` → Common status after interruption with `Ctrl + C` / SIGINT

The number is a clue. The program's error message and context tell you
what actually happened.

So `[1]` is not automatically guilty.

Pedro can remain free... for now.

<a id="learning-terminal"></a>

### 💻 TERMINAL

[🧭 Navigation](#learning-terminal-navigation) · [📄 Files & Directories](#learning-terminal-files-directories) · [🔎 Search](#learning-terminal-search) · [📋 Clipboard](#learning-terminal-clipboard) · [🔀 Redirection & Pipes](#learning-terminal-redirection-pipes) · [🔣 Symbols & Sequences](#learning-terminal-symbols-sequences)

<a id="learning-terminal-navigation"></a>

#### 🧭 NAVIGATION

##### 📍 Find your current location

1. What do I want to do?

Find out which directory I am currently in.

2. What do I type?

`pwd`

3. What might the terminal return?

`/home/user/projects`

4. What does each part mean?

`pwd` → Print the current working directory.

5. What just happened?

The terminal showed your location. Nothing was modified.

---

##### 👀 See what is here

`ls`

Lists files and directories in the current location. It only reads the
directory; it does not modify its contents.

---

##### 🚶 Move into a directory

`cd projects`

##### 🧩 Visual Breakdown

```text
cd projects
│  │
│  └── Destination directory
└───── Command
```

`cd` changes the shell's current directory.

---

##### ⬆️ Move to the parent directory

`cd ..`

`..` represents the parent of the current directory: exactly one level
up.

<a id="learning-terminal-files-directories"></a>

#### 📄 FILES & DIRECTORIES

##### 👁️ Display a complete file

`cat script.py`

`cat` writes the file's contents to standard output. It does not edit
the file.

---

##### 📖 Read a file without editing it

`less README.md`

`less` opens a text viewer that lets you navigate through the file while
leaving it unchanged.

---

##### ✏️ Open or create a file for editing

`nano script.py`

Nano opens the file in a text editor. If the named file does not exist,
Nano can create it when you save.

---

##### 📁 Create a directory

`mkdir examples`

Creates a directory named `examples`.

---

##### 🏗️ Create a complete directory path

`mkdir -p project/examples`

##### 🧩 Visual Breakdown

```text
mkdir -p project/examples
│     │  │
│     │  └── Path
│     └───── Option
└─────────── Command
```

With `-p`, `mkdir` can also create missing parent directories.

---

##### 📄 Copy a file

`cp source.txt backup.txt`

##### 🧩 Visual Breakdown

```text
cp source.txt backup.txt
│  │          │
│  │          └── Destination
│  └───────────── Source
└──────────────── Command
```

The original remains in place. An existing destination file may be overwritten.
Use `cp -i -- source.txt backup.txt` for an overwrite prompt and confirm the
backup exists with the content you intended before relying on it.

Using a `.bak` suffix is a common convention for identifying a backup
copy:

`cp -i -- script.py script.py.bak`

`.bak` is only a naming convention. It has no magical backup behavior.

---

##### 🚚 Move or rename

`mv old.txt new.txt`

When source and destination are in the same directory, this effectively
renames the file. An existing destination can be overwritten; `mv -i -- old.txt new.txt`
asks first. These examples assume regular files, not destination directories.

---

##### 🗑️ Delete a file

`rm temporary.txt`

`rm` deletes directly. It does not automatically create a backup or move
the file to a recycle bin.

---

##### 🗑️ Delete a directory and its contents

`rm -r directory`

`-r` makes the operation recursive.

Be careful: this can remove an entire directory tree.

<a id="learning-terminal-search"></a>

#### 🔎 SEARCH

##### 🔍 Search inside a file

`grep error script.py`

Searches `script.py` for lines matching `error`.

To include line numbers:

`grep -n error script.py`

`grep` treats the pattern as a regular expression; use `grep -Fn -- "a.b" file`
for a literal string and quote patterns containing shell metacharacters.

To search for TAB characters using PCRE syntax (GNU grep with PCRE support):

`grep -nP '\t' script.py`

<a id="learning-terminal-clipboard"></a>

#### 📋 CLIPBOARD

`wl-copy` copies data to the Wayland clipboard.

That makes it Wayland-specific rather than a universal shell command.

##### Copy a complete file

`cat script.py | wl-copy`

##### 🧩 Visual Breakdown

```text
cat script.py | wl-copy
│   │         │ │
│   │         │ └── Receives data and copies it
│   │         └──── Pipe
│   └────────────── File
└────────────────── Produces the file contents
```

##### Copy normal output and errors

`command 2>&1 | wl-copy`

`2>&1` merges standard error into standard output before the pipe sends
the combined stream to `wl-copy`. This changes the session clipboard; it does
not create a backup. The command may fail when no Wayland session is available.

<a id="learning-terminal-redirection-pipes"></a>

#### 🔀 REDIRECTION & PIPES

##### `|` --- Pipe

`command1 | command2`

The pipe connects the first command's standard output to the second command's
standard input; standard error is separate unless redirected.
A pipeline can hide an earlier failure: Bash normally reports its last command's
status. In Bash, `set -o pipefail` changes that behavior; Fish also exposes
individual statuses through `$pipestatus`. Do not assume copying output proves success.

##### `>` --- Redirect output

`command > file`

Instead of displaying standard output normally, the shell writes it to
`file`.

Be aware that `>` truncates an existing destination before the program starts,
even if the program later fails. Never use the same file as input and redirected
output. `>>` appends instead, but still changes the file.

##### `&&` --- Continue only after success

`command1 && command2`

The second command runs only if the first returns a successful exit
status.

##### `2>&1` --- Merge error output with standard output

File descriptor `1` is standard output and `2` is standard error.

`2>&1` tells the shell to send standard error to the same destination
currently used by standard output.

You do not need to memorize file descriptors on day one. The useful
mental model is:

`command 2>&1 | wl-copy`

→ Send normal output and errors through the pipe.

<a id="learning-terminal-symbols-sequences"></a>

#### 🔣 SYMBOLS & SEQUENCES

`/` → Separates components in a path.

`~` → Represents the current user's home directory in shell expansion.

`.` → Represents the current directory in path contexts.

`..` → Represents the parent directory.

`|` → Pipes one command's standard output into another command's
standard input.

`>` → Redirects standard output to a file.

`&&` → Runs the next command only after successful completion of the
previous one.

`2>&1` → Redirects standard error to the current destination of standard
output.

`\t` → Common escape notation for a TAB character; interpretation
depends on the tool or language reading it.

`\` at the end of a shell line → Continues the command on the next line.

Example:

```sh
printf '%s\n' \
    file1.csv \
    file2.csv \
    file3.csv
```

The shell treats this as one command.

Visually it spans several lines. Logically it is:

`printf '%s\n' file1.csv file2.csv file3.csv`

It prints the names, without deleting files. The backslash must immediately
precede the newline; trailing spaces break the continuation.

<a id="learning-python"></a>

### 🐍 PYTHON

[▶️ Running Your First Program](#learning-python-running-your-first-program) · [🔍 Checking Syntax](#learning-python-checking-syntax)

<a id="learning-python-running-your-first-program"></a>

#### ▶️ RUNNING YOUR FIRST PROGRAM

Suppose `hello.py` contains:

```python
print("Hello")
```

Run it with:

`python hello.py`

The terminal prints:

`Hello`

##### 🧩 Visual Breakdown

```text
python hello.py
│      │
│      └── Python file to run
└───────── Python interpreter command
```

A Python program can also receive command-line arguments:

`python script.py input.csv`

Inside Python, tools such as `sys.argv` can access those arguments.

<a id="learning-python-checking-syntax"></a>

#### 🔍 CHECKING SYNTAX

`python -m py_compile script.py`

##### 🧩 Visual Breakdown

```text
python -m py_compile script.py
│      │  │          │
│      │  │          └── File to compile
│      │  └───────────── Module
│      └──────────────── Run a module
└─────────────────────── Python command
```

If the syntax is valid, this normally produces no terminal output.

If Python encounters a syntax problem, it reports the error.

This checks whether Python can compile the file; it does not run the
script's normal application flow. It normally writes a `.pyc` file under
`__pycache__/`. It does not test runtime behavior, imports, or logic; a successful
compile is not a passing application test.

<a id="learning-git"></a>

### 🧬 GIT & GITHUB

[🌎 Git vs GitHub](#learning-git-git-vs-github) · [🧠 Mental Model](#learning-git-mental-model) · [📦 Creating A Repository](#learning-git-creating-a-repository) · [🔎 Checking Status](#learning-git-checking-status) · [🔄 Fetch & Pull](#learning-git-fetch-pull) · [📥 Staging Changes](#learning-git-staging-changes) · [💾 Creating A Commit](#learning-git-creating-a-commit) · [🌿 Branches](#learning-git-branches) · [🪪 Configuring Identity](#learning-git-configuring-identity) · [🙈 .gitignore](#learning-git-gitignore) · [🌎 Connecting GitHub](#learning-git-connecting-github) · [🔐 Authentication](#learning-git-authentication) · [🚀 First Push](#learning-git-first-push) · [🔁 Everyday Workflow](#learning-git-everyday-workflow)

<a id="learning-git-git-vs-github"></a>

#### 🌎 GIT VS GITHUB

Git is the version-control system running on your machine.

It tracks changes and creates a history of your project.

GitHub is an online service that can host Git repositories and make
them available remotely.

You can use Git without GitHub.

GitHub uses Git repositories, but Git and GitHub are not the same thing.

---

<a id="learning-git-mental-model"></a>

#### 🧠 MENTAL MODEL

A basic Git workflow looks like this:

```text
                  LOCAL MACHINE

             ┌─────────────────┐
             │  WORKING TREE   │
             │   files edited  │
             └────────┬────────┘
                      │
                   git add
                      │
                      ▼
             ┌─────────────────┐
             │  STAGING AREA   │
             │ changes selected│
             └────────┬────────┘
                      │
                  git commit
                      │
                      ▼
             ┌─────────────────┐
             │ LOCAL REPOSITORY│
             │ commit history  │
             └────────┬────────┘
                      │
                   git push
                      │
                      ▼

                     🌎

             ┌─────────────────┐
             │     GITHUB      │
             │ remote repository│
             └─────────────────┘
```

The working tree is what you are currently editing.

The staging area contains changes selected for the next commit.

A commit records a snapshot in the local repository's history.

A remote is another repository your local repository can communicate
with.

---

<a id="learning-git-creating-a-repository"></a>

#### 📦 CREATING A REPOSITORY

Inside a project directory:

`git init`

Git creates a hidden `.git/` directory containing repository metadata
and history.

Do not treat `.git/` as ordinary project content to casually edit.

---

<a id="learning-git-checking-status"></a>

#### 🔎 CHECKING STATUS

`git status`

This tells you what Git currently sees: untracked files, modified files,
staged changes, and whether the working tree is clean.

A clean status does not list ignored files by default. It is not proof that
there are no local artifacts or that a project is ready to publish.

Branch comparisons use a local upstream reference, such as `origin/main`.
They do not query GitHub: “up to date” can describe an outdated snapshot.
See [fetch and pull](#learning-git-fetch-pull) before concluding that a local
branch includes the latest remote commits.

---

<a id="learning-git-fetch-pull"></a>

#### 🔄 FETCH, STATUS & PULL

| Command | Practical question / effect |
| --- | --- |
| `git status` | What changed locally, and how does this branch compare with its locally stored upstream? No network refresh |
| `git fetch origin` | What history is available from `origin` now? Downloads objects and refreshes tracking references with standard configuration; leaves the current branch and working files in place |
| `git pull --ff-only` | Can this branch advance to its upstream? Fetches first, then updates the branch and files if a fast-forward is possible; refuses divergent histories |

`origin` is a remote name. `origin/main` is a **local remote-tracking reference**,
not a live view of GitHub. Bare `git fetch` chooses remotes according to
configuration; naming `origin` makes the source explicit here.

Example: you are on `main`, tracking `origin/main`, with a clean working tree.
Someone has added one commit on GitHub since your last fetch:

```text
Before fetch:
Local main / origin/main: A
GitHub main:              A──B

After fetch:
Local main:               A
Local origin/main:        A──B

After fast-forward pull:
Local main / origin/main: A──B
```

1. Run `git status`: it may say `up to date with 'origin/main'`, because both
   local references still point to A. Wording depends on locale/version.
2. Run `git fetch origin`: refresh the local remote-tracking reference to B.
3. Run `git status` again: it now reports that `main` is behind by one commit
   and can be fast-forwarded. The working tree can still be clean.
4. After reviewing that state, run `git pull --ff-only` to bring in the change.
   It fetches again, so a remote update since step 2 may affect the result.
5. Run `git status` to confirm the resulting state against the fetched snapshot.

**Fast-forward** means the old branch tip is an ancestor of the target:
Git moves the branch pointer forward without creating a merge commit.
If local and remote histories each have their own new commits, they have
**diverged**; `--ff-only` refuses instead of selecting a merge/rebase strategy.
Stop and review those histories before choosing how to integrate them.

This walkthrough assumes the stated branch, upstream and clean working tree.
If `status` shows local edits or another branch/upstream, resolve that context
before pulling. A plain `git pull` may follow different integration settings;
use `--ff-only` to make the intended restriction explicit. A successful fetch
is a snapshot at that moment, not a promise that GitHub will remain unchanged.

References: [status](https://git-scm.com/docs/git-status),
[fetch](https://git-scm.com/docs/git-fetch),
[pull](https://git-scm.com/docs/git-pull),
[fast-forward merge](https://git-scm.com/docs/git-merge#_fast_forward_merge).

---

<a id="learning-git-staging-changes"></a>

#### 📥 STAGING CHANGES

Stage one file:

`git add README.md`

Stage the current set of changes in the current directory scope:

`git add .`

Staging does not publish anything and does not create a commit.

It selects changes for the next commit. Later edits are not staged automatically.
Before committing, inspect `git diff --cached`; use `git diff` for unstaged edits.

---

<a id="learning-git-creating-a-commit"></a>

#### 💾 CREATING A COMMIT

`git commit -m "Initial release"`

##### 🧩 Visual Breakdown

```text
git commit -m "Initial release"
│   │      │  │
│   │      │  └── Commit message
│   │      └───── Message option
│   └──────────── Subcommand
└──────────────── Git executable
```

A commit records the staged changes in local Git history.

The first commit in a repository is commonly called the root commit.

Git identifies commits with hashes; interfaces often show a shortened
form of the full ID.

---

<a id="learning-git-branches"></a>

#### 🌿 BRANCHES

A branch is a movable name pointing into a line of development.

To rename the current branch to `main`:

`git branch -m main`

For a new simple project, `main` can serve as the primary branch. Renaming a
local branch does not rename the remote branch.

For changes to an existing project, work on a separate branch:

```sh
git switch -c docs-improvement
```

This creates a branch at the current commit. Check `git status` first; uncommitted
changes may carry over. Use `git switch main` to return when appropriate.

---

<a id="learning-git-configuring-identity"></a>

#### 🪪 CONFIGURING IDENTITY

Git needs an author name and email before it can create commits.

For this repository only (run inside it):

```sh
git config user.name "Your Name"
git config user.email "you@example.com"
```

To intentionally apply the same defaults across your repositories, set them globally:

`git config --global user.name "Your Name"`

`git config --global user.email "you@example.com"`

`--global` applies the setting to your user-level Git configuration
rather than only the current repository.

The configured email can appear in commit metadata. Use an address you
are comfortable associating with your commits, or use an appropriate
privacy-preserving address provided by your hosting service.

##### A useful failure

An illustrative first workflow:

```text
git init → git add . → git commit → [128] author identity unknown
        → configure user.name and user.email → retry commit
```

The failed commit does not automatically erase the staging area.
After fixing the identity problem, the staged changes can still be
committed.

`128` alone does not mean "missing identity." It is a status Git can use
for fatal failures; the accompanying message tells you the actual cause.

---

<a id="learning-git-gitignore"></a>

#### 🙈 .GITIGNORE

A `.gitignore` file contains patterns for files and directories Git
should leave untracked.

Example:

```gitignore
*.bak
__pycache__/
*.pyc
```

`*.bak` → Match names ending in `.bak`.

`__pycache__/` → Ignore that directory.

`*.pyc` → Ignore Python bytecode files.

Ignore rules do not remove files already tracked or erase committed secrets.
Review staged files before publishing. If a real credential leaks, revoke or
rotate it; adding its filename to `.gitignore` does not undo the exposure.

`.gitignore` is useful for generated files, local artifacts, backups,
caches, and other content that does not belong in repository history.

---

<a id="learning-git-connecting-github"></a>

#### 🌎 CONNECTING GITHUB

A local repository can be connected to a remote repository:

`git remote add origin URL`

##### 🧩 Visual Breakdown

```text
git remote add origin URL
│   │      │   │      │
│   │      │   │      └── Remote repository URL
│   │      │   └───────── Conventional remote name
│   │      └───────────── Action
│   └──────────────────── Remote subcommand
└──────────────────────── Git executable
```

`origin` is a conventional name. It is not a special GitHub account or
server.

Check configured remotes with:

`git remote -v`

You may see separate fetch and push entries for the same remote.

---

<a id="learning-git-authentication"></a>

#### 🔐 AUTHENTICATION

GitHub authentication is separate from Git's local author identity.

The GitHub CLI can authenticate your GitHub account:

`gh auth login`

For a browser-based login flow, follow the instructions displayed by
GitHub CLI.

Do not share passwords, access tokens, or one-time authentication codes.

If you interrupt a command with `Ctrl + C`, the process may terminate
with status `130`.

That is not GitHub rejecting you. It means you interrupted the running
process.

---

<a id="learning-git-first-push"></a>

#### 🚀 FIRST PUSH

For a new repository with at least one commit on `main`, and a remote you own:

`git push -u origin main`

##### 🧩 Visual Breakdown

```text
git push -u origin main
│   │    │  │      │
│   │    │  │      └── Local branch to push
│   │    │  └───────── Remote name
│   │    └──────────── Set upstream
│   └───────────────── Subcommand
└───────────────────── Git executable
```

This sends commits from local `main` to `origin` and configures an
upstream relationship. It can publish all reachable committed content, including
anything sensitive in earlier commits. If rejected because the remote has its
own history, inspect and reconcile it; do not reach for a force push.

After that, the usual push can often be shortened to:

`git push`

---

<a id="learning-git-everyday-workflow"></a>

#### 🔁 EVERYDAY WORKFLOW

Once the repository is configured, a reviewable workflow is:

```text
Create a work branch → Edit → Inspect diff → Stage selected files
                    → Inspect staged diff → Commit → Push branch → Open PR
```

After creating `docs-improvement` and editing the documentation:

```sh
git status
git diff
git add README.md ARSENAL.md
git diff --cached
git commit -m "docs: clarify command examples"
git push -u origin docs-improvement
gh pr create --base main --head docs-improvement
```

Run each step after reviewing the preceding result. The last two commands publish
the branch and create a PR on GitHub; they require authentication and permission.
Adjust branch names to your repository. Opening a PR does not merge it.

The mental model is:

Edit → Inspect → Stage → Commit → Push

Do not memorize the commands as a magic incantation. Know which boundary
each command crosses.

`git add` → Working tree to staging area.

`git commit` → Staging area to local history.

`git push` → Local history to the remote repository.

<a id="learning-nano"></a>

### ✏️ NANO

These are traditional bindings. Nano 8+ also supports `Ctrl + F` for forward
search. Custom bindings or modernbindings mode can differ; `Ctrl + G` opens
help with traditional bindings. Check the shortcut bar in your own session.

[🧭 Navigation](#learning-nano-navigation) · [✏️ Editing](#learning-nano-editing) · [💾 Save & Exit](#learning-nano-save-exit)

<a id="learning-nano-navigation"></a>

#### 🧭 NAVIGATION

##### 🔍 Search for text

Inside Nano:

`Ctrl + W`

Type the search text and confirm.

Nano moves the cursor to a matching occurrence.

Use:

`Alt + W`

to move to the next occurrence.

To go directly to a line and column:

`Alt + G`

Nano shortcuts act inside Nano. They are not shell commands.

<a id="learning-nano-editing"></a>

#### ✏️ EDITING

`Alt + A` → Start or end text selection.

`Ctrl + K` → Cut the current line or selected text, depending on
context.

`Ctrl + U` → Insert the last cut/copied text.

`Alt + U` → Undo.

`Alt + E` → Redo.

`Ctrl + \` → Start search and replace.

Shortcut availability can depend on Nano version, terminal behavior, and
keyboard layout.

<a id="learning-nano-save-exit"></a>

#### 💾 SAVE & EXIT

`Ctrl + O` → Start Nano's Write Out action.

Nano asks you to confirm the filename. Press `Enter` when the displayed
name is correct.

`Ctrl + X` → Exit Nano.

If there are unsaved changes, Nano can ask what you want to do.

`Ctrl + C` → Cancel the current action when applicable.

It does not universally mean "close Nano."

<a id="learning-fish"></a>

### 🐟 FISH

[🖥️ Sessions](#learning-fish-sessions) · [🔎 Command Lookup](#learning-fish-command-lookup) · [⚙️ Functions](#learning-fish-functions)

<a id="learning-fish-sessions"></a>

#### 🖥️ SESSIONS

`exit`

Ends the current Fish shell session.

If that shell is the only process keeping a terminal window open, the
terminal application may then close the window.

<a id="learning-fish-command-lookup"></a>

#### 🔎 IDENTIFYING A COMMAND WITH TYPE

In Fish, `type` explains what a name resolves to. It can show a function's
definition, a builtin, or an executable's path. It does not run the named command.

```fish
type -t string
type -a git
```

In an ordinary Fish session, the first prints `builtin`; the second lists
available definitions for `git`, often an executable path. Your functions and
`PATH` can change the result. `-t` shows the category; `-a` includes all matches.
A missing name returns failure.

After defining `hello` in [Functions](#learning-fish-functions), `type hello`
shows its definition and `type -t hello` prints `function`.

Fish implements **aliases as wrapper functions**, so they also report `function`.
An alias-generated definition can include its original alias description;
`type -t` alone does not distinguish aliases from other functions.

For a personal command such as `arsenal`, `type arsenal` helps check what it
would open without opening the manual or redefining/saving the function.

References: [Fish type](https://fishshell.com/docs/current/cmds/type.html),
[Fish alias](https://fishshell.com/docs/current/cmds/alias.html).

<a id="learning-fish-functions"></a>

#### ⚙️ FUNCTIONS

A Fish function lets you give a reusable sequence of shell commands a
name.

Example:

```fish
function hello
    echo "Hello"
end

hello
```

Expected output: `Hello`. Run this in Fish; newlines (or semicolons) separate commands.

##### 🧩 Visual Breakdown

```text
function hello
│        │
│        └── Function name
└─────────── Begin function definition
    echo "Hello"
    └── Command executed by the function
end
└── End function definition
```

Once the function exists in the current Fish session:

`funcsave hello`

saves that defined function so Fish can autoload it in future sessions.

`funcsave` does not invent the function for you. The function must
already be defined. It writes to your Fish configuration directory and can
replace a saved function of the same name; use a name you intend to keep.

<a id="learning-utilities"></a>

### 🧰 UTILITIES

[🧹 Indentation Cleanup](#learning-utilities-indentation-cleanup)

<a id="learning-utilities-indentation-cleanup"></a>

#### 🧹 INDENTATION CLEANUP

Suppose a file contains TAB characters. First inspect them:

```sh
grep -nP '\t' file.py
```

This finds tabs anywhere, not just indentation. `grep` returns 1 if none match;
that is not a reason to run a conversion blindly.

`expand -t 4` uses tab stops every four columns; it does not replace every tab
with exactly four spaces. `-i` limits conversion to leading whitespace, which
avoids changing tabs after nonblank text. Neither option understands your language:
leading tabs inside multiline strings are still data, and Make recipes can need tabs.

Preview without writing any file:

```sh
expand -i -t 4 -- file.py
```

To save a candidate, the following block is **Bash syntax**, not Fish. Run it in
Bash in a directory you control, using a regular input file. It refuses an
existing candidate destination via Bash's noclobber option:

```bash
(
    set -C
    expand -i -t 4 -- file.py > file.spaces.py
)
```

The subshell keeps `set -C` from changing the parent shell's options. The original
stays untouched. A failed conversion can leave a partial candidate: check the exit
status and review the output before using it. Noclobber is not a transactional
backup system or a defense against a hostile process changing your directory.

Review the changes:

```sh
diff -u -- file.py file.spaces.py
```

For `diff`, 0 means identical, 1 means differences, and values above 1 mean trouble.
Do not chain the review to a replacement with `&&`: a useful diff normally returns 1.
For Python, compile the candidate and run the project's actual tests as appropriate.
Compilation alone cannot prove that string contents or behavior were preserved.

Only after reviewing should you decide whether to apply the edit in your editor
or version-controlled working tree. Keep a separate verified backup if needed;
no automatic `mv` is included here. The candidate and any bytecode are disposable
artifacts, not files to publish accidentally.

So yes, command sequences can look like a satanic spell the first time you see them.
They're just several boring little commands wearing a trench coat. Inspect the pockets.

[Back to the map](#map)

<a id="references"></a>

## References and maintenance

Use the upstream documentation for complete behavior and version differences:

- [GNU Coreutils](https://www.gnu.org/software/coreutils/manual/coreutils.html): file operations, `expand`, `printf`.
- [GNU grep](https://www.gnu.org/software/grep/manual/grep.html): matching, PCRE support, exit status.
- [Bash manual](https://www.gnu.org/software/bash/manual/bash.html): redirections, pipelines and noclobber.
- [Python py_compile](https://docs.python.org/3/library/py_compile.html).
- [Git add](https://git-scm.com/docs/git-add), [gitignore](https://git-scm.com/docs/gitignore), [push](https://git-scm.com/docs/git-push).
- [GitHub CLI authentication](https://cli.github.com/manual/gh_auth_login).
- [GNU Nano manual](https://www.nano-editor.org/dist/latest/nano.html).
- [Fish language](https://fishshell.com/docs/current/language.html) and [funcsave](https://fishshell.com/docs/current/cmds/funcsave.html).
- [wl-clipboard](https://github.com/bugaevc/wl-clipboard).

For scope, review notes and how to improve an entry, see the [README](README.md)
and [contribution guide](CONTRIBUTING.md). This manual is a selected reference,
not a guarantee that every command works on every shell, version or platform.
