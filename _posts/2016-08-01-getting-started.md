---
layout: post
title: Getting started
---

If you just want to download an image and display it, showing a placeholder until it comes, use a SimpleDraweeView.

But before that, you need to initialize the ASS SDK class. You should only call ASSSDK.initialize once. Your Application class would be a good place. Doing it in each Activity is wrong.

{% highlight js %}
[MyApplication.java]
public class MyApplication extends Application {
	Override
	public void onCreate() {
		super.onCreate();
		ASSSDK.initialize(this);
	}
}
{% endhighlight %}

You need to specify your application class in the XML. For images from the network, you will also need to request Internet permission from your users. Your AndroidManifest.xml should look something like this:
