# Developer Arsenal

A practical developer encyclopedia and quick-reference manual for everyday development tools.

══════════════════════════════

This arsenal is divided into two:

⚡ QUICK MODE

Need to remember something?
Find it, grab the command, and keep working.

🎓 LEARNING MODE

Don't understand something?
See a real example, break it down, understand what happened, then return to Quick Mode.

══════════════════════════════

### 🗺️ MAP

```text
⚡ QUICK MODE
│
├── 💻 Terminal
│   ├── Navigation
│   ├── Files & Directories
│   ├── Search
│   ├── Clipboard
│   ├── Redirection & Pipes
│   ├── Options
│   └── Symbols & Sequences
│
├── 🐍 Python
│   ├── Running Programs
│   └── Syntax Checking
│
├── 🧬 Git & GitHub
│   ├── Repository
│   ├── Status
│   ├── Staging
│   ├── Commits
│   ├── Branches
│   ├── Identity
│   ├── .gitignore
│   ├── Remotes
│   ├── Push
│   └── GitHub CLI
│
├── ✏️ Nano
│   ├── Navigation
│   ├── Editing
│   └── Save & Exit
│
├── 🐟 Fish
│   ├── Sessions
│   └── Functions
│
└── 🧰 Utilities
    └── Indentation Cleanup
```

══════════════════════════════════════════════════════════
                      ⚡ QUICK MODE
══════════════════════════════════════════════════════════

━━━━━━━━━━━━━━━━━━━━━━ 💻 TERMINAL ━━━━━━━━━━━━━━━━━━━━━━

## 🧭 NAVIGATION

`pwd` → Show the current directory

`cd path` → Move to another directory

`cd ..` → Move to the parent directory

`ls` → List files and directories

────── o ──────

## 📄 FILES & DIRECTORIES

`cat file` → Display the entire contents of a file

`nano file` → Open or create a file for editing

`less file` → View a file without editing it

`mkdir directory` → Create a directory

`mkdir -p path/directory` → Create a directory path, including missing
parent directories

`cp source destination` → Copy a file

`mv source destination` → Move or rename a file

`rm file` → Delete a file

`rm -r directory` → Delete a directory and its contents recursively

`.bak` → Common suffix used to identify a backup copy

### 🔒 Backup

`cp source destination.bak` → Create a backup copy

────── o ──────

## 🔎 SEARCH

`grep pattern file` → Search for a pattern inside a file

`grep -n pattern file` → Show matching lines with line numbers

`grep -P '\t' file` → Search for TAB characters inside a file

────── o ──────

## 📋 CLIPBOARD

`wl-copy` → Copy data to the Wayland clipboard

`cat file | wl-copy` → Copy an entire file to the clipboard

`command | wl-copy` → Copy a command's standard output

`command 2>&1 | wl-copy` → Copy both standard output and errors

────── o ──────

## 🔀 REDIRECTION & PIPES

`command1 | command2` → Send the output of one command to another

`command > file` → Write command output to a file

`command1 && command2` → Run the second command only if the first
succeeds

`command 2>&1` → Merge error output with standard output

────── o ──────

## ⚙️ OPTIONS

`mkdir -p` → Create missing parent directories

`rm -r` → Remove directories recursively

`grep -n` → Show line numbers for matches

`grep -P` → Interpret the pattern as a Perl-compatible regular
expression

────── o ──────

## 🔣 SYMBOLS & SEQUENCES

`/` → Separate parts of a path

`~` → Home directory

`.` → Current directory

`..` → Parent directory

`|` → Pipe output into another command

`>` → Redirect output into a file

`&&` → Continue only if the previous command succeeds

`2>&1` → Merge standard error into standard output

`\t` → Represent a TAB character

