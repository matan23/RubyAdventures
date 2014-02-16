RubyAdventures
==============

# Procfile

## Simple way to boot multidependecy apps (web,workers,memcached,redis..)


### Specify ENV variables .env


### Example
web:    bundle exec thin start -p $PORT  
worker: bundle exec rake resque:work QUEUE=*  
clock:  bundle exec rake resque:scheduler 

### Concurrency

#####run 1 of each process type, and 2 workers
$ foreman start -c worker=2

####do not run a clock process
$ foreman start -c clock=0


### Scheduled Jobs and Custom Clock Process
[https://devcenter.heroku.com/articles/scheduled-jobs-custom-clock-processes]

### More
https://devcenter.heroku.com/articles/procfile#more-process-type-examples

# Rspec
http://www.neo.com/2013/12/20/custom-failure-messages-in-rspec-given
