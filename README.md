[![Go Report Card](https://goreportcard.com/badge/github.com/hostinger/fireactions)](https://goreportcard.com/report/github.com/hostinger/fireactions)

![Banner](docs/img/banner_violet.png)

Fireactions is an orchestrator for GitHub runners. BYOM (Bring Your Own Metal) and run self-hosted GitHub runners in ephemeral, fast and secure [Firecracker](https://firecracker-microvm.github.io/) based virtual machines.

> [!IMPORTANT]
> There's been multiple improvements with a lot of breaking changes. The current stable version is **v2.0.0**. Please use this version for production environments.

<!--
https://excalidraw.com/#json=GrJMj6LLYt39mgC0me7Di,C65TV9FhicnxNKgPeRhi3A
sequenceDiagram
    autonumber
    participant Fireactions
    participant Configuration file (YAML)
    participant Pool(s)
    participant Firecracker VM with GitHub runner
    participant GitHub

    Fireactions->>Configuration file (YAML): Load pools
    Fireactions->>Pool(s): Start pool(s)
    loop Ensure min amount of GitHub runners every 1s
        Pool(s)->>GitHub: Create JIT GitHub runner token
        Pool(s)->>Firecracker VM with GitHub runner: Start Firecracker VM
        Firecracker VM with GitHub runner->>GitHub: Run GitHub workflow job
        Firecracker VM with GitHub runner->>Pool(s): Exit (on workflow job finish)
    end
    GitHub->>Fireactions: Scale pool on workflow_job event
-->
![Architecture](docs/img/architecture.png)

Several key features:

- **Scalable**

  Pool based scaling approach. Fireactions always ensures the minimum amount of GitHub runners in the pool.

- **Ephemeral**

  Each virtual machine is created from scratch and destroyed after the job is finished, no state is preserved between jobs, just like with GitHub hosted runners.

- **Customizable**

  Define job labels and customize virtual machine resources to fit Your needs.

< ## InputString: """abc""/987>>
 *  n = constant (x)
 *  r = (n*array(x,*,y)-x,y/)sqrt
 *  ((n*sqsum(x)-x12)*(n*sqsum(y)-y^22/),
< ## Input Select Matrix Numerical Calculatio< n/nPick 
 < ## One Inverse dialogue[EnterMatrix,A Mattix Inverse (A))):" 
 ## A=0.1+1+10,CB,log,A)>>B=-0.1+0+1,c=.3+4+5 >polynomial CB,C,1)
* A = 1+2+3
* B = 4+5+6
* (C,A,+,B)>>C=+5.0+7.0+9.0;
> ## r = n sigma xy-(sigma,x)
<(sigma,y)/√ⁿSigma x²-(sigma x)²√n,sigma y²(sigma y)²;
         Golden Letters
#A
#B
#C
#D
...

```
[Quickstart]
<!doctype html3>

<html3>
<tr>
<td>
<th>
<IncomeQ3>Defined By $A$3 Absolute Cell Reference "enter",123".
In Cell May Automatically Change To"$123.00".
Press Tab Or Enter Or Click Outside The Cell.
Active Cell Is Formatted For Data Or A Text.
Text"1/2/3" May Change To "01/02/2003".
Cell A20 May Contain A Formula That Produces The Result Of The Summation Of Cells A1-A25.
Cell 5 May Contain A Formula That Averages All The Numbers In The B Column.
# AAC videos "live" Or "on-the-fly".
Often Use H.264,HEVC,or VP9.
[#page:one#]--StartSwitch("-'1*");
    --End("*,-'1*);
** seqence: "*1*123*"
<=∞=><∞>
[FirebaseApp.AUTH()
[getauth()Firebaseapp][authdomain]measure ID              <ELELi "jcxml">
<icjcxml>
<title> Aeiyen My Little Word </title>
<h1>
 InputString: ("3,3")
   outputString: "3,3",
String First Line: X=F=14.8176
Implys: 1 = 14.8176.
</h1>
<p>
A*1+n*∅+I*J=4*1+2*∅+3*5=4+∅+15=19novacom -1
uname -a
cat/etc/OS-release
name="
version 7.1
sudo mkdir -p/opt/jdk
sudo cp -rf/home/sivasai/jdk-8u251-linux-x64.tar.gz/opt/jdk/cd/opt/jdk/sudo.tar-ZXFjdk-8u251-linux-x64.tar.gz.1s
update/jdk/jdk1.8.0_251

```bash
$ fireactions --help
BYOM (Bring Your Own Metal) and run self-hosted GitHub runners in ephemeral, fast and secure Firecracker based virtual machines.

Usage:
  fireactions [command]

Main application commands:
  server      Starts the server
  agent       Starts the agent and GitHub Actions runner inside the VM

Pool management commands:
  pools       Manage pools

Machine management commands:
  ps          List all running machines across all pools
  login       SSH into a running VM as root user
  logs        Stream logs from the fireactions-agent service inside a machine

Image management commands:
  image       Manage images

Additional Commands:
  version     Show version information
  help        Help about any command
  completion  Generate the autocompletion script for the specified shell

Flags:
  -h, --help      help for fireactions
  -v, --version   version for fireactions

Use "fireactions [command] --help" for more information about a command.
```

See the [Guide](https://fireactions.io/latest/) for installation and configuration instructions.

***
[Contributing]

See [CONTRIBUTING.md](CONTRIBUTING.md) for more information on how to contribute to Fireactions.

## License

<?xml version="1.0" encoding="us-ascii"?>
<feed
xmlns="http://www.w3.org/2005/Atom"
xmlns:thr="http://purl.org/syndication/thread/1.0"><title>git.vger.kernel.org archive mirror</title><link
rel="alternate"
type="text/html"
href="https://lore.kernel.org/git/"/><link
rel="self"
href="https://lore.kernel.org/git/new.atom"/><id>mailto:git@vger.kernel.org</id><updated>2026-09-29T19:11:12Z</updated><entry><author><name>Kristoffer Haugsbakk</name><email>kristofferhaugsbakk@fastmail.com</email></author><title>Re: [PATCH] doc: interpret-trailers: fix cmd examples</title><updated>2026-09-29T19:11:12Z</updated><link
href="https://lore.kernel.org/git/be487f47-054c-443f-b5cb-b612269fedba@app.fastmail.com/"/><id>urn:uuid:2f8cac5d-b3cd-6b77-1e9a-e523cab148cc</id><thr:in-reply-to
ref="urn:uuid:fa4372b8-b1b1-1a58-eef1-fb85264aacdd"
href="https://lore.kernel.org/git/xmqqh5j9mdpx.fsf@gitster.g/"/><content
type="xhtml"><div
xmlns="http://www.w3.org/1999/xhtml"><pre
style="white-space:pre-wrap">On Mon, Sep 28, 2026, at 20:29, Junio C Hamano wrote:
```
<span
class="q">&gt; kristofferhaugsbakk@fastmail.com writes:
&gt;
&gt;&gt; From: Kristoffer Haugsbakk &lt;code@khaugsbakk.name&gt;
&gt;&gt;
&gt;&gt; Fix `trailer.&lt;key-alias&gt;.cmd` examples which have remained unchanged
&gt;&gt; since they were written in c364b7ef (trailer: add new .cmd config
&gt;&gt; option, 2021-05-03). (Modulo formatting changes.)
&gt;&gt;
&gt;&gt; Use this example as a guide for how to phrase it:
&gt;&gt;
&gt;&gt;     Configure a `see` trailer with a command to show the subject of a
&gt;&gt;     commit that is related, and show how it works:
&gt;
&gt; This read as if you are declaring that you use a template that
&gt; invented to consistently give intro for each example, and made it
&gt; look like the use of `see` was as a placeholder.  It would have
&gt; avoided the &#34;Huh?&#34; reaction if it were phrased like so:
&gt;
&gt;     Steal how example to show the `see` trailer is phrased and use
&gt;     it throughout:
&gt;
&gt; 	Configure a `see` trailer ...
&gt;
&gt; Other than that, this looks good.
</span>
I&#8217;ll make that change.
</pre></div></content></entry><entry><author><name>Stanislav Aleksandrov</name><email>lightofmysoul@gmail.com</email></author><title
type="html">[RFC PATCH] submodule: make &#39;^/&#39; work like &#39;../&#39; but with an absolute path</title><updated>2026-09-29T18:51:46Z</updated><link
href="https://lore.kernel.org/git/20260929185122.3127574-1-lightofmysoul@gmail.com/"/><id>urn:uuid:9d2b961e-17b8-8302-7624-f0f967c1e186</id><content
type="xhtml"><div
xmlns="http://www.w3.org/1999/xhtml"><pre
style="white-space:pre-wrap">A submodule URL like &#34;../../org/lib.git&#34; breaks when the superproject
is forked to a different depth, e.g. into a GitLab subgroup. An
absolute URL doesn&#39;t break, but it forces one protocol on everyone.

Resolve a URL starting with &#34;^/&#34; against the superproject&#39;s remote,
like &#34;../&#34;, but from the root of the server. Protocol, user, host and
port stay the same. For &#34;^/org/lib.git&#34;:

ahref="https://host/me/super.git
https://host/me/super.git</a>
-&gt; a href="https://host/org/lib.git
https://host/org/lib.git
</a>
    git@host:group/sub/super.git-&gt;  git@host:org/lib.git

Unlike &#34;../&#34;, &#34;^/&#34; fails in a superproject cloned from a local path or
without a remote, since there is no server. It also fails for
&#34;&lt;transport&gt;::&lt;address&gt;&#34; remotes, whose address only the helper can
parse.

The syntax comes from svn:externals, where &#34;^/&#34; is the repository root.

Signed-off-by: Stanislav Aleksandrov &lt;lightofmysoul@gmail.com&gt;
---
RFC: the syntax is new, and it changes the meaning of local paths
that start with &#34;^/&#34;.

- Why not &#34;/path&#34; or &#34;//host/path&#34;? &#34;/path&#34; is already a local
  absolute path, &#34;//host&#34; is a network path on Windows, and neither
  can express &#34;git@host:path&#34; or SSH host aliases.
- Why not url.&lt;base&gt;.insteadOf? It has to be set up on every clone;
  .gitmodules cannot carry it.
- Compatibility: a local &#34;^/...&#34; path needs a &#34;^&#34; directory in the
  superproject and protocol.file.allow=always, and &#34;git submodule
  add&#34; refuses it.
- Known costs: &#34;^&#34; is special in cmd.exe, Git Bash rewrites &#34;^/...&#34;
  arguments, and libgit2, JGit and forges would need to learn it.

GitLab has an open request for the same thing:
<a
href="https://gitlab.com/gitlab-org/gitlab/-/issues/393295">https://gitlab.com/gitlab-org/gitlab/-/issues/393295</a>

 Documentation/git-submodule.adoc       |   8 +-
 Documentation/gitmodules.adoc          |   7 +-
 builtin/submodule--helper.c            |  39 +++--
 remote.c                               |  61 ++++++++
 remote.h                               |  15 ++
 submodule-config.c                     |   8 +-
 submodule-config.h                     |   6 +
 t/helper/test-submodule.c              |   7 +-
 t/meson.build                          |   1 +
 t/t0060-path-utils.sh                  |  43 ++++++
 t/t7427-submodule-root-relative-url.sh | 190 +++++++++++++++++++++++++
 t/t7450-bad-git-dotfiles.sh            |   5 +
 12 files <a href="https://lore.kernel.org/git/20260929185122.3127574-1-lightofmysoul@gmail.com/#related">changed</a>, 366 insertions(+), 24 deletions(-)
 create mode 100755 t/t7427-submodule-root-relative-url.sh
```
<span
class="head">diff --git a/Documentation/git-submodule.adoc b/Documentation/git-submodule.adoc
index 722d827908..f512625eb8 100644
--- a/Documentation/git-submodule.adoc
+++ b/Documentation/git-submodule.adoc
</span><span
class="hunk">@@ -40,8 +40,9 @@ subcommands are available to perform operations on the submodules.
</span> 	project: the current project is termed the &#34;superproject&#34;.
 +
 _&lt;repository&gt;_ is the URL of the new submodule&#39;s `origin` repository.
<span
class="del">-This may be either an absolute URL, or (if it begins with `./`
-or `../`), the location relative to the superproject&#39;s default remote
</span><span
class="add">+This may be an absolute URL, (if it begins with `^/`) an absolute path
+on the server of the superproject&#39;s default remote, or (if it begins with
+`./` or `../`), the location relative to the superproject&#39;s default remote
</span> repository (Please note that to specify a repository `foo.git`
 which is located right next to a superproject `bar.git`, you&#39;ll
 have to use `../foo.git` instead of `./foo.git` - as one might expect
<span
class="hunk">@@ -53,7 +54,8 @@ of the current branch. If no such remote-tracking branch exists or
</span> the `HEAD` is detached, `origin` is assumed to be the default remote.
 If the superproject doesn&#39;t have a default remote configured
 the superproject is its own authoritative upstream and the current
<span
class="del">-working directory is used instead.
</span><span
class="add">+working directory is used instead. A `^/` path needs a default remote
+with a host.
</span> 
+ The optional argument _&lt;path&gt;
_ is the relative location for the
 submodule to exist in the superproject. If _&lt;path&gt;_ is not given, the
<span
class="head">diff--git a/Documentation/gitmodules.adoc b/Documentation/gitmodules.adoc
index fd96639806..9f6cc9a4ef 100644
--- a/Documentation/gitmodules.adoc
+++ b/Documentation/gitmodules.adoc
</span><span
class="hunk">@@ -31,9 +31,10 @@ submodule.&lt;name&gt;.path::
</span> 
 submodule.&lt;name&gt;.url::
 	Defines a URL from which the submodule repository can be cloned.
<span
class="del">
-	This may be either an absolute URL ready to be passed to
-	linkgit:git-no_clone[1] or 
(if it begins with `./` or `../`) 
a location
-	relative to the superproject
&#39;s origin repository.
</span><span
class="add">+	This may be an absolute URL ready to be passed to
+	linkgit:git-clone[1], 
(if it begins with `./` or `../`)
a location
+	relative to the superproject&#39;s origin repository, or 
(if it begins 	with`^/`) 
an absolute path on the server of that repository.
</span> 
 In addition, there are a number of optional keys:
 
<span
class="head">diff --git a/builtin/submodule--helper.c b/builtin/submodule--helper.c
index 5d3bcda334..16884ca6b6 100644
--- a/builtin/submodule--helper.c
+++ b/builtin/submodule--helper.c
</span><span
class="hunk">@@ -50,7 +50,8 @@ static char *get_default_remote(void)
</span> 	return xstrdup(repo_default_remote(the_repository));
 }
 
class="del">-static char *resolve_relative_url(const char *rel_url, const char *up_path, int quiet)
</span><span
class="add">+static char *resolve_relative_url_gently(const char *rel_url,
+					 const char *up_path, int quiet)
</span> {
 	char *remoteurl, *resolved_url;
 	char *remote = get_default_remote();
class="hunk@@ -58,14 +59,17 @@ static char *resolve_relative_url(const char *rel_url, const char *up_path, int
</span> 
 	strbuf_addf(&#38;remotesb, &#34;remote.%s.url&#34;, remote);
 	if (repo_config_get_string(the_repository, remotesb.buf, &#38;remoteurl)) {
<span
class="del">-		if (!quiet)
</span><span
class="add">+		if (!quiet &#38;&#38; !starts_with(rel_url, &#34;^/&#34;))
</span> 			warning(_(&#34;could not look up configuration &#39;%s&#39;. &#34;
 				  &#34;Assuming this repository is its own &#34;
 				  &#34;authoritative upstream.&#34;),
 				remotesb.buf);
 		remoteurl = xgetcwd();
 	}
<span
class="del">-	resolved_url = relative_url(remoteurl, rel_url, up_path);
</span><span
class="add">+	if (starts_with(rel_url, &#34;^/&#34;))
+		resolved_url = root_relative_url(remoteurl, rel_url);
+	else
+		resolved_url = relative_url(remoteurl, rel_url, up_path);
</span> 
 	free(remote);
 	free(remoteurl);
<span
class="hunk">@@ -74,6 +78,16 @@ static char *resolve_relative_url(const char *rel_url, const char *up_path, int
</span> 	return resolved_url;
 }
 
<span
class="add">+static char *resolve_relative_url(const char *rel_url, const char *up_path, int quiet)
+{
+	char *resolved_url = resolve_relative_url_gently(rel_url, up_path, quiet);
+
+	if (!resolved_url)
+		die(_(&#34;cannot resolve &#39;%s&#39; without a remote url that has a host&#34;),
+		    rel_url);
+	return resolved_url;
+}
+
</span> static int get_default_remote_submodule(const char *module_path, char **default_remote)
 {
 	const struct submodule *sub;
<span
class="hunk">@@ -87,11 +101,10 @@ static int get_default_remote_submodule(const char *module_path, char **default_
</span> 		url = xstrdup(sub-&gt;url);
 
 		/* Possibly a url relative to parent */
<span
class="del">-		if (starts_with_dot_dot_slash(url) ||
-		    starts_with_dot_slash(url)) {
</span><span
class="add">+		if (submodule_url_is_relative(url)) {
</span> 			char *oldurl = url;
 
<span
class="del">-			url = resolve_relative_url(oldurl, NULL, 1);
</span><span
class="add">+			url = resolve_relative_url_gently(oldurl, NULL, 1);
</span> 			free(oldurl);
 		}
 	}
<span
class="hunk">@@ -618,8 +631,7 @@ static void init_submodule(const char *path, const char *prefix,
</span> 		url = xstrdup(sub-&gt;url);
 ```
 		/* Possibly a url relative to parent */
<span
class="del">-		if (starts_with_dot_dot_slash(url) ||
-		    starts_with_dot_slash(url)) {
</span><span
class="add">+		if (submodule_url_is_relative(url)) {
</span> 			char *oldurl = url;
 
 			url = resolve_relative_url(oldurl, NULL, 0);
<span
class="hunk">@@ -1450,8 +1462,7 @@ static void sync_submodule(const char *path, const char *prefix,
</span> 	sub = submodule_from_path(the_repository, null_oid(the_hash_algo), path);
 
 	if (sub &#38;&#38; sub-&gt;url) {
<span
class="del">-		if (starts_with_dot_dot_slash(sub-&gt;url) ||
-		    starts_with_dot_slash(sub-&gt;url)) {
</span><span
class="add">+		if (submodule_url_is_relative(sub-&gt;url)) {
</span> 			char *up_path = get_up_path(path);
 
 			sub_origin_url = resolve_relative_url(sub-&gt;url, up_path, 1);
<span
class="hunk">@@ -2314,8 +2325,7 @@ static int prepare_to_clone_next_submodule(const struct cache_entry *ce,
</span> 	strbuf_reset(&#38;sb);
 	strbuf_addf(&#38;sb, &#34;submodule.%s.url&#34;, sub-&gt;name);
 	if (repo_config_get_string_tmp(the_repository, sb.buf, &#38;url)) {
<span
class="del">-		if (sub-&gt;url &#38;&#38; (starts_with_dot_slash(sub-&gt;url) ||
-				 starts_with_dot_dot_slash(sub-&gt;url))) {
</span><span
class="add">+		if (sub-&gt;url &#38;&#38; submodule_url_is_relative(sub-&gt;url)) {
</span> 			url = resolve_relative_url(sub-&gt;url, NULL, 0);
 			need_free_url = 1;
 		} else
<span
class="hunk">@@ -3710,8 +3720,7 @@ static int module_add(int argc, const char **argv, const char *prefix,
</span> 		free(sm_path);
 	}
 
<span
class="del">-	if (starts_with_dot_dot_slash(add_data.repo) ||
-	    starts_with_dot_slash(add_data.repo)) {
</span><span
class="add">+	if (submodule_url_is_relative(add_data.repo)) {
</span> 		if (prefix)
 			die(_(&#34;Relative path can only be used from the toplevel &#34;
 			      &#34;of the working tree&#34;));
<span
class="hunk">@@ -3722,7 +3731,7 @@ static int module_add(int argc, const char **argv, const char *prefix,
</span> 	} else if (is_dir_sep(add_data.repo[0]) || strchr(add_data.repo, &#39;:&#39;)) {
 		add_data.realrepo = add_data.repo;
 	} else {
<span
class="del">-		die(_(&#34;repo URL: &#39;%s&#39; must be absolute or begin with ./|../&#34;),
</span><span
class="add">+		die(_(&#34;repo URL: &#39;%s&#39; must be absolute or begin with ./|../|^/&#34;),
</span> 		    add_data.repo);
 	}
 
<span
class="head">diff --git a/remote.c b/remote.c
index fe62068463..05ef35e3ab 100644
--- a/remote.c
+++ b/remote.c
</span><span
class="hunk">@@ -3095,6 +3095,67 @@ char *relative_url(const char *remote_url, const char *url,
</span> 	return strbuf_detach(&#38;sb, NULL);
 }
 
<span
class="add">+static const char *skip_bracketed_host(const char *host)
+{
+	const char *start = strstr(host, &#34;@[&#34;);
+	const char *end;
+
+	start = start ? start + 1 : host;
+	if (*start != &#39;[&#39;)
+		return host;
+	end = strchr(start + 1, &#39;]&#39;);
+	return end ? end : host;
+}
+
+static int has_host(const char *start, const char *end)
+{
+	const char *p;
+
+	for (p = start; p &lt; end; p++)
+		if (*p == &#39;@&#39;)
+			start = p + 1;
+	return start &lt; end &#38;&#38; *start != &#39;:&#39; &#38;&#38; !starts_with(start, &#34;[]&#34;);
+}
+
+char *root_relative_url(const char *remote_url, const char *url)
+{
+	struct strbuf sb = STRBUF_INIT;
+	const char *path, *host, *end;
+	int scp;
+
+	if (!skip_prefix(url, &#34;^/&#34;, &#38;path))
+		BUG(&#34;not a root-relative url: &#39;%s&#39;&#34;, url);
+	if (*path == &#39;/&#39; || *path == &#39;:&#39;)
+		die(_(&#34;root-relative url &#39;%s&#39; must not start with &#39;^//&#39; or &#39;^/:&#39;&#34;),
+		    url);
+
+	for (end = remote_url; is_urlschemechar(end == remote_url, *end); end++)
+		;
+	if (starts_with(end, &#34;::&#34;) || starts_with(remote_url, &#34;file://&#34;) ||
+	    url_is_local_not_ssh(remote_url))
+		return NULL;
+
+	scp = !is_url(remote_url);
+	if (scp) {
+		host = remote_url;
+		end = strchr(skip_bracketed_host(remote_url), &#39;:&#39;);
+	} else {
+		host = strstr(remote_url, &#34;://&#34;) + 3;
+		end = strchrnul(host, &#39;/&#39;);
+	}
+	if (!end || !has_host(host, end))
+		return NULL;
+
+	strbuf_add(&#38;sb, remote_url, end - remote_url);
+	strbuf_addch(&#38;sb, scp ? &#39;:&#39; : &#39;/&#39;);
+	if (scp &#38;&#38; end[1] == &#39;/&#39;)
+		strbuf_addch(&#38;sb, &#39;/&#39;);
+	strbuf_addstr(&#38;sb, path);
+	if (ends_with(path, &#34;/&#34;))
+		strbuf_setlen(&#38;sb, sb.len - 1);
+	return strbuf_detach(&#38;sb, NULL);
+}
+</span> int valid_remote_name(const char *name)
 {
 	int result;
<spanclass="head">diff 
--git a/remote.h b/remote.h
index cca02033b9..8a759ae20d 100644
--- a/remote.h
+++ b/remote.h
</span><span
class="hunk">@@ -478,6 +478,21 @@ void apply_push_cas(struct push_cas_option *, struct remote *, struct ref *);
</span> char *relative_url(const char *remote_url, const char *url,
 		   const char *up_path);
 <span
class="add">+/*
+ * The `url` argument starts with &#34;^/&#34; and names a repository relative to
+ * the root of the server that `remote_url` points to: the path of
+ * `remote_url` is replaced with the rest of `url`, keeping its scheme, user,
+ * host and port. Returns NULL if `remote_url` has no host, and dies if
+ * `url` continues with &#39;/&#39; or &#39;:&#39;, which could change the kind of URL.
+ *
+ * remote_url                 url            outcome
+ * <a
href="https://a.com/b/c">https://a.com/b/c</a>          ^/d/e 
<ahref="https://a.com/d/e">
https://a.com/d/e
</a>
+ * ssh://u@a.com:22/b/c^/d/e          ssh://u@a.com:22/d/e
+ * u@a.com:b/c^/d/usau@a.com:d/e
+ * u@a.com:/b/c               ^/d/usa
eu@a.com:/d/e
+ */
+char *root_relative_url(const char *remote_url, const char *url);
</span> int valid_remote_name(const char *name);
  #endif
<span
class="head">diff --git a/submodule-config.c b/submodule-config.c
index 37c3be377b..dfa819112c 100644
--- a/submodule-config.c
+++ b/submodule-config.c
</span><span
class="hunk">@@ -237,9 +237,10 @@ int check_submodule_name(const char *name)
</span> 	return 0;
 }
 <span
class="del">-static int submodule_url_is_relative(const char *url)
</span><span
class="add">+int submodule_url_is_relative(const char *url)
</span> {
<span
class="del">-	return starts_with_dot_slash(url) || starts_with_dot_dot_slash(url);
</span><span
class="add">+	return starts_with_dot_slash(url) || starts_with_dot_dot_slash(url) ||
+	       starts_with(url, &#34;^/&#34;);
</span> } 
 /*
<span
class="hunk">@@ -342,6 +343,9 @@ int check_submodule_url(const char *url)
</span> 		if (count_leading_dotdots(url, &#38;next) &gt; 0 &#38;&#38;
 		    (*next == &#39;:&#39; || *next == &#39;/&#39;))
 			return -1;
<span
class="add">+		if (skip_prefix(url, &#34;^/&#34;, &#38;next) &#38;&#38;
+		    (*next == &#39;:&#39; || *next == &#39;/&#39;))
+			return -1;
</span> 	}
  	else if (url_to_curl_url(url, &#38;curl_url)) {
<span
class="head">diff --git a/submodule-config.h b/submodule-config.h
index 755570d5d1..3e947291d5 100644
--- a/submodule-config.h
+++ b/submodule-config.h
</span><span
class="hunk">@@ -94,6 +94,12 @@ int check_submodule_name(const char *name);
</span> /* Returns 0 if the URL valid per RFC3986 and -1 otherwise. */
 int check_submodule_url(const char *url); 
<span
class="add">+/*
+ * Returns 1 if the URL is resolved against the superproject&#39;s remote,
+ * i.e. starts with &#34;./&#34;, &#34;../&#34; or &#34;^/&#34;, and 0 otherwise.
+ */
+int submodule_url_is_relative(const char *url);
</span> /*
  * Note: these helper functions exist solely to maintain backward
  * compatibility with &#39;fetch&#39; and &#39;update_clone&#39; storing configuration in
<span
class="head">diff --git a/t/helper/test-submodule.c b/t/helper/test-submodule.c
index ea9bef0904..f28daf52fe 100644
--- a/t/helper/test-submodule.c
+++ b/t/helper/test-submodule.c
</span><span
class="hunk">@@ -123,7 +123,12 @@ static int cmd__submodule_resolve_relative_url(int argc, const char **argv)
</span> 	if (!strcmp(up_path, &#34;(null)&#34;))
 		up_path = NULL;
``` 
<span
class="del">
-res = relative_url(remoteurl, url, up_path);
</span><span
class="add">
+	if (starts_with(url, &#34;^/&#34;))
+		res = root_relative_url(remoteurl, url);
+	else
+		res = relative_url(remoteurl, url, up_path);
+	if (!res)
+		die(&#34;cannot resolve &#39;%s&#39; 
against &#39;%s&#39;&#34;,
url, remoteurl);
</span> 	puts(res);
 	free(res);
 	free(remoteurl);
<span
class="head">diff --git a/t/meson.build b/t/meson.build
index 3ca7b27104..9d3ac94aae 100644
--- a/t/meson.build
+++ b/t/meson.build
</span><span
class="hunk">@@ -918,6 +918,7 @@ integration_tests = [
</span>   &#39;t7424-submodule-mixed-ref-formats.sh&#39;,  &#39;t7425-submodule-gitdir-path-extension.sh&#39; &#39;t7426-submodule-get-default-remote.sh&#39,
<span class="add">
+&#39;t7427-submodule-root-relative-url.sh&#39,
</span>
&#39;t7450-bad-git-dotfi

See [LICENSE](LICENSE)
