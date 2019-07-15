<h1>Create new issue using a specified template</h1>
<p>Creates a new issue starting from the specified template.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/list/{campaignId}/issue/template/{template}</code></pre>
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
							  <td>campaignId</td>
							  <td>Int</td>
							  <td>The list where to send the emails</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
							<tr>
							  <td>template</td>
							  <td>Int</td>
							  <td>The template, previously created, to do the send</td>
							  <td>Yes</td>
							  <td>-</td>
							</tr>
						</tbody></table>
<h2>Body Fields</h2>
<table>
							<tbody><tr>
								<th>Parameter</th>
								<th>Type</th>
								<th>Description</th>
								<th>Required</th>
								<th>Default</th>
							</tr>
							<tr>
								  <td>name</td>
								  <td>String</td>
								  <td>The name/title of the issue</td>
								  <td>Yes</td>
								  <td>-</td>
								</tr>
								<tr>
								  <td>subject</td>
								  <td>String</td>
								  <td>The subject used in the issue</td>
								  <td>Yes</td>
								  <td>-</td>
								</tr>
						</tbody></table>
<h2>Returns</h2>
<table>
							 <tbody><tr>
								  <td>200</td>
								  <td>Successful request</td>
								</tr>
								<tr>
								  <td>400</td>
								  <td>Other errors, details are in the body</td>
								</tr>
								<tr>
								  <td>401</td>
								  <td><strong>[Unauthorized]</strong> User_key, Token or Session_key are invalid or not provided</td>
								</tr>
								<tr>
								  <td>404</td>
								  <td><strong>[Not found]</strong> The User_key was not found</td>
								</tr>
								<tr>
								  <td>500</td>
								  <td>The issue can’t be created</td>
								</tr>
						</tbody></table>