# 👤 Customize the Author Attribution in the Blogger Theme

This guide explains how to customize the author name and link that appears in the post footer of the MorDictionary Blogger theme. By default, the theme shows posts as authored by "MorMandarin." You can easily replace this with your own Blogger profile.

---

## ⚒️ Step-by-Step Instructions

### 1. Find Your Blogger Profile URL

1. Go to [https://www.blogger.com/edit-profile.g](https://www.blogger.com/edit-profile.g)
2. Locate your Blogger **Profile URL** in the page. It should look like:
   ```
   https://www.blogger.com/profile/12345678901234567890
   ```

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

