<h1>Two Factor Authentication API</h1>
<p>This is the part of the API that provides the Two Factor Authentication. The flow of 2FA is:</p>
<ul>
<li>The User specifies his number in your App.</li>
<li>Your App sends a 2FA request via API.</li>
<li>The platform sends a text message to the specified recipient.</li>
<li>User receives the PIN via text message</li>
<li>User enters the PIN in your App.</li>
<li>Your App sends the 2FA verify via API and receives the authorization or an invalid pin error.</li>
<p>The text message is sent with the highest quality on a preferred route, to guarantee a quick delivery.</p>
<blockquote>Remember to provide the authentication HTTP headers as described in the Authenticate using a session key and the Authenticate using a user tokeny sections.</blockquote>
<blockquote>All the query string parameters in URL must be UTF-8 URL Encoded.</blockquote>