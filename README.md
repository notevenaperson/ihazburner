# ihazburner

Quickly find out if your [burner email address](https://en.wikipedia.org/wiki/Disposable_email_address) is banned for account registration on most web-services. 

The habit of re-using email addresses is one of the ways contemporary web-services spy on you. It seems disposable email addresses undermine their businesses so much they're willing to maintain huge blocklists of domains that offer temporary email addresses, not unlike privacy-minded individuals, who for diametrically opposed reasons obsessively maintain blocklists of trackers and ad server domains.

**ihazburner** can't know which blocklists the web-service you're trying to register an account in is aware of. As such, the combined blocklists ihazburner checks will probably be overkill or not extensive enough. Its purpose isn't to be right all the time, but throw an educated guess of which of your options of disposable email addresses are worth trying to register with. It eases the main deterrent against using burner email addresses by essentially automating the tedious process of trying burner domains in a registration form one-by-one. 

Yes, I'm aware a lengthy description for an improvised script that just duct-tapes curl and grep for this very specific purpose is a little overkill.
# Usage
Takes a list of burner email addresses or domains (one per line) in [stdin](https://en.wikipedia.org/wiki/stdin), prints out the ones not present in common burner blocklists.

## Examples
```sh
$ cat burners2try.txt
fnord@qux.net
loremimpsum@foobar.xyz
thud@waldo.me

#stdin example
$ ihazburner < burners2try.txt
## or
$ cat burners2try.txt | ihazburner
```
