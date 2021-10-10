+++
title = "Philippines Unicode Keyboard Layout for Linux Is Now Available!"
description = "Filipino Linux users around the world can now download and use the first release of the Philippines Unicode Keyboard Layout."                                                    # For Schema.org; OpenGraph; Twitter Cards; and post summary

date = "2010-10-23T19:40:10"                                        # manually adjust to local timezone
#lastmod = "2021-04-07T17:53:01"                                     # manually adjust to local timezone

aliases = ["/p/philippines-unicode-keyboard-linux.html"]
slug = "philippines-baybayin-linux"
translationKey = "philippines-baybayin-linux-2010296"
relCanonical = "https://im.youronly.one/techmagus/projects/keyboard/philippines-baybayin-linux-2010296/"                                                   # the actual URL of the post; also used for disqus ID and url
#disqus_url = ""                                                    # automatic in YourOnly.One setup
#disqus_identifier = ""                                             # highly recommended by Disqus; automatic in YourOnly.One setup

channels = ["techmagus"]
categories = ["unicode", "linux"]                                                   # taxonomy
keywords = [""]                                                     # meta keywords
series = [""]                                                       # subset of series taxonomy
tags = [""]                                                         # taxonomy

comments = true
#weight = "20"                                                        # post weight, if we want granular control of post order

#featured = true
#math = true
toc = true

#videos = [""]                                                       # used by og:video, etc.
#audio = [""]                                                        # used by og:audio, etc.
images = ["https://3.bp.blogspot.com/-IPzJrxh1_vg/TncoS7FQ61I/AAAAAAAAAVQ/65UR2jN6Aes/s1600/Philippines-Dvorak%252520Simplified%252520%252528Latin%252529.png"]                                                       # used by og:images, etc.; first image is cover image

#draft = true

#license = ""                                                       # only set if the post license is not the same as the site license

#contenttypes = [""]                                                 # Semantic Web JSON-LD
#[semweb]                                                            # Semantic Web JSON-LD
#  type = ""

# Duplicate for more Image entries
#[[semweb.image]]
#  # If different from default author
#  #author = ""
#  #sameas = [""]
#  #name = ""
#  about = ""
#  #caption = ""
#  url = ""
#  contentlocation = ""
#  contentreferencetime = "2018-05-19"
#  datecreated = "2018-05-19"
#  datepublished = "2020-08-13"
#  copyrightholder = ""
#  copyrightnotice = "Credit to"
#  copyrightyear = "2018"
#  licenseurl = "https://creativecommons.org/licenses/by-sa/4.0/"
#  acquirelicenseurl = "https://youronly.one/p/legal-notice/"

# For /yuki/ choose one and remove everything else
[author]
  #name = "techmagus"
  #email = ""
  homepage = "https://im.youronly.one/techmagus/"
  avatar = "https://rsc.youronly.one/img/y/techmagus-Architetto-Esperiment-chimico.webp"
  #emoji = ""
  #descriptionshort = ""
  #descriptionlong = ""
  #motto = ""
  #locationorigin = ""
  #locationcurrent = ""
  #rel = "me noopener"
+++

Today, 23<sup>rd</sup> of October 2010, Filipino Linux users around the world can now download and use the first release of the <b>Philippines Unicode Keyboard Layout</b>, officially launched at the [Philippines Ubuntu 10.10 Maverick Meerkat Release Party]({{/* < ref "20101018-ubuntu-release-party.md" > */}} "Philippines Ubuntu 10.10 Maverick Meerkat Release Party")!

What is this all about? Simple: being able to type the characters that Filipinos use, especially the ₱eso sign and <span lang="fil-Tglg">ᜊᜌ᜔ᜊᜌᜒᜈ᜔</span> (Baybayin) glyphs that has been available for use since Unicode 3.2 (March 2002). Other characters are: Ññ, ©, ®, ™, ¢, ¥, ¶, Pahilís (acute diacritic), Paiwà (grave diacritic), Pakupyâ (circumflex diacritic), Ng̃ (the shortened form of nan͠g), and many more.

How about Windows users? <del>You will have to wait more or less 2 weeks, it will be usable for Windows 7, Vista, and XP; both 64-bit and 32-bit installations.</del> <ins>It is now available for [download]({{< ref "philippines-unicode-keyboard-layout-windows.md" >}} "Philippines Unicode Keyboard Layout for Windows").</ins> Windows is too complicated as compared to Linux (seriously).

Without further ado, here are the steps to get you started with using our very own Unicode Keyboard Layout.

<!--more-->

