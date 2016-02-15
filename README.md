# springboard
Watch a directory for new files and bounce them on somewhere else:

OR Simple "drop folder to POST request (or whatever)".

# usage

Example:

> springboard post --mime text/xml --uname homer --pass s1mps0n https://my.server.com/service ./incoming

Which basically says, when new files appear in the "./incoming" directory send them as an http POST request to the url provided, using basic auth to let us in and force the mimetype to expect XML files.

For the full range of options always best to do:

> springboard -h
 
And similarly for the options pertaining to the subcommands and actions:
 
> springboard post -h

# installing

1. Get go (version 1.4+)
2. Make sure you have set $GOPATH to a sensible place you can write to. 
3. Issue:
> go get -u github.com/draxil/springboard

You will want to make sure that your $GOPATH/bin is in your $PATH or else put $GOPATH/bin/springboard somewhere in your $PATH.

# actions
 
 So far there are two actions:
 
 * post - Send the file content as an HTTP POST request
 * echo - Echo the file path to stdout (good for building shell pipelines)
 
# Watcher API

The code effective funtionality could be useful to a go coder independent of the command itself. I'll post a godoc link here once the documentation is in any kind of shape. If you particularly want this please shout at me.

# status / plans
 
 This is at an early stage of development and is subject to change! Upcoming additions:
 
* Error handling behaviour
* Picking up files that appeared while springboard was "off" 
* Filtering / regex for being selective

Please feel free to shout at me if I'm missing something you need.
