---
title: jack deploy
---

So far we have been using an empty folder as our project to mainly demonstrate jack's ability to download and manage configuration files.  Jack can also deploy application code to the Elastic Beanstalk environment.  For this next step, we will deploy a small test sinatra app available on GitHub at [tongueroo/sinatra](https://github.com/tongueroo/sinatra).

Clone the project and cd into it:

```sh
git clone https://github.com/tongueroo/sinatra.git
cd sinatra
```

Now we can use the `jack deploy` command to deploy the app:

```sh
jack deploy hi-web-stag
```

You should see similiar output below:

<img src="/img/tutorials/jack-deploy.png" class="doc-photo" />

The jack deploy command simply is a wrapper command to the `eb deploy` command.  If you need to pass `eb deploy` options down through to the underlying command you can use the `EB_OPTIONS` environment variable.  Here's an example:

```sh
EB_OPTION='--nohang' jack deploy hi-web-stag
```

<a id="prev" class="btn btn-basic" href="{% link _docs/jack-diff.md %}">Back</a>
<a id="next" class="btn btn-primary" href="{% link _docs/jack-terminate.md %}">Next Step</a>
<p class="keyboard-tip">Pro tip: Use the <- and -> arrow keys to move back and forward.</p>

