# linux-magic

Get Top 50 processes consuming the most RAM:
`ps -e -o pid,rss,cmd --sort=-rss| awk 'NR>1 {print $1, $3, $4, $5, $2/1024 " MiB"}' | head -n 50`
