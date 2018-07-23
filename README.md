# cheatsheet-ruby-A4
<a href="https://github.com/DennyZhang?tab=followers"><img align="right" width="200" height="183" src="https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/fork_github.png" /></a>

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com) [![LinkedIn](https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/linkedin.png)](https://www.linkedin.com/in/dennyzhang001) <a href="https://www.dennyzhang.com/slack" target="_blank" rel="nofollow"><img src="http://slack.dennyzhang.com/badge.svg" alt="slack"/></a> [![Github](https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/github.png)](https://github.com/DennyZhang)

File me [tickets](https://github.com/DennyZhang/cheatsheet-ruby-A4/issues) or star [the repo](https://github.com/DennyZhang/cheatsheet-ruby-A4).

See more CheatSheets from Denny: [here](https://github.com/topics/denny-cheatsheets)

Table of Contents
=================

   * [cheatsheet-ruby-A4](#cheatsheet-ruby-A4)
      * [Summary](#summary)
      * [List](#list)
      * [String](#string)
      * [Integer](#integer)
      * [Conversion](#conversion)
      * [Dict &amp; Set](#dict--set)
      * [File](#file)
      * [Code Snippets](#code-snippets)
   * [More links](#more-links)

<a href="https://www.dennyzhang.com"><img align="right" width="185" height="37" src="https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/dns_small.png"></a>

## Summary
| Name                                  | Comment                                        |
| :------------------------------------ | ---------------------------------------------- |
| Check syntax                          | `ruby -c my.rb`                                |
| Generate random key                   | `r = Random.new, r.rand(10...42)`              |
| Install package with specific version | `gem install rubocop -v "0.44.1"`              |
| Get RubyGem env                       | `gem env`                                      |
| Check whether variable is nil         | `if value.nil?`                                |
| Run system command                    | `system("commandhere")`                        |
| Run bash command                      | `stdin, stdout, stderr = Open3.popen3('ls .')` |

## List

| Name                     | Comment                                 |
| :--------------------    | --------------------------------------- |
| Check existence          | `['Cat', 'Dog', 'Bird'].include? 'Dog'` |
| Find item                | `l1.find_index(x)`                      |
| Remove item from list    | `l1.delete_at(2)`                       |
| Remove duplicate entries | `[1,2,2,1,4,4,5,6,7,8,5,6].uniq`        |
| Deep copy a list         | `l1=l.dup`                              |

## String

| Name                      | Comment                                            |
| :------------------------ | ------------------------------------------------   |
| Substring                 | `string[1..3]`                                     |
| Search substring          | `"option=name=bob".index("name")`                  |
| Replace                   | `"Welcome to PHP Essentials!".gsub("PHP", "Ruby")` |
| Remove trailing comma     | `"ab;123;".chomp(";")`                             |
| Strip whitespace          | `host = host.strip()`                              |

## Integer

| Name                      | Comment                        |
| :------------------------ | ------------------------------ |

## Conversion

| Name                      | Comment                                   |
| :------------------------ | ----------------------------------------- |
| Convert string to int     | `"1,112".delete(',').to_i`                |
| Round float to 2 digits   | `(5.65235534).round(2)`                   |
| Format datetime           | `puts time.strftime("%Y-%m-%d %H:%M:%S")` |

## Dict & Set

| Name                      | Comment                               |
| :---------------------    | -----------------------------------   |

## File
| Name                           | Comment                             |
| :----------------------------- | ----------------------------------- |
| Check whether directory exist  | `File.directory?('xxx")`            |
| Check whether files exist      | `File.file?('hello.rb')`            |
| Read file to string            | `contents = File.read('filename')`  |

- Write to file
```
# append
File.open('/tmp/test.txt', 'a') { |file| file.write("your text\n") }

# overwrite
File.open('/tmp/test.txt', 'w') { |file| file.write("your text\n") }
```

## Code Snippets
- Get ip from eth0
```
ruby -rsocket -e 'p IPSocket.getaddress(Socket.gethostname)'

require 'socket'
Socket::getaddrinfo(Socket.gethostname,"echo",Socket::AF_INET)[0][3]
```

- Get hostname
```
require 'socket'
hostname = Socket.gethostbyname(Socket.gethostname).first
```

- Get hostname from ip

```
    def get_hostname_by_ip(ip_address)
      require 'resolv'
      dns = Resolv.new

      hostname = ip_address
      begin
        hostname = dns.getname(ip_address)
      rescue
        # TODO: show error message
        puts "ERROR: Exception"
      end
      return hostname
    end
  end
```

# More links
- TODO: Need to automatically generate pdf

- License: Code is licensed under [MIT License](https://www.dennyzhang.com/wp-content/mit_license.txt).

<a href="https://www.dennyzhang.com"><img align="right" width="201" height="268" src="https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/denny_201706.png"></a>

<a href="https://www.dennyzhang.com"><img align="right" src="https://raw.githubusercontent.com/USDevOps/mywechat-slack-group/master/images/dns_small.png"></a>