<ol>
  <li>Download the PH-UKL-Linux file (available in 7-zip and zip format) <a href="https://bitbucket.org/paninap/ph-ukl/downloads" rel="noopener external nofollow" referrerpolicy="strict-origin-when-cross-origin">here</a></li>
  <li>Extract the content of the archive file you just downloaded</li>
  <li>Install the font included so your system can display Baybayin (Alibata) glyphs</li>
  <li>Then copy the file "ph" to the correct folder by typing in the terminal (be sure to adjust ~/Downloads/ to where the file is on your end)
    <pre class="command-line" data-user="me" data-host="host"><code class="language-shell-session">
      sudo cp ~/Downloads/ph /usr/share/X11/xkb/symbols
    </code></pre>
  </li>
  <li>Open these two files by typing:
    <pre class="command-line" data-user="me" data-host="host"><code class="language-shell-session">
      gksu gedit /usr/share/X11/xkb/rules/evdev.lst
    </code></pre>
    <pre class="command-line" data-user="me" data-host="host"><code class="language-shell-session">
      gksu gedit /usr/share/X11/xkb/rules/base.lst
    </code></pre>
  </li>
  <li>Search for:
    <pre><code class="language-clike match-braces rainbow-braces">
      ! layout
    </code></pre>
  </li>
  <li>After it add:
    <pre><code class="language-clike match-braces rainbow-braces">
      ph              Philippines
    </code></pre>
  </li>
  <li>Search for:
    <pre><code class="language-clike match-braces rainbow-braces">
      ! variant
    </code></pre>
  </li>
  <li>After it add:
    <pre class="line-numbers"><code class="language-clike match-braces rainbow-braces">
      qwerty-bay            ph: QWERTY (Baybayin)
      capewell-dvorak       ph: Capewell-Dvorak (Latin)
      capewell-dvorak-bay   ph: Capewell-Dvorak (Baybayin)
      capewell-qwerf2k6     ph: Capewell-QWERF 2006 (Latin)
      capewell-qwerf2k6-bay ph: Capewell-QWERF 2006 (Baybayin)
      colemak               ph: Colemak (Latin)
      colemak-bay           ph: Colemak (Baybayin)
      dvorak                ph: Dvorak (Latin)
      dvorak-bay            ph: Dvorak (Baybayin)
    </code></pre>
  </li>
  <li>Open these two files by typing:
    <pre class="command-line" data-user="me" data-host="host"><code class="language-shell-session">
      gksu gedit /usr/share/X11/xkb/rules/evdev.xml
    </code></pre>
    <pre class="command-line" data-user="me" data-host="host"><code class="language-shell-session">
      gksu gedit /usr/share/X11/xkb/rules/base.xml
    </code></pre>
  </li>
  <li>Search for:
    <pre><code class="language-clike match-braces rainbow-braces">
      &lt;layoutlist>
    </code></pre>
  </li>
  <li>After it add:
    <pre class="line-numbers"><code class="language-clike match-braces rainbow-braces">
      &lt;layout>
        &lt;configItem>
          &lt;name>ph&lt;/name>
          &lt;shortDescription>Phi&lt;/shortDescription>
          &lt;description>Philippines&lt;/description>
          &lt;languageList>&lt;iso639Id>eng&lt;/iso639Id>
                        &lt;iso639Id>bik&lt;/iso639Id>
                        &lt;iso639Id>ceb&lt;/iso639Id>
                        &lt;iso639Id>fil&lt;/iso639Id>
                        &lt;iso639Id>hil&lt;/iso639Id>
                        &lt;iso639Id>ilo&lt;/iso639Id>
                        &lt;iso639Id>pam&lt;/iso639Id>
                        &lt;iso639Id>pag&lt;/iso639Id>
                        &lt;iso639Id>phi&lt;/iso639Id>
                        &lt;iso639Id>tgl&lt;/iso639Id>
                        &lt;iso639Id>war&lt;/iso639Id>&lt;/languageList>
        &lt;/configItem>
        &lt;variantList>
          &lt;variant>
            &lt;configItem>
              &lt;name>qwerty-bay&lt;/name>
              &lt;description>QWERTY (Baybayin)&lt;/description>
              &lt;languageList>&lt;iso639Id>bik&lt;/iso639Id>
                            &lt;iso639Id>ceb&lt;/iso639Id>
                            &lt;iso639Id>fil&lt;/iso639Id>
                            &lt;iso639Id>hil&lt;/iso639Id>
                            &lt;iso639Id>ilo&lt;/iso639Id>
                            &lt;iso639Id>pam&lt;/iso639Id>
                            &lt;iso639Id>pag&lt;/iso639Id>
                            &lt;iso639Id>phi&lt;/iso639Id>
                            &lt;iso639Id>tgl&lt;/iso639Id>
                            &lt;iso639Id>war&lt;/iso639Id>&lt;/languageList>
            &lt;/configItem>
          &lt;/variant>
          &lt;variant>
            &lt;configItem>
              &lt;name>capewell-dvorak&lt;/name>
              &lt;description>Capewell-Dvorak (Latin)&lt;/description>
            &lt;/configItem>
          &lt;/variant>
          &lt;variant>
            &lt;configItem>
              &lt;name>capewell-dvorak-bay&lt;/name>
              &lt;description>Capewell-Dvorak (Baybayin)&lt;/description>
              &lt;languageList>&lt;iso639Id>bik&lt;/iso639Id>
                            &lt;iso639Id>ceb&lt;/iso639Id>
                            &lt;iso639Id>fil&lt;/iso639Id>
                            &lt;iso639Id>hil&lt;/iso639Id>
                            &lt;iso639Id>ilo&lt;/iso639Id>
                            &lt;iso639Id>pam&lt;/iso639Id>
                            &lt;iso639Id>pag&lt;/iso639Id>
                            &lt;iso639Id>phi&lt;/iso639Id>
                            &lt;iso639Id>tgl&lt;/iso639Id>
                            &lt;iso639Id>war&lt;/iso639Id>&lt;/languageList>
            &lt;/configItem>
          &lt;/variant>
          &lt;variant>
            &lt;configItem>
              &lt;name>capewell-qwerf2k6&lt;/name>
              &lt;description>Capewell-QWERF 2006 (Latin)&lt;/description>
            &lt;/configItem>
          &lt;/variant>
          &lt;variant>
            &lt;configItem>
              &lt;name>capewell-qwerf2k6-bay&lt;/name>
              &lt;description>Capewell-QWERF 2006 (Baybayin)&lt;/description>
              &lt;languageList>&lt;iso639Id>bik&lt;/iso639Id>
                            &lt;iso639Id>ceb&lt;/iso639Id>
                            &lt;iso639Id>fil&lt;/iso639Id>
                            &lt;iso639Id>hil&lt;/iso639Id>
                            &lt;iso639Id>ilo&lt;/iso639Id>
                            &lt;iso639Id>pam&lt;/iso639Id>
                            &lt;iso639Id>pag&lt;/iso639Id>
                            &lt;iso639Id>phi&lt;/iso639Id>
                            &lt;iso639Id>tgl&lt;/iso639Id>
                            &lt;iso639Id>war&lt;/iso639Id>&lt;/languageList>
            &lt;/configItem>
          &lt;/variant>
          &lt;variant>
            &lt;configItem>
              &lt;name>colemak&lt;/name>
              &lt;description>Colemak (Latin)&lt;/description>
            &lt;/configItem>
          &lt;/variant>
          &lt;variant>
            &lt;configItem>
              &lt;name>colemak-bay&lt;/name>
              &lt;description>Colemak (Baybayin)&lt;/description>
              &lt;languageList>&lt;iso639Id>bik&lt;/iso639Id>
                            &lt;iso639Id>ceb&lt;/iso639Id>
                            &lt;iso639Id>fil&lt;/iso639Id>
                            &lt;iso639Id>hil&lt;/iso639Id>
                            &lt;iso639Id>ilo&lt;/iso639Id>
                            &lt;iso639Id>pam&lt;/iso639Id>
                            &lt;iso639Id>pag&lt;/iso639Id>
                            &lt;iso639Id>phi&lt;/iso639Id>
                            &lt;iso639Id>tgl&lt;/iso639Id>
                            &lt;iso639Id>war&lt;/iso639Id>&lt;/languageList>
            &lt;/configItem>
          &lt;/variant>
          &lt;variant>
            &lt;configItem>
              &lt;name>dvorak&lt;/name>
              &lt;description>Dvorak (Latin)&lt;/description>
            &lt;/configItem>
          &lt;/variant>
          &lt;variant>
            &lt;configItem>
              &lt;name>dvorak-bay&lt;/name>
              &lt;description>Dvorak (Baybayin)&lt;/description>
              &lt;languageList>&lt;iso639Id>bik&lt;/iso639Id>
                            &lt;iso639Id>ceb&lt;/iso639Id>
                            &lt;iso639Id>fil&lt;/iso639Id>
                            &lt;iso639Id>hil&lt;/iso639Id>
                            &lt;iso639Id>ilo&lt;/iso639Id>
                            &lt;iso639Id>pam&lt;/iso639Id>
                            &lt;iso639Id>pag&lt;/iso639Id>
                            &lt;iso639Id>phi&lt;/iso639Id>
                            &lt;iso639Id>tgl&lt;/iso639Id>
                            &lt;iso639Id>war&lt;/iso639Id>&lt;/languageList>
            &lt;/configItem>
          &lt;/variant>
        &lt;/variantList>
      &lt;/layout>
    </code></pre>
  </li>
