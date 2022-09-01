### Garleak: A Security Tool for Detecting Credentials in Source Code Repositories




#### Discover where your sensitive data has been leaked.

<p>Very often it happens that when mocking/just starting out with a new project on github, sensitive data gets added. API keys, usernames, passwords and emails are easily added.... and then forgotten.</p>

<p>GarLeak identifies where the mistakes are in your repos. </p>

<p>It works by trying to find words like 'username', 'password', and 'email' and shortenings in quoted strings, config style or JSON format. It captures the value assigned to it (after meeting some conditions) for further work.</p>

</td>
</tr>
</table>



### Command line usage
The program can be simply called by `garleak`. There are 3 types of arguments.
- Arguments for changing whether there is a hit
- Arguments for cloning a repo
- Arguments concerned with printing results

Note that all arguments mentioned below have a short one letter + dash (e.g. `-delete` -> `-d`) version.

Find out more by using `garleak -h` at commandline, or read on.
#### Hits

```bash
garleak                               # default "smart" filter
garleak --find-anything               # find anything remotely suspicious
garleak --excluding $ . [ example ,   # exclude some string matches (e.g. `$` occurs)
garleak --case-sensitive              # set it to be strict about case
```


### Printing results

``` bash
garleak --verbose              # longer output
garleak --no-banner (-b)       # do not print banner
garleak --no-fancy-color (-f)  # turn off colors
```


#### Author : Mohammadreza Ashouri
#### Granola Team -  2022
#### mo@granola.team
