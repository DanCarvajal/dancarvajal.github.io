---
layout: post
title: Styling TinyLetter's Signup Form
author: Dan Carvajal
---
[TinyLetter](https://tinyletter.com/) is an email newsletter service from Mailchimp that I use for my personal email newsletter. I really enjoy its minimalist nature but it's weak on the styling features for it's signup form. Obviously I wanted to take a crack at styling it which it turns out it's a pretty easy process. Here's a quick breakdown of how to go about styling Tinyletter's signup form.

## Tinyletter's Basic Signup Form

Tinyletter off the bat gives you a basic embeddable signup form (which looks like a holdover from 2005 era Blogger). This certainly would not do for a respectable establishment like dancarvajal.com.

Let's start with their base code below.
{% highlight html %}
<form style="border:1px solid #ccc;padding:3px;text-align:center;" action="https://tinyletter.com/DanCarvajal" method="post" target="popupwindow" onsubmit="window.open('https://tinyletter.com/DanCarvajal', 'popupwindow', 'scrollbars=yes,width=800,height=600');return true">
  <p>
    <label for="tlemail">Enter your email address</label></p><p><input type="text" style="width:140px" name="email" id="tlemail" />
  </p>
  <input type="hidden" value="1" name="embed"/><input type="submit" value="Subscribe"/>
  <p>
    <a href="https://tinyletter.com">powered by TinyLetter</a>
  </p>
</form>
{% endhighlight %}

This is a very basic signup form with the expected structure for its `<form>` and `<input>` tags. It turns out there are only two pieces of their code that you actually need for making your own form.

First you need the opening form markup with everything within the `style` attribute stripped out:
{% highlight html %}
<form action="https://tinyletter.com/DanCarvajal" method="post" target="popupwindow" onsubmit="window.open('https://tinyletter.com/DanCarvajal', 'popupwindow', 'scrollbars=yes,width=800,height=600');return true">
{% endhighlight %}
This markup holds all the event action information that TinyLetter needs to get user emails from your website into their newsletter list.

Second you'll need TinyLetter's `id` attribute for the text `<input>` tag, which looks like this:
{% highlight html %}
<input id="tlemail" />
{% endhighlight %}
This `id` attribute is what TinyLetter actually looks for because it's applied to the whatever text `<input>` type you choose for users to type in their email.

The last thing you'll need for your form is some sort of utilization of the `type="submit"` attribute in your code, whether it's applied to a `<button>` or another `<input>` tag.

With these basic elements you can build a signup form however you choose to with regular html and css styles.

##My Tinyletter Form

Below is my redo of the Tinyletter signup form markup.

{% highlight html %}
<div class="row">
  <div class="col-lg-8 col-md-offset-2">
    <form class="form-inline" role="form" action="https://tinyletter.com/DanCarvajal" method="post" target="popupwindow" onsubmit="window.open('https://tinyletter.com/DanCarvajal', 'popupwindow', 'scrollbars=yes,width=800,height=600');return true">
      <div class="form-group">
        <label class="control-label" for="email">Sign Up for Updates</label>
        <input type="email" class="form-control" name="email" id="tlemail" placeholder="your email">
      </div>
      <button type="submit" class="btn btn-default">Submit</button>
    </form>
  </div>
</div>
{% endhighlight %}

You can see I reused the basic `<form>` element from the TinyLetter markup and then applied `id="tlemail"` attribute to my `<input type="email">` tag rather than TinyLetter's `<input type="text">`.

Since this site utilizes the Bootstrap3 framework I utilized bootstrap's `form-inline` class to get the horizontal look I wanted as well as lots of Bootstrap's other from elements that I learned about at  [W3Schools.](http://www.w3schools.com/bootstrap/bootstrap_forms.asp).

Finally I customized the CSS styling in my main custom style sheet ([which you can see here](https://github.com/DanCarvajal/dancarvajal.github.io/blob/master/_sass/_dan_awesome_sauce.scss)).

After all my changes were made I ended up with this:

{% include newsletter.html %}

So that is how you can style Tinyletter's signup form. I really hope this was a helpful guide and that it gives you confidence to poke around in other people's code to learn how things work. Much like a lot of the web it turns out rudimentary styling is pretty easy some with basic html and css knowledge. While you're still here why not sign up for my newsletter?
