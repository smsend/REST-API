<a href="https://www.smsend.it/rest-api/" title="smSend developer guide"><img src="https://www.smsend.it/img/visual/smsend-developers.jpg" alt="smSend developer guide" title="smSend developer guide"></a>
<h1><b>smSend Rest-API</b></h1>
<a href="https://www.smsend.it/rest-api/" title="smSend developer guide">https://wwww.smsend.it</a>
<p>The API is divided into subsections, which are briefly described below.</p>
<p>For details about each section, please refer to the respective section.</p>
<p><b>Getting started:</b></p>
<ol><li><a href="https://www.smsend.it/gotolog.aspx">Create an account for free</a></li>
<li>Explore our professional SMS gateway platform</li>
<li><a href="https://www.smsend.it/rest-api/">Explore API documentation</a>
<li>Test your app with our SMS REST API</li>
</ol>
<ol>
  <li>
    <p><b>Authentication:</b><br>
      This section describes how to authenticate requests to the smSend API. All API methods require authentication.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Authentication%20API/Authenticate%20using%20a%20session%20key.md">Authentication  using a session key</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Authentication%20API/Authenticate%20using%20a%20user%20token.md">Authentication  using a user token</a>
      </li>
    </ul>
  </li>
  <li>
    <p><b>User:</b><br>
      The following are utility functions regarding the Authenticated User (e.g. the user status, password reset, etc)</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/User%20API/Dashboard.md">Dashboard</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/User%20API/Verify%20session.md">Verify session</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/User%20API/Reset%20password.md">Reset password</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/User%20API/User%20status.md">User status</a>
      </li>
    </ul>
  </li>
  <li>
    <p><b>Contacts:</b><br>
      This part of the API is used to manage contacts. A contact can be used both in SMS and Email sending, provided that a phone number and/or an email address are given.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20API/Add%20a%20contact.md">Add a contact</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20API/Add%20multiple%20contacts.md">Add multiple contacts</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20API/Get%20a%20contact.md">Get a contact</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20API/Registration%20of%20a%20contact%20to%20a%20list.md">Registration of a contact to a list</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20API/List%20contact%E2%80%99s%20custom%20fields.md">List contact’s custom fields</a>
      </li>
      <li><a href="https://github.com/smsend/REST-API/blob/master/Contacts%20API/Add%20contact%20to%20sms%20blacklist.md">Add contact to sms blacklist</a></li>
      <li><a href="https://github.com/smsend/REST-API/blob/master/Contacts%20API/Add%20multiple%20contacts%20to%20sms%20blacklist.md">Add multiple contacts to sms blacklist</a></li>
      <li><a href="https://github.com/smsend/REST-API/blob/master/Contacts%20API/Add%20phone%20number%20to%20sms%20blacklist.md">Add phone number to sms blacklist</a></li>
    </ul>
  </li>
  <li>
    <p><b>Contacts Groups:</b><br>
      This section describes how groups of contacts are created, updated and deleted. SMS messages and emails can be directly sent to groups of contacts.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20groups%20API/Create%20a%20contacts%20group.md">Create a contacts group</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20groups%20API/Modify%20an%20existing%20contacts%20group.md">Modify an existing contacts group</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20groups%20API/Delete%20a%20contacts%20group.md">Delete a contacts group</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20groups%20API/List%20contacts%20groups.md">List contacts groups</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20groups%20API/Add%20a%20contact%20to%20a%20group.md">Add a contact to a group</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Contacts%20groups%20API/Remove%20a%20contact%20from%20a%20group.md">Remove a contact from a group</a>
      </li>
    </ul>
  </li>
  <li>
    <p><b>TPOA:</b><br>
      Here are described the methods to work with TPOA Aliases (Transmission Path Originating Address, i.e. the SMS Sender Alias). TPOA Aliases can be used only with some specific high quality SMS message types.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/TPOA%20API/Create%20a%20new%20alias.md">Create a new alias</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/TPOA%20API/Get%20all%20aliases.md">Get all aliases</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/TPOA%20API/Get%20a%20specific%20alias.md">Get a specific alias</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/TPOA%20API/Remove%20an%20alias.md">Remove an alias</a>
      </li>
    </ul>
  </li>
  <li>
    <p><b>Sending SMS messages:</b><br>
      This is the part of the API that allows to send SMS messages, to single recipients, saved contacts or groups of contacts.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/SMS%20Send%20API/Send%20an%20SMS%20message.md">Send an SMS message</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/SMS%20Send%20API/Send%20a%20parametric%20SMS%20message.md">Send a parametric SMS message</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/SMS%20Send%20API/Send%20an%20SMS%20message%20to%20a%20group.md">Send an SMS message to a group</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/SMS%20Send%20API/Get%20SMS%20message%20state.md">Get SMS message state</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/SMS%20Send%20API/Delete%20a%20scheduled%20message.md">Delete a scheduled message</a>
      </li>
    </ul>
  </li>
  <li>
    <p><b>SMS messages history:</b><br>
      Used to retrieve the SMS messages sending history.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/SMS%20History%20API/Get%20sent%20SMS%20messages%20history.md">Get sent SMS messages history</a>
      </li>
    </ul>
  </li>
  <li>
    <p><b>SMS Blacklist / Stop SMS:</b><br>
      This section allow to insert and to retrieve the list of SMS blacklist / Stop SMS.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/SMS%20Blacklist%20API/Add%20Phone%20Number%20to%20Blacklist.md">Add Phone Number to Blacklist</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/SMS%20Blacklist%20API/Add%20multiple%20numbers%20to%20sms%20blacklist.md">Add multiple numbers to sms blacklist</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/SMS%20Blacklist%20API/Retrieve%20list%20of%20phone%20numbers%20in%20blacklist.md">Retrieve list of phone numbers in blacklist</a>
      </li>
    </ul>
  </li>
  <li>
    <p><b>Receiving SMS messages:</b><br>
      The methods described in this section are used to retrieve the received SMS messages.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Received%20SMS%20API/Get%20new%20received%20messages.md">Get new received messages</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Received%20SMS%20API/Get%20the%20received%20SMS%20messages.md">Get the received SMS messages</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Received%20SMS%20API/Get%20the%20received%20SMS%20messages%20after%20a%20specified%20message..md">Get the received SMS messages after a specified message</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Received%20SMS%20API/Get%20the%20MO%20received%20messages..md">Get the MO received messages</a>
      </li>
    </ul>
  </li>
  <li>
    <p><b>Landing pages API:</b><br>
      This is the part of the API that regards the Landing Pages service.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Landing%20pages%20API/List%20the%20published%20landing%20pages.md">List the published landing pages</a>
      </li>
    </ul>
  </li>
  <li>
    <p><b>Email Campaign API:</b><br>
      This API exposes methods for creating and managing Email campaigns.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Email%20Campaign%20API/Create%20a%20new%20list.md">Create a new list</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Email%20Campaign%20API/Modify%20a%20list.md">Modify a list</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Email%20Campaign%20API/Get%20list%20of%20campaigns%20by%20statuses.md">Get list of campaigns by statuses</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Email%20Campaign%20API/Add%20a%20contacts%20group%20to%20a%20list%20of%20distribution.md">Add a contacts group to a list of distribution</a>
      </li>
      <li>
       <a href="https://github.com/smsend/REST-API/blob/master/Email%20Campaign%20API/Create%20a%20new%20email%20draft.md">Create a new email draft</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Email%20Campaign%20API/Create%20new%20issue%20using%20a%20specified%20template.md">Create new issue using a specified template</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Email%20Campaign%20API/Send%20an%20issue%20to%20preloaded%20contacts.md">Send an issue to preloaded contacts</a>
      </li>
    </ul>
  </li>
  <li>
    <p><b>Subaccounting:</b><br>
      If enabled as a superaccount, the user can create subaccounts that can be assigned to third-parties. Superaccounts may or may not share credits with their subaccounts.</p>
    <ul>
      <li>
        Get the list of subaccounts
      </li>
      <li>
        Create a subaccount
      </li>
      <li>
        Edit subaccount
      </li>
      <li>
        Change subaccount password
      </li>
      <li>
        Get subaccount
      </li>
      <li>
        Move credits from/to subaccount
      </li>
      <li>
        Get subaccount available credits
      </li>
      <li>
        Get a subaccount’s purchases
      </li>
      <li>
        Create a subaccount purchase
      </li>
      <li>
        Delete a subaccount’s purchase
      </li>
    </ul>
  </li>
  <li>
    <p><b>Two Factor authentication:</b><br>
      This API provides the Two Factor Authentication via SMS.</p>
    <ul>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Two%20Factor%20Authentication%20API/Request%20a%202FA%20Pin.md">Request a 2FA Pin</a>
      </li>
      <li>
        <a href="https://github.com/smsend/REST-API/blob/master/Two%20Factor%20Authentication%20API/Verify%20a%202FA%20Pin.md">Verify a 2FA Pin</a>
      </li>
    </ul>
  </li>
</ol>
