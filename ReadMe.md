# Dev Tools
Basic commads

## Amazon Linux AMI 2 - NGINX Installation
```
  sudo amazon-linux-extras install nginx1.12
```

## Amazon Linux AMI 2 - PHP 7.2 Installation
```
  sudo yum -y install epel-release
  sudo yum-config-manager --enable remi-php72
  sudo amazon-linux-extras install php7.2
  sudo yum -y install php-xml php-cli php-mcrypt php-json php-gd
```

## CodeDeploy Installation
```
  sudo yum update && sudo yum upgrade
  sudo yum install wget
  wget https://aws-codedeploy-ap-southeast-1.s3.amazonaws.com/latest/install
  sudo yum install ruby
  chmod +x install
  sudo ./install auto
  sudo service codedeploy-agent status
```

### Install Composer
```
  cd ~
  sudo curl -sS https://getcomposer.org/installer | sudo php
  sudo mv composer.phar /usr/local/bin/composer
  sudo ln -s /usr/local/bin/composer /usr/bin/composer
  composer -v
```

### Bash Commands
Create new branch based on `main`
Format: `users/<username>/<ticket_id>-<name>`

Code:
```
git_create_branch() {
        GIT="$(which git)"
        DEFAULT_BRANCH="users/mdar4993"
        TICKET_NO=$1
        BRANCH_NAME=$2

        BRANCH_TO_CREATE="$DEFAULT_BRANCH/$1-$2"
        #echo "$1 $2"

        $GIT checkout main && $GIT pull

        if [ -n `$GIT rev-parse --verify $CREATE_BRANCH 2>/dev/null` ]
        then
                $GIT checkout $BRANCH_TO_CREATE
        else
                $GIT checkout -b $BRANCH_TO_CREATE
        fi
}
```

## Sublime
### Settings
```
  {
  	"auto_indent": true,
  	"bold_folder_labels": true,
  	"color_scheme": "Packages/Babel/Monokai Phoenix.tmTheme",
  	"detect_indentation": true,
  	"draw_white_space": "all",
  	"font_face": "menlo",
  	"font_size": 22,
  	"highlight_line": true,
  	"ignored_packages":
  	[
  		"Vintage"
  	],
  	"line_padding_bottom": 6,
  	"line_padding_top": 6,
  	"show_full_path": true,
  	"smart_indent": true,
  	"tab_size": 2,
  	"theme": "Material-Theme.sublime-theme",
  	"translate_tabs_to_spaces": true,
  	"use_tab_stops": true
  }

```


#### Key Bindings
```
[
  {"keys": ["super+f11"], "command": "clone_file"},
  {
    "keys": ["ctrl+alt+t"],
    "command": "open_terminal",
    "args": {
      "parameters": ["-T", "Custom Window Title"]
    }
  },
  { "keys": ["super+i"], "command": "copy_path" },
  {
    "keys": ["super+shift+w"],
    "command": "toggle_setting",
    "args": {
        "setting": "word_wrap"
    }
  },
  {
    "keys": ["tab"],
    "command": "expand_abbreviation_by_tab",
    "context": [
      { "operand": "source.js", "operator": "equal", "match_all": true, "key": "selector" },
      { "match_all": true, "key": "selection_empty" },
      { "operator": "equal", "operand": false, "match_all": true, "key": "has_next_field" },
      { "operand": false, "operator": "equal", "match_all": true, "key": "auto_complete_visible" },
      { "match_all": true, "key": "is_abbreviation" }
    ]
  },
  {
    "keys": ["super+shift+r"],
    "command": "reveal_in_side_bar",
  }
]
```
