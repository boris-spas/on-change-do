# poll

  Polls a file or directory content  and executes a given command if a change
  has occurred. Uses a hash of the content for comparison. 

  Usage :  poll [options] /path/to/observe command_to_execute_on_change

  Options:
  -a|all        Include hidden files in obervation.
  -h|help       Display this message.
  -l|lazy       Don't react to changes that happen during execution of the
                command. Usefull if	the command changes the oberved to path.
  -s|sha        Set the command used to calculate hash. The default is shasum.
  -t|timeout    Set the time to sleep between looking for changes.
  -v|version    Display script version.

  Example : poll -l -s shasum5.18 -t 0.5 /tmp/ 'echo change detected at \`date\`'


