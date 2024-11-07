---
icon: arrow-down-to-arc
layout:
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# Installation

### Step 1: Create a new Unity project

* **Suggested Unity version**: 2022.3.3 or higher
* [**Suggested template**](#user-content-fn-1)[^1]: URP (Universal Rendering Pipeline)

<figure><img src="../.gitbook/assets/1730945956416.png" alt=""><figcaption></figcaption></figure>

### Step 2: Import UPM package

The latest Penguin Action Toolkit package is published on GitHub, and you can use either way below to download and import it to your project.

#### <mark style="color:orange;">Add package from git URL</mark>

1. Open the **Package Manager** window (Window -> Package Manager)
2. Click the **add** ![](https://docs.unity3d.com/2022.3/Documentation/uploads/Main/iconAdd.png) button in the status bar on the left corner. The options for adding packages appear.
3. Select **Add package from git URL** from the add menu.
4. Copy and paste the git link of the latest released package. \
   Please make sure the link is ended with "#pat"
5. Click **Add** and wait for about 2-3 minutes.&#x20;

#### <mark style="color:orange;">Add package from disk</mark>

1. Download the latest released package from GitHub. Make sure you have **unzipped** it.
2. Open the **Package Manager** window (Window -> Package Manager)
3. Click the **add** ![](https://docs.unity3d.com/2022.3/Documentation/uploads/Main/iconAdd.png) button in the status bar on the left corner. The options for adding packages appear.
4. Select **Add package from disk** from the add menu to bring up a file browse.&#x20;
5. Click _package.json_ in your unzipped folder to import the package.&#x20;

### Step 3: Import the sample assets

Since we do encourage our users to modify the core scripts, it would be better for all the assets to be mutable. Before using PAT, please make sure you've imported the <mark style="color:orange;">**General Resources**</mark> in the Samples panel.&#x20;

<figure><img src="../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>





[^1]: otherwise some demo assets may not work properly