</ol>

You're done! Sort of. You need to activate it to actually use it, follow the next few steps to do so.

<ol>
  <li>Go to: Preferences &gt; Keyboard &gt; Layouts</li>
  <li>Click the "Add…" button</li>
  <li>Search for the new keyboard you installed either "By country" (Philippines) or "By language" (English; Filipino; Cebuano; Philippine Languages; etc.)</li>
  <li>There are different variants that you can choose from:
    <ol style="list-style: lower-alpha;">
      <li>Philippines (default; QWERTY - Latin)</li>
      <li>Philippines - QWERTY (Baybayin)</li>
      <li>Philippines - Capewell-Dvorak (Latin)</li>
      <li>Philippines - Capewell-Dvorak (Baybayin)</li>
      <li>Philippines - Capewell-QWERF 2006 (Latin)</li>
      <li>Philippines - Capewell-QWERF 2006 (Baybayin)</li>
      <li>Philippines - Colemak (Latin)</li>
      <li>Philippines - Colemak (Baybayin)</li>
      <li>Philippines - Dvorak (Latin)</li>
      <li>Philippines - Dvorak (Baybayin)</li>
    </ol>
  </li>
  <li>Click the "Add" button</li>
  <li>Select the new layout that you added then click the "Move Up" button and place it on top
    <figure class="figure_box">
      <div class="separator" style="clear: both; text-align: center;"><a href="https://2.bp.blogspot.com/-s6u_KKylKpg/TMJT_n8RdXI/AAAAAAAAAHw/ErsBqZlFJeg/s1600/Philippines%252520National%252520Keyboard%252520Layout.png" imageanchor="1" style="margin-left: 1em; margin-right: 1em;"><img loading="lazy" border="0" src="https://2.bp.blogspot.com/-s6u_KKylKpg/TMJT_n8RdXI/AAAAAAAAAHw/ErsBqZlFJeg/s1600/Philippines%252520National%252520Keyboard%252520Layout.png" data-original-width="576" data-original-height="551" /></a></div>
    </figure>
  </li>
