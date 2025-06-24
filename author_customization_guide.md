# 👤 Customize the Author Attribution in the Blogger Theme

This guide explains how to customize the author name and link that appears in the post footer of the MorDictionary Blogger theme. By default, the theme shows posts as authored by "MorMandarin." You can easily replace this with your own Blogger profile.

---

## ⚒️ Step-by-Step Instructions

### 1. Find Your Blogger Profile URL

1. Go to **Settings**  
2. Scroll down to **View Profile** — click on _"View Profile"_  
3. Copy the **Numeric ID** from the hyperlink on the profile page  
4. Paste the **Numeric ID** into the **Create Author Display** JavaScript

![Guide Screenshot: How to Find Your Blogger Numeric ID](Guide%20Screenshots/Guide%20Click%20Here%20to%20Find%20Your%20Bloggers%20Numeric%20ID.png)

![Instruction Screenshot: Put your own numeric ID into the code](Guide%20Screenshots/Put%20your%20own%20numeric%20id%20into%20the%20code%20instruction.png)

![Screenshot: Find "Create Author Display" and put in your Numeric ID](Guide%20Screenshots/Find%20Create%20Author%20Display%20and%20Put%20in%20Your%20Numeric%20ID.png)

---

### 2. Locate the Author Attribution Code

In your Blogger theme's JavaScript section, look for a line that looks like this:

```js
authorDisplay.innerHTML = `<a class='author-name' href='https://www.blogger.com/profile/01795026804926642553' rel='noopener noreferrer' target='_blank'>By: MorMandarin</a>`;
```

---

### 3. Replace It with Your Profile

Change the `href` attribute and display name to your own:

```js
authorDisplay.innerHTML = `<a class='author-name' href='https://www.blogger.com/profile/YOUR_PROFILE_ID' rel='noopener noreferrer' target='_blank'>By: YourName</a>`;
```

#### Example:

```js
authorDisplay.innerHTML = `<a class='author-name' href='https://www.blogger.com/profile/12345678909876543210' rel='noopener noreferrer' target='_blank'>By: Jane Doe</a>`;
```

---

## 🔧 Optional: Where to Place the Code

This script typically lives at the end of the theme's XML or in a separate `<script>` block near the closing `</body>` tag.

You can edit this in **Theme → Edit HTML**.

---

## 🕺 Optional: Dynamic Author Name (Advanced)

If you'd prefer to pull the author name directly from Blogger's system (limited compatibility), you can try:

```xml
<data:post.author.name/>
```

> ⚠️ Note: This works only in HTML widgets, not JavaScript.

---

Happy blogging! 😊

