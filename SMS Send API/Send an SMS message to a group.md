<h1>Send an SMS message to a group</h1>
<p>Send an SMS message to a set of contacts groups.</p>
<h2>Landing Pages URLs</h2>
<p>It is possible to include a link to a published Landing Page by specifying the <pre><code>id_landing parameter</code></pre> and by adding the following placeholder in the message body: <pre><code>%PAGESLINK____________%</code></pre>.</p>
<p>Landing pages must be first created and published in your user panel, since you will need <pre><code>id_landing</code></pre> to send it.</p>
<p>A list of published landing pages can be retrieved by using the Landing Pages APIs</p>
<h2>Short URLs</h2>
<p>When including URLs in the message, it may be convinient to use short URLs to limit the number of characters used in the SMS message.</p>
<p>Our API can automatically generate a short link starting from a long one, and add it in the message.</p>
<p>o use this feature, use the <pre><code>%SHORT_LINK%</code></pre> placeholder in the message body, that will be replaced with the generated short link, and the respective <pre><code>short_link_url</code></pre> parameter, that should be set to a valid URL. For shortlink dns personalization please contact us at helpdesk@smsend.it</p>
<h2>Sender Alias</h2>
<p>Alphanumeric aliases require to be registered first, and need to be approved both from Us and AGCOM.</p>
<p>Aliases can be used only with high-quality message types.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/smstogroups</code></pre>
<h2>Body Fields</h2>
<table>
							<tbody><tr>
							  <td>Parameter</td>
							  <td>Type</td>
							  <td>Description</td>
							  <td>Required</td>
							  <td>Default</td>
							</tr>
							<tr>
								<td>message_type</td>
								<td>String (“N” for High quality with reception notification, “L” for Medium Quality, “LL” For Low Cost)</td>
								<td>The type of SMS.</td>
								<td>Yes</td>
								<td>-</td>
							</tr>
							<tr>
								<td>message</td>
								<td>String (max 1000 chars with “gsm” encoding, 450 with “ucs2” encoding)</td>
								<td>The body of the message. *Message max length could be 160 chars when using low-quality SMSs</td>
								<td>Yes</td>
								<td>-</td>
							</tr>
							<tr>
								<td>recipient</td>
								<td>List(String)</td>
								<td>A list of contact group names</td>
								<td>Yes</td>
								<td>-</td>
							</tr>
							<tr>
								<td>sender</td>
								<td>String</td>
								<td>The Sender name. If the message type allows a custom TPOA and the field is left empty, the user’s preferred TPOA is used. Must be empty if the message type does not allow a custom TPOA</td>
								<td>No</td>
								<td>“”</td>
							</tr>
							<tr>
								<td>scheduled_delivery_time</td>
								<td>String [ddMMyy, yyyyMMdd, ddMMyyHHmm, yyyyMMddHHmmss, yyyy-MM-dd HH:mm, yyyy-MM-dd HH:mm.0]</td>
								<td>The messages will be sent at the given scheduled time</td>
								<td>No</td>
								<td>null</td>
							</tr>
								<tr>
								<td>scheduled_delivery_timezone</td>
								<td>Timezone(IANA time zone)</td>
								<td>Optional timezone applied to <kbd class="pre">scheduled_delivery_time</kbd> date</td>
								<td>No</td>
								<td>-</td>
							</tr>
							<tr>
								<td>order_id</td>
								<td>String (max 32 chars, accepts only any letters, numbers, underscore, dot and dash)</td>
								<td>Specifies a custom order ID</td>
								<td>No</td>
								<td>Generated UUID</td>
							</tr>
							<tr>
								<td>returnCredits</td>
								<td>Bool</td>
								<td>Returns the number of credits used instead of the number of messages. i.e. when message is more than 160 chars long more than one credit is used</td>
								<td>No</td>
								<td>“false”</td>
							</tr>
							<tr>
								<td>returnRemaining</td>
								<td>Bool</td>
								<td>Returs the number of remaining SMSs</td>
								<td>No</td>
								<td>false</td>
								</tr>
								<tr>
								<td>allowInvalidRecipients</td>
								<td>Bool</td>
								<td>Sending to an invalid recipient does not block the operation</td>
								<td>No</td>
								<td>false</td>
							</tr>
							<tr>
								<td>encoding</td>
								<td>String (“gsm” or “ucs2”)</td>
								<td>The <a target="_blank" href="https://en.wikipedia.org/wiki/GSM_03.38">SMS encoding</a>. Use UCS2 for non standard character sets</td>
								<td>No</td>
								<td>“gsm”</td>
							</tr>
								<tr>
								<td>id_landing</td>
								<td>int</td>
								<td>The id of the <em>published</em> page. Also add the <kbd class="pre">%PAGESLINK____________%</kbd> placeholder in the message body</td>
								<td>No</td>
								<td>-</td>
							</tr>
							<tr>
								<td>campaign_name</td>
								<td>String</td>
								<td>The campaign name</td>
								<td>No</td>
								<td>-</td>
							</tr>
							<tr>
								<td>short_link_url</td>
								<td>String</td>
								<td>The url where the short link redirects. Also add the <kbd class="pre">%SHORT_LINK%</kbd> placeholder in the message body</td>
								<td>No</td>
								<td>-</td>
							</tr>
						</tbody></table>
<h2>Returns</h2>
<table>
							<tbody><tr>
							  <td>Code</td>
							  <td>Description</td>
							</tr>
							<tr>
							  <td>200</td>
							  <td>Successful request</td>
							</tr>
							<tr>
							  <td>400</td>
							  <td>Groups could not be found, or other errors, details are in the body</td>
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