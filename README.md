# Linux Script Toolkit
The Linux Script Toolkit is a collection of useful scripts designed to streamline network and system diagnostics on Linux servers. It includes tools for diagnosing network latency with Curl-Latency-Diagnoser, monitoring connection states and potential socket exhaustion with Linux-Connection-State, and analyzing web server access logs with Access-Log-Analyzer.

## Curl-Latency-Diagnoser
Combination of curl options for diagnosing application latency behavior over networks

### Usage

- download the latency-print.txt to your server<br>
```curl -L -o latency-print.txt http://tinyurl.com/pllhtu2```

- replace google.com with an IP or the domainname you like to test

- Print results to screen in one second loops:<br>
```while true; do echo -n `date`; curl -sLo /dev/null -w@latency-print.txt google.com ; sleep 1; done ```

- Print results to a file(latency-results.txt) for future usage in one second loops:<br>
```while true; do echo -n `date`; curl -sLo /dev/null -w@latency-print.txt google.com ; sleep 1; done | tee latency-results.txt```


## Linux-Connection-State
Useful netstat command with handful of options for live monitoring a Linux instance for socket exhaustion and related issues

### Usage

- download the connection-state.sh to your server<br>
```curl -L -o connection-state.sh http://tinyurl.com/connection-state```

- Issue command below to run it:<br>
```bash conection-state.sh```


## Access-Log-Analyzer
Analyzing the number of hits of your web application per IP 

Pass the access.log or access_log file name when asked and wait unitl results are printed to the screen.

From the script:

             === ACCESS LOG ANALYZER ===                      
                                                              
Please enter the access.log or access_log location       
                                                              
Usually under /var/httpd/access_log for RedHat family distributions. RHEL, CentOS, Fedora, Amazon Linux AMI    
                                                              
Usually under /var/apache2/access.log for Debian family distributions. Debian, Ubuntu, Mint..                    
