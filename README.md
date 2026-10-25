# CH Media Portfolio: setup guide

This folder is your whole website. Follow the steps below once. After that you add and edit projects from a web page on your own site (`yoursite.netlify.app/admin`), with no coding and no Claude needed.

Everything here is free. You need a GitHub account and a Netlify account.

---

## Part A: Put the files on GitHub

1. Go to **github.com** and create a free account (or sign in).
2. Click the **+** at the top right, then **New repository**.
   - Name it `ch-media` (or anything you like).
   - Choose **Public**.
   - Click **Create repository**.
3. On the new page, click **uploading an existing file**.
4. Unzip this folder on your computer. Select **everything inside it** (the `admin`, `content` and `media` folders plus the other files) and drag it all into the GitHub page.
5. Scroll down and click **Commit changes**.
6. In your repository, open the `admin` folder, then click `config.yml`, then the **pencil icon** (edit).
7. Change this line:

   `repo: YOUR-GITHUB-USERNAME/YOUR-REPO-NAME`

   to your real details, for example `repo: choward05/ch-media`. Click **Commit changes**.

## Part B: Put the site online with Netlify

1. Go to **netlify.com** and sign up with **Continue with GitHub**.
2. Choose **Add new project**, then **Import an existing project**, then **GitHub**, and pick your `ch-media` repository.
3. Leave the build command and publish directory empty. Click **Deploy**.
4. In about a minute your site is live at an address like `something.netlify.app`. It is https automatically.
5. To pick a nicer name: **Project configuration**, then **Change project name**.

## Part C: Turn on the admin login (one time)

The admin page needs GitHub to confirm it's you.

1. On GitHub open **Settings**, then **Developer settings**, then **OAuth Apps**, then **New OAuth App**.
2. Fill in:
   - **Application name:** anything, such as `CH Media Admin`
   - **Homepage URL:** your Netlify site address
   - **Authorization callback URL:** `https://api.netlify.com/auth/done`
3. Click **Register application**. Copy the **Client ID**, then click **Generate a new client secret** and copy that too. GitHub only shows the secret once.
4. In Netlify open your project, then **Project configuration**, then **Security**, then **OAuth**. Under **Authentication Providers** click **Install Provider**, choose **GitHub**, paste the Client ID and Client Secret, and save.

(Netlify sometimes renames menu items. If you can't find one, search "OAuth" in your project settings.)

## Part D: Add and edit projects

1. Go to `your-site.netlify.app/admin` and click **Login with GitHub**.
2. Open **My Site**, then **Portfolio**.
3. Under **Projects**, click **Add projects**. Fill in the title, date and description.
4. Under **Photos and videos**, click **Add**, then upload a file from your computer. For a long video, paste a **YouTube or Vimeo link** instead (see tips below).
5. Click **Publish**, then **Publish now**. Your site updates in about a minute.

The same page edits the headline, intro, About text, focus tags and contact line.

## Tips and limits

- **Video size:** GitHub rejects files over 100 MB, and big files slow your site. Keep uploaded videos under about 50 MB. For anything longer, upload to YouTube (set it to Unlisted if you want) and paste the link. It plays inside your site.
- **Photos:** resize them to about 2000 pixels wide before uploading so pages load fast.
- **Who can log in:** only people with write access to your GitHub repository.
- **Deleting a project:** remove it in the admin page. The file stays in the `media/uploads` folder on GitHub until you delete it there.

## Your own web address and Google

- **Own domain:** buy one from a registrar such as Cloudflare, Namecheap or Porkbun (about $10 to $20 a year). In Netlify open **Domain management** and click **Add a domain**. https is set up for you at no extra cost.
- **Google:** go to **search.google.com/search-console**, add your site address, and use **URL Inspection** to request indexing. It usually takes a few days to a couple of weeks before the site shows up in search.

---

## What's in this folder

| File | What it does |
| --- | --- |
| `index.html` | The website itself |
| `content/site.json` | All your text and project list (the admin page edits this) |
| `media/uploads/` | Your photos and videos |
| `admin/` | The admin page and its settings |
| `logo.png`, `favicon.png` | Your CH logo |
| `robots.txt` | Tells Google it may read the site |