`\` → Continue a command on the next line

━━━━━━━━━━━━━━━━━━━━━━━ 🐍 PYTHON ━━━━━━━━━━━━━━━━━━━━━━━

## ▶️ RUNNING PROGRAMS

`python script.py` → Run a Python program

`python script.py argument` → Run a Python program with a command-line
argument

────── o ──────

## 🔍 SYNTAX CHECKING

`python -m py_compile script.py` → Check Python syntax without running
the program

━━━━━━━━━━━━━━━━━━━━ 🧬 GIT & GITHUB ━━━━━━━━━━━━━━━━━━━━

## 📦 REPOSITORY

`git init` → Initialize a Git repository in the current directory

────── o ──────

## 🔎 STATUS

`git status` → Show the current state of the working tree and staging
area

────── o ──────

## 📥 STAGING

`git add file` → Add a file to the staging area

`git add .` → Add all current changes to the staging area

────── o ──────

## 💾 COMMITS

`git commit -m "message"` → Create a commit with a message

────── o ──────

## 🌿 BRANCHES

`git branch -m main` → Rename the current branch to `main`

────── o ──────

## 🪪 IDENTITY

`git config --global user.name "Your Name"` → Set your global Git author
name

`git config --global user.email "you@example.com"` → Set your global Git
author email

────── o ──────

## 🙈 .GITIGNORE

`.gitignore` → Define files and directories Git should ignore

`*.bak` → Ignore files ending in `.bak`

`directory/` → Ignore a directory

────── o ──────

## 🌎 REMOTES

`git remote add origin URL` → Add a remote repository named `origin`

`git remote -v` → Show configured remotes and their URLs

────── o ──────

## 🚀 PUSH

`git push -u origin main` → Push `main` to `origin` and set its upstream
branch

`git push` → Push commits to the configured upstream branch

────── o ──────

## 🐙 GITHUB CLI

`gh --version` → Show the installed GitHub CLI version

`gh auth login` → Authenticate GitHub CLI

━━━━━━━━━━━━━━━━━━━━━━━━ ✏️ NANO ━━━━━━━━━━━━━━━━━━━━━━━━

## 🧭 NAVIGATION

`Ctrl + W` → Search for text

`Alt + W` → Find the next occurrence

`Alt + G` → Go to a specific line and column

────── o ──────

## ✏️ EDITING

`Ctrl + K` → Cut the current line or selected text

`Ctrl + U` → Paste the last cut text

`Alt + A` → Start or end text selection

`Alt + U` → Undo

`Alt + E` → Redo

`Ctrl + \` → Search and replace

────── o ──────

## 💾 SAVE & EXIT

`Ctrl + O` → Write the current buffer to a file

`Enter` → Confirm the filename when saving

`Ctrl + X` → Exit Nano

`Ctrl + C` → Cancel the current action when applicable

━━━━━━━━━━━━━━━━━━━━━━━━ 🐟 FISH ━━━━━━━━━━━━━━━━━━━━━━━━

## 🖥️ SESSIONS

`exit` → Exit the current Fish shell session

────── o ──────

## ⚙️ FUNCTIONS

`function name` → Start defining a function

`end` → End the function definition

`funcsave name` → Save a defined function for future Fish sessions

━━━━━━━━━━━━━━━━━━━━━━ 🧰 UTILITIES ━━━━━━━━━━━━━━━━━━━━━

## 🧹 INDENTATION CLEANUP

`grep -nP '\t' file` → Find TAB characters and show their line numbers

`expand -t 4 file > file.tmp` → Convert TAB stops to spaces and write
the result to a temporary file

`mv file.tmp file` → Replace the original file with the converted file

### Safe sequence

cp file file.bak && expand -t 4 file > file.tmp && mv file.tmp file

→ Create a backup, convert TAB indentation, and replace the original
only if each previous step succeeds.

══════════════════════════════════════════════════════════
                   🏁 END OF QUICK MODE
══════════════════════════════════════════════════════════

### 🗺️ MAP

```text
🎓 LEARNING MODE
│
├── 🧠 Fundamentals
│   ├── Command Anatomy
│   │   ├── Commands
│   │   ├── Options
│   │   └── Arguments
│   ├── Shortcuts
│   └── Exit Codes
│
├── 💻 Terminal
│   ├── Navigation
│   ├── Files & Directories
│   ├── Search
│   ├── Clipboard
│   ├── Redirection & Pipes
│   └── Symbols & Sequences
│
├── 🐍 Python
│   ├── Running Your First Program
│   └── Checking Syntax
│
├── 🧬 Git & GitHub
│   ├── Git vs GitHub
│   ├── Mental Model
│   ├── Creating a Repository
│   ├── Checking Status
│   ├── Staging Changes
│   ├── Creating a Commit
│   ├── Branches
│   ├── Configuring Identity
│   ├── .gitignore
│   ├── Connecting GitHub
│   ├── Authentication
│   ├── First Push
│   └── Everyday Workflow
│
├── ✏️ Nano
│   ├── Navigation
│   ├── Editing
│   └── Save & Exit
│
├── 🐟 Fish
│   ├── Sessions
│   └── Functions
│
└── 🧰 Utilities
    └── Indentation Cleanup
