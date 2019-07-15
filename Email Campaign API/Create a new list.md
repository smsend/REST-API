<h1>Create a new list</h1>
<p>Create a new sending list.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user token sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>
<hr>
<h2>HTTP Headers</h2>
<pre><code>user_key / Session_key</code></pre>
<h2>HTTP Method</h2>
<pre><code>POST</code></pre>
<h2>HTTP Request</h2>
<pre><code>https://app.gateway.smsend.it/API/v1.0/REST/list</code></pre>
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
                              <td>title</td>
                              <td>String</td>
                              <td>The list name</td>
                              <td>Yes</td>
                              <td>-</td>
                            </tr>
                            <tr>
                              <td>id_language</td>
                              <td>String (e.g. “ita”)</td>
                              <td>The list default language</td>
                              <td>Yes</td>
                              <td>-</td>
                            </tr>
                            <tr>
                              <td>email_sender</td>
                              <td>a valid email</td>
                              <td>The sender’s email address</td>
                              <td>Yes</td>
                              <td>-</td>
                            </tr>
                            <tr>
                              <td>reply_to</td>
                              <td>a valid email</td>
                              <td>The email to be used for the ‘reply_to’ email field</td>
                              <td>Yes</td>
                              <td>-</td>
                            </tr>
                            <tr>
                              <td>company_name</td>
                              <td>String</td>
                              <td>The company name</td>
                              <td>Yes</td>
                              <td>-</td>
                            </tr>
                            <tr>
                              <td>company_address</td>
                              <td>String</td>
                              <td>The company address</td>
                              <td>Yes</td>
                              <td>-</td>
                            </tr>
                            <tr>
                              <td>company_url</td>
                              <td>String</td>
                              <td>The company website URL</td>
                              <td>Yes</td>
                              <td>-</td>
                            </tr>
                            <tr>
                              <td>company_phone</td>
                              <td>String</td>
                              <td>The company phone number</td>
                              <td>Yes</td>
                              <td>-</td>
                            </tr>
                            <tr>
                              <td>company_fax</td>
                              <td>String</td>
                              <td>The company FAX number</td>
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
                                  <td>201</td>
                                  <td>List created, The HTTP location header that points to the created list</td>
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