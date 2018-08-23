# Wulai Web SDK for JavaScript

## Quickstart

The **Wulai Web SDK** for JavaScript provides a rich set of client-side functionality that: 

- Provides you a live chat tool on your websites.
- Enables you to deploy Wulai chatbot very quickly.
- Helps you to collect users interactions online.

This quickstart will show you how to set up the SDK. If you don't want to set up now, you can explore some samples below.

>**Supported Browsers**
>
>The Wulai Web SDK supports the latest two versions of the most popular browsers: Chrome, Firefox, Edge and Safari (including iOS).

### Basic Setup

The Web SDK for JavaScript doesn't have any standalone files that need to be downloaded or installed, instead you simply need to include a short piece of regular JavaScript in your HTML that will asynchronously load the SDK into your pages. The async load means that it does not block loading other elements of your page.

The following snippet of code will give the basic version of the SDK where the options are set to their most common defaults. You should insert it directly after the opening `<head>` and `<body>` tags on each page you want to load it:

1. After `<head>` tag

```
<script src="http://your-url-address/static/build/wulai.min.js"></script>
```

This is the 1st release of Wulai Web SDK `wulai-1.0.min.js`

2. After `<body>` tag

```
<script>
  var wulai = new WuLai({
    autoOpen:     false,  // is live chat window auto opened，default false
    fullScreen:   false,  // is full screen，default false
    minimize:     0,      // minimize，0-disappear，1-hide at the bottom
    userId:       "",     // User ID
    pubkey:       "XXX",  //
    env:          "prod",
    async:        false,
    userInfo: {
      "extra" : "something"
    }
  });
  wulai.setServiceName("BotName");  // Set the Bot Name

</script>
```

This code will load and initialize the SDK. You must replace the value in *your-url-address* with the url of a specific domain. You can find help with the domain name setup from our support.

## Reference

### Open the Live-chat window

> General usage

`wulai.open()`

> Advanced usage

When you want to change some initialized infomation, you can use `open()` method to fulfill it.

```
wulai.open({
  fullScreen:   true,
  userId:       "XXXXX",
  minimize:     0,
  pubkey:       "XXX", // Wulai key
  env:          "prod", // production or development env
  async:        false,
  userInfo: {
    "extra" : "something"
  }
});
```