```

══════════════════════════════════════════════════════════
                     🎓 LEARNING MODE
══════════════════════════════════════════════════════════

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

━━━━━━━━━━━━━━━━━━━━━ 🧠 FUNDAMENTALS ━━━━━━━━━━━━━━━━━━━━━

## 🧩 COMMAND ANATOMY

A common command-line pattern looks like this:

command -option argument

### 🧩 Visual Breakdown

```text
command -option argument
│       │       │
│       │       └── Argument → What the command receives or acts on
│       └────────── Option → Changes how the command behaves
└────────────────── Command → The program or instruction being executed
```

### Command

A command tells the system which program or instruction you want to
execute.

`pwd`

Here, `pwd` is the command. It prints the path of the current working
directory.

### Option

An option modifies how a command behaves.

`grep -n error file.txt`

### 🧩 Visual Breakdown

```text
grep -n error file.txt
│    │  │     │
│    │  │     └── File to search
│    │  └──────── Pattern to search for
│    └─────────── Option: show line numbers
└──────────────── Command

Options belong to the command that interprets them. The same option can
mean different things for different commands.
```

### Argument

An argument provides information to a command.

`cp source.txt backup.txt`

### 🧩 Visual Breakdown

```text
cp source.txt backup.txt
│  │          │
│  │          └── Destination argument
│  └───────────── Source argument
└──────────────── Command

Arguments can tell a command what to work with, what to search for,
where to operate, or other data it needs.
```

────── o ──────

## ⌨️ SHORTCUTS

A shortcut is a key combination interpreted by the program you are
currently using.

For example, inside Nano:

`Ctrl + O`

This starts Nano's Write Out action.

You did not type a shell command. You triggered an action inside Nano.

Shortcuts are context-dependent: the same key combination can behave
differently in different programs.

────── o ──────

## 🚦 EXIT CODES

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

`128` → Seen when Git terminates with a fatal error; the message
explains the actual cause

`130` → Common status after interruption with `Ctrl + C` / SIGINT

The number is a clue. The program's error message and context tell you
what actually happened.

So `[1]` is not automatically guilty.

Pedro can remain free... for now.

━━━━━━━━━━━━━━━━━━━━━━ 💻 TERMINAL ━━━━━━━━━━━━━━━━━━━━━━

## 🧭 NAVIGATION

### 📍 Find your current location

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

────── o ──────

### 👀 See what is here

`ls`

Lists files and directories in the current location. It only reads the
directory; it does not modify its contents.

────── o ──────

### 🚶 Move into a directory

`cd projects`

### 🧩 Visual Breakdown

```text
cd projects
│  │
│  └── Destination directory
└───── Command

`cd` changes the shell's current directory.
```

────── o ──────

### ⬆️ Move to the parent directory

`cd ..`

`..` represents the parent of the current directory: exactly one level
up.

## 📄 FILES & DIRECTORIES

### 👁️ Display a complete file

`cat script.py`

`cat` writes the file's contents to standard output. It does not edit
the file.

────── o ──────

### 📖 Read a file without editing it

`less README.md`

`less` opens a text viewer that lets you navigate through the file while
leaving it unchanged.

────── o ──────

### ✏️ Open or create a file for editing

`nano script.py`

Nano opens the file in a text editor. If the named file does not exist,
Nano can create it when you save.

────── o ──────

### 📁 Create a directory

`mkdir examples`

Creates a directory named `examples`.

────── o ──────

### 🏗️ Create a complete directory path

`mkdir -p project/examples`

### 🧩 Visual Breakdown

```text
mkdir -p project/examples
│     │  │
│     │  └── Path
│     └───── Option
└─────────── Command