</ol>

Let's not forget to add the first Baybayin <span lang="fil-Tglg">ᜊᜌ᜔ᜊᜌᜒᜈ᜔</span>) keyboard layout, it is QWERTY-based. Simply repeat the process above but place it as second in your Layouts list. Then if you want to switch between Philippines Latin and Philippines Baybayin scripts, simply press <b>Shift+CAPS_Lock</b>. It is the default shortcut in Ubuntu 10.10 Maverick Meerkat.

The font included in the zip file is a Unicode-only and Website-embed compatible version of <a href="https://nordenx.com" rel="noopener external nofollow" referrerpolicy="strict-origin-when-cross-origin">Nordenx</a>'s Baybayin brush font.

See the [keyboard layout images here]({{< ref "philippines-unicode-keyboard-layout.md" >}} "Philippines Unicode Keyboard Layout").

Official source repository: <a href="https://bitbucket.org/paninap/ph-ukl/" rel="noopener external nofollow" referrerpolicy="strict-origin-when-cross-origin">https://bitbucket.org/paninap/ph-ukl/</a><br />If you have suggestions or bugs to report, please do not hesitate to <a href="https://bitbucket.org/paninap/ph-ukl/issues" rel="noopener external nofollow" referrerpolicy="strict-origin-when-cross-origin">file a ticket here</a>.

*** The <b>Philippines Unicode Keyboard Layout</b> is a project of <i>Ubuntu Philippines LoCo Team</i>. Project contact: JC John Sese Cuneta; XMPP/Jabber jcjohn.sesecuneta@talkr.im. ***

-------

{{< image
  type="imagecoverattrib"

  imglink="https://3.bp.blogspot.com/-IPzJrxh1_vg/TncoS7FQ61I/AAAAAAAAAVQ/65UR2jN6Aes/s1600/Philippines-Dvorak%252520Simplified%252520%252528Latin%252529.png"
  imgrel="me noopener"

  imgtitle="Philippines-Dvorak Simplified (Latin)"
  imgcaption=""

  licensecode="cc0"
  licenseurl="https://creativecommons.org/publicdomain/zero/1.0/"
  licensename="CC Zero / Public Domain dedication"

  attribto="YourOnly.One"
  attriblink="https://youronly.one"
  attribrel="me noopener"
>}}
