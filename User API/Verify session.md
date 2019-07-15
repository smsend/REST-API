<h1>Verify session</h1>
<p>Checks whether the user session is still active and valid (without renewal).</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user tokeny sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/checksession</code></pre>
<h2>Returns</h2>
<table>
<tr>
<th>Code</th>
<th>Description</th>
</tr>
<tr><td>200</td><td>String “true” if the session is valid, “false” otherwise.</td></tr>
<tr><td>404</td><td>[Unauthorized] User_key, Token or Session_key are invalid or not provided</td></tr>
<tr><td>400</td><td>Other errors, details are in the body</td></tr>