With `-p`, `mkdir` can also create missing parent directories.
```

────── o ──────

### 📄 Copy a file

`cp source.txt backup.txt`

### 🧩 Visual Breakdown

```text
cp source.txt backup.txt
│  │          │
│  │          └── Destination
│  └───────────── Source
└──────────────── Command

The original remains in place and a copy is created at the destination.

Using a `.bak` suffix is a common convention for identifying a backup
copy:

`cp script.py script.py.bak`

`.bak` is only a naming convention. It has no magical backup behavior.
```

────── o ──────

### 🚚 Move or rename

`mv old.txt new.txt`

When source and destination are in the same directory, this effectively
renames the file.

────── o ──────

### 🗑️ Delete a file

`rm temporary.txt`

`rm` deletes directly. It does not automatically create a backup or move
the file to a recycle bin.

────── o ──────

### 🗑️ Delete a directory and its contents

`rm -r directory`

`-r` makes the operation recursive.

Be careful: this can remove an entire directory tree.

## 🔎 SEARCH

### 🔍 Search inside a file

`grep error script.py`

Searches `script.py` for lines matching `error`.

To include line numbers:

`grep -n error script.py`

To search for TAB characters using PCRE syntax:

`grep -nP '\t' script.py`

## 📋 CLIPBOARD

`wl-copy` copies data to the Wayland clipboard.

That makes it Wayland-specific rather than a universal shell command.

### Copy a complete file

`cat script.py | wl-copy`

### 🧩 Visual Breakdown

```text
cat script.py | wl-copy
│   │         │ │
│   │         │ └── Receives data and copies it
│   │         └──── Pipe
│   └────────────── File
└────────────────── Produces the file contents
```

### Copy normal output and errors

`command 2>&1 | wl-copy`

`2>&1` merges standard error into standard output before the pipe sends
the combined stream to `wl-copy`.

## 🔀 REDIRECTION & PIPES

### `|` --- Pipe

`command1 | command2`

The first command produces data. The pipe sends that data to the second
command.

### `>` --- Redirect output

`command > file`

Instead of displaying standard output normally, the shell writes it to
`file`.

Be aware that `>` replaces the destination file's existing contents.

### `&&` --- Continue only after success

`command1 && command2`

The second command runs only if the first returns a successful exit
status.

### `2>&1` --- Merge error output with standard output

File descriptor `1` is standard output and `2` is standard error.

`2>&1` tells the shell to send standard error to the same destination
currently used by standard output.

You do not need to memorize file descriptors on day one. The useful
mental model is:

`command 2>&1 | wl-copy`

→ Send normal output and errors through the pipe.

## 🔣 SYMBOLS & SEQUENCES

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

rm file1.csv \
    file2.csv \
    file3.csv

The shell treats this as one command.

Visually it spans several lines. Logically it is:

`rm file1.csv file2.csv file3.csv`

━━━━━━━━━━━━━━━━━━━━━━━ 🐍 PYTHON ━━━━━━━━━━━━━━━━━━━━━━━

## ▶️ RUNNING YOUR FIRST PROGRAM

Suppose `hello.py` contains:

`print("Hello")`

Run it with:

`python hello.py`

The terminal prints:

`Hello`

### 🧩 Visual Breakdown

```text
python hello.py
│      │
│      └── Python file to run
└───────── Python interpreter command

A Python program can also receive command-line arguments:

`python script.py input.csv`

Inside Python, tools such as `sys.argv` can access those arguments.
```

## 🔍 CHECKING SYNTAX

`python -m py_compile script.py`

### 🧩 Visual Breakdown

```text
python -m py_compile script.py
│      │  │          │
│      │  │          └── File to compile
│      │  └───────────── Module
│      └──────────────── Run a module
└─────────────────────── Python command

If the syntax is valid, this normally produces no terminal output.

If Python encounters a syntax problem, it reports the error.

