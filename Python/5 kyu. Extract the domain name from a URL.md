# Extract the domain name from a URL

Write a function that when given a URL as a string, parses out just the domain name and returns it as a string. For example:
```
* url = "http://github.com/carbonfive/raygun" -> domain name = "github"
* url = "http://www.zombie-bites.com"         -> domain name = "zombie-bites"
* url = "https://www.cnet.com"                -> domain name = cnet"
```

# Solution
```
def domain_name(url):
    if 'http://' in url:
        url = url.split('http://')[1]
    if 'https://' in url:
        url = url.split('https://')[1]    
    if 'www.' in url:
        url = url.split('www.')[1]
    url = url.split('.')[0]
    return url
```