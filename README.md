# [Netlify Form](https://docs.netlify.com/forms/setup/#submit-forms-via-ajax)

> Netlify comes with built-in form handling. Our build bots do it by parsing your HTML files directly at deploy time, so there's no need for you to make an API call or include extra JavaScript on your site.

## HTML forms
```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>netlify HTML Form</title>
  </head>
  <body>
    <div class="app">
      <h1>Netlify HTML Form</h1>
      <form
        name="contact"
        method="POST"
        data-netlify-recaptcha="true"
        data-netlify="true"
      >
        <p>
          <label
            >Your Name: <input type="text" name="name" placeholder="Name"
          /></label>
        </p>
        <p>
          <label
            >Your Email: <input type="email" name="email" placeholder="Email"
          /></label>
        </p>
        <p>
          <label
            >Your Role:
            <select name="role[]" multiple>
              <option value="leader">Leader</option>
              <option value="follower">Follower</option>
            </select></label
          >
        </p>
        <p>
          <label
            >Message:
            <textarea name="message" placeholder="Message" rows="4"></textarea
          ></label>
        </p>
        <p>
          <label>File Upload: <input type="file" name="file"/></label> 
        </p>
        <div data-netlify-recaptcha="true"></div> 
        <p>
          <button type="submit">Send</button>
        </p>
      </form>
    </div>
  </body>
</html>
```

### File Upload
```html
<label>File Upload: <input type="file" name="file"/></label> 
```


### Spam Filters
```html
<form name="contact" method="POST" data-netlify-recaptcha="true" data-netlify="true">
  <p>
    <label>Email: <input type="text" name="name" /></label>
  </p>
  <p>
    <label>Message: <textarea name="message"></textarea></label>
  </p>
  <div data-netlify-recaptcha="true"></div>
  <p>
    <button type="submit">Send</button>
  </p>
</form>
```

### Form Notification
> You can send notifications for verified form submissions from your site dashboard at **Settings > Forms > Form notifications**. These notifications can be sent via email, webhook, or Slack. In the configuration options, you can choose to be notified for a single specific form, or for all verified submissions to any form on your site.

:memo: **참고 자료**   
[https://www.youtube.com/watch?v=6ElQ689HRcY](https://www.youtube.com/watch?v=6ElQ689HRcY)   
[https://www.youtube.com/watch?v=hF7xJhzrr9s](https://www.youtube.com/watch?v=hF7xJhzrr9s)   




