<h1>Create a new alias</h1>
<p>Creates a new TPOA Alias.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/alias</code></pre>
<h2>Body Fields</h2>
<p>The body must contain a Json with a JsonObject field named alias that contains all the alias info:</p>
<table>
								<tbody><tr>
								  <th>Parameter</th>
								  <th>Type</th>
								  <th>Description</th>
								  <th>Required</th>
								  <th>Default</th>
								</tr>
								<tr>
									<td>alias</td>
									<td>String</td>
									<td>The sender that will be shown on SMS</td>
									<td>Yes</td>
									<td></td>
								</tr>
								<tr>
									<td>company-name</td>
									<td>String</td>
									<td>The name of company associated to this alias</td>
									<td>Yes</td>
									<td></td>
								</tr>
								<tr>
									<td>contact-name</td>
									<td>String</td>
									<td>The name of physical person rappresenting the company</td>
									<td>Yes</td>
									<td></td>
								</tr>
								<tr>
									<td>contact-surname</td>
									<td>String</td>
									<td>The surname of physical person rappresenting the company</td>
									<td>Yes</td>
									<td></td>
								</tr>
								<tr>
									<td>cod-fiscale</td>
									<td>String</td>
									<td>The fiscal code of company</td>
									<td>Yes</td>
									<td></td>
								</tr>
								<tr>
									<td>vat-number</td>
									<td>String</td>
									<td>The vat number of company</td>
									<td>Yes</td>
									<td></td>
								</tr>
								<tr>
									<td>contact-address</td>
									<td>String</td>
									<td>The address of company</td>
									<td>Yes</td>
									<td></td>
								</tr>
								<tr>
									<td>contact-city</td>
									<td>String</td>
									<td>The city of company</td>
									<td>Yes</td>
									<td></td>
								</tr>
								<tr>
									<td>contact-pcode</td>
									<td>String</td>
									<td>The ZIP/Postal-code/CAP code of company</td>
									<td>Yes</td>
									<td></td>
									</tr>
								<tr>
									<td>contact-type</td>
									<td>String enum(SERVICE_PHONE, MAIN_PHONE, FAX, EMAIL, PEC, WEB)</td>
									<td>The type of contact referred to contact-info</td>
									<td>Yes</td>
									<td></td>
								</tr>
								<tr>
									<td>contact-info</td>
									<td>String</td>
									<td>The value of contact</td>
									<td>Yes</td>
									<td></td>
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
							</tbody></table>