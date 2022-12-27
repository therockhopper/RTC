---
title: "Scripting Tmux"
draft: false
---
TL:DR here is a starter script.
```zsh
#!/bin/zsh

session="Project Name"
project_path="~/Documentslight"

tmux new-session -d -s $session

window=0

window=1
tmux new-window -t $session:$window -n 'ProjectOne'
tmux send-keys -t $session:$window "cd $project_path" C-m
tmux send-keys -t $session:$window 'nvim package.json'

window=2
tmux new-window -t $session:$window -n 'ProJectTwo'
tmux send-keys -t $session:$window "cd $project_path" C-m

tmux attach-session -t $cnn_session
```

Explaniation