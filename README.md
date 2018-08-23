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
<script src="http://server.url/static/build/wulai.min.js"></script>
```

2. After `<body>` tag

```
<script>
  var wulai = new WuLai({
    autoOpen:     true,   // 是否自动打开，默认false
    fullScreen:   false,  // 是否全屏，默认false
    minimize:     0,      // 最小化方式，0表示消失，1表示最小化到底部
    userId:       "",     // 用户ID
    userInfo: {
      "campaign": {
        "gclid":        "gcl_id_123",
        "utm_source":   "source_a",
        "utm_medium":   "medium_b",
        "utm_campaign": "utm_campaign_c",
        "utm_term":     "term_x",
        "utm_content":  "content_y"
      }
    }
  });
  wulai.setServiceName("BotName");

</script>
```
