## Addressing the Performance Inequality Gap

## The Mobile Performance Inequality Gap, 2021

### Setting the Benchmarks

Alex Russel, a lead performance developer at Google is a firm believer in “an internet for everyone”. He highlights this in a poignant  [Chrome Dev Summit talk in 2016](https://www.youtube.com/watch?v=4bZvq3nodf4)  where he showed that when we construct the digital world to the limits of the best devices, we build a less usable one for  [80+% of the world’s users](https://www.idc.com/promo/smartphone-market-share/os) .

Since things have changed since 2016, the updated golden web performance standard to achieve now is **~100KiB of HTML/CSS/fonts and ~300-350KiB of JS** (**gzipped**). This rule-of-thumb limit typically lasts about two years and is a hard target to meet. Most modern development tooling easily surpasses this amount in lieu of providing a robust and intuitive developer experience but there is a high cost in doing so if you’re attempting to cater to an international market, as the data suggests.

> Your company’s poor site performance can manifest as lower engagement, higher bounce rates, or a reduction in conversions.

### Business Impacts

The harmful business impact of poor performance is constantly re-validated. Big decreases in performance predictably lead to (somewhat lower) decreases in user engagement and conversion. The scale of the effect can be deeply situational or hard to suss out without solid metrics, but it’s there. When doing user research, Google’s Web Team found some interesting patterns:

- Users hate delays and unreliability on mobile: the level of stress caused by mobile delays is  [comparable to watching a horror movie](https://blog.hubspot.com/marketing/mobile-website-load-faster) .

- Fifty percent of smartphone users are more likely to use a company’s mobile site when browsing or shopping because they  [don’t want to download an app](https://www.thinkwithgoogle.com/data/smartphone-user-mobile-shopping-preferences/) .

- One of the top reasons for uninstalling an app is the  [limited storage](https://www.thinkwithgoogle.com/data/why-users-uninstall-travel-apps/)  (whereas an installed PWA usually takes less than 1MB).

- Smartphone users are more likely to purchase from mobile sites that  [offer relevant recommendations](https://www.thinkwithgoogle.com/data/smartphone-mobile-app-and-site-purchase-data/) on products, and 85% of smartphone users say  [mobile notifications are useful](https://www.thinkwithgoogle.com/data/smartphone-user-notification-preferences/).

### Google's approach to this problem?

According to those observations, Google found that customers prefer experiences that are **fast, installable, reliable, and engaging** (**F.I.R.E.**)! This means companies need to be laser-focused when it comes to performance budgeting. Check out the average device capability worldwide.

> From 2017 data, the default global baseline is a ~$200 Android device on a 400Kbps link with a 400ms round-trip time (“RTT”). This translates into a budget of ~130-170KB of critical-path resources, depending on composition — the more JS you include, the smaller the bundle must be.

The single most important thing to understand about the landscape of devices your sites will run on is that they are not new phones. Two numbers set the stage:

- 45% of  [mobile connections occur over 2G worldwide](https://goo.gl/fDkY1g) 

- 75%  [of connections occur on either 2G or 3G](https://goo.gl/fDkY1g) 

*The median user is on a slow network.* Just how slow is a matter of some debate.

This makes some intuitive sense: smartphones are not in their first year (and haven’t been for more than a dozen years), and most users do not replace their devices every year. Most smartphone sales today are replacements (that is, to users who have previously owned a smartphone), and the longevity of devices continues to rise.

The worldwide device replacement average is  [now 33 months](https://www.statista.com/statistics/786876/replacement-cycle-length-of-smartphones-worldwide/) . In markets near  [smartphone saturation](https://www.theverge.com/2019/1/3/18166399/iphone-android-apple-samsung-smartphone-sales-peak) , that means we can expect the median device to be nearly 18 months old.

## PWAs leverage modern web capabilities

How we can solve this issue of performance inequality? By recognizing the issue within our own products and services and using Progressive Web Applications as a way to overcome some technical obstacles and deliver performative, highly optimized apps quickly and effectively. 

**Progressive Web Apps (PWAs)** are web apps that use [service workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API), [manifests](https://developer.mozilla.org/en-US/docs/Web/Manifest), and other web-platform features in combination with [progressive enhancement](https://developer.mozilla.org/en-US/docs/Glossary/Progressive_Enhancement) to give users an experience on par with native apps.

PWAs provide a number of [advantages](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#advantages_of_web_applications) to users — including being [installable](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#installability), [progressively enhanced](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#progressive_enhancement_support), [responsively designed](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#responsiveness), [re-engageable](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#re-engageability), [linkable](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#linkability), [discoverable](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#discoverability), [network independent](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#network_independence), and [secure](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#secure).


![Progressive Web Apps Offline Users’ Journey](https://cdn.hashnode.com/res/hashnode/image/upload/v1641673515707/I-52YJII5.jpeg)

PWAs are not created with a single technology. They represent a new philosophy for building web apps, involving some specific patterns, APIs, and other features. It's not that obvious if a web app is a PWA or not from first glance. An app could be considered a PWA when it meets certain requirements, or implements a set of given features: works offline, is installable, is easy to synchronize, can send push notifications, etc.

There are some key principles a web app should try to observe to be identified as a PWA. It should be:

- [Discoverable](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#discoverability), so the contents can be found through search engines.

- [Installable](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#installability), so it can be available on the device's home screen or app launcher.

- [Linkable](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#linkability), so you can share it by sending a URL.

- [Network independent](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#network_independence), so it works offline or with a poor network connection.

- [Progressively enhanced](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#progressive_enhancement_support), so it's still usable on a basic level on older browsers, but fully functional on the latest ones.

- [Re-engageable](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#re-engageability), so it's able to send notifications whenever there's new content available.

- [Responsively designed](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#responsiveness), so it's usable on any device with a screen and a browser—mobile phones, tablets, laptops, TVs, refrigerators, etc.

- [Secure](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#secure), so the connections between the user, the app, and your server are secured against any third parties trying to get access to sensitive data.

Offering these features and making use of all the [advantages](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Introduction#advantages_of_web_applications) offered by web applications can create a compelling, highly flexible offering for your users and customers all while keeping the performance inequality gap top of mind.

### Is it worth doing all that?

Absolutely! With a relatively small amount of effort required to implement the core PWA features, the benefits for people using older and slower devices are huge. For example:

- A decrease in loading times after the app has been installed, thanks to caching with [service workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API), along with saving precious bandwidth and time. PWAs have near-instantaneous loading (from the second visit).

- The ability to update only the content that has changed when an app update is available. In contrast, with a native app, even the slightest modification can force the user to download the entire application again.

- A look and feel that is more integrated with the native platform—app icons on the home screen or app launcher, applications that automatically run in full-screen mode, etc.

- Re-engaging with users through the use of system notifications and push messages, leading to more engaged users and better conversion rates.

It's well worth trying out a PWA approach, so you can see for yourself if it works for your app.

## Advantages of web applications

A fully-capable progressive web application should provide all of the following advantages to the user.

### Discoverability

The eventual aim is that web apps should have better representation in search engines, be easier to expose, catalogue and rank, and have metadata usable by browsers to give them special capabilities.

Some of the capabilities have already been enabled on certain web-based platforms by proprietary technologies like [Open Graph](https://ogp.me/), which provides a format for specifying similar metadata in the [HTML](https://developer.mozilla.org/en-US/docs/Glossary/HTML) [<head>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/head) block using [<meta>](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/meta) tags.

The relevant web standard here is the [Web app manifest](https://developer.mozilla.org/en-US/docs/Web/Manifest), which defines features of an app such as name, icon, splash screen, and theme colours in a [JSON](https://developer.mozilla.org/en-US/docs/Glossary/JSON)-formatted manifest file. This is for use in contexts such as app listings and device home screens.

### Installability

A core part of the web app experience is for users to have app icons on their home screen, and be able to tap to open apps into their native container that feels nicely integrated with the underlying platform.

Modern web apps can have this native app feel via properties set inside the Web app manifest, and via a feature available in modern smartphone browsers called [web app installation](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Installing).

### Linkability

One of the most powerful features of the web is the ability to link to an app at a specific URL without the need for an app store or a complex installation process. This is how it has always been.

### Network independence

Modern web apps can work when the network is unreliable, or even non-existent. The basic ideas behind network independence are to be able to:

Revisit a site and get its contents even if no network is available.

Browse any kind of content the user has previously visited at least once, even under situations of poor connectivity.

Control what is shown to the user in situations where there is no connectivity.

This is achieved using a combination of technologies: [Service Workers](https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API) to control page requests (for example storing them offline), the [Cache API](https://developer.mozilla.org/en-US/docs/Web/API/Cache) for storing responses to network requests offline (very useful for storing site assets), and client-side data storage technologies such as [Web Storage](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API) and [IndexedDB](https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API) to store application data offline.

### Progressive enhancement support

Modern web apps can be developed to provide an excellent experience to fully capable browsers, and an acceptable (although not quite as shiny) experience to less capable browsers. We've been doing this for years with best practices such as [progressive enhancement](https://developer.mozilla.org/en-US/docs/Glossary/Progressive_Enhancement). By using progressive enhancement, PWAs are cross-browser. This means developers should take into account the differences in the implementation of some PWA features and technologies between different browser implementations.

### Re-engage ability

One major advantage of native platforms is the ease with which users can be re-engaged by updates and new content, even when they aren't looking at the app or using their devices. Modern web apps can now do this too, using new technologies such as Service Workers for controlling pages, the [Web Push API](https://developer.mozilla.org/en-US/docs/Web/API/Push_API) for sending updates straight from server to app via a service worker, and the [Notifications API](https://developer.mozilla.org/en-US/docs/Web/API/Notifications_API) for generating system notifications to help engage users when they're not actively using their web browser.

### Responsiveness

Responsive web apps use technologies like [media queries](https://developer.mozilla.org/en-US/docs/Web/CSS/Media_Queries) and [viewport](https://developer.mozilla.org/en-US/docs/Glossary/Viewport) to make sure that their UIs will fit any form factor: desktop, mobile, tablet, or whatever comes next.

### Secure

The web platform provides a secure delivery mechanism that prevents snooping while simultaneously ensuring that content hasn’t been tampered with, as long as you take advantage of [HTTPS](https://developer.mozilla.org/en-US/docs/Glossary/https) and develop your apps with security in mind.

It's also easy for users to ensure that they're installing the right app because its URL will match your site's domain. This is very different from apps in app stores, which may have several similarly-named apps, some of which may even be based on your site, which only adds to the confusion. Web apps eliminate that confusion and ensure that users get the best possible experience.