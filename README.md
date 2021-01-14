# custom-starship.toml-file
A custom starship.toml file for anyone to use.

![Screenshot from 2020-12-14 23-16-10](https://user-images.githubusercontent.com/46455250/102116185-7f4e6e00-3e34-11eb-8754-f33e379d2112.png)


Store the file in `./config`.
Please check first if you have `FiraCode NF Bold`.

```
# Replace the "❯" symbol in the prompt with "➜"
[character]
success_symbol = "[➜](bold green)" 

# Use custom format
format = """
[┌───────────────────](bold green)
[│](bold green)$directory$rust$package
[└─>](bold green) """

# Wait 10 milliseconds for starship to check files under the current directory.
scan_timeout = 10

[username]
style_user = "green bold"
style_root = "black bold"
format = " [$user]($style) ~ "
disabled = false
show_always = true

[cmd_duration]
min_time = 500
format = "took [$duration](bold yellow)"

[directory]
format = "[$path]($style)[$read_only]($read_only_style) "
style = "bold #f57800"
read_only = "🔒"
read_only_style = "red"

[git_branch]
format = "on [$symbol $branch ]($style)"
symbol = " "
style = "bold purple"

[git_commit]
#format = "[\\($hash\\)]($style) [\\($tag\\)]($style)"
style = "bold green"

[git_status]
format ='([\[$all_status$ahead_behind\]]($style))'
conflicted = "="
ahead =	"⇡${count} "
behind = "⇣${count} "
diverged = "⇕⇡${ahead_count}⇣${behind_count}"
untracked = "?${count} "
stashed = "$${count} "
modified = "!${count} "
staged = "+${count} "
renamed = "»${count} "
deleted = "✘${count} "
style =	"bold red"
disabled = false

[git_state]
rebase = "REBASING"
merge =	"MERGING"
revert = "REVERTING"
cherry_pick = "CHERRY-PICKING"
bisect = "BISECTING"
am = "AM"
am_or_rebase = "AM/REBASE"
style =	"bold yellow"
format = '\([$state( $progress_current/$progress_total)]($style)\) '
disabled = false

[hg_branch]
symbol = " "
style =	"bold purple"
format = "on [$symbol$branch]($style) "

[memory_usage]
format = "via $symbol [${ram}( | ${ram_pct})]($style)"
symbol = " "
style = "bold dimmed green"

[nodejs]
format = "via [$symbol$version]($style) "
symbol = "⬢ "
style = "bold green"
disabled = false
not_capable_style = "bold red"

[status]
format = "[$symbol$status]($style)"
symbol = "✖"
style = "bold red"
disabled = true

[battery]
full_symbol = ""
charging_symbol = ""
discharging_symbol = ""

[docker]
symbol = " "

[conda]
symbol = " "

[dart]
symbol = " "

[package]
symbol = " "

[perl]
symbol = " "

[php]
symbol = " "

[python]
symbol = " "

[ruby]
symbol = " "

[rust]
symbol = " "

[swift]
symbol = "ﯣ "
```
