# mytmux
My tmux configs
add this to your .bashrc file "[ -z "$TMUX" ] && export TERM=xterm-256color"
also if using scripting avoid to type password by adding "username ALL = NOPASSWD: ALL" with visudo or "username ALL = NOPASSWD: /usr/local/bin/script.sh".
Para iniciar a shell com o tmux adicionar o seguinte ao .bashrc :

if [[ "$TERM" != "screen-256color" ]]
then
    tmux attach-session -t "$USER" || tmux new-session -s "$USER"
    exit
fi

