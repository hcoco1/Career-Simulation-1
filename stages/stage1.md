##### Navigation

[Back to Home 🏠](../README.md) | [Back to Introduction ](introduction.md)  |  [Next: Stage: Analysis](stage2.md)

## Stage Identification

The first step in a digital forensics investigation is to identify the devices and resources containing the data that will be a part of the investigation (Gonzalez, 2022).

With Splunk storing its files within the /opt/splunk directory, the first step was to locate the config.conf file (Figure 1). Basic file navigation commands were utilized to navigate to the specified directory and confirm the presence of the file. This initial step ensured accurate file identification, which is crucial for precise modifications.


```bash
fstack@:~$ find /opt/splunk/ -name "config.conf"
/opt/splunk/etc/system/local/config.conf
```
<small>**Fig.1** Command to locate the `config.conf` file (find)</small>



Subsequently, an assessment of the file permissions of config.conf was conducted using the ls -l command (Figure 2). The output revealed the permissions as 777, indicating full permissions for the file's owner, group, and others. This information provided insights into potential issues affecting its integrity (Principle of least privileges).

```bash
fstack@~$ cd /opt/splunk/etc/system/local; ls -l
-rwxrwxrwx 1 root root 238 Feb 16:59 config.conf
```
<small>**Fig.2** Commands to list the `config.conf` file (cd, ls -l)</small>

Ensuring the file's integrity, the md5sum command was employed to calculate and record the MD5 hash value of config.conf. This served as a baseline for comparison after making modifications to the file, enabling verification of the integrity of changes made.

```bash
fstack@:/opt/splunk/etc/system/local$ md5sum config.conf 
ad1f9b6cbcee6cd3efa6438149db5c1c  config.conf
```
<small>**Fig.3** Command to hash the `config.conf` file (md5sum)</small>

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

[Back to Home 🏠](../README.md) | [Back to Introduction ](introduction.md)  |  [Next: Stage: Analysis](stage2.md)