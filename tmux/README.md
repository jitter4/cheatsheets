## seesion new
tmux

tmux new -s \<database_name\>

## rename session
tmux rename-session -t 0 database

## new window
(ctrl-B) c

## Right split
(ctrl-B) %

## Down split
(ctrl-B) "

## detach sessio
(ctrl-B) d

## list session
tmux ls

## attch session
tmux attach -t \<seesion_number\>

## full screen pane
(ctrl-B) z

## rename current window
(ctrl-B) ,
