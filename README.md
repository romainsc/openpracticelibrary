# Open Practice Library

## About

The [Open Practice Library](https://rht-labs.github.io/practice-library/) provides information about practices and ideas that we use here at Red Hat Open Innovation Labs. To learn more about the philosophy behind the library, see [about.md](content/page/about.md).

## Adding Content (Content Writers)
### Pre-requisites
#### Github
To create or edit a practice, you will need a [Github](https://github.com) account. You don't need to have any content in Github as it is only used for authentication purposes.

#### Template
A simple template is shown below which contains some example headers for use within the practice library.

|Header|Comment|
|----------------|--------|
|What is it?| A brief description of the practice|
|Why use it?| A short paragraph describing the use case(s) for the use of this practice. |
|How does it fit? | Relevant section(s) of the Open Practice Library for which this practice can be used|
|Who do you need?| A list of personas or roles required to run the practice.|
|Suggested Time| A rough idea of how long it will take to complete this practice.  Some practices can be quite short (such as the Daily Standup which will only last 10-15 minutes)|
|Difficulty| From the point of view of facilitator and participants, how hard is this practice? A simple "Easy", "Medium" and "Hard" will suffice.|
|Materials Needed|What materials are required to run the practice? For example, a large whiteboard, sticky notes, whiteboard markers etc|
|How to use|A step-by-step guide on how to run the practice|
|Related Practices| Which practices can be used in conjunction, before or after this practice|

### Creating Content

<b>Before you continue, please check the Pre-Requisites above (for example, that you have a valid GitHub.com account)</b>

We are using [Netlify](https://www.netlify.com/) as the backend CRM and all content will be added here.  No technical knowledge is required as the interface is fairly WYSIWYG.
- Visit <a href="https://quirky-benz-f1ebba.netlify.com/admin/" target=_blank>Netifly Admin Page </a> and click "Login with Netifly Identity".
- Select "Continue with GitHub" and enter your Github credentials.
- Click "New Practices".
- Fill in the Title with the name of your Practice.  Leave the publish date as is.
- You can either use Rich Text or Markdown format for the content.  Rich Text could be easier for non-technical people and you can use the style icons at the top of the Body section to add headers and formatting.

Once you have added your content, click the blue "Save" button at the top of the screen.

Change the Status to "In Review".

This will raise a pull request on the underlying Github repository which can then be actioned by one of the site moderators.  

<b>If you try to publish the Practice yourself, you will see an error as it needs to be curated by a moderator.</b>

<b>You will receive emails once the content has been actioned. </b>

These actions could be to add/change or content if everything is good, you will receive and email saying that the content has been merged (accepted in to the library).

### Editing Content
You can use the first steps in the above workflow to edit content.  Select the practice you wish edit.  Don't forget to update the date and click "Save" once you have edited the content.  

An email will be sent to the moderators who will approve the change.

## Publishing Content (Moderators)
As a moderator, you will receive and email to say that new content has been added:
<pre>
Automatically generated by Netlify CMS
You can view, comment on, or merge this pull request online at:

  https://github.com/openpracticelibrary/practice-library-test/pull/9
Commit Summary

    Create Practices “chrisj-test-of-workflow”

File Changes

    A content/practices/chrisj-test-of-workflow.md (5)

Patch Links:

    https://github.com/openpracticelibrary/practice-library-test/pull/9.patch
    https://github.com/openpracticelibrary/practice-library-test/pull/9.diff

—
You are receiving this because you are subscribed to this thread.
Reply to this email directly, view it on GitHub, or mute the thread.
</pre>

 - Go to the [Pull Request Page](https://github.com/openpracticelibrary/practice-library-test/pulls) and click on the relevant pull request.  
 - To see what have been added, go to the "Files changed" tab.
 - If you require more information or would like changed to be made, write the comment in the "Leave a Comment" box.  

 <i>Note: Add @username in the comment so the originator receives the email.  The originators user name can be found in the "Commits" tab.</i>
 - If you are happy with the content and there are no conflicts, click the "Merge pull Request" button followed by the "Confirm Merge" button.  Add some additional comments if required.
 - Once merged, you can delete the branch (this will hopefully be automated at some point).  Click the "Delete Branch" button.
 - If you go back to the [List of Practices](https://quirky-benz-f1ebba.netlify.com/admin/#/collections/practices) you should see the newly added practice.
 - Change the status of the Practice from "In Review" to "Ready".  

 <i>Note: The order is a little quirky at the moment - not sure why.  It's mainly alphabetical with a few exceptions.</i>


<hr>
### Previous README.

## Practices

Create a new markdown file in `/content/practices`. If you have hugo installed, you can run `hugo new practices/my_new_practice.md`.

## Pages

Create a new markdown file in `/content/pages`. If you have hugo installed, you can run `hugo new pages/my_new_page.md`.

### Drafts

Content is created in draft status by default. To publish, set `draft: false` in the front matter or run `hugo undraft`. For example, typing `hugo undraft page/my_new_page.md` will publish the corresponding page.

### Style

These style guidelines apply to the Markdown files in the `/content` directory.

- Use hyphens, not underscores, to separate parts of a filename. (The filenames are turned into URLs when the site is built.)
- Where possible, avoid putting HTML in Markdown. Exception: the `<sup>` tag and anchors, which we're using for footnotes.
- When linking to external sites, place the link into an "external references" section, and use a footnote anchor to point to the link.
- Don't put the document's title into a heading (`# My Title`). Instead, just include the title in the document's front matter (`title: my title`).

## Developing

Open Practice Library is built with [Hugo](http://gohugo.io/) and the [Minimo theme](https://minimo.netlify.com/). To run it locally:

1. Check out this repo.
2. [Install Hugo](https://gohugo.io/getting-started/installing/).
3. [Install Node.js](https://nodejs.org/en/download/).
4. Run `git submodule update --init --recursive` to download the theme.
5. Navigate to the top level of the repo.
6. Run `npm install` to install the npm packages.
7. Run `npx grunt-cli lunr-index` to build the search index.
8. Run `hugo server` to run the site locally.

Alternately, you can run `hugo server -D` to preview drafts.

### Deploying

The site is [published to GitHub pages](https://help.github.com/articles/configuring-a-publishing-source-for-github-pages/#publishing-your-github-pages-site-from-a-docs-folder-on-your-master-branch) using a `docs` directory on the master branch.

To push changes to GitHub pages, follow steps 1-6 of the "developing" instructions, then:

1. Delete the `docs` directory. (Hugo won't delete old files by default.)
2. Run `npx grunt-cli lunr-index` to build the search index.
3. Run `hugo` (without any parameters) to rebuild the `docs` directory.
4. Add, commit, and push these changes.
5. Create a pull request.
6. Merge to master, or ask someone else to merge to master.

Once the changes are merged up, the new content will be deployed automatically.
