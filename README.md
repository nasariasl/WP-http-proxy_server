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
![2024-03-14_004255](https://github.com/nasariasl/WP-http-proxy_server/assets/17225652/2aaf8b7f-0bbe-4a59-9720-33977f279b72)

4.You can use Logs in Glider or CCProxy Log-folder to monitor Wordpress outgoing requests for Debug.
![2024-03-14_004516](https://github.com/nasariasl/WP-http-proxy_server/assets/17225652/0e0ab832-fcae-4772-8c26-eb6c7489ec50)

5.You Can Use Apache,Winginx,Uwamp and ... to Create a Website on HTTP Protocol To monitor log Folder in CCProxy
![2024-03-14_004441](https://github.com/nasariasl/WP-http-proxy_server/assets/17225652/eed2b68d-b7e7-40d6-b5ad-6994051ac442)

