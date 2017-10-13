### Sublime text settings for Rails development

#### Install Sublime Text 3 on Ubuntu 16.04

```
wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | sudo apt-key add -

echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list

sudo apt-get update

sudo apt-get install sublime-text

```

*In addition: to remove Sublime Text 3*

```
sudo apt-get remove sublime-text && sudo apt-get autoremove
```

**1. Plugins:**

- AdvancedNewFile
- All Autocomplete
- AutoAligner
- BeautifyRuby
- Bootstrap 3 Autocomplete
- Bootstrap 3 Snippet
- Emmet
- Git, GitGutter
- Markdown Preview
- Ruby on Rails Snippets
- SCSS
- Slime
- SublimeERB
- SublimeLinter, SublimeLinter-ruby
- Trimmer

**2. Key binding settings:**

```
[
  { "keys": ["ctrl+alt+down"], "command": "goto_definition" },
  { "keys": ["ctrl+alt+up"], "command": "jump_back" },
  {
    "keys": ["cmd+l"],
    "command": "show_overlay",
    "args": {"overlay": "goto", "text": ":"}
  },
  { "keys": ["ctrl+shift+t"], "command": "reopen_last_file" },
  { "keys": ["ctrl+shift+."], "command": "erb", "context":
    [
      { "key": "selector", "operator": "equal", "operand": "text.html.ruby, text.haml, source.yaml, source.css, source.scss, source.js, source.coffee" }
    ]
  },
  { "keys": ["super+shift+d"], "command": "duplicate_lines" }
]
```

**3. User settings:**
```
{
  "auto_complete": true,
  "auto_complete_commit_on_tab": true,
  "color_scheme": "Packages/User/SublimeLinter/Mariana (SL).tmTheme",
  "copy_with_empty_selection": true,
  "ensure_newline_at_eof_on_save": true,
  "ignored_packages":
  [
    "Vintage"
  ],
  "index_files": true,
  "rulers":
  [
    79
  ],
  "tab_size": 2,
  "theme": "Adaptive.sublime-theme",
  "translate_tabs_to_spaces": true,
  "trim_trailing_white_space_on_save": true
}
```
