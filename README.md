### Slanger
---
https://github.com/stevegraham/slanger


```
gem install slanger
redis-server &> /dev/null &
slanger --app_key XXXXXXX --secret your-pusher-secret

fs,file-max = 50000

/etc/security/limits.conf
* hard nofile 50000
* soft nofile 50000
* hard nproc 50000
* soft nproc 50000

gem install slanger
redis-server &> /dev/null &
slanger --app_key XXXXXXX --secret your-pusher-secret

start on started networking and runlevel [2345]
stop on runlevel [016]
respawn
script
  LANG=en_US.UTF-8 /usr/local/rvm/gems/ruby-RUBY_VERSION/wrappers/slanger --app_key KEY --secret SECRET --reids_address redis://REDIS_IP:REDIS_PORT/REDIS_DB
end script

service slanger start
service slanger stop


```

```ruby
Pusher.host = 'slanger.example.com'
Pusher.port = 4567


```


```
<script type="text/javascript">
  var pusher = new Pusher('#(Pusher.key)',{
    wsHost: "0.0.0.0",
    wsPort: "8080",
    wssPort: "8080",
    enabledTransports: ['ws', 'flash']
  });
</script>


```

