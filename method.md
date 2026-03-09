**Lab name: Stored XSS into HTML context with nothing encoded**
<br>
*Link to Lab* https://portswigger.net/web-security/cross-site-scripting/stored/lab-html-context-nothing-encoded
<br><br><br><br><br>
When I enetered the Lab, I was once again presented with a website full of blogs.
<img width="892" height="892" alt="image" src="https://github.com/user-attachments/assets/c854c448-4c4c-4545-ae4b-c6b1de5d0f0e" />
<br>
This site seemed very similar to the previous one but it was missing a search bar. After looking around the site for longer, I discovered that the comments section may be a useful stored XSS entry point.
Once again I decided to use the simple payload:
```
<script>alert()</script>
```
When this is inputed in the "comment" part of the forms submission, an alert popped up an the lab was marked as solved.
However when I later tried placing the same payload into the "name" no alert popped up and due to the format, I was unable to place it into either "website" or "email".
Due to needing to submit a form to trial if a payload works, stored XSS may be riskier when attempting to be stealthy as companies can see the data you have tried inputting.
