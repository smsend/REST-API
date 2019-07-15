<h1>User status</h1>
<p>Used to retrieve the services status of the user identified by the id.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user tokeny sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/status?getMoney={value}</code></pre>
<h2>Parameters</h2>
<table>
<tr>
<th>Parameter</th>
<th>Type</th>
<th>Description</th>
<th>Required</th>
<th>Default</th>

</tr>
<tr><td>getMoney</td><td>String “true” or “false”</td><td>Add user current money to response</td><td>No</td><td>"false"</td></tr>
<tr><td>typeAliases</td><td>String “true” or “false”</td><td>Returns the actual names for the message types instead of the internal ID. This is not done by default only because of retrocompatibility issues.</td><td>No, but suggested</td><td>"false"</td></tr>
</table>
<h2>Returns</h2>
<table>
<tr>
<th>Code</th>
<th>Description</th>
</tr>
<tr><td>200</td><td>A Json object representing the user status</td></tr>
<tr><td>400</td><td>Other errors, details are in the body</td></tr>
<tr><td>401</td><td>[Unauthorized] User_key, Token or Session_key are invalid or not provided</td></tr>
<tr><td>404</td><td>[Not found] Credentials are incorrect</td></tr></table>