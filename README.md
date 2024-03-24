# Instructions for creating a proxy server for troubleshooting and diagnosing outgoing requests in WordPress

1.Create a HTTP Proxy Server (With programs like CCProxy,Glider,...)
Glider Project in Git : https://github.com/nadoo/glider
CCProxy Official Website: https://www.youngzsoft.net/ccproxy/proxy-server-download.htm
 
in Glider You can use Below Command to craete a HTTP Proxy With Username and password:
glider -verbose -listen http://Username:Password:3128

2.Open Http Proxy Used Ports in Firewall
 
3.Edit wp-config.php and put the following code in the file:
/* Configure HTTP Proxy Server */
define('WP_PROXY_HOST', 'HTTP_Proxy_Server_ip');
define('WP_PROXY_PORT', '3128'); 
define('WP_PROXY_USERNAME', 'Username'); 
define('WP_PROXY_PASSWORD', 'Password');
define('WP_PROXY_BYPASS_HOSTS', 'localhost');
![2024-03-14_004255](https://github.com/nasariasl/WP-http-proxy_server/assets/17225652/874d47d4-ef9e-44f8-bbb9-e569aebe39f3)

4.You can use Logs in Glider or CCProxy Log-folder to monitor Wordpress outgoing requests for Debug.
![2024-03-14_004516](https://github.com/nasariasl/WP-http-proxy_server/assets/17225652/d1a14b0b-0951-4f65-a699-728748332fcd)


5.You Can Use Apache,Winginx,Uwamp and ... to Create a Website on HTTP Protocol To monitor log Folder in CCProxy
![2024-03-14_004441](https://github.com/nasariasl/WP-http-proxy_server/assets/17225652/1734acc4-aa97-40f8-b341-bdd4fc5ad387)


