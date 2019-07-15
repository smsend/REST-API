<h1>List contacts groups</h1>
<p>Returns the list of existing contacts groups, paginated.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/groups?pageNumber={page}&pageSize={size}</code></pre>
<h2>Parameters</h2>
<table>
							<tbody><tr>
								<th>Parameter</th>
								<th>Type</th>
								<th>Description</th>
								<th>Required</th>
								<th>Default</th>
							</tr>
							<tr>
							  <td>pageNumber</td>
							  <td>int</td>
							  <td>The page number</td>
							  <td>No</td>
							  <td>1</td>
							</tr>
							<tr>
							  <td>pageSize</td>
							  <td>int</td>
							  <td>The page size</td>
							  <td>No</td>
							  <td>5</td>
							</tr>
						</tbody></table>
<h2>Returns</h2>
<table>
							<tbody><tr>
								<th>Code</th>
								<th>Description</th>
							</tr>
							<tr>
							  <td>200</td>
							  <td>The paginated list of contacts groups, as a Json Object</td>
							</tr>
							<tr>
							  <td>401</td>
							  <td><strong>[Unauthorized]</strong> User_key, Token or Session_key are invalid or not provided</td>
							</tr>
							<tr>
							  <td>404</td>
							  <td><strong>[Not found]</strong> The User_key was not found</td>
							</tr>
						</tbody></table>