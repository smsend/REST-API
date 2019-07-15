<h1>Get list of campaigns by statuses</h1>
<p>Get list of campaigns by statuses. If statuses is not specified by default return only ACTIVE campaign.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>GET</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/list?statuses=UserParam(statuses)</code></pre>
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
								<td>statuses</td>
								<td>String</td>
								<td>List of campaign statuses separated by comma (ACTIVE, ARCHIVED, TO_ACTIVATE)</td>
								<td>No</td>
								<td>ACTIVE</td>
							</tr>
						</tbody></table>
<h2>Returns</h2>
<table>
							<tbody><tr>
								<th>Code</th>
								<th>Description</th>
							</tr>
							 <tr>
								  <td>204</td>
								  <td>List of campaign</td>
								</tr>
								<tr>
								  <td>400</td>
								  <td>Other errors, details are in the body</td>
								</tr>
								<tr>
								  <td>401</td>
								  <td><strong>[Unauthorized]</strong> User_key, Token or Session_key are invalid or not provided</td>
								</tr>
						</tbody></table>