# Proxy-Handler

A file that contains 2 classes (one is used as data object), so you
don't really have to care about the first which is Proxies, you just
need to read the attributes in order to be able to use it as you want
to.


# Classes

## Proxies

### attributes

| Name       | Description                      | Value                        | Default Value |
|:-----------|:---------------------------------|:-----------------------------|:--------------|
| ip         | The ip of the proxy              | string ip:port               | No            |
| being_used | Boolean value of the proxy usage | Boolean                      | False         |
| banned     | Boolean value of the ban status  | boolean                      | False         |
| proxy      | Dictionary to be used directly   | Dictionary                   | No            |
| proxy_type | Type of the proxy                | string socks4/socks5/http(s) | No            |


## Handler

### Parameters

| Name             | Description                                                                                                  | Value   | Optional | Default Value          |
|:-----------------|:-------------------------------------------------------------------------------------------------------------|:--------|:---------|:-----------------------|
| timeout          | maximum response time for the proxy                                                                          | integer | yes      | 10                     |
| display_messages | if true, it will display messages such as proxy not working, proxy working, waiting to get unused proxies... | boolean | yes      | false                  |
| url              | URL to check the proxies (must have http(s)://www.site.com)                                                  | string  | yes      | https://www.google.com |
| success_key      | String to check if it's inside the response html, if not, it's considered as not working                     | string  | yes      | ```</html>```              |

### Attributes