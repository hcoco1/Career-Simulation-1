##### Navigation

[Back to Home 🏠](../README.md) | [Back to Stage: Analysis](stage2.md)  |  [Next: Summary](summary.md)

## Stage  Preservation

After the devices involved in an investigation have been seized and stored in a secure location, the digital forensics investigator or forensics analyst uses forensic techniques to extract any data that may be relevant to the investigation and stores it securely. This phase can involve the creation of a digital copy of the relevant data, which is known as a “forensic image.”(Gonzalez, 2022)

As a precautionary measure, a backup of the edited config.conf file was created by copying the file to the /home/fstack directory (Figure 6). This action ensured the preservation of the modified file for future reference or restoration purposes, providing an additional layer of security and risk mitigation.


```bash
fstack@~$ sudo tar -cJf /home/fstack/config.conf.tar.xz config.conf
fstack@~$ ls -l /home/fstack
drwxr-xr-x  2 fstack fstack   4096 Aug 31  2022  Music
drwxr-xr-x  2 fstack fstack   4096 Aug 31  2022  Pictures
drwxr-xr-x  2 fstack fstack   4096 Aug 31  2022  Public
drwxr-xr-x  2 fstack fstack   4096 Aug 31  2022  Templates
drwxr-xr-x  2 fstack fstack   4096 Aug 31  2022  Videos
-rw-rw-r--  1 fstack fstack   1032 Jan 31 06:12  auditd.enable
-rw-r--r--  1 root   root      320 Feb 19 03:12  config.conf.tar.xz
```
<small>**Fig.6** Commands to backup and list the config.conf file (tar, ls -l)</small>

<div id="disqus_thread"></div>
<script>
    /**
    *  RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
    *  LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables    */
    /*
    var disqus_config = function () {
    this.page.url = PAGE_URL;  // Replace PAGE_URL with your page's canonical URL variable
    this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
    };
    */
    (function() { // DON'T EDIT BELOW THIS LINE
    var d = document, s = d.createElement('script');
    s.src = 'https://hcoco1-1.disqus.com/embed.js';
    s.setAttribute('data-timestamp', +new Date());
    (d.head || d.body).appendChild(s);
    })();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript">comments powered by Disqus.</a></noscript>

##### Navigation

[Back to Home 🏠](../README.md) | [Back to Stage: Analysis](stage2.md)  |  [Next: Summary](summary.md)