This checks whether Python can compile the file; it does not run the
script's normal application flow.
```

━━━━━━━━━━━━━━━━━━━━ 🧬 GIT & GITHUB ━━━━━━━━━━━━━━━━━━━━

## 🌎 GIT VS GITHUB

Git is the version-control system running on your machine.

It tracks changes and creates a history of your project.

GitHub is an online service that can host Git repositories and make
them available remotely.

You can use Git without GitHub.

GitHub uses Git repositories, but Git and GitHub are not the same thing.

────── o ──────

## 🧠 MENTAL MODEL

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
             │ remote repository
             └─────────────────┘
```

The working tree is what you are currently editing.

The staging area contains changes selected for the next commit.

A commit records a snapshot in the local repository's history.

A remote is another repository your local repository can communicate
with.

────── o ──────

## 📦 CREATING A REPOSITORY

Inside a project directory:

`git init`

Git creates a hidden `.git/` directory containing repository metadata
and history.

Do not treat `.git/` as ordinary project content to casually edit.

────── o ──────

## 🔎 CHECKING STATUS

`git status`

This tells you what Git currently sees: untracked files, modified files,
staged changes, and whether the working tree is clean.

A clean working tree means Git sees no changes waiting to be committed.

────── o ──────

## 📥 STAGING CHANGES

Stage one file:

`git add README.md`

Stage the current set of changes in the current directory scope:

`git add .`

Staging does not publish anything and does not create a commit.

It selects changes for the next commit.

────── o ──────

## 💾 CREATING A COMMIT

`git commit -m "Initial release"`

### 🧩 Visual Breakdown

```text
git commit -m "Initial release"
│   │      │  │
│   │      │  └── Commit message
│   │      └───── Message option
│   └──────────── Subcommand
└──────────────── Git executable

A commit records the staged changes in local Git history.

The first commit in a repository is commonly called the root commit.

Git identifies commits with hashes; interfaces often show a shortened
form of the full ID.
```

────── o ──────

## 🌿 BRANCHES

A branch is a movable name pointing into a line of development.

To rename the current branch to `main`:

`git branch -m main`

For a new simple project, `main` can serve as the primary branch.

────── o ──────

## 🪪 CONFIGURING IDENTITY

Git needs an author name and email before it can create commits.

Set them globally:

`git config --global user.name "Your Name"`

`git config --global user.email "you@example.com"`

`--global` applies the setting to your user-level Git configuration
rather than only the current repository.

The configured email can appear in commit metadata. Use an address you
are comfortable associating with your commits, or use an appropriate
privacy-preserving address provided by your hosting service.

### A useful failure

A real first workflow can look like this:

git init ↓ git add . ↓ git commit ↓ \[128\] 💀 Git reports a fatal
problem: author identity is unknown ↓ configure user.name and user.email
↓ git commit ↓ SUCCESS

The failed commit does not automatically erase the staging area.
After fixing the identity problem, the staged changes can still be
committed.

`128` alone does not mean "missing identity." It is a status Git can use
for fatal failures; the accompanying message tells you the actual cause.

────── o ──────

## 🙈 .GITIGNORE

A `.gitignore` file contains patterns for files and directories Git
should leave untracked.

Example:

*.bak
__pycache__/
*.pyc

`*.bak` → Match names ending in `.bak`.

`__pycache__/` → Ignore that directory.

`*.pyc` → Ignore Python bytecode files.

`.gitignore` is useful for generated files, local artifacts, backups,
caches, and other content that does not belong in repository history.

────── o ──────

## 🌎 CONNECTING GITHUB

A local repository can be connected to a remote repository:

`git remote add origin URL`

### 🧩 Visual Breakdown

```text
git remote add origin URL
│   │      │   │      │
│   │      │   │      └── Remote repository URL
│   │      │   └───────── Conventional remote name
│   │      └───────────── Action
│   └──────────────────── Remote subcommand
└──────────────────────── Git executable

`origin` is a conventional name. It is not a special GitHub account or
server.

Check configured remotes with:

`git remote -v`

You may see separate fetch and push entries for the same remote.
```

────── o ──────

## 🔐 AUTHENTICATION

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

────── o ──────

## 🚀 FIRST PUSH

`git push -u origin main`

### 🧩 Visual Breakdown

