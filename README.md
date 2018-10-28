#NAVER SENS CLIENT


* support only send sms yet

##Install
<pre>
pip install naver-sens-client
</pre>

##Usage
<pre><code>
sens_client = SensClient(service_id, secret_key, access_key_id)
</code></pre>
and then
<pre><code>
response = sens_client.send_sms(to_mobile_number, content, from_mobile_number)
</code></pre>

or

<pre><code>
sens_client.set_from_number(from_mobile_number)
response = sens_client.send_sms(to_mobile_number, content)
</code></pre>

then confirm response.
<pre><code>
print(response.status_code)
print(response.content.decode('utf-8'))
</code></pre>

##More detail
[Naver Sens API DOCUMENT/KR-KO](https://sens.ncloud.com/assets/html/docs/index.html?url=https://api-sens.ncloud.com/docs/openapi/ko)