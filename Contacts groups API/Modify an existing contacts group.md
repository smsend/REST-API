<h1>Modify an existing contacts group</h1>
<p>Updates a given contacts group</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>PUT</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/group/{group_id}</code></pre>
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
                                <td>The name of the group</td>
                                <td>Yes</td>
                                <td>-</td>
                            </tr>
                            <tr>
                                <td>description</td>
                                <td>String</td>
                                <td>The description of the group</td>
                                <td>Yes</td>
                                <td>-</td>
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
							  <td>An empty string, and the HTTP Location header containing the path to the updated group</td>
							</tr>
							<tr>
							  <td>400</td>
							  <td>If the given group_id is invalid, if the address book is locked, if the group name is invalid, or other errors, with a code error</td>
							</tr>
							<tr>
							  <td>401</td>
							  <td><strong>[Unauthorized]</strong> User_key, Token or Session_key are invalid or not provided</td>
							</tr>
							<tr>
							  <td>404</td>
							  <td><strong>[Not found]</strong> If the requesting user does not exist.</td>
							</tr>
						</tbody></table>