```text
git push -u origin main
│   │    │  │      │
│   │    │  │      └── Local branch to push
│   │    │  └───────── Remote name
│   │    └──────────── Set upstream
│   └───────────────── Subcommand
└───────────────────── Git executable

This sends commits from local `main` to `origin` and configures an
upstream relationship.

After that, the usual push can often be shortened to:

`git push`
```

────── o ──────

## 🔁 EVERYDAY WORKFLOW

Once the repository is configured, a simple workflow is:

Edit files
    ↓
git status
    ↓
git add .
    ↓
git commit -m "Describe the change"
    ↓
git push

The mental model is:

Edit → Inspect → Stage → Commit → Push

Do not memorize the commands as a magic incantation. Know which boundary
each command crosses.

`git add` → Working tree to staging area.

`git commit` → Staging area to local history.

`git push` → Local history to the remote repository.

━━━━━━━━━━━━━━━━━━━━━━━━ ✏️ NANO ━━━━━━━━━━━━━━━━━━━━━━━━

## 🧭 NAVIGATION

### 🔍 Search for text

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

## ✏️ EDITING

`Alt + A` → Start or end text selection.

`Ctrl + K` → Cut the current line or selected text, depending on
context.

`Ctrl + U` → Insert the last cut/copied text.

`Alt + U` → Undo.

`Alt + E` → Redo.

`Ctrl + \` → Start search and replace.

Shortcut availability can depend on Nano version, terminal behavior, and
keyboard layout.

## 💾 SAVE & EXIT

`Ctrl + O` → Start Nano's Write Out action.

Nano asks you to confirm the filename. Press `Enter` when the displayed
name is correct.

`Ctrl + X` → Exit Nano.

If there are unsaved changes, Nano can ask what you want to do.

`Ctrl + C` → Cancel the current action when applicable.

It does not universally mean "close Nano."

━━━━━━━━━━━━━━━━━━━━━━━━ 🐟 FISH ━━━━━━━━━━━━━━━━━━━━━━━━

## 🖥️ SESSIONS

`exit`

Ends the current Fish shell session.

If that shell is the only process keeping a terminal window open, the
terminal application may then close the window.

## ⚙️ FUNCTIONS

A Fish function lets you give a reusable sequence of shell commands a
name.

Example:

function hello echo "Hello" end

### 🧩 Visual Breakdown

```text
function hello
│        │
│        └── Function name
└─────────── Begin function definition

    echo "Hello"
    └── Command executed by the function

end
└── End function definition

Once the function exists in the current Fish session:

`funcsave hello`

saves that defined function so Fish can autoload it in future sessions.

`funcsave` does not invent the function for you. The function must
already be defined.
```

━━━━━━━━━━━━━━━━━━━━━━ 🧰 UTILITIES ━━━━━━━━━━━━━━━━━━━━━

## 🧹 INDENTATION CLEANUP

Suppose a source file contains TAB characters and you want to normalize
them using tab stops of width 4.

First, inspect the file:

`grep -nP '\t' file.py`

If matches appear, their line numbers help you see where TAB characters
exist.

Then create a backup:

`cp file.py file.py.bak`

Now generate transformed content:

`expand -t 4 file.py > file.tmp`

`expand -t 4` expands TAB characters according to tab stops every four
columns.

It does not mean that every TAB is blindly replaced by exactly four
spaces.

Finally:

`mv file.tmp file.py`

replaces the original path with the transformed temporary file.

### 🧩 Visual Breakdown

```text
cp file.py file.py.bak &&
expand -t 4 file.py > file.tmp &&
mv file.tmp file.py

First, `cp` creates the backup.

Then `expand` generates the transformed content.

`>` writes that output to a temporary file.

If that succeeds, `&&` allows the next command to run.

Finally, `mv` replaces the original path with the temporary file.

So yes, the sequence looks like a satanic spell the first time you see
it.

It isn't.

It's just several boring little commands wearing a trench coat.

Before running destructive or replacement operations on important files,
verify your paths and keep a backup you know how to restore.
```

══════════════════════════════════════════════════════════
                  🏁 END OF LEARNING MODE
══════════════════════════════════════════════════════════
