drafts-ab-edit.py is a python script for manipulating the [Action Backups][backup] generated by the [Drafts iOS app][drafts]. Use it to easily setup [Dropbox Actions][dropbox-actions] from the comfort of your OSX terminal.

Basic Instructions:

1. From the Drafts iOS app, backup your existing actions using the appropriate button in Preferences menu.
2. From your mac, Run `drafts-ab-edit.py add ~/Dropbox/<file>.txt` to add the Dropbox Actions you want to create
3. From the Drafts iOS app, restore your actions from the Drafts iOS app

# Usage

Run `drafts-ab-edit.py --help` for more info

# Examples

Adding a file with a particular template:

	drafts-ab-edit.py add ~/Dropbox/list.txt -t "- [[draft]]"

If your template is more complex you can use a file:

	drafts-ab-edit.py add ~/Dropbox/log.txt -tf log-template.txt

File `log-template.txt`:

	# [[date|YYYY-MM-DD]]
	[[title]]

	[[body]]

Adding multiple files to a particular Action Pane:

	drafts-ab-edit.py add ~/Dropbox/Books.txt ~/Dropbox/Movies.txt --pane 3

Adding all files with a particular prefix. The prefix is removed from the action name

	drafts-ab-edit.py add ~/Dropbox/runx-*.txt --prefix 4

The script also supports removing action via the `rm` command and listing all existing dropbox actions via `list`

# Requirements

Python 2.7, Drafts 3.0 

# License 

This code is public domain.

[drafts]:http://agiletortoise.com/drafts/
[backup]:http://agiletortoise.com/support/drafts/action_management.html
[dropbox-actions]:http://agiletortoise.com/support/drafts/dropbox_actions.html

