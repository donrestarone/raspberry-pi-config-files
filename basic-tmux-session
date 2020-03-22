cd '/home/pi/Documents/startup-scripts'

session="servers"

tmux new-session -d -s $session

tmux split-window -h
tmux send-keys './start-rails-server.sh' 'C-m'
tmux split-window -v -t 0
tmux send-keys './start-redis-server.sh' 'C-m'
tmux split-window -v -t 1
tmux send-keys './start-sidekiq-server.sh' 'C-m'
tmux split-window -v -t 1
tmux send-keys './start-frontend.sh' 'C-m'
