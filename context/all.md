## Description
Note content from https://notes.thorg.app in Markdown format with note content wrapped in XML tags.

Note links are in the format of wiki links `[[<note_name>]]`
Transcluded note links are in the format of `![[<transcluded_note_name>]]`

Each note content will start with XML tag <note name="<note_name>" title="<note_title>"> and end with </note>

Notes are hierarchical by name using '.' as separator.
Example [[grandparent.parent.child]] is a child of [[grandparent.parent]] which is a child of [[grandparent]].

### Notes
<note name="root" title="Thorg Notes Landing Page">
	
	![[t]]
</note>
<note name="t" title="Thorg (Thought Organizer)">
	
	Welcome to **Thorg** (Thought Organizer)!
	
	We are in the **early stages** of the product (even though it took quite a bit of development effort to get here).
	But even at this early stage, if you are a current [Dendron](https://www.dendron.so/) user, we believe there is value in giving Thorg a try. We are working to fill the gaps to make Thorg fully standalone, and to implement more exciting features around the three pillars that **Thorg** focuses on:
	- Search
	- Visualization
	- Refactoring
	
	The following commands (and more) are available to try out now:
	
	![[t.ext._.highlighted-commands]]
	
	## How to install Thorg
	![[t.ext.how-to.install-thorg]]
	
	## How to reach out
	![[t.ext.contact-us]]
	
	## Our view on Data
	![[t.ext.data.thorg-view-on-data]]
</note>
<note name="t.ext" title="Thorg External Hierarchy">
	
	Hierarchy for external documentation.
	
	Check out the children of this note, as well as the top-level ancestor of this note: [[t]].
</note>
<note name="t.ext._.data_type_anchorPoint.frontMatterFormat" title="Anchor Point frontMatterFormat">
	
	#not-ready-yet.in-queue-to-start: Anchor point is an upcoming feature to make it easy to navigate to exact places in a codebase from notes.
</note>
<note name="t.ext._.highlighted-commands" title="Thorg Highlighted Commands">
	
	### Commands
	
	#### Search Without Hierarchy Filtering
	- [[t.ext.command.search.quick.all]] - [[Search|t.ext.command.search._.search-definition]] across all notes through quick pick interface (including searching [[note content|t.ext.data.type.note.content]]).
	  - **[[t.ext.command.search.quick.visited-since]]** - Search filtered to notes that have been [[visited|t.ext.data.type.note.visited]] since a specified time.
	  - [[t.ext.command.search.quick.updated-since]] - Search filtered to notes that have been updated since a specified time.
	
	#### Search With Hierarchy Filtering
	- [[t.ext.command.search.quick.in-subtree.all]] - Similar to quick search all, but **filtered** to only the notes that are [[descendants|t.ext.data.type.note.descendants]] of the currently focused note.
	  - **[[t.ext.command.search.quick.in-subtree.visited-since]]** - Search with subtree filter, limited to notes that have been visited since a specified time.
	  - [[t.ext.command.search.quick.in-subtree.updated-since]] - Search with subtree filter, limited to notes that have been updated since a specified time.
	
	### Next: Setup Shortcuts
	Once you have checked out the highlighted commands, look at [[t.ext._.setup-of-shortcuts]] to set up your shortcut schema in an ergonomic and quickly accessible way.
</note>
<note name="t.ext._.review-script-prior-to-running-them" title="Remember to Review Scripts from Internet Prior to Running Them">
	
	Remember to review scripts from internet prior to running them! 
	
	Whenever you encounter someone on the internet asking you to run a script like
	
	```bash
	curl -fsSL https://some-script.sh | bash 
	```
	
	Make sure to look at that script by going to `https://some-script.sh` in your browser and, prior to running the script (`| bash` portion is what runs the script). If you aren't a pro of the language that the script is written in, then at least ask GPT/Claude/LLM-of-your-choice to review the script for whether it is safe to run and is free of doing anything malicious. By asking LLM a question as *"Is this script safe to run from security perspective?"*
	
</note>
<note name="t.ext._.setup-of-shortcuts" title="Setup of Thorg Shortcuts">
	
	As of the Alpha release, Thorg comes **ready** for keyboard shortcuts but does NOT have pre-configured shortcuts. We assume our users' keyboards are already heavily loaded with shortcuts. Therefore, we propose adjusting existing shortcuts to use two-chord combinations, making room for an array of hot-keyed commands.
	
	For now, we provide shortcut recommendations but leave the actual setup in your hands. If we receive feedback that you agree with our recommended approach, we will automate this shortcut setup.
	
	Below we offer recommendations for a shortcut schema, with snippets you can add to your [[keybindings.json|t.ext.vscode.how-to.change-your-keybindings-json]].
	
	Also, regarding `keybindings.json`, we recommend you [[t.ext.tip.vscode.source-control.your-keybindings]].
	
	## Approach: Ergonomic Two-Key Shortcuts That Are Easy to Remember
	
	The suggested approach for creating shortcuts is to use multi-chord shortcuts that are **both**:
	- Ergonomically accessible
	- Easy to remember
	
	Before we get into the suggested shortcuts, let's make a small keyboard adjustment that makes a world of difference for hand ergonomics: 
	
	<details class="bordered">
	<summary>Get rid of CAPS LOCK to allow CTRL its rightful place on the home row</summary>
	
	![[t.ext.tip.keyboard.get-rid-of-caps-lock]]
	</details>
	
	
	Now that CTRL lives on the home row and we can use `CTRL+<SomeKey>` shortcuts with ease, let's start with our first multi-chord entry point: `CTRL+t`
	
	![[t.ext._.setup-of-shortcuts.ctrl-t-setup]]
	
	![[t.ext._.setup-of-shortcuts.ctrl-y-setup]]
	
	<details class="bordered">
	<summary>Quick search with updated-since, shortcut setup</summary>
	
	![[t.ext._.setup-of-shortcuts.updated-since-setup]]
	</details>
	
	
	
	
</note>
<note name="t.ext._.setup-of-shortcuts.ctrl-t-setup" title="Thorg Ctrl+T Shortcut Setup - For Quick Search">
	
	
	<details class="bordered">
	<summary>But CTRL+t is taken for ShowAllSymbols! - Yes, let's free CTRL+t first</summary>
	
	![[t.ext._.setup-of-shortcuts.ctrl-t-setup.free-ctrl-t]]
	</details>
	
	Now that we've freed CTRL+t from being tied to a single command, we can use it as an entry point for multiple commands.
	
	<details class="bordered">
	<summary>Use CTRL+t as entry point for Thorg commands</summary>
	
	
	![[t.ext._.setup-of-shortcuts.ctrl-t-setup.add-shortcuts]]
	</details>
</note>
<note name="t.ext._.setup-of-shortcuts.ctrl-t-setup.add-shortcuts" title="Add Ctrl+T Thorg Shortcuts">
	
	`CTRL+t` is used as the entry point for primary Thorg commands. Think of `CTRL+t` as meaning `Thorg` for most commands you assign under it.
	
	### Pre-Req
	- [[CTRL+t has been freed|t.ext._.setup-of-shortcuts.ctrl-t-setup.free-ctrl-t]]
	
	### Add CTRL+t Thorg Shortcuts
	Add the following to your [[keybindings.json|t.ext.vscode.how-to.change-your-keybindings-json]]:
	
	
	```json
	  {
	    "key": "ctrl+t ctrl+t",
	    "command": "thorg.search.quick.all"
	  },
	  {
	    "key": "ctrl+t ctrl+h",
	    "command": "thorg.search.quick.visited-since.2-hours-ago"
	  },
	  {
	    "key": "ctrl+t ctrl+d",
	    "command": "thorg.search.quick.visited-since.today"
	  },
	  {
	    "key": "ctrl+t ctrl+y",
	    "command": "thorg.search.quick.visited-since.yesterday"
	  },
	  {
	    "key": "ctrl+t ctrl+w",
	    "command": "thorg.search.quick.visited-since.1-week-ago"
	  },
	  {
	    "key": "ctrl+t ctrl+m",
	    "command": "thorg.search.quick.visited-since.1-month-ago"
	  },
	  {
	    "key": "ctrl+t ctrl+e",
	    "command": "thorg.search.quick.visited-since.1-year-ago"
	  },
	```
	
	### Description of Additions
	The following are descriptions of the shortcuts added to [[keybindings.json|t.ext.vscode.how-to.change-your-keybindings-json]] above:
	
	- `CTRL+t` + `CTRL+t`:
	  - Assigned to [[thorg.search.quick.all|t.ext.command.search.quick.all]] for quick [[search|t.ext.command.search._.search-definition]] across all notes.
	  - To remember: Thorg, Thorg Main Command.
	
	- `CTRL+t` + `CTRL+h`:
	  - Assigned to [[thorg.search.quick.visited-since.2-hours-ago|t.ext.command.search.quick.visited-since]].
	    - Through practice, limiting this shortcut to one hour has proven too restrictive, while 4 hours is too permissive. Logically, this shortcut could also be set to:
	      - [[thorg.search.quick.visited-since.1-hour-ago|t.ext.command.search.quick.visited-since]]
	      - [[thorg.search.quick.visited-since.4-hours-ago|t.ext.command.search.quick.visited-since]]
	  - To remember: Thorg, Hour.
	
	- `CTRL+t` + `CTRL+d`:
	  - Assigned to [[thorg.search.quick.visited-since.today|t.ext.command.search.quick.visited-since]]
	  - To remember: Thorg, Day.
	
	- `CTRL+t` + `CTRL+y`:
	  - Assigned to [[thorg.search.quick.visited-since.yesterday|t.ext.command.search.quick.visited-since]]
	  - To remember: Thorg, Yesterday.
	
	- `CTRL+t` + `CTRL+w`:
	  - Assigned to [[thorg.search.quick.visited-since.1-week-ago|t.ext.command.search.quick.visited-since]]
	  - To remember: Thorg, Week.
	
	- `CTRL+t` + `CTRL+m`:
	  - Assigned to [[thorg.search.quick.visited-since.1-month-ago|t.ext.command.search.quick.visited-since]]
	  - To remember: Thorg, Month.
	
	- `CTRL+t` + `CTRL+e`:
	  - Assigned to [[thorg.search.quick.visited-since.1-year-ago|t.ext.command.search.quick.visited-since]]
	  - To remember: Thorg, (Second letter of y)Ear (we aren't using `y` since it's used for yesterday)
	
	
	### Q&A:
	<details class="bordered-when-open">
	<summary>Why use visited-since and not updated-since for primary shortcuts?</summary>
	
	![[t.ext._.setup-of-shortcuts.ctrl-t-setup.add-shortcuts.why-favor-visited-since]]
	</details>
	
</note>
<note name="t.ext._.setup-of-shortcuts.ctrl-t-setup.add-shortcuts.why-favor-visited-since" title="Why use visited-since and not updated-since for primary shortcuts">
	
	#### Why Use Visited-Since and Not Updated-Since as Primary Shortcuts?
	
	##### Visited Encompasses Modified for Most Cases
	We choose [[visited-since commands|t.ext.command.search.quick.visited-since]] over [[updated-since|t.ext.command.search.quick.updated-since]] because if you perform modifications on a note, you'll likely stay in that note longer than your configured [[t.ext.feature.visit-history.visit-event.min-visitation-threshold]]. Therefore, your visit will be recorded as a [[t.ext.feature.visit-history.visit-event]] for the modified note and will be picked up by [[visited-since commands|t.ext.command.search.quick.visited-since]].
	
	##### Updated-Since Does Not Encompass Visited Notes
	You could visit and stay at a note for a prolonged period **without** making modifications or updates. In such cases, the note will be fresh in your memory and likely related to the area you're currently working on. A note that has been read has a higher chance of being re-visited, and it's picked up by [[visited-since|t.ext.command.search.quick.visited-since]] commands. However, such a note that has been read but not modified is out of reach of [[updated-since|t.ext.command.search.quick.updated-since]] commands.
	
	
	#### Also see
	- [[t.ext._.setup-of-shortcuts.ctrl-t-setup.add-shortcuts.why-favor-visited-since.when-updated-since-can-be-better]]
</note>
<note name="t.ext._.setup-of-shortcuts.ctrl-t-setup.add-shortcuts.why-favor-visited-since.when-updated-since-can-be-better" title="When Updated since Can Be Better Than Visited-Since">
	
	While for most use cases we expect visited-since commands to be the preferred time-based search filter ([[see why|t.ext._.setup-of-shortcuts.ctrl-t-setup.add-shortcuts.why-favor-visited-since]]), there are times when updated-since commands such as:
	- [[t.ext.command.search.quick.updated-since]]
	- [[t.ext.command.search.quick.in-subtree.updated-since]]
	
	can be better suited for your search needs. The main use case is when you're **sharing** a [[vault|t.ext.data.type.vault]] with other people and want to search according to updates that others have made. In such cases, **you** haven't visited the notes they modified, so your [[t.ext.feature.visit-history]] won't reflect their visits. However, note modifications are always shared. Therefore, updated-since commands are more useful for discovering **others'** interactions with the notes.
	
	If you're NOT sharing the vault or simply want to focus on your own note interactions, then visited-since commands such as:
	- [[t.ext.command.search.quick.visited-since]]
	- [[t.ext.command.search.quick.in-subtree.visited-since]]
	
	will be more useful to you.
</note>
<note name="t.ext._.setup-of-shortcuts.ctrl-t-setup.free-ctrl-t" title="Free Ctrl+T">
	
	Out of the box, VSCode assigns `CTRL+t` to `workbench.action.showAllSymbols`. You'll need to free and remap this so you can use `CTRL+t` as an entry point for **many** commands rather than just a single command.
	
	#### Step 1: Free "ctrl+t" from Being Tied to a Single Command
	- [[Open command palette|t.ext.vscode.how-to.open-command-palette]]
	- Type `Preferences: Open keyboard shortcuts (JSON)`
	
	Add the following to the file:
	```json
	  {
	    "key": "ctrl+t",
	    "command": "-workbench.action.showAllSymbols"
	  },
	  {
	    "key": "ctrl+t",
	    "command": "-editor.action.transposeLetters",
	    "when": "textInputFocus && !editorReadonly"
	  }
	```
	
	#### Step 2: Assign New Shortcut for `workbench.action.showAllSymbols`
	The recommended shortcut for `workbench.action.showAllSymbols` is `CTRL+t` + `T` (the second time you press T is without CTRL).
	
	To set this up, add the following to your `keyboard shortcuts (JSON)` file (`keybindings.json`):
	
	```json
	  {
	    "key": "ctrl+t t",
	    "command": "workbench.action.showAllSymbols"
	  },
	```
	
	This setup will leave `CTRL+t` + `CTRL+t` available for [[t.ext.command.search.quick.all]]. 
</note>
<note name="t.ext._.setup-of-shortcuts.ctrl-y-setup" title="Ctrl+Y Shortcut Setup - For In-Subtree Searches">
	
	<details class="bordered">
	<summary>Free CTRL+y</summary>
	
	![[t.ext._.setup-of-shortcuts.ctrl-y-setup.free-ctrl-y]]
	</details>
	
	
	<details class="bordered">
	<summary>Add Thorg CTRL+y shortcuts</summary>
	
	![[t.ext._.setup-of-shortcuts.ctrl-y-setup.add-ctrl-h-shortcuts]]
	</details>
	
</note>
<note name="t.ext._.setup-of-shortcuts.ctrl-y-setup.add-ctrl-h-shortcuts" title="CTRL+y Thorg Subtree Search Shortcuts">
	
	
	`CTRL+y` is used as the entry point for Thorg in-subtree search commands. To remember this, think of the `Y` character representing the branching of a tree.
	
	### Pre-Req
	- [[t.ext._.setup-of-shortcuts.ctrl-y-setup.free-ctrl-y]]
	
	### Shortcuts Overview
	
	Add the following to your [[keybindings.json|t.ext.vscode.how-to.change-your-keybindings-json]]:
	
	```json
	  {
	    "key": "ctrl+y ctrl+t",
	    "command": "thorg.search.quick.in-subtree.all"
	  },
	  {
	    "key": "ctrl+y ctrl+h",
	    "command": "thorg.search.quick.in-subtree.visited-since.2-hours-ago"
	  },
	  {
	    "key": "ctrl+y ctrl+d",
	    "command": "thorg.search.quick.in-subtree.visited-since.today"
	  },
	  {
	    "key": "ctrl+y ctrl+y",
	    "command": "thorg.search.quick.in-subtree.visited-since.yesterday"
	  },
	  {
	    "key": "ctrl+y ctrl+w",
	    "command": "thorg.search.quick.in-subtree.visited-since.1-week-ago"
	  },
	  {
	    "key": "ctrl+y ctrl+m",
	    "command": "thorg.search.quick.in-subtree.visited-since.1-month-ago"
	  },
	  {
	    "key": "ctrl+y ctrl+e",
	    "command": "thorg.search.quick.in-subtree.visited-since.1-year-ago"
	  },
	```
	
	### Description of Shortcuts
	
	- `CTRL+y` + `CTRL+t`:
	  - Assigned to `thorg.search.quick.in-subtree.all` for quick search across all notes in the current hierarchy.
	  - To remember: Subtree, Thorg (All).
	
	- `CTRL+y` + `CTRL+h`:
	  - Assigned to `thorg.search.quick.in-subtree.visited-since.2-hours-ago`
	  - Searches within subtree for notes visited in the last 2 hours.
	  - To remember: Subtree, Hour.
	
	- `CTRL+y` + `CTRL+d`:
	  - Assigned to `thorg.search.quick.in-subtree.visited-since.today`
	  - Searches within subtree for notes visited today.
	  - To remember: Subtree, Day.
	
	- `CTRL+y` + `CTRL+y`:
	  - Assigned to `thorg.search.quick.in-subtree.visited-since.yesterday`
	  - Searches within subtree for notes visited since yesterday.
	  - To remember: Subtree, Yesterday.
	
	- `CTRL+y` + `CTRL+w`:
	  - Assigned to `thorg.search.quick.in-subtree.visited-since.1-week-ago`
	  - Searches within subtree for notes visited in the last week.
	  - To remember: Subtree, Week.
	
	- `CTRL+y` + `CTRL+m`:
	  - Assigned to `thorg.search.quick.in-subtree.visited-since.1-month-ago`
	  - Searches within subtree for notes visited in the last month.
	  - To remember: Subtree, Month.
	
	- `CTRL+y` + `CTRL+e`:
	  - Assigned to `thorg.search.quick.in-subtree.visited-since.1-year-ago`
	  - Searches within subtree for notes visited in the last year.
	  - To remember: Subtree, (Second letter of y)Ear (we used `y` for yesterday).
	
	## Notes
	- These shortcuts mirror the [[ctrl+t|t.ext._.setup-of-shortcuts.ctrl-t-setup.add-shortcuts]] shortcut pattern but scope searches to the current note's [[hierarchy|t.ext.data.type.note.hierarchy]].
</note>
<note name="t.ext._.setup-of-shortcuts.ctrl-y-setup.free-ctrl-y" title="Free Ctrl+Y">
	
	Out of the box, VSCode assigns `CTRL+y` to `redo`. You'll need to free and remap this so you can use `CTRL+y` as an entry point for **many** commands rather than just a single command.
	
	#### Step 1: Free "ctrl+y" from Being Tied to a Single Command
	- [[Open command palette|t.ext.vscode.how-to.open-command-palette]]
	- Type `Preferences: Open keyboard shortcuts (JSON)`
	
	Add the following to the file:
	```json
	  {
	    "key": "ctrl+y",
	    "command": "-chatEditor.action.acceptHunk",
	    "when": "chatEdits.hasEditorModifications && editorFocus && !chatEdits.isRequestInProgress || chatEdits.hasEditorModifications && notebookCellListFocused && !chatEdits.isRequestInProgress"
	  },
	  {
	    "key": "ctrl+y",
	    "command": "-redo"
	  }
	```
	
	#### Step 2: Assign New Shortcut for `redo`
	The recommended shortcut for `redo` is `CTRL+y` + `Y` (the second time you press Y is without CTRL).
	
	To set this up, add the following to your `keyboard shortcuts (JSON)` file (`keybindings.json`):
	
	```json
	  {
	    "key": "ctrl+y y",
	    "command": "redo"
	  }
	```
	
	This setup will leave `CTRL+y` available as an entry point for multiple commands.
	
</note>
<note name="t.ext._.setup-of-shortcuts.updated-since-setup" title="Updated-Since Command Shortcut Setup">
	
	
	
	![[t.ext._.setup-of-shortcuts.ctrl-t-setup.add-shortcuts.why-favor-visited-since.when-updated-since-can-be-better]]
	
	If you have a workflow that depends on updated-since, set up shortcuts for the following commands: [[thorg.search.quick.updated-since.XXX|t.ext.command.search.quick.updated-since]] and [[thorg.search.quick.in-subtree.updated-since.XXX|t.ext.command.search.quick.in-subtree.updated-since]]. Pick an entry key and follow a pattern similar to the [[t.ext._.setup-of-shortcuts.ctrl-t-setup]] setup.
	
</note>
<note name="t.ext.as-context-for-llm" title="Thorg Documentation As Context for LLM">
	
	This **[single file](https://raw.githubusercontent.com/Thorg-App/thorg-public-notes-context-for-llm/refs/heads/main/context/all.md)** from [this](https://github.com/Thorg-App/thorg-public-notes-context-for-llm) git repo contains all notes from [notes.thorg.app](https://notes.thorg.app), ready to add as LLM context.
	
	#### Individual files
	<details class="bordered-when-open">
	<summary>Individual files in public repo</summary>
	
	![[t.ext.as-context-for-llm.public-repo]]
	</details>
	
</note>
<note name="t.ext.as-context-for-llm.public-repo" title="Public Repo (with notes.thorg.app content)">
	
	<div class="centered xxlarge">
	
	**[thorg-public-notes](https://github.com/Thorg-App/thorg-public-notes)**
	</div>
	
	**thorg-public-notes**: Repository that contains [[vault|t.ext.data.type.vault]] that is published to https://notes.thorg.app
	Gives you externally facing Thorg markdown documentation in markdown format.
	
	Also note if you want to load in entire context of Thorg externally facing documentation than look at [[t.ext.as-context-for-llm]].
	
</note>
<note name="t.ext.command" title="Thorg Command">
	
	This hierarchy contains all VSCode commands that Thorg exposes.
	
	See child notes for details.
</note>
<note name="t.ext.command.externalFile" title="externalFile">
	
	Commands in this hierarchy work on files that are external to your note workspace.
	
	
	
</note>
<note name="t.ext.command.logs" title="thorg.logs - Commands">
	
	Commands for interacting with Thorg logs.
	
	
</note>
<note name="t.ext.command.logs.capture" title="thorg.logs.capture - Commands">
	
	Commands for capturing thorg logs.
</note>
<note name="t.ext.command.logs.capture.combined" title="thorg.logs.capture.combined - Commands">
	
	Commands for capturing combined Thorg logs (combining logs from multiple log files).
</note>
<note name="t.ext.command.logs.capture.combined.recent" title="thorg.logs.capture.combined.recent - Command To capture Recent logs">
	
	Command to capture recent Thorg logs by combining multiple log files into a single file based on a date range.
	
	**Use case:** Instead of [[getting Thorg logs manually|t.ext.contact-us.submit-git-hub-issue.how-to.submit-logs.how-to-get-logs.manually]], use this command to simplify log gathering. 
	
	This command prompts you for a time range and gathers logs from multiple files (pre-init, client, and server) based on your specified range.
	
	**Note:** If your issue is reproducible, we recommend enabling `DEBUG` level logging in [[t.ext.configuration.values.advancedConfig.logLevel]].
	
	### How to use
	1. [[Open the command palette|t.ext.vscode.how-to.open-command-palette]]
	2. Type **Capture combined logs** and select **Thorg/Logs: Capture Combined Logs (Recent)**
	3. Choose the date range from the quick pick menu
	   1. Example if the issue happened at activation time you only need to gather the logs since activation (first option).
	4. Wait for the log gathering report showing the combined log file location
	
</note>
<note name="t.ext.command.noteEditor.multiple.git.closeAllUnmodifiedEditors" title="thorg.noteEditor.multiple.git.closeAllUnmodifiedEditors">
	
	
	This command is similar to VSCode's built-in `git.closeAllUnmodifiedEditors` (which closes editors that have all their changes committed to git).
	
	**Key difference:** This command does **NOT** close `Thorg` panels, whereas `git.closeAllUnmodifiedEditors` has the side effect of closing `Thorg` panels as well.
	
	
</note>
<note name="t.ext.command.noteEditor.single.select.markdown.all" title="thorg.noteEditor.single.select.markdown.all">
	
	Selects all markdown content of the currently open note **without the [[t.ext.data.type.note.frontmatter]]**.
	
	
	
</note>
<note name="t.ext.command.search" title="Search">
	
	![[t.ext.command.search._.search-definition]]
	
	### Quick search:
	![[t.ext.command.search.quick]]
</note>
<note name="t.ext.command.search._.search-definition" title="Search Definition">
	
	### Definition
	When we say **"Search"** in Thorg, we mean searching the [[note content|t.ext.data.type.note.content]] along with key metadata including [[note title|t.ext.data.type.note.data.title]] and [[note name|t.ext.data.type.note.name]].
	
	### Tips
	![[t.ext.command.search._.tips]]
</note>
<note name="t.ext.command.search._.tips" title="Search Tips">
	
	- When you enter search terms without quotation marks, their placement in the note is irrelevant.
	  - Use quotation marks around search terms to search for them in exact sequence.
	- **Full words** match better. While search has some fuzziness enabled, aim to use complete words that you remember.
	  - Example: If you remember the note has `in-hierarchy visited` but don't want to type "hierarchy":
	    - ✅ DO: Try searching `in visited` to see if that's enough
	    - ❌ AVOID: Typing partial words like `in hier visit`
	
</note>
<note name="t.ext.command.search.quick" title="Quick Search (Commands in 'thorg.search.quick' namespace)">
	
	Quick search commands in this hierarchy use the VSCode quick pick widget for fast searching without navigating to a search view. This enables snappy searches, but comes with visualization limitations (such as the inability to widen the quick pick to fit longer note names).
	
	If you use a non-standard zoom level in VSCode, you may want to adjust [[t.ext.configuration.values.visualPreferences.vsc_quickPick_maxLabelLength]].
	
	See child notes in this hierarchy for the different quick search commands available, as well as [[t.ext._.highlighted-commands]].
</note>
<note name="t.ext.command.search.quick._.tip" title="Quick Search Tip">
	
	- [[t.ext.command.search.quick.tip.empty query to get recently visited notes]]
</note>
<note name="t.ext.command.search.quick.all" title="Quick Search All">
	
	[[Searches|t.ext.command.search._.search-definition]] across all notes using quick search interface.
	
	### Command ID
	```txt
	thorg.search.quick.all
	```
	
	### Highlights
	- When you enter search terms without quotation marks, their placement in the note is irrelevant.
	  - Use quotation marks around search terms to search for them in exact sequence.
	
	
	### Also see
	#### Shortcuts
	- [[t.ext._.setup-of-shortcuts.ctrl-t-setup]]
	
	### Related Tips
	![[t.ext.command.search.quick._.tip]]
	
	### Similar commands
	- [[t.ext.command.search.quick.visited-since]] - Like quick search all, but filters by [[last visited|t.ext.data.type.note.visited]] before performing the [[search|t.ext.command.search._.search-definition]].
	- [[t.ext.command.search.quick.updated-since]] - Like quick search all, but filters by [[last updated|t.ext.data.type.note.updated]] before performing the [[search|t.ext.command.search._.search-definition]].
	- [[t.ext.command.search.quick.in-subtree.all]] - Like quick search all, but filters to notes in the [[t.ext.data.type.note.subtree]].
</note>
<note name="t.ext.command.search.quick.in-subtree._.tip" title="In-Subtree Command Tips">
	
	- [[t.ext.tip.vscode.assign-shortcut-to-open-a-frequent-file]] - Assign a shortcut to open an [[t.ext.data.type.note.ancestor-note]] of your frequently visited tree/hierarchy.
	- [[t.ext.command.search.quick.tip.empty query to get recently visited notes]]
	
</note>
<note name="t.ext.command.search.quick.in-subtree.all" title="Quick Search In Subtree">
	
	<div class="command-definition">
	
	Search all notes in the **[[subtree|t.ext.data.type.note.subtree]]** of the currently selected/opened [[note|t.ext.data.type.note]].
	</div>
	
	### Command ID
	```txt
	thorg.search.quick.in-subtree.all
	```
	
	### Behavior
	- **Includes current note** → Yes
	- **Includes descendant notes** → Yes
	- **No note selected** → Warning message
	
	### Example
	<details class="bordered-when-open">
	<summary>Usage Example</summary>
	
	![[t.ext.command.search.quick.in-subtree.all.example]]
	</details>
	
	### Also see
	#### Shortcuts
	- [[t.ext._.setup-of-shortcuts.ctrl-y-setup]]
	
	#### Related Tips
	![[t.ext.command.search.quick.in-subtree._.tip]]
	 
	#### Related Commands
	- [[t.ext.command.search.quick.in-subtree.visited-since]] - Like quick search in subtree, but also filters by [[last visited|t.ext.data.type.note.visited]] before performing the [[search|t.ext.command.search._.search-definition]].
	- [[t.ext.command.search.quick.in-subtree.updated-since]] - Like quick search in subtree, but also filters by [[last updated|t.ext.data.type.note.updated]] before performing the [[search|t.ext.command.search._.search-definition]].
</note>
<note name="t.ext.command.search.quick.in-subtree.all.example" title="Thorg Search In Subtree Example">
	
	## File Structure
	```txt
	workspace/
	├── vault-public/
	│   ├── recipes.italian.md
	│   ├── recipes.italian.pasta.md
	│   ├── recipes.italian.pasta.carbonara.md
	│   └── recipes.italian.pasta.carbonara.classic.md
	└── vault-private/
	    ├── family.traditions.cooking.md
	    └── recipes.italian.pasta.grandmas-recipe.md
	```
	
	
	**Public Notes:**
	- `recipes.italian` - Main Italian recipes overview
	- `recipes.italian.pasta` - Pasta cooking guide
	- `recipes.italian.pasta.carbonara` - Carbonara recipe
	- `recipes.italian.pasta.carbonara.classic` - Traditional carbonara method
	
	**Private Notes:**
	- `family.traditions.cooking` - Personal family cooking traditions (different hierarchy)
	- `recipes.italian.pasta.grandmas-recipe` - Secret family recipe
	
	## Search Example
	
	### Current Context
	- **Selected Note**: `recipes.italian.pasta`
	- **Command**: `thorg.search.quick.in-subtree.all`
	
	### Search Scope
	Searches the hierarchy of the current note (`recipes.italian.pasta`):
	
	**Included:**
	✅ recipes.italian.pasta (current note)
	✅ recipes.italian.pasta.carbonara (child)
	✅ recipes.italian.pasta.carbonara.classic (grandchild)
	✅ recipes.italian.pasta.grandmas-recipe (child, in different vault)
	
	**Excluded:**
	❌ recipes.italian (parent - not included)
	❌ family.traditions.cooking (different hierarchy - not included)  
	
</note>
<note name="t.ext.command.search.quick.in-subtree.updated-since" title="Quick Search, In Subtree, Updated Since">
	
	[[Searches|t.ext.command.search._.search-definition]] in notes filtered by:
	- Notes in the [[subtree|t.ext.data.type.note.subtree]] of the current note
	- Notes updated since a specified time
	
	
	### Command IDs
	```txt
	thorg.search.quick.in-subtree.updated-since.1-hour-ago
	thorg.search.quick.in-subtree.updated-since.2-hours-ago
	thorg.search.quick.in-subtree.updated-since.4-hours-ago
	
	thorg.search.quick.in-subtree.updated-since.today
	thorg.search.quick.in-subtree.updated-since.yesterday
	
	thorg.search.quick.in-subtree.updated-since.1-week-ago
	thorg.search.quick.in-subtree.updated-since.2-weeks-ago
	thorg.search.quick.in-subtree.updated-since.1-month-ago
	
	thorg.search.quick.in-subtree.updated-since.2-months-ago
	thorg.search.quick.in-subtree.updated-since.3-months-ago
	thorg.search.quick.in-subtree.updated-since.6-months-ago
	
	thorg.search.quick.in-subtree.updated-since.1-year-ago
	thorg.search.quick.in-subtree.updated-since.2-years-ago
	```
	
</note>
<note name="t.ext.command.search.quick.in-subtree.visited-since" title="Quick Search, In Subtree, Visited Since">
	
	[[Searches|t.ext.command.search._.search-definition]] in notes **filtered** by:
	- Notes in the [[t.ext.data.type.note.subtree]] of the current note
	- Notes [[visited|t.ext.data.type.note.visited]] since a specified time
	
	### Like
	This command is like [[t.ext.command.search.quick.in-subtree.all]], but with [[visited|t.ext.data.type.note.visited]]-since filtering.
	
	### Command IDs
	```txt
	thorg.search.quick.in-subtree.visited-since.1-hour-ago
	thorg.search.quick.in-subtree.visited-since.2-hours-ago
	thorg.search.quick.in-subtree.visited-since.4-hours-ago
	
	thorg.search.quick.in-subtree.visited-since.today
	thorg.search.quick.in-subtree.visited-since.yesterday
	
	thorg.search.quick.in-subtree.visited-since.1-week-ago
	thorg.search.quick.in-subtree.visited-since.2-weeks-ago
	
	thorg.search.quick.in-subtree.visited-since.1-month-ago
	thorg.search.quick.in-subtree.visited-since.2-months-ago
	thorg.search.quick.in-subtree.visited-since.3-months-ago
	thorg.search.quick.in-subtree.visited-since.6-months-ago
	
	thorg.search.quick.in-subtree.visited-since.1-year-ago
	thorg.search.quick.in-subtree.visited-since.2-years-ago
	```
	
	### Also see
	#### Shortcuts
	- [[t.ext._.setup-of-shortcuts.ctrl-y-setup]]
	
	#### Related Tips
	![[t.ext.command.search.quick.in-subtree._.tip]]
	 
</note>
<note name="t.ext.command.search.quick.tip.empty query to get recently visited notes" title="Tip: Use Empty Query (' ') to get recently visited notes">
	
	When using quick search commands such as:
	- [[t.ext.command.search.quick.all]]
	- [[t.ext.command.search.quick.in-subtree.all]]
	- [[t.ext.command.search.quick.in-subtree.updated-since]]
	
	To quickly access recently visited notes, just type a space ("` `") in the search query: **you will get the most recently visited notes** (see [[t.ext.feature.visit-history]] for more details).
	
	Note: For a note to be considered visited, you must spend more than the [[minimum visit threshold time|t.ext.feature.visit-history.visit-event.min-visitation-threshold]] focused on that note. 
	
	
	
</note>
<note name="t.ext.command.search.quick.updated-since" title="Quick Search, Updated Since">
	
	[[Searches|t.ext.command.search._.search-definition]] across notes filtered to those updated within specific time ranges (varies by command).
	
	### Command IDs
	```txt
	thorg.search.quick.updated-since.1-hour-ago
	thorg.search.quick.updated-since.2-hours-ago
	thorg.search.quick.updated-since.4-hours-ago
	
	thorg.search.quick.updated-since.today
	thorg.search.quick.updated-since.yesterday
	
	thorg.search.quick.updated-since.1-week-ago
	thorg.search.quick.updated-since.2-weeks-ago
	
	thorg.search.quick.updated-since.1-month-ago
	thorg.search.quick.updated-since.2-months-ago
	thorg.search.quick.updated-since.3-months-ago
	thorg.search.quick.updated-since.6-months-ago
	
	thorg.search.quick.updated-since.1-year-ago
	thorg.search.quick.updated-since.2-years-ago
	```
	
	### Also see
	#### Shortcuts
	- [[t.ext._.setup-of-shortcuts.ctrl-t-setup]]
	
	#### Similar commands
	- [[t.ext.command.search.quick.in-subtree.updated-since]] - Similar to this command, but also filters to notes in the [[subtree|t.ext.data.type.note.subtree]].
	
	#### Tips
	![[t.ext.command.search.quick.in-subtree._.tip]]
</note>
<note name="t.ext.command.search.quick.visited-since" title="Quick Search, Visited Since">
	
	[[Searches|t.ext.command.search._.search-definition]] across notes filtered to those [[visited|t.ext.data.type.note.visited]] within specific time ranges (varies by command).
	
	### Command IDs
	```txt
	thorg.search.quick.visited-since.1-hour-ago
	thorg.search.quick.visited-since.2-hours-ago
	thorg.search.quick.visited-since.4-hours-ago
	
	thorg.search.quick.visited-since.today
	thorg.search.quick.visited-since.yesterday
	
	thorg.search.quick.visited-since.1-week-ago
	thorg.search.quick.visited-since.2-weeks-ago
	
	thorg.search.quick.visited-since.1-month-ago
	thorg.search.quick.visited-since.2-months-ago
	thorg.search.quick.visited-since.3-months-ago
	thorg.search.quick.visited-since.6-months-ago
	
	
	thorg.search.quick.visited-since.1-year-ago
	thorg.search.quick.visited-since.2-years-ago
	```
	
	### Also see
	#### Shortcuts
	- [[t.ext._.setup-of-shortcuts.ctrl-t-setup]]
	
	#### Similar commands
	- [[t.ext.command.search.quick.in-subtree.visited-since]]
</note>
<note name="t.ext.concept" title="Thorg General Concept">
	
	<div class="centered">
	
	This hierarchy contains general concepts that haven't yet been organized into a more specific category.
	
	See the children of this hierarchy for individual concepts.
	</div>
	
	
	
</note>
<note name="t.ext.concept.javaExecutablePath" title="javaExecutablePath">
	
	This is the **full** path (`/some/path/bin/java`) to the Java executable that will be used to start [[t.ext.thorgServer]] by the Thorg Visual Studio Code extension.
	
	**Auto-installed by default**: If you accept the default values during [[t.ext.startup.first-startup]], Thorg will automatically install Java and set this value for you - no manual configuration needed. Thorg installs the OpenJDK JRE (Java Runtime Environment) outside your system `$PATH`, so it won't interfere with your existing system setup.
	
	If you opt out of automatic installation, you'll be prompted to enter the path to the Java executable during initial setup. In this case, make sure you enter the FULL path (`/some/path/bin/java`) to your Java installation. The validation prompts will guide you through entering the correct path.
	
	### Required version
	![[t.ext.startup.required-java-version]]
	
	### Where is it stored?
	Stored in [[t.ext.configuration.values.startupSetup.javaExecutablePath]]
	
</note>
<note name="t.ext.concept.machineName" title="Machine Name">
	
	### What is it?
	*machineName*: A name for your machine that is unique under your chosen username.
	
	Valid examples: [`macos-laptop-1`, `windows-desktop`, `machine-1`]
	
	
	### Why it exists?
	Primary use case: to disambiguate changes made on different machines while using the same username. This prevents unnecessary Git merge conflicts in data such as [[t.ext.feature.visit-history]]. Thorg segments the files it creates using the *machineName* you provide. 
	
	### Avoid sharing this value across machines
	Do NOT share or re-use this value across machines. Sharing it will cause Git merge conflicts in your [[t.ext.feature.visit-history]]. 
	
	### Example scenario
	#### Starting scenario
	You have a **laptop** and **desktop** that you use. Valid values for *machineName* would be "laptop" and "desktop" respectively.
	
	#### IF you got a 2nd laptop for prolonged usage
	If you need a 2nd laptop while retaining your previous laptop, a valid value for *machineName* on the brand new laptop would be "laptop2".
	
	#### IF you got a 2nd laptop without overlap in usage
	If you sold your laptop and don't plan any overlap in usage between the old and new laptop, it's OK to give the new laptop the designation "laptop" for *machineName*.
	
	
	### When do you specify it?
	You will specify it during the initial start up of Thorg.
	
	### Where is it stored?
	In [[t.ext.configuration.values.startupSetup.machineName]]
	
	
	
</note>
<note name="t.ext.concept.serverPort" title="serverPort">
	
	This is the [port](https://en.wikipedia.org/wiki/Port_(computer_networking)) on which [[Thorg Server|t.ext.thorgServer]] runs.
	
	### How Port is Determined
	The port is dynamically allocated when the Thorg server starts up. The server finds an available port and writes it to [[t.ext.data.type.workspace.thorg-dir.tmp.server.instance.port-file]].
</note>
<note name="t.ext.concept.thorgUsername" title="Thorg Username (Concept)">
	
	
	### Set/Modify
	Set during Thorg setup. Can be modified through [[t.ext.configuration.values.startupSetup.thorgUsername]].
	
	### Use case
	The primary use case in V1 is separating [[t.ext.feature.visit-history]] files when users decide to share visit history files between multiple users.
</note>
<note name="t.ext.configuration" title="Configuration">
	
	Configuration hierarchy for Thorg.
	
	- To learn how to change configuration, visit [[t.ext.configuration.how-to-change-thorg-configuration]]
	- To see available configuration values, go to [[t.ext.configuration.values]]
	
	
</note>
<note name="t.ext.configuration.how-to-change-thorg-configuration" title="How to Change Thorg Configuration Value">
	
	Thorg configuration/settings are changed through VSCode settings.
	
	### Open Settings
	- Open Command Palette ([[t.ext.vscode.how-to.open-command-palette]])
	- In the Command Palette, search for `Preferences: Open Settings (UI)`
	- Press Enter
	
	### Filter for Thorg Settings
	In the Settings search box, type `thorg` to filter for Thorg settings.
	
	![](./assets/submodule/for_external/Screenshot-2025_11_07T10_24_38.png){max-width: 700px, display: block, margin: 0 auto, border: 5px solid black}
	
	#### Through Search (if you know what you're looking for)
	If you know what you're looking for, start typing the search term. VSCode settings will auto-update. 
	
	<details>
	<summary>Tip: Typing less in Settings leads to more precise results</summary>
	
	As of 2025, typing less in VSCode settings is likely to yield better results than typing the full phrase, as it avoids overmatching unrelated terms.
	
	For example if you type in 
	```
	thorg min visitation
	```
	
	You'll get the single setting for [[t.ext.configuration.values.visitHistory.minVisitationFocusTimeMillis]].
	
	However, if you type the full setting name:
	```
	thorg min visitation focus time millis
	```
	You'll get matches unrelated to Thorg. 
	</details>
	
	
	
	#### Through Tree (if you're exploring)
	
	If you don't know which settings you're looking for and want to explore available Thorg settings:
	
	On the left-hand side in Settings, you'll see a tree view. Look under `Thorg` for configuration sections.
	
	### More info
	- [[t.ext.configuration.how-to-change-thorg-configuration.how-to-restart-thorg-for-config-changes]] - Most settings require a restart to take effect in early iterations of Thorg.
</note>
<note name="t.ext.configuration.how-to-change-thorg-configuration.how-to-restart-thorg-for-config-changes" title="How to Restart Thorg for Config Changes">
	
	Configuration changes that require a restart will state this in their description. (In V1, most configuration changes require a restart.)
	
	![[t.ext.thorgServer.how-to.restart]]
	
	
</note>
<note name="t.ext.configuration.settings" title="Thorg Configuration/Settings">
	
	### How to Change Thorg Configuration
	![[t.ext.configuration.how-to-change-thorg-configuration]]
	
	
	
</note>
<note name="t.ext.configuration.values" title="Thorg Setting Values">
	
	### How to Change Thorg Configuration
	[[t.ext.configuration.how-to-change-thorg-configuration]]
	
	### Values 
	- [[t.ext.configuration.values.startupSetup]]
	- [[t.ext.configuration.values.visitHistory]]
	- [[t.ext.configuration.values.visualPreferences]]
	- [[t.ext.configuration.values.advancedConfig]]
	- [[t.ext.configuration.values.thorgDeveloper]]
</note>
<note name="t.ext.configuration.values.advancedConfig" title="thorg.advancedConfig - VSCode Config Section">
	
	Bucket for advanced configuration.
	
	### Values
	- [[t.ext.configuration.values.advancedConfig.logLevel]]
	
	
</note>
<note name="t.ext.configuration.values.advancedConfig.logLevel" title="thorg.advancedConfig.logLevel - VSCode Config">
	
	Log level at which Thorg will log. Default is `INFO`.
	
	### Regular Operation
	Recommended to keep at `INFO` level.
	
	### Switching to DEBUG When Submitting Logs
	Switch the log level to `DEBUG` (or `TRACE`) when you have a reproducible issue and are collecting [[logs|t.ext.contact-us.submit-git-hub-issue.how-to.submit-logs.how-to-get-logs]] for [[issue|t.ext.contact-us.submit-git-hub-issue]] submission.
	
	### How to Change
	[[t.ext.configuration.how-to-change-thorg-configuration]]
</note>
<note name="t.ext.configuration.values.startupSetup" title="thorg.startupSetup - VSCode Config Section">
	
	#### Values
	- [[t.ext.configuration.values.startupSetup.javaExecutablePath]]
	- [[t.ext.configuration.values.startupSetup.machineName]]
	- [[t.ext.configuration.values.startupSetup.serverMaxHeapSpaceMB]]
	- [[t.ext.configuration.values.startupSetup.thorgUsername]]
	
	#### How to Modify
	See [[t.ext.configuration.how-to-change-thorg-configuration]].
	
</note>
<note name="t.ext.configuration.values.startupSetup.javaExecutablePath" title="thorg.startupSetup.javaExecutablePath - VSCode Config">
	
	![[t.ext.concept.javaExecutablePath]]
	
	### How to Change
	[[t.ext.configuration.how-to-change-thorg-configuration]]
	
</note>
<note name="t.ext.configuration.values.startupSetup.machineName" title="thorg.startupSetup.machineName - VSCode Config">
	
	Configuration `thorg.startupSetup.machineName` sets the machine name.
	
	![[t.ext.concept.machineName]]
	
	### How to Change
	[[t.ext.configuration.how-to-change-thorg-configuration]]
</note>
<note name="t.ext.configuration.values.startupSetup.serverMaxHeapSpaceMB" title="thorg.startupSetup.serverMaxHeapSpaceMB - VSCode Config">
	
	Configuration that defines the maximum amount of heap space allocated to the process running [[t.ext.thorgServer]] on a [JVM](https://en.wikipedia.org/wiki/Java_virtual_machine). This depends on the number of notes you have.
	
	Note that the maximum heap space does not mean all of it will be used, but it does influence when the JVM decides to garbage collect.
	
	### How to Change
	[[t.ext.configuration.how-to-change-thorg-configuration]]
	
</note>
<note name="t.ext.configuration.values.startupSetup.thorgUsername" title="thorg.startupSetup.thorgUsername - VSCode Config">
	
	![[t.ext.concept.thorgUsername]]
	
	### How to Change
	[[t.ext.configuration.how-to-change-thorg-configuration]]
	
</note>
<note name="t.ext.configuration.values.thorgDeveloper" title="thorg.thorgDeveloper - VSCode Config Section">
	
	This section is meant for developers of **Thorg**. To clarify: not for software developers in general, but specifically for developers working on Thorg itself.
	
	### Values
	- [[t.ext.configuration.values.thorgDeveloper.developmentMode]]
</note>
<note name="t.ext.configuration.values.thorgDeveloper.developmentMode" title="thorg.thorgDeveloper.developmentMode - VSCode Config">
	
	This mode is meant for developers of **Thorg**.
	
	Turning this ON is NOT recommended. In typical operation, this should remain at its default value: Disabled.
</note>
<note name="t.ext.configuration.values.visitHistory" title="thorg.visitHistory - VSCode Config Section">
	
	<div class="centered">
	
	Configuration section for [[t.ext.feature.visit-history]].
	</div>
	
	#### Values
	- [[t.ext.configuration.values.visitHistory.minVisitationFocusTimeMillis]]
	- [[t.ext.configuration.values.visitHistory.autoUnfocusTtlSeconds]]
	
	#### How to Change
	[[t.ext.configuration.how-to-change-thorg-configuration]]
</note>
<note name="t.ext.configuration.values.visitHistory.autoUnfocusTtlSeconds" title="thorg.visitHistory.autoUnfocusTtlSeconds - VSConfig (Default: 180 seconds)">
	
	Configuration value that sets the auto unfocus time:
	
	![[t.ext.feature.visit-history.visit-event.UNFOCUS.auto-unfocus-due-to-ttl]]
	
	### How to Change
	[[t.ext.configuration.how-to-change-thorg-configuration]]
</note>
<note name="t.ext.configuration.values.visitHistory.minVisitationFocusTimeMillis" title="thorg.visitHistory.minVisitationFocusTimeMillis - VSCode Config (Default: 3 seconds)">
	
	Configuration that sets the min-visitation-threshold for [[t.ext.feature.visit-history]]:
	
	![[t.ext.feature.visit-history.visit-event.min-visitation-threshold]]
	
	### How to Change
	[[t.ext.configuration.how-to-change-thorg-configuration]]
	
</note>
<note name="t.ext.configuration.values.visualPreferences" title="thorg.visualPreferences - VSCode Config Section">
	
	- [[t.ext.configuration.values.visualPreferences.vsc_quickPick_maxLabelLength]]
	
</note>
<note name="t.ext.configuration.values.visualPreferences.vsc_quickPick_maxLabelLength" title="thorg.visualPreferences.vsc.quickPick.maxLabelLength: Max Length of VSCode Quick Pick Labels (Before Truncation)">
	
	Configuration for the max length of labels within [Quick Picks](https://code.visualstudio.com/api/ux-guidelines/quick-picks) used by Thorg. Labels exceeding this value will be truncated. You can adjust this value based on your VSCode zoom level.
	
	### Likely Questions
	
	#### Why don't we make quick pick wider?
	VSCode does not allow changing the width of quick pick. An issue about this has been open for over half a decade:
	
	- [Option to widen the command palette · Issue-85374 · microsoft/vscode](https://github.com/microsoft/vscode/issues/85374) - open since 2019
	  - Similar issue has been open since 2017 [Allow to change the width of quick open · Issue-38225 · microsoft/vscode](https://github.com/microsoft/vscode/issues/38225)
	
	#### Why is this a config and not auto-adjusted?
	This is a configuration instead of being pre-set and auto-adjusting because the number of characters that fit into quick pick varies based on zoom level, and we haven't found the hook to get the proper zoom ratio from VSCode. We provide a sensible default, but if you work with a more zoomed in/out view, adjust this setting to control label truncation in quick pick.
</note>
<note name="t.ext.contact-us" title="Contact Us">
	
	### For Discussions - Discord
	[[t.ext.contact-us.discord]]
	
	### For Bugs and Detailed Feature Requests - Submit GitHub Issue
	[[t.ext.contact-us.submit-git-hub-issue]]
	
	### For General Questions - Try LLM First, Then Discord
	First, try chatting with an LLM using the documentation as [[t.ext.as-context-for-llm]].
	
	Then head to [[t.ext.contact-us.discord]].
	
	### For Official Correspondence
	[[t.ext.contact-us.email]]
</note>
<note name="t.ext.contact-us.discord" title="Thorg Discord Server">
	
	<div class="centered">
	
	[Join the Thorg Discord!](https://discord.gg/qHv4MsB6wg)
	</div>
	
	Discord is the main communication channel for Thorg's community.
	
</note>
<note name="t.ext.contact-us.email" title="Email: contact@thorg.app">
	
	<div class="centered xxxlarge">
	
	contact@thorg.app
	</div>
	
</note>
<note name="t.ext.contact-us.submit-git-hub-issue" title="Thorg - Submit Git Hub Issue">
	
	
	<div class="centered xxlarge">
	
	**-->>[Submit Issue for VSCode Thorg Extension](https://github.com/Thorg-App/issues-thorg-vscode/issues/new/choose)<<--**
	</div>
	
	If you have a reproducible issue, we would greatly appreciate it if you could send us logs along with the issue. See [[t.ext.contact-us.submit-git-hub-issue.how-to.submit-logs]].
	
	
</note>
<note name="t.ext.contact-us.submit-git-hub-issue.highlighted-known-issue" title="Highlighted Known Issue">
	
	Hierarchy for highlighted known issues.
	
	See child notes for specific highlighted known issues.
</note>
<note name="t.ext.contact-us.submit-git-hub-issue.highlighted-known-issue.no-windows-support-yet" title="Thorg does NOT support Windows Yet, Vote here for Windows Support ✅">
	
	**[Vote here for: Feature Add support for windows. · Issue-1 · Thorg-App/issues-thorg-vscode](https://github.com/Thorg-App/issues-thorg-vscode/issues/1)**
</note>
<note name="t.ext.contact-us.submit-git-hub-issue.how-to" title="How To">
	
	How-to guides related to issue submission.
	
	Reminder: If you're submitting an issue for the VSCode extension, the link is [here](https://github.com/Thorg-App/issues-thorg-vscode/issues/new/choose).
</note>
<note name="t.ext.contact-us.submit-git-hub-issue.how-to.submit-logs" title="How to Submit Logs">
	
	To de-risk sharing any user information publicly, please do **NOT** directly attach your user logs to GitHub issues (which you submit [[here|t.ext.contact-us.submit-git-hub-issue]]). That said, logs will help us **greatly** in triaging your issue, and we would very much appreciate if you voluntarily share your logs with us through a private communicadtion channel.
	
	### How to Get Logs
	![[t.ext.contact-us.submit-git-hub-issue.how-to.submit-logs.how-to-get-logs]]
	
	### How to Share Logs
	
	#### 1) Let Us Know You Shared Logs in the GitHub Issue
	If you would like to share your Thorg logs, please create the [[issue|t.ext.contact-us.submit-git-hub-issue]] with the following heading:
	
	```txt
	### LOGS
	I was able to email logs to contact@thorg.app and included the GitHub issue ID in the subject: Yes
	```
	
	
	#### 2) Share Your Logs by Sending Us an Email
	Email the logs (as an attachment) to [[t.ext.contact-us.email]] with the subject line: 
	
	> LOGS for https://github.com/Thorg-App/issues-thorg-vscode/issues/<YOUR_ISSUE_NUMBER>
	
	### Log deletion
	Your logs will only be used to diagnose the issue you've reported and we (Thorg) will **completely** delete your logs in a timely manner.
	
</note>
<note name="t.ext.contact-us.submit-git-hub-issue.how-to.submit-logs.how-to-get-logs" title="How to Get Thorg Logs">
	
	#### Two ways of getting Thorg logs
	
	- [[Use command to gather logs for you (Recommended)|t.ext.command.logs.capture.combined.recent]] 
	- [[t.ext.contact-us.submit-git-hub-issue.how-to.submit-logs.how-to-get-logs.manually]]
	
	
	#### If the Issue Is Reproducible: please use DEBUG logging.
	If you can reproduce the issue, it would be ideal if you could send us logs at **DEBUG** log level by changing the [[t.ext.configuration.values.advancedConfig.logLevel]] setting.
</note>
<note name="t.ext.contact-us.submit-git-hub-issue.how-to.submit-logs.how-to-get-logs.manually" title="Manually get Thorg logs">
	
	
	You can manually collect thorg logs by going through 2 main locations for Thorg logs:
	
	- [[t.ext.file.home-thorg-dir.not-under-scm.logs]] - Contains initialization/pre-startup logs. These are logs that occur before we found [[t.ext.data.type.workspace]] directory and before we're able to get [[t.ext.thorgServer]] up and running. If you're having initialization issues, please share the logs from this directory.
	- [[t.ext.data.type.workspace.thorg-dir.tmp.logs]] - This is where the main logs are stored from both the server and client. If the issue happened post-initialization, logs from this directory should be sufficient.
</note>
<note name="t.ext.data" title="Data">
	
	See [[t.ext.data.thorg-view-on-data]] for how Thorg handles data.
	
	See [[t.ext.data.type]] for the main data types used within Thorg.
</note>
<note name="t.ext.data.thorg-view-on-data" title="Thorg's View on Data">
	
	![[t.ext.data.thorg-view-on-data.you-own-your-data]]
	
	![[t.ext.data.thorg-view-on-data.transparent-data-model]]
</note>
<note name="t.ext.data.thorg-view-on-data.transparent-data-model" title="Transparent Data Model">
	<div class="centered">
	
	#### Don't let your knowledge be stuck in proprietary format.
	</div>
	
	**Transparent Data Model** means **you have full access to all the data Thorg creates and uses**, without obfuscation.
	
	This goes beyond simply exporting to common formats—which often omit critical details. Instead, **you have direct access to 100% of the raw data** that Thorg creates, exactly as Thorg uses it.
	
	We aim to store data in **open, human-readable formats** (example: *non-encoded JSON*), making it easy to inspect, parse, and manage.
	
	When custom formats are needed for performance, we keep them in text format and document them thoroughly so you can parse them easily if desired. Example: [[t.ext.feature.visit-history.file.content-format]]. 
	
	#### Where to find Thorg-created data
	Besides the [[t.ext.data.type.note.frontmatter]] added to each [[t.ext.data.type.note]], the main places to look for Thorg-created data are:
	
	- [[t.ext.data.type.workspace.thorg-dir]]
	- [[t.ext.file.home-thorg-dir]]
	
	#### Clarification
	Transparent Data Model does NOT mean your data is accessible to anyone but you. It means you can understand what the data is. See [[t.ext.data.thorg-view-on-data.you-own-your-data]].
	
</note>
<note name="t.ext.data.thorg-view-on-data.you-own-your-data" title="You Own Your Data">
	
	
	<div class="centered">
	
	#### **Your data is your data. You own your data.**
	
	We do **NOT** have access to your [[notes|t.ext.data.type.note]]. All note data is stored **locally**, and **you retain full ownership and control**.
	
	When we start collecting anonymized app usage data (not note data), we will provide a way to opt out.
	</div>
	
</note>
<note name="t.ext.data.type" title="Data Types">
	
	Hierarchy for the definitions of data types used in Thorg.
</note>
<note name="t.ext.data.type.note" title="Note">
	
	<div class="centered">
	
	In short: A Thorg note is a [Markdown](https://en.wikipedia.org/wiki/Markdown) file with [YAML](https://en.wikipedia.org/wiki/YAML) [FrontMatter](https://jekyllrb.com/docs/front-matter/) that contains a globally unique `id` field.
	</div>
	
	
	
	### Frontmatter
	![[t.ext.data.type.note.frontmatter]]
	
	### Notes
	In V1 a [note from Dendron](https://wiki.dendron.so/notes/4p7e51zwb8jsvpnnh108txw/) is a valid Thorg Note.
</note>
<note name="t.ext.data.type.note-link" title="Note Link">
	
	Represents a link between notes.
	
	### Examples
	![[t.ext.data.type.note-link.example]]
	
	### Vocabulary
	![[t.ext.data.type.note-link.vocabulary]]
	
	
</note>
<note name="t.ext.data.type.note-link.example" title="Example Note links using Note Name">
	
	
	
	![[t.ext.data.type.note-link.example.wiki-link]]
	
	![[t.ext.data.type.note-link.example.embed]]
	
	![[t.ext.data.type.note-link.example.fully-qualified-link]]
</note>
<note name="t.ext.data.type.note-link.example.embed" title="Embed">
	
	You have a note file `some.note-1.md`
	
	#### Transcluded/Embedded note
	To transclude/embed its content into your note, use its name with embed syntax: 
	
	```md
	![[some.note-1]]
	```
</note>
<note name="t.ext.data.type.note-link.example.fully-qualified-link" title="Fully Qualified Link">
	
	You have a note file `some.note-1.md`
	
	#### Fully qualified path
	To specify the note in a particular [[vault|t.ext.data.type.vault]] (most useful when using multiple vaults), start the path from your [[workspace|t.ext.data.type.workspace]].
	
	In this example, `some.note-1.md` lives at `$YOUR_THORG_WORKSPACE/vault-1/some.note-1.md` 
	
	```md
	[[vault-1/some.note-1]]
	```
</note>
<note name="t.ext.data.type.note-link.example.wiki-link" title="Wiki Link">
	
	
	You have a note file `some.note-1.md`
	
	#### Regular wiki link
	To reference it as a link from your current note, use the [[note name|t.ext.data.type.note.name]]:
	
	```md
	[[some.note-1]]
	```
</note>
<note name="t.ext.data.type.note-link.type.wiki-link" title="Wiki Link">
	
	A wiki link references a note using its [[t.ext.data.type.note.name]] **without** embedding the note's contents.
	
	
	Let's say you have a target note:
	```md
	some.note-1.md
	```
	
	#### Simple wiki link
	To reference it as a link from your current note, use the following syntax: 
	
	```md
	[[some.note-1]]
	```
	
	### Simple wiki links are unnamed
	![[t.ext.data.type.note-link.type.wiki-link.unnamed]]
	
	### Named wiki links
	![[t.ext.data.type.note-link.type.wiki-link.named]]
</note>
<note name="t.ext.data.type.note-link.type.wiki-link.named" title="Named Link">
	
	<div class="bordered">
	
	#status.not-implemented: this is not implemented yet, but will be. You can start using the pattern of typed relationships to add consistency in defining relationship between notes, and later on these relationships will come to life in visualizations :). 
	</div>
	
	
	## Named link
	To name a link, prefix it with a relationship note using the syntax `[[rel.<name-of-relationship>]]:[[some-dst-note]]`
	
	### Example of **named** note links from note-A
	
	
	```md
	---
	title: note-A
	---
	
	### Relationshps
	- [[rel.depends-on]]:**[[component-A]]**
	- [[rel.dependency-of]]:[[component-B]]
	```
	
	#### Dissecting one of the two named relationships above
	
	```txt
	[[rel.depends-on]]:**[[component-A]]**
	```
	
	- `[[rel.depends-on]]` is a note, but because it starts with the `rel.` hierarchy, it is treated as a special type of note: [[t.ext.data.type.relationship-note]].
	- `[[component-A]]` is the destination of the note link. 
	
	With `[[rel.depends-on]]:**[[component-A]]**` we create a named relationship of:
	```mermaid
	graph LR
	   noteA --depends-on--> component-A
	```
</note>
<note name="t.ext.data.type.note-link.type.wiki-link.unnamed" title="Unnamed note link">
	
	A simple [[t.ext.data.type.note-link]] like `[[some-dst-note]]` is an **unnamed** note link.
	
	For a link to have a name, it needs to be prefixed with a `[[rel.<X>]]` note.
	
	#### Upcoming: Named Note Links
	Upcoming feature is support for [[t.ext.data.type.note-link.type.wiki-link.named]]
	
</note>
<note name="t.ext.data.type.note-link.vocabulary" title="Note Link Vocabulary">
	
	- **Origin Note**: The note from which the link originates.
	- **Target Note**: The note to which the link points. 
</note>
<note name="t.ext.data.type.note.ancestor-note" title="Ancestor Note">
	
	**Ancestor notes** are notes positioned higher in Thorg's note hierarchy, serving as organizational parents to descendant notes. They provide structure and context for more specific topics nested beneath them.
	
	![[t.ext.data.type.note.hierarchy]]
	
	
</note>
<note name="t.ext.data.type.note.children" title="Children">
	
	Children of a note are defined based on the lowercase [[t.ext.data.type.note.name]].
	
	For example, `a1.a2` is a child of `a1`.
	
	#### Note & children
	<details>
	<summary>A note can have multiple children, and children can have the same name (in multi-vault scenarios).</summary>
	
	In this example we have the following notes:
	- a1 (vault1)
	- a1.a2 (vault1)
	- a1.a2.a3 (vault1)
	- a1 (vault2)
	- a1.a2 (vault2)
	- a1.a2.a3 (vault2)
	
	The 2 children of a1 are: a1.a2 (vault1) and a1.a2 (vault2)
	
	![img](./assets/images/Screenshot_2023-07-21_at_7.36.41_PM.png){max-width: 300px}
	</details>
	
	<details>
	<summary>A note can be childless.</summary>
	
	In this example we have the following notes:
	- a1 (vault1)
	- a1.a2 (vault1)
	- a1.a2.a3 (vault1)
	- a1 (vault2)
	- a1.a2 (vault2)
	- a1.a2.a3 (vault2)
	
	Notes a1.a2.a3 (vault1) and a1.a2.a3 (vault2) are childless.
	
	![img](./assets/images/Screenshot_2023-07-21_at_7.36.41_PM.png){max-width: 300px}
	</details>
	
	
	#### Children vs Descendants
	Children are direct children of a note, while [[t.ext.data.type.note.descendants]] include all levels below the note in the [[hierarchy|t.ext.data.type.note.hierarchy]].
	
	#### Thorg hierarchy
	<details class="bordered-when-open">
	<summary>Thorg hierarchy</summary>
	
	![[t.ext.data.type.note.hierarchy]]
	</details>
	
</note>
<note name="t.ext.data.type.note.ConnectorNoteInBundle" title="ConnectorNoteInBundle">
	
	### Note Connector in Bundle
	Note connectors in bundles serve as a linkage or intermediate note among other notes. Consider the following notes in a bundle:
	
	```
	a1
	a1.a2.A3-1
	a1.a2.A3-2
	```
	
	Here, `a1.a2` acts as the connector note. It could be a [[t.ext.data.type.note.stub]] or a regular [[t.ext.data.type.note]]. The key characteristics of a connector note are:
	
	1. **Non-originality:** The connector note is not part of the original set of notes that were bundled.
	2. **Linkage:** It serves to connect the original notes within the bundle.
	
</note>
<note name="t.ext.data.type.note.content" title="Note Content">
	
	In **Thorg**, when we refer to note **content**, this is synonymous with the **Markdown content** of the note.
	
	This **excludes** the [[t.ext.data.type.note.frontmatter]] data of the note.
</note>
<note name="t.ext.data.type.note.data.title" title="Note Title (Concept)">
	
	Title is envisioned to represent a very readable name for the note, to be used in visualizations and previews.
	
	If the [[frontmatter|t.ext.data.type.note.frontmatter]] contains [[t.ext.data.type.note.frontmatter.field.title]], we will use the value from the frontmatter.
	
	If the title is not provided in frontmatter, we will use [[t.ext.data.type.note.name]] to formulate the title of the note.
</note>
<note name="t.ext.data.type.note.descendants" title="descendents">
	
	Descendants are notes that appear below a given note in the hierarchy, which is determined by [[t.ext.data.type.note.name]].
	
	For example, if a note is named `project.documentation`, its descendants include:
	- `project.documentation.api`
	- `project.documentation.api.endpoints`
	- `project.documentation.api.authentication`
	- `project.documentation.api.endpoints.users` (nested descendant)
	
	Descendants include both direct children (one level below) and all nested levels beneath the note in the hierarchy.
	
	See also: [[t.ext.data.type.note.children]] for direct children only.
	
	Learn more about Thorg hierarchy usage below:
	
	![[t.ext.data.type.note.hierarchy]]
</note>
<note name="t.ext.data.type.note.file-name.should-have-markdown-extension" title="Should Have Markdown Extension">
	
	Note file names should have the markdown extension.
	
	Example:
	```txt
	note_name.md
	```
</note>
<note name="t.ext.data.type.note.frontmatter" title="Frontmatter Documentation">
	
	![[t.ext.data.type.note.frontmatter.field]]
	
	![[t.ext.data.type.note.frontmatter.note-must-have-a-valid-frontmatter]]
</note>
<note name="t.ext.data.type.note.frontmatter.field" title="Frontmatter Fields">
	
	### Required fields
	<details class="bordered-when-open">
	<summary>id</summary>
	
	![[t.ext.data.type.note.frontmatter.field.id]]
	</details>
	
	### For now required as well:
	<details class="bordered-when-open">
	<summary>title</summary>
	
	![[t.ext.data.type.note.frontmatter.field.title]]
	</details>
	
	<details class="bordered-when-open">
	<summary>desc (description)</summary>
	
	![[t.ext.data.type.note.frontmatter.field.desc]]
	</details>
	
	
	<details class="bordered-when-open">
	<summary>updated</summary>
	
	![[t.ext.data.type.note.frontmatter.field.updated]]
	</details>
	
	<details class="bordered-when-open">
	<summary>created</summary>
	
	![[t.ext.data.type.note.frontmatter.field.created]]
	</details>
	
	
	
</note>
<note name="t.ext.data.type.note.frontmatter.field.context" title="Context field in Frontmatter">
	
	`context` is an optional field in note frontmatter which will be used when gathering context for the note. 
	
	Example value: 
	
	```yaml
	---
	context: 
	  - /some/file/path-1
	  - /some/file/path-2
	---
	```
	
	Context gathering will be used largely to feed LLMs with data.
</note>
<note name="t.ext.data.type.note.frontmatter.field.created" title="created timestamp in frontmatter">
	
	`created` - timestamp in milliseconds since the Unix epoch, when the note was created.
	
	### Example:
	```yaml
	---
	created: 1743465475934
	---
	```
</note>
<note name="t.ext.data.type.note.frontmatter.field.desc" title="Desc">
	
	Description field in the [[t.ext.data.type.note.frontmatter]] of the note.
	
	```md
	---
	desc: ''
	---
	```
</note>
<note name="t.ext.data.type.note.frontmatter.field.id" title="Note id in frontmatter">
	
	The ID in frontmatter is the minimum value needed to deem a markdown file as a parseable note.
	
	### Format
	```yaml
	---
	id: <globally-unique-string>
	---
	```
	
	```yaml
	---
	id: 5wq691vs7bkjf59xdsdsadf
	---
	```
	
	### Why is `id` required?
	
	#### Stable links
	Without an `id`, whenever you publish (web view), you would publish with the file name. This makes the links very brittle if any refactoring occurs. We want to allow linking to published notes in a much more stable fashion, so you can refactor note hierarchies without breaking links to your published views.
	
	#### Long-term metadata
	A globally unique, **stable** identifier tied to the file allows us to store metadata about that note, such as [[t.ext.feature.visit-history]].
</note>
<note name="t.ext.data.type.note.frontmatter.field.title" title="Note Title (Frontmatter Field)">
	
	The frontmatter note title is stored within the FrontMatter of a note and is used to set a particular value for [[t.ext.data.type.note.data.title]].
	
	An example note title set in frontmatter:
	
	```yml
	---
	title: Note Title in Frontmatter
	...
	---
	```
	
	The note title use case is to have a display name for a note in visualizations and previews that is different from its file name. 
	
	## Notes
	Not to be confused with [[t.ext.data.type.note.name]]
</note>
<note name="t.ext.data.type.note.frontmatter.field.updated" title="updated timestamp in frontmatter">
	
	`updated` - timestamp in milliseconds since the Unix epoch, when the note was last updated.
	
	### Example:
	```yaml
	---
	updated: 1743465432741
	---
	```
</note>
<note name="t.ext.data.type.note.frontmatter.note-must-have-a-valid-frontmatter" title="Note Must Have a Valid Frontmatter">
	
	Each note in Thorg must have valid FrontMatter.
	
	FrontMatter is a YAML value at the beginning of the note surrounded by `---`.
	
	An example of basic valid FrontMatter:
	
	```yaml
	---
	id: ezbbhbn8i8thheiak1ng2vq
	title: Note Must Have a Valid Frontmatter
	desc: ''
	updated: 1685861421330
	created: 1685861421330
	---
	```
	
	### Frontmatter Documentation:
	[[t.ext.data.type.note.frontmatter]]
</note>
<note name="t.ext.data.type.note.frontmatter.structure.dates-are-in-millis-since-epoch" title="Dates Are in Millis since Epoch">
	
	FrontMatter date fields such as:
	```
	---
	...
	updated: 1685895360737
	created: 1685895360737
	---
	```
	
	are in milliseconds since epoch.
	
	> An integer value representing the timestamp (the number of milliseconds since midnight at the beginning of January 1, 1970, UTC — a.k.a. the epoch).
	
	Example JavaScript to convert to human-readable format:
	
	```js
	var timestamp = 1685894903640;
	var date = new Date(timestamp);
	console.log(date);
	```
</note>
<note name="t.ext.data.type.note.frontmatter.structure.id-should-be-unique-without-spaces" title="Id Should Be Unique without Spaces">
	
	The FrontMatter `id` is a required field (actually, it's the most important metadata field).
	
	The `id` field within the FrontMatter should be globally unique and should NOT contain spaces. 
	
	Example of a valid id:
	```yaml
	---
	id: 638jn1w6ns8ptmqzkqvycmg
	...
	---
	```
	
</note>
<note name="t.ext.data.type.note.frontmatter.structure.required-dates" title="Required Dates">
	
	FrontMatter must have the required date fields.
	
	At the time of this writing, the following dates are required:
	
	```yaml
	---
	...
	updated: 1685864809617
	created: 1685864781451
	---
	```
	
	<details>
	<summary>Dates must be in Millis since epoch</summary>
	
	![[t.ext.data.type.note.frontmatter.structure.dates-are-in-millis-since-epoch]]
	</details>
	
	
	
</note>
<note name="t.ext.data.type.note.hierarchy" title="Thorg Note Hierarchy">
	
	**Thorg** uses a dot-delimited hierarchy system to organize notes into logical, navigable structures, creating parent-child relationships that enable powerful organization and cross-referencing capabilities.
	
	## Core Hierarchy Concepts
	
	### Dot Notation
	Thorg hierarchies use periods (`.`) as delimiters to establish parent-child relationships:
	
	```txt
	workspace/.thorg
	workspace/vault-1/grandparent.parent.child.md
	workspace/vault-1/grandparent.parent.md
	workspace/vault-1/grandparent.md
	```
	
	Each additional dot represents a deeper level in the hierarchy:
	- `grandparent` - **Root level**
	- `grandparent.parent` - **Second level** 
	- `grandparent.parent.child` - **Third level**
	
	
	<details class="bordered xxsmall">
	<summary>Subfolders in vaults in the future</summary>
	
	![[t.ext.data.type.note.hierarchy.sub-folders-in-vault-in-the-future]]
	</details>
	
	## File Structure and Note Names
	
	| Component | Description | Example |
	| :--- | :--- | :--- |
	| **File Path** | Physical location on disk | `/../workspace/vault-1/grandparent.parent.child.md` |
	| **[[t.ext.data.type.note.name]]** | Hierarchical identifier (File path without vault path, without file extensions) | `grandparent.parent.child` |
	| **Parent Note** | One level up in hierarchy | `grandparent.parent` |
	| **Root Note** | Top-level ancestor | `grandparent` |
	
	## Cross-Vault Hierarchy Support
	
	Thorg's hierarchy system extends **across multiple vaults**, allowing you to maintain consistent organization while separating content by access level or purpose.
	
	### Example: Public and Private Vaults
	
	**Public Vault Structure:**
	```txt
	topics.programming.javascript.md
	topics.programming.python.md
	```
	
	**Private Vault Addition:**
	```txt
	topics.programming.personal-notes.md
	topics.programming.javascript.private-examples.md
	```
	
	The hierarchy remains intact across vaults, with all notes sharing the same ancestor (`topics.programming`).
	
	## Navigation and Linking
	
	### Wiki Links
	Reference any note in the hierarchy using wiki links:
	- `[[grandparent.parent.child]]` - Link to specific note
	- `[[grandparent.parent]]` - Link to parent note
	
	### Hierarchy Benefits
	
	```mermaid
	graph TD
	    A[Root Note] --> B[Parent Notes];
	    B --> C[Child Notes];
	    C --> D[Grandchild Notes];
	    
	    B --> E[Cross-Vault Children];
	    
	    style A fill:#f96,stroke:#333,stroke-width:3px;
	    style E fill:#6f9,stroke:#333,stroke-width:2px,stroke-dasharray: 5 5;
	```
	
	## Best Practices for Thorg Hierarchies
	
	1. **Meaningful Names**: Use descriptive, **concise** terms that indicate content relationships (use [[title in frontmatter|t.ext.data.type.note.frontmatter.field.title]] for more verbose note names)
	   - ✅ `projects.web-app.frontend.components`
	   - ❌ `stuff.thing1.more.items`
	
	2. **Logical Grouping**: Place related content under common ancestors
	   ```txt
	   documentation.api.endpoints.users
	   documentation.api.endpoints.auth
	   documentation.api.endpoints.products
	   ```
	
	3. **Sibling Organization**: Notes under one parent should be conceptually related
	   ```txt
	   tools.editors.vscode
	   tools.editors.neovim
	   tools.editors.sublime
	   ```
	
	
</note>
<note name="t.ext.data.type.note.hierarchy.sub-folders-in-vault-in-the-future" title="Sub Folders in Vault in the Future">
	
	We aim to support sub-folders within [[t.ext.data.type.vault]] for hierarchies in the future to increase compatibility with other markdown-based tooling. However, sub-folders in vaults are NOT the priority for initial releases.
</note>
<note name="t.ext.data.type.note.name" title="Note Name">
	
	Note name is how you reference other notes using wiki links and how you establish note hierarchies.
	
	### Note name is hierarchy
	Note names establish the hierarchy of notes, with dot (`.`) as the delimiter between a parent and child note.
	
	For example, consider these files:
	```txt
	workspace/.thorg
	workspace/vault-1/grandparent.parent.child.md
	workspace/vault-1/grandparent.parent.md
	```
	
	File `grandparent.parent.child.md` has the note name `grandparent.parent.child` and its parent note name is `grandparent.parent`.
	
	
	### Note linking
	![[t.ext.data.type.note-link.example]]
	
	------------------------------------------------------
	### Further notes
	<details class="bordered-when-open">
	<summary>Hierarchies and Cross vault Hierarchy support</summary>
	
	Note names are most important for hierarchy support and cross vault hierarchies.
	
	For example let's say you have **public-vault** with notes 
	
	```txt
	grandparent.parent.child-1.md
	grandparent.parent.child-2.md
	```
	
	And you want to attach a personal note to this hierarchy in a **personal-vault**, you can do so as follows:
	
	```txt
	grandparent.parent.private-child-1.md
	```
	
	and `grandparent.parent.private-child-1.md` will become a sibling of `grandparent.parent.child-1` and `grandparent.parent.child-2`.
	</details>
	
	
	
</note>
<note name="t.ext.data.type.note.name.fully-qualified-note-name" title="Fully Qualified Note Name">
	
	Fully qualified note name is the file path within the workspace without the .md extension.
	
	For example, if you have:
	
	```md
	/your-workspace/vault-1/note-1.md
	```
	
	The **fully qualified name** will be `vault-1/note-1` (while the **name** will be `note-1`).
	
	This is similar to a fully qualified class name in **Java**.
</note>
<note name="t.ext.data.type.note.parents" title="Parents">
	
	Parents of a note are defined based on the lowercase [[t.ext.data.type.note.name]].
	
	
	<details>
	<summary>1. Top-level notes (e.g., a1) will NOT have a parent.</summary>
	
	In this example we have the following notes:
	- a1 (vault1)
	- a1.a2 (vault1)
	- a1.a2.a3 (vault1)
	- a1 (vault2)
	- a1.a2 (vault2)
	- a1.a2.a3 (vault2)
	
	Notes a1 (vault1) and a1 (vault2) do not have parents, while all other notes in this example do.
	
	![img](./assets/images/Screenshot_2023-07-21_at_7.36.41_PM.png){max-width: 300px}
	</details>
	
	<details>
	<summary>2. A note can have multiple parents (in multi-vault scenarios).</summary>
	
	In this example we have the following notes:
	- a1 (vault1)
	- a1.a2 (vault1)
	- a1.a2.a3 (vault1)
	- a1 (vault2)
	- a1.a2 (vault2)
	- a1.a2.a3 (vault2)
	
	Note a1.a2 (vault1) has 2 parents: a1 (vault1) and a1 (vault2)
	
	![img](./assets/images/Screenshot_2023-07-21_at_7.36.41_PM.png){max-width: 300px}
	</details>
	
</note>
<note name="t.ext.data.type.note.stub" title="Stub Note">
	
	A stub note is an in-memory creation (without writing files). Stubs mainly exist to help with navigation and to make it easier to create missing notes in the hierarchy. 
	
	This is best explained with an example. Let's say you have the following real notes:
	- a1
	- a1.a2.a3-I
	- a1.a2.a3-II
	- a1.a2.a3-III
	- a1.b2.b3-I
	- a1.b2.b3-II
	- a1.b2.b3-III
	
	Two stubs will be created in the above scenario:
	- a1.a2
	- a1.b2
	
	These stubs help with navigation so that instead of having 6 notes directly under note `a1`, `a1` now has 2 children: `a1.a2` and `a1.b2`. Each of these in turn has 3 children of their own. `a1.a2` has `a1.a2.a3-I`, `a1.a2.a3-II`, and `a1.a2.a3-III`, while `a1.b2` has `a1.b2.b3-I`, `a1.b2.b3-II`, and `a1.b2.b3-III`, making the hierarchy much more manageable.
	
	### Characteristics of a stub note:
	- A stub cannot be a leaf note.
	- A stub must have a descendant that is a real file note.
	  - If all stub children are removed, the stub note disappears.
	- A stub can have a stub as a child. Inversely, a stub can have a stub as a parent.
	  - As long as there is a descendant leaf that is a real note.
</note>
<note name="t.ext.data.type.note.subtree" title="subtree">
	
	The sub-tree of a note includes:
	- The starting [[note|t.ext.data.type.note]].
	- All the [[t.ext.data.type.note.descendants]] of the starting note.
</note>
<note name="t.ext.data.type.note.updated" title="updated">
	
	Front-matter stored value that is used by the app to determine when the note was updated.
	
	```yml
	---
	updated: 1724977062712
	...
	---
	```
	
	You may ask yourself: the file has an update timestamp in its metadata, so why do we need this? The main use case is to differentiate between refactoring updates and actual note updates. For example, a note can contain a link to a different note that gets renamed. In such cases, the file metadata update date would be increased, but we would want to keep the `updated` date as it was. 
	
</note>
<note name="t.ext.data.type.note.visited" title="Note.visited">
	
	`Note.visited` answers the question: When was the note last visited?
	
	Visited means you navigated to the note and spent more time in the note than the [[t.ext.feature.visit-history.visit-event.min-visitation-threshold]] prior to leaving the note. 
	
	See [[t.ext.feature.visit-history.visit-event]] for more info.
	
	### Relationships
	- [[rel.powered-by]]: **[[t.ext.feature.visit-history]]**
	
	
</note>
<note name="t.ext.data.type.relationship-note" title="Relationship Note">
	
	A special type of note that lives in the `rel.` [[note hierarchy|t.ext.data.type.note.hierarchy]].
	
	### Example of relationship note
	```txt
	rel.depends-on
	```
	
	### Use case: Assigning names to relationships
	![[t.ext.data.type.note-link.type.wiki-link.named]]
</note>
<note name="t.ext.data.type.vault" title="Vault">
	
	A vault is a **folder** located under your [[t.ext.data.type.workspace]] where you store your [[notes|t.ext.data.type.note]] and supporting assets (e.g., images).
	
	To be considered a valid vault, the folder MUST contain a `root.md` file with an id. See [[t.ext.data.type.vault.id]]
	
	<details class="bordered-when-open">
	<summary>Comparison with other software</summary>
	
	#### Like Dendron vault
	Thorg vault is similar to [Dendron Vault](https://wiki.dendron.so/notes/6682fca0-65ed-402c-8634-94cd51463cc4/). 
	
	#### Unlike Obsidian Vault
	However, [Obsidian Vault](https://help.obsidian.md/vault) is more akin to [[Thorg Workspace|t.ext.data.type.workspace]]. 
	</details>
	
	### Vault name
	![[t.ext.data.type.vault.name]]
	
	### Vault Id
	![[t.ext.data.type.vault.id]]
	
	### Relationships
	- [[rel.many-to-many]]:**[[t.ext.data.type.workspace]]**
	  - A vault can be part of multiple workspaces, and a workspace can have multiple vaults.
	
</note>
<note name="t.ext.data.type.vault.id" title="vault Id">
	[vault Id](thorg://notes/d0hjf6wbbrfeiriivbahumm)
	The vault id comes from the [[t.ext.data.type.note.frontmatter.field.id]] of the `root.md` note located directly under your vault folder.
	
	#### Example
	```txt
	YOUR_WORKSPACE_DIR/YOUR_VAULT_1/root.md
	```
	
	
	`YOUR_WORKSPACE_DIR/YOUR_VAULT_1/root.md` contents:
	
	```md
	---
	id: abc123
	---
	```
	
	`abc123` is the **vault id** of `YOUR_VAULT_1`
	
	
</note>
<note name="t.ext.data.type.vault.name" title="Vault Name">
	
	The Thorg vault name is simply the name of the folder under your workspace.
	
	To keep things simple, there is no separate name configuration for the vault.
</note>
<note name="t.ext.data.type.workspace" title="Workspace">
	
	A workspace is a collection of one or more [[t.ext.data.type.vault]]s.
	
	This is a folder containing all the files necessary to manage your information in Thorg.
	
</note>
<note name="t.ext.data.type.workspace.thorg-dir" title="Thorg Workspace Directory ($WORKSPACE/.thorg)">
	
	
	The **Thorg workspace directory (`$WORKSPACE/.thorg`)** resides under your [[t.ext.data.type.workspace]] directory and holds **Thorg-specific files** that are typically shared by default when using shared vaults.
	
	---
	
	### Source Control Guidance
	
	We recommend tracking the `$WORKSPACE/.thorg` directory in source control **with appropriate exclusions**:
	
	When Thorg initializes this directory, it creates the following subdirectories:
	
	- [[t.ext.data.type.workspace.thorg-dir.data]] - ✅ Include in source control.
	- [[t.ext.data.type.workspace.thorg-dir.tmp]] - 🚫 Exclude from source control (Thorg will automatically add a `.gitignore` entry for this folder).
	
	### Thorg-related files outside of `$WORKSPACE/.thorg`
	Thorg stores additional files outside of the workspace/vault. See [[t.ext.file.home-thorg-dir]]
	
	### Related 
	- [[t.ext.data.thorg-view-on-data.transparent-data-model]]
</note>
<note name="t.ext.data.type.workspace.thorg-dir.data" title=".thorg/data">
	
	`.thorg/data`
	
	✅ **Include in source control**.
	
	Contains data and metadata worth versioning.
	
	
	
	
</note>
<note name="t.ext.data.type.workspace.thorg-dir.tmp" title="$WORKSPACE/.thorg/tmp">
	
	`$WORKSPACE/.thorg/tmp`
	
	🚫 **Exclude from source control**.
	
	Used for temporary files.
	
	- Thorg will automatically create a `.gitignore` file inside `.thorg` to ignore `.thorg/tmp`. If you use a different version control system, make sure to **manually exclude** `.thorg/tmp`.
	
	
	### Child dirs
	- [[t.ext.data.type.workspace.thorg-dir.tmp.server]]
	- [[t.ext.data.type.workspace.thorg-dir.tmp.logs]]
	
</note>
<note name="t.ext.data.type.workspace.thorg-dir.tmp.logs" title="$WORKSPACE/.thorg/tmp/logs">
	
	### Description
	Directory where the main logs for this Thorg workspace are stored.
	
	Contains date-based log files from both the server and the client.
	
	### File format
	![[t.ext.data.type.workspace.thorg-dir.tmp.logs.file-format-of-logs]]
</note>
<note name="t.ext.data.type.workspace.thorg-dir.tmp.logs.file-format-of-logs" title="File Format of Log Files">
	
	### Format
	```txt
	<log_type>.<UTC_DATE>.log
	
	# If the logs are rotated within the same date there will be rotation suffix
	<log_type>.<UTC_DATE>.log.[ROTATION_SUFFIX_NUMBER]
	```
	
	### Example
	```txt
	vsc_client.2025_11_12.log
	vsc_client.2025_11_12.log.1
	```
</note>
<note name="t.ext.data.type.workspace.thorg-dir.tmp.server" title="$WORKSPACE/.thorg/tmp/server (directory for temporary server files)">
	
	### Children Directories
	![[t.ext.data.type.workspace.thorg-dir.tmp.server.instance]]
	
</note>
<note name="t.ext.data.type.workspace.thorg-dir.tmp.server.instance" title="$WORKSPACE/.thorg/tmp/server/instance">
	
	Contains files that represent the Thorg server instance for this workspace.
	
	Specifically:
	- `server.pid`: Contains the PID (Process ID) of the Thorg server running for this workspace.
	- `server.port`: Contains the port the Thorg server is using.
</note>
<note name="t.ext.data.type.workspace.thorg-dir.tmp.server.instance.port-file" title="$WORKSPACE/.thorg/tmp/server/instance/server.port">
	
	This file holds the [[t.ext.concept.serverPort]] of the [[t.ext.thorgServer]] that is running for this [[workspace|t.ext.data.type.workspace]].
	
	### Location
	Located at `$WORKSPACE/.thorg/tmp/server/instance/server.port` when a Thorg server instance is running for this workspace.
	
	This file is deleted when the server terminates gracefully.
	
	### How Port is Determined
	The port is dynamically allocated when the Thorg server starts up. The server finds an available port and writes it to this file.
	
	### Related
	- [[t.ext.thorgServer.default-port]]
	
</note>
<note name="t.ext.feature" title="Feature Hierarchy">
	
	Contains descriptions of features that do not fit well into the [[t.ext.command]] hierarchy.
	
	
</note>
<note name="t.ext.feature.visit-history" title="Visit History">
	
	### Summary
	Visit history records your note visitation history per user, tracking where you have been and when. In V1, this enables navigation to recently visited notes. Future iterations of Thorg will use this for more elaborate features.
	
	By default, history is stored under your user directory (only you have access to your visitation history).
	
	### Does not track your brain
	Visit history gives you a good idea of the notes you've opened recently to help filter your search. However, Thorg doesn't track your eyes or your brain -- just keep in mind that we can't guarantee a note visit included an actual read.
	
	### What is a visit event
	![[t.ext.feature.visit-history.visit-event]]
	
	### Visit history file storage
	![[t.ext.feature.visit-history.file]]
	
	### Caveats
	- A visit does not necessarily mean the note was read by the user. The note could have been opened without being read.
</note>
<note name="t.ext.feature.visit-history.file" title="Visit history File">
	
	<div class="centered">
	
	Storage file for [[visit events|t.ext.feature.visit-history.visit-event]]
	</div>
	
	![[t.ext.feature.visit-history.file.content-format]]
	
	![[t.ext.feature.visit-history.file.location]]
	
	
	
</note>
<note name="t.ext.feature.visit-history.file.content-format" title="Visit history file Content Format">
	
	The visit history **file contains the [[note id|t.ext.data.type.note.frontmatter.field.id]]** in the file name. Therefore, we do NOT need to duplicate the note id in the events themselves (see [[t.ext.feature.visit-history.file.location]] for details on file location).
	
	The contents of the visit log file are in compact **text** format with the following structure per line:
	
	### Line Structure
	
	```txt
	<ACTION_TYPE>:<TIMESTAMP_SINCE_EPOCH_IN_MILLIS>
	```
	
	- **ACTION_TYPE**: Has 2 possible values:
	  - `F` - [[t.ext.feature.visit-history.visit-event.FOCUS]] event
	  - `U` - [[t.ext.feature.visit-history.visit-event.UNFOCUS]] event (when you leave the note)
	
	- **TIMESTAMP_SINCE_EPOCH_IN_MILLIS**: The timestamp when the event occurred, in milliseconds since epoch.
	
	### Example content
	```txt
	F:1753911954503
	U:1753911959100
	```
	
	This translates to:
	- `F:1753911954503`: Note was focused at timestamp [1753911954503]
	- `U:1753911959100`: Note lost focus at timestamp [1753911959100]
	
	
	### Stored transparently
	Per [[t.ext.data.thorg-view-on-data.transparent-data-model]], we use a human-readable format to store data in a transparent (non-proprietary) way. We opted away from JSONL to keep files compact while retaining human readability and ease of parsing, so you can see what is being recorded and parse it if you desire.
	
</note>
<note name="t.ext.feature.visit-history.file.location" title="Visit History file Location - (Where visit history data is written to)">
	 
	### Location
	```txt
	$HOME/
	  .thorg/
	    usr/
	      {user_name}/
	        qc/
	         h/
	            v/
	              vid_{vault_id}/
	                {machine_name}/
	                  nid_{note-id}.visit_log
	```
	
	- `$HOME/` - Your user directory.
	- `.thorg/` - Thorg directory under your home folder ([[t.ext.file.home-thorg-dir]]).
	- `usr/` - Stands for split by thorg username.
	- `{user_name}/` - [[t.ext.concept.thorgUsername]]
	- `qc/` - Stands for *quick changing*.
	- `h/` - Folder stands for *history*.
	- `v/` - Folder stands for *visit*.
	- `vid_{vault_id}/` - [[t.ext.data.type.vault.id]]
	- `{machine_name}/` - [[t.ext.concept.machineName]]
	  - Machine name exists to prevent merge conflicts when you share your visit history for the same user across multiple machines.
	- `nid_{note-id}.visit_log` - Visit log for the [[t.ext.data.type.note]], indexed by [[note_id|t.ext.data.type.note.frontmatter.field.id]].
	  - By including the note id in the file name, we avoid storing the note id within the events themselves (see [[t.ext.feature.visit-history.file.content-format]]).
	
	### Recommendation
	![[t.ext.file.home-thorg-dir._.banner-for-descendent-dirs-to-be-backed-up]]
</note>
<note name="t.ext.feature.visit-history.visit-event" title="Visit Event">
	
	#### What are visit events
	Events that power [[t.ext.feature.visit-history]] to answer the question: When did you visit a [[t.ext.data.type.note]] and for how long?
	
	### Two types of Visit Events:
	![[t.ext.feature.visit-history.visit-event.FOCUS]]
	![[t.ext.feature.visit-history.visit-event.UNFOCUS]]
	
	### Where are visit events stored?
	Visit events are stored in [[visit history files|t.ext.feature.visit-history.file]]
	
	### Available configuration of [[t.ext.feature.visit-history]]:
	![[t.ext.configuration.values.visitHistory]]
</note>
<note name="t.ext.feature.visit-history.visit-event.FOCUS" title="FOCUS - Visit Event">
	
	#### What is a FOCUS event?
	`FOCUS`: A [[visit event|t.ext.feature.visit-history.visit-event]] that represents you focusing on the editor view of a particular [[note|t.ext.data.type.note]].
	
	#### When is FOCUS eligible to be persisted?
	![[t.ext.feature.visit-history.visit-event.FOCUS.eligible-for-persistence-when]]
	
	
	#### What is NOT a visit event
	<details class="bordered-when-open">
	<summary>Rapidly jumping in and out of pre-existing note: Not a visit event</summary>
	
	If you jump into a note for less than the [[minimum amount|t.ext.feature.visit-history.visit-event.min-visitation-threshold]] of time (default is a few seconds) and jump out before the minimum time passes, we will NOT record that as a visit event. From the visitation history, it will appear as if you haven't opened that note at all (unless you just created the note).
	
	</details>
	
	<details class="bordered-when-open">
	<summary>Seeing the preview of an embedded note: Not a visit event</summary>
	
	If note-A has note-B [[embedded|t.ext.data.type.note-link.example.embed]] in it and you preview note-A, you will see note-B's contents. However, this is NOT considered a visit to note-B (only a visit to note-A).
	
	You need to navigate to note-B explicitly for it to be considered a visit to note-B.
	</details>
	
	
	#### FOCUS is written to file with UNFOCUS
	<details class="bordered-when-open">
	<summary>FOCUS is persisted to file with UNFOCUS</summary>
	
	A `FOCUS` visit event is persisted into the [[t.ext.feature.visit-history.file]] when its corresponding [[t.ext.feature.visit-history.visit-event.UNFOCUS]] is processed and persisted.
	
	Therefore, if you want your FOCUS event to be persisted (after it has met [[FOCUS eligibility for persistence|t.ext.feature.visit-history.visit-event.FOCUS.eligible-for-persistence-when]]), you need to trigger an UNFOCUS event, which is triggered by:
	
	![[t.ext.feature.visit-history.visit-event.UNFOCUS.triggered-by]]
	</details>
	
</note>
<note name="t.ext.feature.visit-history.visit-event.FOCUS.eligible-for-persistence-when" title="FOCUS eligible for persistence WHEN">
	
	#### For pre-existing notes
	You need to spend more than the [[t.ext.feature.visit-history.visit-event.min-visitation-threshold]] with the note in focus for the [[t.ext.feature.visit-history.visit-event.FOCUS]] to be eligible for persistence.
	
	#### For brand new notes
	FOCUS will be eligible for persistence right away for a newly created note.
</note>
<note name="t.ext.feature.visit-history.visit-event.min-visitation-threshold" title="Min Visitation Time Threshold">
	
	**Min Visitation Threshold**: The amount of time you need to spend focused in a note for it to be recorded as a `FOCUS` [[visit event|t.ext.feature.visit-history.visit-event]] (default: 3 seconds).
	
	**Use case**: Avoid polluting [[t.ext.feature.visit-history]] with rapid `FOCUS` and `UNFOCUS` events when you rapidly iterate through tabs without stopping to do any meaningful interaction with a note.
	
	**Example**: If you rapidly open notes without spending time in them, by default we will NOT record `FOCUS`.
	
	### How to configure 
	See [[t.ext.configuration.values.visitHistory.minVisitationFocusTimeMillis]]
	
	### Overridden on note creation
	![[t.ext.feature.visit-history.visit-event.min-visitation-threshold.overridden-on-note-creation]]
	
</note>
<note name="t.ext.feature.visit-history.visit-event.min-visitation-threshold.overridden-on-note-creation" title="Minimum visitation threshold, Overridden on note creation">
	
	[[t.ext.feature.visit-history.visit-event.min-visitation-threshold]] is NOT taken into account when you create a brand new note. During creation, even if you did NOT spend the time to meet the minimum visitation threshold, we will still record a [[t.ext.feature.visit-history.visit-event.FOCUS]] for the newly created note.
</note>
<note name="t.ext.feature.visit-history.visit-event.UNFOCUS" title="UNFOCUS - Visit Event">
	
	#### What is an UNFOCUS event?
	`UNFOCUS`: A [[visit-event|t.ext.feature.visit-history.visit-event]] that symbolizes loss of focus from a [[t.ext.data.type.note]].
	
	It can only occur after a [[t.ext.feature.visit-history.visit-event.FOCUS]] for the note in question.
	
	#### Triggered by:
	
	![[t.ext.feature.visit-history.visit-event.UNFOCUS.triggered-by]]
</note>
<note name="t.ext.feature.visit-history.visit-event.UNFOCUS.auto-unfocus-due-to-ttl" title="Auto-unfocus: Automatically Records UNFOCUS after a period of inactivity.">
	
	If you open a note and then stop interacting with it, after a period of inactivity we will automatically record an `UNFOCUS` [[visit event|t.ext.feature.visit-history.visit-event]] (default: **180 seconds** of inactivity).
	
	If you keep interacting with a note (including typing, scrolling, or moving the cursor position within the note), we will keep resetting the timer until auto-unfocus occurs.
	
	### How to configure
	[[t.ext.configuration.values.visitHistory.autoUnfocusTtlSeconds]]
</note>
<note name="t.ext.feature.visit-history.visit-event.UNFOCUS.triggered-by" title="UNFOCUS triggered-by">
	
	[[t.ext.feature.visit-history.visit-event.UNFOCUS]] is triggered when you unfocus the editor view of the [[note|t.ext.data.type.note]] that you had in focus. There are two main categories that trigger unfocus:
	
	- **User action:**
	  - Navigating to a different note
	  - Navigating to settings
	  - Focusing on non-editor view of the note (e.g., Dendron preview)
	  - Focusing on a different application (e.g., IntelliJ)
	  - Closing VSCode
	
	- **Prolonged user inaction:**
	  - If you focus on a [[note|t.ext.data.type.note]] editor and then leave it without any actions (not scrolling or changing cursor position) for a period longer than [[t.ext.configuration.values.visitHistory.autoUnfocusTtlSeconds]], we will [[auto-unfocus|t.ext.feature.visit-history.visit-event.UNFOCUS.auto-unfocus-due-to-ttl]].
</note>
<note name="t.ext.file" title="File">
	
	Hierarchy for documenting specific files stored by Thorg.
	
	Much of the file-specific documentation is stored in more specific hierarchies, and this note serves as an index to those hierarchies.
	
	### HOME/.thorg
	![[t.ext.file.home-thorg-dir]]
</note>
<note name="t.ext.file-format.free-mind" title="FreeMind (.mm)">
	
	<details>
	<summary>Advantages of FreeMind format</summary>
	
	The `.mm` file format is associated with FreeMind, a widely-used, open-source mind mapping software. The format is based on XML (eXtensible Markup Language), making it both human-readable and machine-processible. Below are the key characteristics of the `.mm` format and the reasons why it's beneficial for interoperability among various mind mapping tools, especially for outputting notes.
	
	### Characteristics of .mm File Format
	
	1. **XML-based Structure**: The `.mm` format leverages XML to structure data, ensuring a clear hierarchy and relationship among the various elements and nodes in a mind map.
	2. **Textual Content**: Being text-based, it's lightweight and can be edited with basic text editors if needed, although understanding the structure requires familiarity with the format.
	3. **Hierarchical Organization**: Reflects the inherent structure of mind maps, with nodes, sub-nodes, and attributes clearly defined, making it intuitive for representing complex ideas and relationships.
	4. **Metadata Support**: Allows inclusion of metadata such as icons, colors, and links, which can enrich the information and visual appeal of the mind map.
	
	### Advantages for Interoperability
	
	1. **Wide Adoption**: As FreeMind is a popular tool, the `.mm` format has been widely adopted by various mind mapping and note-taking software. This widespread use promotes interoperability.
	2. **Standardized Format**: Being XML-based, it conforms to a standard that many tools can easily parse and understand. This standardization reduces the complexity of converting or importing/exporting data between different software.
	3. **Extensible and Flexible**: New elements or attributes can be added to the `.mm` format without breaking compatibility with existing parsers, allowing for future enhancements and customizations.
	4. **Tool Agnostic**: The format doesn't lock users into a specific tool. You can create a mind map in one application and continue working on it in another that supports the `.mm` format.
	5. **Facilitates Collaboration**: Due to its interoperability, it's easier to collaborate across different platforms and tools. Teams can work on the same mind map using different software that supports the `.mm` format.
	6. **Preserves Visual Elements**: Unlike some formats that only retain textual data, the `.mm` format also keeps visual elements (such as colors, shapes, and icons), ensuring that visual cues important for mind maps are not lost during transitions.
	
	In conclusion, the `.mm` format's XML-based, standardized, and extensible nature makes it a robust choice for mind mapping and note-taking, especially when you need to use or share your notes across different platforms or collaborate with others who might use different software.
	</details>
	
	<details>
	<summary>Downsides of FreeMind Format</summary>
	
	While the `.mm` (FreeMind) file format offers numerous benefits, particularly in terms of interoperability and structure, it does have certain limitations and downsides:
	
	1. **Lack of Rich Media Support**: The most notable limitation is its inability to embed rich media such as images or videos directly within the file. While it can link to external media resources, it cannot store them within the mind map file itself. This can be a significant drawback for users who rely on visual aids or need to include multimedia content for comprehensive note-taking or brainstorming.
	
	2. **Limited Formatting Options**: The `.mm` format, being primarily text-based and structured around XML, doesn't support advanced formatting options. While it can represent basic visual elements like colors and fonts, it falls short in offering rich text capabilities (such as different font styles within a node) that some other proprietary formats provide.
	
	3. **Dependency on External Links**: For including images or other rich media, the format relies on external links. This dependency can lead to broken links or missing content if external resources are moved, renamed, or deleted. It also means the mind map is not entirely self-contained, which can be problematic for portability or when working offline.
	
	4. **Complexity for Manual Editing**: Although the XML-based structure is a strength in terms of standardization and tool interoperability, it can be cumbersome for users who wish to edit the file directly with a text editor. The verbose nature of XML can make manual edits error-prone and less intuitive compared to other formats.
	
	5. **Version Compatibility Issues**: As with many file formats, newer versions of mind mapping software might extend the `.mm` format with additional features or customizations. This can potentially lead to compatibility issues when opening files with older software versions or different applications that may not support the latest extensions.
	
	6. **Lack of Advanced Features**: Some proprietary mind mapping tools offer advanced features like task management, integration with other productivity software, or complex data visualization options. The `.mm` format, while sufficient for basic and intermediate mind mapping needs, may not fully support these advanced functionalities.
	
	In summary, while the `.mm` file format is excellent for basic mind mapping and ensures interoperability across different platforms, its limitations in handling rich media, advanced formatting, and more complex features might make it less suitable for users who require these capabilities in their note-taking or mind mapping activities.
	</details>
	
	
</note>
<note name="t.ext.file.home-thorg-dir" title="$HOME/.thorg (Directory)">
	
	Documentation of files stored in the `$HOME/.thorg` directory. Contains user-specific files.
	
	### Highlighted Files Under $HOME/.thorg
	- [[t.ext.file.home-thorg-dir.usr.username-dir]]
	  - [[t.ext.feature.visit-history.file.location]]
	- [[t.ext.file.home-thorg-dir.not-under-scm]] - Recommended to be outside of source control. Automatically excluded from Git. 
	
	### Recommendation
	- [[t.ext.file.home-thorg-dir.back-up-this]]
	
</note>
<note name="t.ext.file.home-thorg-dir._.banner-for-descendent-dirs-to-be-backed-up" title="As descendent of $HOME/.thorg: Recommended to be backed up.">
	
	Per [[t.ext.file.home-thorg-dir.back-up-this]], this directory is a descendant of `$HOME/.thorg` and is recommended to be under source control.
	
	If you're already backing up (e.g., source controlling) `$HOME/.thorg`, then this directory is already backed up as well as a descendant of `$HOME/.thorg`. If not, it's highly recommended to backup/source control `$HOME/.thorg` per [[t.ext.file.home-thorg-dir.back-up-this]].
	
</note>
<note name="t.ext.file.home-thorg-dir.back-up-this" title="Back up $HOME/.thorg">
	
	### Recommended: Back Up $HOME/.thorg
	It's recommended to back up `$HOME/.thorg` (e.g., via source control), which includes your [[visitation history|t.ext.feature.visit-history]]. This allows you to retain this history for later exploration and share it across machines.
	
	### Tip: Ready to Share Across Machines and Users
	By default, files in `$HOME/.thorg` (including [[visit history|t.ext.feature.visit-history]]) are completely **private** and outside the vault (relevant if you share vaults with other people). However, while these files are private, they're also designed to be shared across multiple machines and multiple users.
	
	For example, rapidly changing files such as [[visit history files|t.ext.feature.visit-history.file.location]] are structured so they can be shared across multiple users and across multiple machines under a single user **without causing Git merge conflicts**.
	
	Therefore, once you backup/source-control `$HOME/.thorg`, you can share it with yourself across multiple machines or even with other users.
	
	### If You Aren't Using Git
	If you are using Git, this directory will contain an auto-populated `.gitignore`. If you aren't using Git, refer to [[t.ext.file.home-thorg-dir.gitignore]] for information on what is recommended to ignore.
</note>
<note name="t.ext.file.home-thorg-dir.gitignore" title="$HOME/.thorg/.gitignore">
	
	Documentation for the `.gitignore` file in [[t.ext.file.home-thorg-dir]]
	
	### What We Will Auto-Ignore:
	- [[t.ext.file.home-thorg-dir.not-under-scm]]
	
</note>
<note name="t.ext.file.home-thorg-dir.not-under-scm" title="$HOME/.thorg/not-under-scm">
	
	
	**$HOME/.thorg/not-under-scm Directory**
	
	This directory stores user data, logs, and configuration files that should NOT be tracked by source control management systems.
	
	### Automatic Git Integration
	
	The directory is automatically excluded via [[t.ext.file.home-thorg-dir.gitignore]]. This means you can use Git to version control your `$HOME/.thorg` directory without including the contents of `not-under-scm` in your repository history.
	
	### Child Directories
	- [[t.ext.file.home-thorg-dir.not-under-scm.logs]]
	- [[t.ext.file.home-thorg-dir.not-under-scm.generated-reports]]
</note>
<note name="t.ext.file.home-thorg-dir.not-under-scm.combined-logs" title="$HOME/.thorg/not-under-scm/combined-logs">
	
	Directory where thorg will combined logs in for user to submit issues.
</note>
<note name="t.ext.file.home-thorg-dir.not-under-scm.generated-reports" title="$HOME/.thorg/not-under-scm/generated-reports">
	
	Directory to contain reports that are generated by Thorg.
	
	### Child directories
	- [[t.ext.file.home-thorg-dir.not-under-scm.generated-reports.error-reports]]
</note>
<note name="t.ext.file.home-thorg-dir.not-under-scm.generated-reports.error-reports" title="$HOME/.thorg/not-under-scm/generated-reports/error-reports">
	
	Directory to contain error reports.
	
</note>
<note name="t.ext.file.home-thorg-dir.not-under-scm.logs" title="$HOME/.thorg/not-under-scm/logs">
	
	This directory contains pre-startup logs and backup logs. The main log location for the running Thorg instance is under the workspace at [[t.ext.data.type.workspace.thorg-dir.tmp.logs]].
	
	### Format of logs
	![[t.ext.data.type.workspace.thorg-dir.tmp.logs.file-format-of-logs]]
</note>
<note name="t.ext.file.home-thorg-dir.usr.username-dir" title="Thorg Username Directory">
	
	### What Is It
	Directory containing files specific to the user delineated by [[t.ext.concept.thorgUsername]].
	
	This includes rapidly changing files that users may want to keep to themselves or potentially share with others (e.g., [[t.ext.feature.visit-history]] files).
	
	### Where Is It Located
	Located at `$HOME/.thorg/usr/${THORG_USERNAME}`.
	
	### Child Directories
	- [[t.ext.file.home-thorg-dir.usr.username-dir.qc]] - contains files that change often (e.g., [[t.ext.feature.visit-history]] related files)
	
	
	### Recommendation
	![[t.ext.file.home-thorg-dir._.banner-for-descendent-dirs-to-be-backed-up]]
	
	
</note>
<note name="t.ext.file.home-thorg-dir.usr.username-dir.qc" title="qc/ (quick changing)">
	
	### Contains:
	- [[Visit history files|t.ext.feature.visit-history.file.location]]
</note>
<note name="t.ext.file.log-paths" title="Log Paths">
	
	![[t.ext.data.type.workspace.thorg-dir.tmp.logs]]
	
	![[t.ext.file.home-thorg-dir.not-under-scm.logs]]
	
	![[t.ext.file.log-paths.log-back-up-file-when-we-fail-to-log]]
	
	
	
</note>
<note name="t.ext.file.log-paths.log-back-up-file-when-we-fail-to-log" title="Log Back up File When We Fail to Log">
	
	File in [[t.ext.file.home-thorg-dir.not-under-scm.logs]] for storing logging failures.
	
	See anchor point for the file path.
</note>
<note name="t.ext.general.how-to-find-out-who-is-listening-on-port-and-shut-it-down-linux-mac" title="How to Find Out Who Is Listening on Port and shut it down (Linux & Mac)">
	
	
	Finding out which process is listening on a given port is quite useful.
	
	You can do this with the following commands (using port 7567 as an example).
	
	## Linux & macOS
	
	```bash
	# `-i` selects by internet address; `:PORT` filters by port number.
	# 
	# Note: On Linux, you may need `sudo` to see process names for ports owned by other users.
	lsof -i :7567
	```
	
	You should get output like:
	
	```txt
	COMMAND   PID               USER   FD   TYPE DEVICE SIZE/OFF NODE NAME
	java    21564 nickolaykondratyev  216u  IPv6  10185      0t0  TCP localhost:7567 (LISTEN)
	```
	
	**PID** is the [Process Identifier](https://en.wikipedia.org/wiki/Process_identifier). In the example above, the PID is 21564.
	
	You can use the PID to shut down the process:
	
	### Graceful shutdown
	
	```bash
	# SIGTERM tells the app to shut down gracefully, allowing it to
	# execute cleanup code and close resources properly.
	# 
	# After sending this signal, allow some time for the app to finish
	# before resorting to SIGKILL.
	kill -SIGTERM 21564
	```
	
	### Forceful shutdown
	
	```bash
	# SIGKILL immediately terminates the process without allowing
	# any cleanup code to run. Use as a last resort.
	kill -SIGKILL 21564
	```
	
</note>
<note name="t.ext.guide.getting-started.from-dendron" title="Guide: Getting started Coming From Dendron">
	
	Thorg aims to work smoothly for those coming from Dendron.
	
	Thorg looks for the `dendron.yml` file to identify the workspace and performs its [[t.ext.data.type.workspace.thorg-dir]] setup right next to it.
	
	After installing Thorg, open your Dendron workspace and look for the Thorg activation message.
	
	### Callouts
	![[t.ext.guide.getting-started.from-dendron.callout]]
	
	
</note>
<note name="t.ext.guide.getting-started.from-dendron.callout" title="Dendron Compatibility Callouts">
	
	<details class="bordered">
	<summary>Vault names come solely from the vault's folder name</summary>
	
	![[t.ext.guide.getting-started.from-dendron.callout.vault-name-is-not-read-from-dendron-yaml]]
	</details>
	
	
</note>
<note name="t.ext.guide.getting-started.from-dendron.callout.vault-name-is-not-read-from-dendron-yaml" title="Vault Name Is Not Read from Dendron Yaml">
	
	
	Vault names are **now derived solely from the vault's folder name** and are **no longer** read from `dendron.yml`. (See [[t.ext.data.type.vault.name]])
	
	Most users won't be affected by this change, as vault names usually already match their corresponding folder names. However, if the `name` property in your `dendron.yml` configuration doesn't match your vault's folder name, an adjustment is needed for smooth operation with Thorg.
	
	### How to Adjust (Both Adjustments Are Needed):
	<details class="bordered-when-open">
	<summary>Adjusting Your Vault's Name in dendron.yml</summary>
	
	Open your `dendron.yml` file (found at the workspace level). You will see a vault configuration similar to this:
	
	```yaml
	workspace:
	    vaults:
	        -
	            fsPath: vault-2
	            name: second-vault
	```
	
	To resolve the mismatch, you have two options:
	1. Rename the `name` property to explicitly match the `fsPath` (the vault's folder name).
	2. Delete the `name` property entirely.
	
	#### Desired `dendron.yml` Configuration Examples:
	
	```yaml
	workspace:
	    vaults:
	        -
	            fsPath: vault-2
	            name: vault-2
	```
	
	OR simply delete the name property:
	
	```yaml
	workspace:
	    vaults:
	        -
	            fsPath: vault-2
	```
	</details>
	
	
	<details class="bordered-when-open">
	<summary>Adjusting Name in Your VS Code Workspace File (.code-workspace)</summary>
	
	Your VS Code workspace file (e.g., `dendron.code-workspace`) might also contain `name` properties for your vaults under the `folders` array.
	
	Locate your `.code-workspace` file (usually at the workspace root) and find entries similar to this:
	
	```json
	{
	    "folders": [
	        {
	            "path": "vault-2",
	            "name": "second-vault"
	        },
	        // ... other folders
	    ],
	    // ... rest of the config
	}
	```
	
	To achieve consistency, you have two options:
	1. Rename the `name` property to explicitly match the `path` (the folder name).
	2. Delete the `name` property entirely.
	
	#### Desired `.code-workspace` Configuration Examples:
	
	```json
	{
	    "folders": [
	        {
	            "path": "vault-2",
	            "name": "vault-2"
	        },
	        // ...
	    ]
	}
	```
	
	OR
	
	```json
	{
	    "folders": [
	        {
	            "path": "vault-2"
	        },
	        // ...
	    ]
	}
	```
	</details>
	
</note>
<note name="t.ext.how-to.install-thorg" title="Install Thorg">
	
	### Pre-Requisites
	
	- You use **MacOS** or **Linux** (No Windows support yet)
	  - If you would like us to prioritize adding Windows support, vote [[here|t.ext.contact-us.submit-git-hub-issue.highlighted-known-issue.no-windows-support-yet]]
	
	<details class="bordered-when-open">
	<summary>You currently use Dendron</summary>
	
	- Why: We are working to fill the gaps to make Thorg run standalone, but right now we rely on Dendron for some functionality that Thorg has not exposed yet (such as note creation).
	</details>
	
	<details class="bordered-when-open">
	<summary>You have a few hundred megabytes of RAM to spare</summary>
	
	- Why: We run a JVM service [[t.ext.thorgServer]] to power Thorg's functionality. This enables more advanced search filtering commands like [[t.ext.command.search.quick.in-subtree.visited-since]].
	- By default, Thorg server starts with 1GB allocated to Java max heap space. You can lower this in the configuration (see [[t.ext.configuration.values.startupSetup.serverMaxHeapSpaceMB]]).
	  - Note: We have successfully run a 10,000 note test workspace (with 80MB of notes) with only 512MB max heap allocated.
	  - Also note that while the default max heap space is set to 1GB, this does not mean JVM/ThorgServer will use the full 1GB—it can operate with much less RAM.
	</details>
	
	
	### Installation steps
	- Download the latest Thorg release from S3 (Or if required due to an issue see: [[t.ext.how-to.install-thorg.previous-releases]])
	![[t.ext.how-to.install-thorg.latest-release]]
	
	- Then follow the steps on [[t.ext.how-to.install-thorg.how-to-install-VSIX-file]]
	
	
</note>
<note name="t.ext.how-to.install-thorg.how-to-install-VSIX-file" title="how-to-install-VSIX-file to VSCode">
	
	There are two ways to install the VSIX file that you downloaded as part of [[t.ext.how-to.install-thorg]]
	
	### Using UI
	![](./assets/submodule/for_external/Screenshot-2025_11_26T13_23_13.png){max-width: 500px, display: block, margin: 0 auto, border: 5px solid black}
	
	Then choose the VSIX file that you downloaded as part of [[t.ext.how-to.install-thorg]].
	
	
	### Using CLI
	```bash
	code --install-extension $thorg-downloaded-vsix-file
	```
	
	[Reference: VSCode documentation](https://code.visualstudio.com/docs/editor/extension-marketplace#_install-from-a-vsix)
</note>
<note name="t.ext.how-to.install-thorg.latest-release" title="Latest Thorg Release">
	
	Latest Thorg release in S3: **[Thorg VSIX v0.1.0](https://thorg-public-releases.s3.us-west-1.amazonaws.com/vsix/thorg-vscode-0.1.0.vsix)**
	
</note>
<note name="t.ext.how-to.install-thorg.previous-releases" title="Previous Thorg Releases">
	
	- [Thorg VSIX v0.1.0](https://thorg-public-releases.s3.us-west-1.amazonaws.com/vsix/thorg-vscode-0.1.0.vsix)
</note>
<note name="t.ext.message-from-app" title="Message from App">
	
	Hierarchy to hold links to be used for messages from the app.
	
</note>
<note name="t.ext.message-from-app.thorg-activated" title="Thorg Activated">
	
	<div class="centered">
	
	Great! Thorg activated!
	</div>
	
	For general documentation of Thorg, start from [[here|t]].
	
	And make sure to checkout highlighted commands:
	
	![[t.ext._.highlighted-commands]]
	
	
</note>
<note name="t.ext.pkm.dendron" title="Dendron">
	
	<div class="centered">
	
	https://wiki.dendron.so/
	</div>
</note>
<note name="t.ext.pkm.obsidian" title="Obsidian">
	
	<div class="centered">
	
	https://obsidian.md/
	</div>
</note>
<note name="t.ext.search.concept.matchType" title="matchType">
	
	
	**Concept: matchType**
	
	### Purpose
	The `matchType` differentiates the source of matches when multiple queries are issued to the index for the same user-provided query. This is particularly useful in scenarios where an initial keyword-based query is followed by a more permissive wildcard-based query if the keyword search returns too few results.
	
	### Key Values
	
	#### Search Related
	- **Keyword Match (`SEARCH_KEYWORD`)**: Results that were directly matched using exact terms as provided by the user.
	- **Wildcard Match (`SEARCH_WILDCARD`)**: Results that were matched using wildcard queries, which are more flexible but typically slower.
	
	#### Lookup Related
	- **`LOOKUP_WILDCARD`**: Results that were retrieved using wildcard lookup.
	
	### Use Case
	In a search system where users may input partial terms (e.g., "inst" instead of "instructions"), the system initially attempts to find matches using exact terms (keyword search). If this initial search yields fewer than a certain number of results, a secondary, broader search using wildcards is conducted. The `matchType` enum allows the system to label each result with the method used to obtain it.
	
	
	
</note>
<note name="t.ext.search.concept.scoreDetail" title="scoreDetail">
	
	Structure containing the details of the match score for a result in a search or lookup query.
	
	### Related
	<details class="bordered-when-open">
	<summary>matchType</summary>
	
	![[t.ext.search.concept.matchType]]
	</details>
	
</note>
<note name="t.ext.search.concept.secondary-query" title="Secondary Query">
	
	A more permissive query issued after the exact search match.
	
	### Use Case
	In a search system where users may input partial terms (e.g., "inst" instead of "instructions"), the system initially attempts to find matches using exact terms (keyword search). If this initial search yields fewer than a certain number of results, a secondary, broader search using wildcards is conducted. The `matchType` enum allows the system to label each result with the method used to obtain it.
	
	### Relationships
	- [[t.ext.search.concept.matchType]]
</note>
<note name="t.ext.search.concept.visitedDateSortThreshold" title="Visited Date Sort Threshold">
	
	**Concept: Visit Date Sort Threshold**
	
	### Purpose
	The `visitedDateSortThreshold` concept refines search result relevance by re-sorting notes with similar match scores based on their last visited date ([[t.ext.data.type.note.visited]]). This ensures that recently visited notes are prioritized within groups of closely matched results.
	
	### Key Idea
	
	- **Threshold-Based Grouping:**
	  Search results are grouped if their match scores fall within a defined similarity threshold. This allows grouping notes with nearly identical relevance scores.
	
	- **Visited Date Sorting:**
	  Within each group of similar scores, notes are further sorted by their last visited date, ensuring that the most recently viewed notes appear higher in the results.
	
	### Use Case
	This concept is valuable when dealing with search results that have close match scores.
	
	### Example
	Consider a scenario where 4 notes have the following match scores and visit dates:
	
	- Note A: Score = 2.0, visited on = 2023-09-01
	- Note B: Score = 0.9, visited on = 2023-09-02
	- Note C: Score = 0.95, visited on = 2023-09-03
	- Note D: Score = 0.5, visited on = 2023-09-04
	
	Let's say we have `visitedDateSortThreshold` set to 0.1. Therefore, notes with match scores within 0.1 difference are eligible for re-sorting based on visit date.
	
	In this example, the search response will be:
	
	1. Note A (least recent visit but highest match score)
	2. Note C (most recent visit out of B, C)
	3. Note B
	4. Note D (most recent visit but low match score)
	
	
	
	
	
	
</note>
<note name="t.ext.startup" title="Startup">
	
	- [[t.ext.startup.finding-workspace]] - How Thorg finds the workspace on each startup
	- [[t.ext.startup.first-startup]] - Information on Thorg's first startup and initial setup
</note>
<note name="t.ext.startup.finding-workspace" title="Finding Workspace - How thorg determines workspace directory">
	
	On startup, Thorg needs to find your [[t.ext.data.type.workspace]] directory.
	
	The workspace directory is expected to be somewhere up the file hierarchy from the starting paths.
	
	The starting paths are determined as follows:
	
	```txt
	Starting paths are:
	  IF vscode.workspace.workspaceFolders is NOT empty
	    vscode.workspace.workspaceFolders
	  ELSE
	    path-of-the-file-you-have-opened
	  END-IF
	```
	
	### For now we use `dendron.yml` to find the workspace directory
	Thorg walks up the parent file chain and looks for a `dendron.yml` file to identify the workspace directory.
	
	### In the near future we will use the .thorg directory to find the workspace
	In the near future, we'll primarily identify the workspace using the [[t.ext.data.type.workspace.thorg-dir]] directory (while continuing to support onboarding based on `dendron.yml`).
</note>
<note name="t.ext.startup.first-startup" title="Thorg Initial Startup">
	
	On initial startup, Thorg presents a setup wizard that requests the following information. Expand the sections below to learn more about each item.
	
	<details class="collapsible-with-transcluded-reference">
	<summary>Thorg Username</summary>
	
	![[t.ext.concept.thorgUsername]]
	</details>
	
	<details class="collapsible-with-transcluded-reference">
	<summary>Machine Name</summary>
	
	![[t.ext.concept.machineName]]
	</details>
	
	<details class="collapsible-with-inline-text">
	<summary>Whether to auto-install Java (JRE)</summary>
	
	On startup, you'll be asked whether to auto-install the JRE.
	
	The recommendation is to let Thorg auto-install a JRE. This ensures you have a stable path to the JRE that [[t.ext.thorgServer]] can run on.
	
	If you decide to provide your own path to the JRE, that's fine too. However, if the path changes (for example, if you update the JRE and it's installed to a slightly different path), Thorg will ask you to re-provide the path on its next startup.
	</details>
	
	
	
</note>
<note name="t.ext.startup.required-java-version" title="Thorg requires Java Version 21+">
	
	Thorg requires <span class="large">Java version **21+**</span> to function.
	
	Note: If you use the Thorg startup UI and choose to manually input the Java path, it will automatically check the version of the Java executable you've entered.
	
	### How to
	- [[t.ext.startup.required-java-version.how-to-check-version]]
</note>
<note name="t.ext.startup.required-java-version.how-to-check-version" title="How to Check Your Java Version">
	
	<details class="bordered">
	<summary>On Unix-like systems (MacOS, Linux)</summary>
	
	![[t.ext.startup.required-java-version.how-to-check-version.unix-like]]
	</details>
	
	
	<details class="bordered">
	<summary>On Windows</summary>
	
	![[t.ext.startup.required-java-version.how-to-check-version.windows]]
	</details>
	
	
</note>
<note name="t.ext.startup.required-java-version.how-to-check-version.interpret-output" title="Interpret Output">
	
	
	## Interpreting the Output
	
	After running the command, you'll see output similar to the examples below. The exact details will vary based on your Java installation.
	
	#### Java 21 example output
	```txt
	Picked up JAVA_TOOL_OPTIONS: -Dkotlinx.coroutines.debug
	openjdk 21.0.9 2025-10-21 LTS
	OpenJDK Runtime Environment Temurin-21.0.9+10 (build 21.0.9+10-LTS)
	OpenJDK 64-Bit Server VM Temurin-21.0.9+10 (build 21.0.9+10-LTS, mixed mode, sharing)
	```
	
	Note: [[t.ext.startup.required-java-version]]
	
	### Other version examples
	<details>
	<summary>Java 11 example output</summary>
	
	#### Java 11 example
	```txt
	openjdk version "11.0.12" 2021-07-20
	OpenJDK Runtime Environment (build 11.0.12+7-post-Debian-2)
	OpenJDK 64-Bit Server VM (build 11.0.12+7-post-Debian-2, mixed mode, sharing)
	```
	</details>
	
	<details class="bordered-when-open">
	<summary>Java 8 example output</summary>
	
	#### Java 8 example
	```txt
	java version "1.8.0_291"
	Java(TM) SE Runtime Environment (build 1.8.0_291-b10)
	Java HotSpot(TM) 64-Bit Server VM (build 25.291-b10, mixed mode)
	```
	</details>
	
	
	
	
</note>
<note name="t.ext.startup.required-java-version.how-to-check-version.unix-like" title="How to check Java version on Unix Like OS (Linux, MacOS)">
	
	<div class="bordered">
	
	1.  **Open a Terminal:**
	    *   **Linux:** Usually `Ctrl+Alt+T`, or find "Terminal" in your applications menu
	    *   **macOS:** Open "Terminal" (find it via Spotlight search or in Applications > Utilities)
	
	2.  **Run the command:**
	    *   In the terminal window, type the following command and press Enter:
	        ```bash
	        java -version
	        ```
	
	</div>
	
	![[t.ext.startup.required-java-version.how-to-check-version.interpret-output]]
</note>
<note name="t.ext.startup.required-java-version.how-to-check-version.windows" title="How to check Java Version On Windows">
	
	
	
	<div class="bordered">
	
	<div class="centered">
	
	[[t.ext.contact-us.submit-git-hub-issue.highlighted-known-issue.no-windows-support-yet]]
	</div>
	
	1.  **Open Command Prompt or PowerShell:**
	    *   Search for "cmd" or "PowerShell" in the Windows search bar and open the application
	
	2.  **Run the command:**
	    *   In the terminal window, type the following command and press Enter:
	        ```bash
	        java -version
	        ```
	
	</div>
	
	![[t.ext.startup.required-java-version.how-to-check-version.interpret-output]]
</note>
<note name="t.ext.thorgServer" title="thorgServer">
	
	Thorg Server is a server written in Kotlin that runs on the JVM. It contains the core logic that powers Thorg functionality.
	
	When the Thorg VSCode extension starts, it will start this server on [[t.ext.concept.serverPort]] if there isn't already a Thorg Server running for the [[workspace|t.ext.data.type.workspace]].
</note>
<note name="t.ext.thorgServer.default-port" title="Default Thorg server port: 7567">
	
	<div class="centered">
	
	The default port for Thorg Server is `7567`
	</div>
	
</note>
<note name="t.ext.thorgServer.how-to" title="Thorg Server How-to">
	
	- [[t.ext.thorgServer.how-to.restart]]
</note>
<note name="t.ext.thorgServer.how-to.restart" title="How to Restart Thorg Server">
	
	To restart Thorg Server, you need to reload VSCode:
	
	![[t.ext.vscode.how-to.reload]]
	
	When VSCode reloads, it will restart the Thorg extension and [[t.ext.thorgServer]] with it.
</note>
<note name="t.ext.tip" title="Tip">
	
	Tips that are Thorg-specific as well as general productivity tips.
	
	See child notes for specific topics.
</note>
<note name="t.ext.tip.keyboard.get-rid-of-caps-lock" title="Get Rid of Caps Lock - And Remap it to CTRL">
	
	TLDR: Remap `CAPS LOCK` to act as `CTRL`.
	
	### Why do this?
	`CAPS LOCK` occupies valuable space on the home row, making it ergonomically accessible. In professional settings, you rarely need to YELL for a prolonged period. The times you need all-caps text (primarily for LLM agent prompts) are minimal compared to how often you use `CTRL` shortcuts. Therefore, it's a worthwhile tradeoff to give up `CAPS LOCK` entirely (just use Shift for capital letters) in favor of having `CTRL` in a more accessible location.
	
	With the default `CTRL` placement, taking `CTRL+<SomeLetter>` shortcuts requires awkward hand positioning. Remapping `CAPS LOCK` to `CTRL` makes shortcuts much easier to use.
	
	### Why not swap them?
	Swapping is an option that can be done after you've become accustomed to using CTRL where CAPS LOCK used to be. However, it's NOT recommended initially, as your muscle memory will default to the previous CTRL position. It takes time for your muscle memory to adjust to ALWAYS use the newly placed CTRL in its **rightful place on the home row**.
	
	### How to do this?
	- [Mac - Change the behavior of the modifier keys](https://support.apple.com/zh-sg/guide/mac-help/mchlp1011/mac)
	- Linux: Ask Claude/GPT how to do it for your distribution.
	- [Windows - Using PowerToys](https://superuser.com/a/1554452/1077967)
	  - NOTE: [[⚠️Thorg does NOT support Windows Yet⚠️|t.ext.contact-us.submit-git-hub-issue.highlighted-known-issue.no-windows-support-yet]]
</note>
<note name="t.ext.tip.note-naming" title="Note Naming Tips">
	
	Tips for naming notes (see [[t.ext.data.type.note.name]]):
	
	- **Keep top-level hierarchy items short** and expand naming as you go deeper.
	  - This is currently necessary due to VSCode quick pick limitations, which require truncating search results. See [[t.ext.configuration.values.visualPreferences.vsc_quickPick_maxLabelLength]] to adjust the truncation length.
	
	- **Use singular naming for all notes**, including parent notes that contain groups or lists. While plural naming works technically (similar to namespace design in code), singular naming creates a more visually cohesive and readable structure throughout your system.
	  - Examples:
	    - Use "Project" instead of "Projects" for a parent note containing multiple projects
	    - Use "Task" instead of "Tasks" for a note grouping several tasks
	  - Concrete example:
	    - ✅ `tech.bash.lang.shell-variable.RANDOM`
	    - ❌ `tech.bash.lang.shell-variables.RANDOM`
	
	- **Don't overthink it**. You can refactor later when you have more context.
	
	
	
</note>
<note name="t.ext.tip.recommended-plugin" title="Recommended Plugin">
	
	Recommended plugins to add (besides Thorg, of course).
	
	<details>
	<summary>Dendron - Essential for Thorg in Alpha</summary>
	
	![[t.ext.tip.recommended-plugin.dendron]]
	</details>
	
	<details>
	<summary>Spell Checker - Avoid making spelling mistakes</summary>
	
	![[t.ext.tip.recommended-plugin.spell-checker]]
	</details>
	
	<details>
	<summary>Markdown all in one - Make markdown editing feel more natural in VSCode</summary>
	
	![[t.ext.tip.recommended-plugin.markdown-all-in-one]]
	</details>
	
	<details>
	<summary>Jumpy - Keyboard driven navigation within your markdown to exact words</summary>
	
	![[t.ext.tip.recommended-plugin.jumpy]]
	</details>
	
	
	
	
</note>
<note name="t.ext.tip.recommended-plugin.dendron" title="Dendron">
	
	<div class="centered">
	
	[Dendron](https://marketplace.visualstudio.com/items?itemName=dendron.dendron)
	</div>
	
	### Why?
	For the Alpha release of Thorg, Dendron is a MUST. Thorg complements features that Dendron lacks, while Thorg does not yet function fully as a standalone tool.
	
	
	
</note>
<note name="t.ext.tip.recommended-plugin.jumpy" title="Jumpy">
	
	<div class="centered">
	
	[vscode-jumpy](https://marketplace.visualstudio.com/items?itemName=wmaurer.vscode-jumpy)
	</div>
	
	### Why?
	Enables keyboard-driven navigation to exact words within your markdown files (without using the mouse).
</note>
<note name="t.ext.tip.recommended-plugin.markdown-all-in-one" title="Markdown All in One">
	
	<div class="centered">
	
	[Markdown all in one](https://marketplace.visualstudio.com/items?itemName=yzhang.markdown-all-in-one)
	</div>
	
	### Why?
	Provides useful shortcuts to make working with markdown in VSCode feel much more natural.
</note>
<note name="t.ext.tip.recommended-plugin.spell-checker" title="Spell Checker">
	
	
	<div class="centered">
	
	[Spell Checker](https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker)
	</div>
	
	### Why?
	Helps you avoid simple spelling mistakes.
</note>
<note name="t.ext.tip.thorg.one-workspace-multiple-vaults" title="Recommendation: One Workspace-Multiple Vaults. Instead of multi-workspace">
	
	**Recommendation:** Use one [[t.ext.data.type.workspace]] with multiple [[vaults|t.ext.data.type.vault]].
	
	**Not Recommended:** Running multiple [[t.ext.data.type.workspace]] instances (which requires multiple [[t.ext.thorgServer]] instances).
	
	**Why multiple workspaces are not recommended:**
	
	This approach is typically unnecessary. The recommendation is to run a single workspace containing all your [[vaults|t.ext.data.type.vault]]. Running multiple workspaces has drawbacks:
	
	1) **Resource overhead:** Requires multiple separate instances of [[t.ext.thorgServer]], consuming more system resources.
	
	2) **Navigation difficulty:** You must remember which VS Code window is running which workspace, making quick navigation between apps cumbersome.
	
	**Better approach:**
	
	Use one [[t.ext.data.type.workspace]] containing multiple [[vaults|t.ext.data.type.vault]]. Organize information using [[hierarchies|t.ext.data.type.note.hierarchy]], then leverage tools like [[t.ext.command.search.quick.in-subtree.all]] to search within specific hierarchies.
</note>
<note name="t.ext.tip.vscode.assign-shortcut-to-open-a-frequent-file" title="Assign Shortcut to Open a Frequently Visited File - Navigate to Exact Note.">
	
	<div class="llm-tag">
	
	#llm.claude-opus-4
	</div>
	
	To create a keyboard shortcut to open a specific frequently visited file without searching:
	
	1. [[Open keybindings.json|t.ext.vscode.how-to.change-your-keybindings-json]]
	2. Add the following command with the path to your file:
	```json
	[
	  {
	    "key": "ctrl+alt+1",
	    "command": "vscode.open",
	    "args": "/absolute/path/to/your/frequently-visited-note.md"
	  }
	]
	```
	
	<details class="bordered-when-open">
	<summary>Note: Use absolute paths</summary>
	
	**Important:** Relative paths have not been reliable so far. Using **absolute paths** has worked well. For example:
	- Windows: `"C:/Users/YourName/projects/myfile.js"`
	- Mac/Linux: `"/home/username/projects/myfile.js"`
	</details>
	
	
	####  Related Use Cases
	- **Using hot-keyed files with search commands**: Combine this with [[t.ext.command.search.quick.in-subtree.all]] or [[t.ext.command.search.quick.in-subtree.visited-since]] by assigning a shortcut to an [[ancestor note|t.ext.data.type.note.ancestor-note]] in the [[note hierarchy|t.ext.data.type.note.hierarchy]]. This lets you quickly search within a particular note hierarchy from anywhere in your workspace.
	
	
	#### For Searchability
	<details class="bordered-when-open">
	<summary>For Searchability</summary>
	
	hot files shortcut hot key
	</details>
	
</note>
<note name="t.ext.tip.vscode.import-obsidian-to-dendron-thorg-format" title="Import Obsidian to Dendron/Thorg Format">
	
	<div class="centered xxlarge">
	
	[obsidian-dendron-importer](https://github.com/luisabellan/obsidian-dendron-importer)
	</div>
	
	Community created plugin to import Obsidian notes into Dendron/Thorg format.
	
	> A VS Code extension for Dendron to import notes from Obsidian vault with automatic conversion from folder structure to dot-notation hierarchy
	
</note>
<note name="t.ext.tip.vscode.sane-git-copilot-configuration" title="Sane Git Copilot Configuration (for Markdown)">
	
	[GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot) is a convenient way to enable AI assistance in VSCode.
	
	However, we do NOT recommend enabling automatic inline suggestions in your markdown files.
	
	<div class="central-tech-thought-centered">
	
	Remember: Writing is thinking.
	</div>
	
	When AI automatically suggests how to finish non-obvious sentences, it can **disrupt your train of thought**. However, using AI to finish obvious sentences can provide a helpful productivity boost (and reduce finger strain).
	
	To get the best of both worlds: enable GitHub Copilot (or your preferred AI assistant), **but** configure it to only show suggestions when you **explicitly** request them. This way, you gain productivity benefits without interrupting your writing (and thinking) process.
	
	
	### PreReqs
	[Set up GitHub Copilot in VS Code](https://code.visualstudio.com/docs/copilot/setup)
	
	### How to Configure GitHub Copilot to Only Show Suggestions When You Request Them
	
	#### Disable Automatic Inline Suggestions in Markdown
	- Go to settings.
	- In your settings, look for:
	```txt
	github.copilot.enable
	```
	- Under `github.copilot.enable` configuration, set `markdown:false`
	
	![img](./assets/images/Screenshot_2025-06-05_at_10.13.04 AM.png){max-width: 500px, display: block, margin: 0 auto, border: 5px solid black}
	
	#### Add Shortcut for Inline Suggestions
	In your keyboard shortcuts, look for:
	
	```txt
	editor.action.inlineSuggest.trigger
	```
	
	Assign an easy-to-use shortcut (I use `CTRL+J CTRL+K` to stay on the home row).
	
	![img](./assets/images/Screenshot_2025-06-05_at_10.17.23 AM.png){max-width: 500px, display: block, margin: 0 auto, border: 5px solid black}
	
	
	### Related
	- [[t.ext.tip.keyboard.get-rid-of-caps-lock]]
</note>
<note name="t.ext.tip.vscode.source-control.your-keybindings" title="Source Control your keybindings.json">
	
	<div class="llm-tag">
	
	#llm.claude-sonnet-4
	</div>
	
	**TLDR:** Source control your `keybindings.json` (keyboard shortcuts) file by symlinking it from the VSCode directory to a directory that holds your environment setup.
	
	## Details
	
	Source control your `keybindings.json` file, which manages your keyboard shortcuts in VSCode. Move the actual file to a `git` repository that holds your environment setup (shell configuration, dotfiles, and utility scripts), then symlink to it from VSCode's settings directory. VSCode continues to operate normally while you gain version control benefits.
	
	## Why Source Control Keybindings When Settings Sync Exists?
	
	While VSCode's built-in Settings Sync can sync keybindings between machines, source controlling them yourself provides multiple advantages:
	
	- **Visibility into changes**: Clearly see changes in the JSON through git diffs.
	- **Complete history ownership**: Own the entire file history and know when changes were made.
	- **Integration with dotfiles**: Your keybindings become part of your broader development environment setup.
	- **Platform independence**: Not tied to a Microsoft or GitHub account for Settings Sync.
	- **Rollback capability**: Easily revert to previous configurations if something breaks or when experimenting.
	
	## How to Set It Up
	
	1. **Locate your keybindings.json file**:
	   - Windows: `%APPDATA%\Code\User\keybindings.json`
	   - macOS: `~/Library/Application Support/Code/User/keybindings.json`
	   - Linux: `~/.config/Code/User/keybindings.json`
	
	2. **Move the file to your dotfiles repository**:
	
	  ```bash
	  # Example: moving to a dotfiles repo
	  mv ~/Library/Application\ Support/Code/User/keybindings.json ~/dotfiles/vscode/
	  ```
	
	3. **Create a symlink back to the original location**:
	   ```bash
	   # macOS/Linux example
	   ln -s ~/dotfiles/vscode/keybindings.json ~/Library/Application\ Support/Code/User/keybindings.json
	   
	   # Windows (run as Administrator)
	   mklink "%APPDATA%\Code\User\keybindings.json" "C:\path\to\dotfiles\vscode\keybindings.json"
	   ```
	
	4. **Commit to your repository**:
	   ```bash
	   cd ~/dotfiles
	   git add vscode/keybindings.json
	   git commit -m "Add VSCode keybindings"
	   ```
	
	Now your keybindings are version controlled, and VSCode will continue to read and write to the file through the symlink as if nothing changed from its perspective.
</note>
<note name="t.ext.troubleshooting" title="Troubleshooting">
	
	Hierarchy for troubleshooting.
</note>
<note name="t.ext.troubleshooting.linux.inotify" title="Troubleshooting Inotify on Linux">
	
	There are two pathways
	- **Shotgun approach** - double all inotify limits - [[t.ext.troubleshooting.linux.inotify.double-inotify-limits]]
	- Dive deeper - find out which limit to increase and increase just that limit: [[t.ext.troubleshooting.linux.inotify.dive-deeper-and-set-by-hand]]
</note>
<note name="t.ext.troubleshooting.linux.inotify.dive-deeper-and-set-by-hand" title="Dive Deeper and Set Inotify by Hand">
	
	
	<details class="bordered">
	<summary>Overview</summary>
	
	On Linux, file system monitoring relies on the [Inotify](https://en.wikipedia.org/wiki/Inotify) facility. Inotify requires a *watch handle* for each directory being monitored. For intelligent IDEs like IntelliJ, VSCode, and Thorg, detecting external file changes is essential for knowing the state of files of interest.
	
	</details>
	
	
	### Troubleshooting
	
	There are couple of different `inotify` limits that you might need to increase. The following script can help you figure out which limit you are breaching.
	
	![[t.ext.troubleshooting.linux.inotify.script-to-see-which-limit-is-low]]
	
	After running the above script you can adjust your limits by editing your system *inotify* configuration values:
	
	![[t.ext.troubleshooting.linux.inotify.sample-inotify-config]]
	
	
	### References
	
	- [Inotify Watches Limit Linux | JetBrains Knowledge Base](https://youtrack.jetbrains.com/articles/SUPPORT-A-1715/Inotify-Watches-Limit-Linux)
	- [Linux Kernel Inotify Increase commit](https://github.com/torvalds/linux/commit/92890123749bafc317bbfacbe0a62ce08d78efb7)
	- [Inotify Wikipedia](https://en.wikipedia.org/wiki/Inotify)
	
</note>
<note name="t.ext.troubleshooting.linux.inotify.double-inotify-limits" title="Double Inotify Limits">
	
	This is the simplified approach will double all 3 of your current `inotify` limits on linux.
	
	```bash
	curl -fsSL https://raw.githubusercontent.com/Thorg-App/script/refs/heads/main/troubleshoot/linux/inotify/inotify_double_current_limits.sh | bash 
	```
	
	Also: [[t.ext._.review-script-prior-to-running-them]]
	
</note>
<note name="t.ext.troubleshooting.linux.inotify.max_user_watches-memory-usage" title="inotify.max_user_watches Memory Usage">
	
	**Per-Watch Cost:**
	- **32-bit systems:** ~540 bytes per watch
	- **64-bit systems:** ~1 KB per watch
	
	**Example:** With `max_user_watches = 1048576`:
	- **Worst case (all watches used):** ~1 GB of kernel memory on 64-bit systems
	- **Real-world usage:** Typically much less, as not all watches are actively used
	
	⚠️ **Important:** Inotify uses **kernel memory** which cannot be swapped out. But it only uses memory when the watches are used not when you set the limit.
	
	
	### Memory is used when you use the watches
	
	```bash
	# Setting this limit doesn't use any memory yet
	# 
	# Memory is only used when watches are actually created
	# If you only have 1000 active watches, you're using ~1MB, not 1GB
	fs.inotify.max_user_watches = 1048576
	```
	
	
</note>
<note name="t.ext.troubleshooting.linux.inotify.sample-inotify-config" title="Sample Inotify Config">
	
	#### Increase Inotify Limits
	
	**One-liner using heredoc:**
	```bash
	sudo tee /etc/sysctl.d/99-inotify.conf > /dev/null <<'EOF'
	# Inotify limits for file watching
	fs.inotify.max_user_watches = 524288
	fs.inotify.max_user_instances = 256
	fs.inotify.max_queued_events = 16384
	EOF
	```
	
	<details class="bordered">
	<summary>OR use your editor of choice to edit config file</summary>
	
	You can use your CLI editor of choice vi/nano/... and edit the */etc/sysctl.d/99-inotify.conf* file new limits like the following: (or )
	
	```txt
	fs.inotify.max_user_watches = 524288
	fs.inotify.max_user_instances = 256
	fs.inotify.max_queued_events = 16384
	```
	</details>
	
	
	**Apply the changes:**
	```bash
	sudo sysctl -p /etc/sysctl.d/99-inotify.conf
	```
	
	**Verify it worked:**
	```bash
	sysctl fs.inotify.max_user_watches; \
	sysctl fs.inotify.max_user_instances; \
	sysctl fs.inotify.max_queued_events
	```
	
	
</note>
<note name="t.ext.troubleshooting.linux.inotify.script-to-see-which-limit-is-low" title="Script to See Which Inotify Limit Is Low">
	
	If you ran into inotify issues and want to find out which inotify limit you are running low on you can start with just checking your current limits, with the simple command in bash:
	
	```bash
	sysctl fs.inotify.max_user_watches; \
	sysctl fs.inotify.max_user_instances; \
	sysctl fs.inotify.max_queued_events
	```
	
	This should print output that contains something like:
	```bash
	fs.inotify.max_user_watches = 524288
	fs.inotify.max_user_instances = 256
	fs.inotify.max_queued_events = 16384
	```
	
	If you want to get the actual limits used, that is not as straightforward and requires some scripting. You can see some options [here](https://unix.stackexchange.com/a/502359/364768), (Also remember [[t.ext._.review-script-prior-to-running-them]])
</note>
<note name="t.ext.vscode.how-to.change-your-keybindings-json" title="How to Change Your keybindings.json">
	
	![[t.ext.vscode.how-to.change-your-keybindings-json.direct-file-modification]]
	
	![[t.ext.vscode.how-to.change-your-keybindings-json.modify-through-UI]]
	
	
	#### Related Tips
	- [[t.ext.tip.vscode.source-control.your-keybindings]]
</note>
<note name="t.ext.vscode.how-to.change-your-keybindings-json.direct-file-modification" title="Direct keybindings.json Modification">
	
	
	### How to Change Your keybindings.json directly
	- [[Open command palette|t.ext.vscode.how-to.open-command-palette]]
	- Type `Preferences: Open keyboard shortcuts (JSON)`
	- Modify the `keybindings.json` file directly.
</note>
<note name="t.ext.vscode.how-to.change-your-keybindings-json.modify-through-UI" title="Modify keybindings.json through UI">
	
	#### Modify shortcuts as Keyboard Shortcuts UI
	keybindings.json are surfaced in the Keyboard Shortcuts UI. That you can opened with:
	- [[Open command palette|t.ext.vscode.how-to.open-command-palette]]
	- Type `Preferences: Open keyboard shortcuts`
	- Modify the keybindings in UI
</note>
<note name="t.ext.vscode.how-to.downgrade-to-previous-version" title="Downgrade to Previous Version">
	
	[How to downgrade to previous version of VSCode](https://stackoverflow.com/a/49347158/7858768)
</note>
<note name="t.ext.vscode.how-to.open-command-palette" title="How to: Open Command Palette">
	
	By default, the command palette is bound to the `Ctrl+Shift+P` shortcut. Per VSCode documentation: [VSCode tips and tricks](https://code.visualstudio.com/docs/getstarted/tips-and-tricks)
	
	### Command ID
	```txt
	workbench.action.showCommands
	```
	Change it through [[t.ext.vscode.how-to.change-your-keybindings-json]]
	
	### Through Menu
	You can find this command pallete by going through top level menu `View -> Command Pallete...`
	
	### Name in Keybindings UI
	In the keybindings UI configuration, the name is `Show All Commands`
	
</note>
<note name="t.ext.vscode.how-to.reload" title="Reload VSCode">
	
	- **Option 1:** Restart the entire VSCode application.
	- **Option 2:** Reload the window:
	  - [[Open Command Palette|t.ext.vscode.how-to.open-command-palette]]
	  - Start typing `Reload Window` and select `Developer: Reload Window` when it appears.
</note>