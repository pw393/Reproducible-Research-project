



<!DOCTYPE html>
<html lang="en" class=" is-copy-enabled is-u2f-enabled">
  <head prefix="og: http://ogp.me/ns# fb: http://ogp.me/ns/fb# object: http://ogp.me/ns/object# article: http://ogp.me/ns/article# profile: http://ogp.me/ns/profile#">
    <meta charset='utf-8'>
    

    <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/frameworks-b94ec35a696398c8a00f27343992e597c93faadce7783164f7f8967248cc818f.css" integrity="sha256-uU7DWmljmMigDyc0OZLll8k/qtzneDFk9/iWckjMgY8=" media="all" rel="stylesheet" />
    <link crossorigin="anonymous" href="https://assets-cdn.github.com/assets/github-f1dd95db316b03c6d429dd35926fdf5b6520abdff62d481127e84cc9ab7460d0.css" integrity="sha256-8d2V2zFrA8bUKd01km/fW2Ugq9/2LUgRJ+hMyat0YNA=" media="all" rel="stylesheet" />
    
    
    
    

    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta http-equiv="Content-Language" content="en">
    <meta name="viewport" content="width=device-width">
    
    <title>coursera-repdata/storm.analysis.md at master · sefakilic/coursera-repdata</title>
    <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="GitHub">
    <link rel="fluid-icon" href="https://github.com/fluidicon.png" title="GitHub">
    <link rel="apple-touch-icon" href="/apple-touch-icon.png">
    <link rel="apple-touch-icon" sizes="57x57" href="/apple-touch-icon-57x57.png">
    <link rel="apple-touch-icon" sizes="60x60" href="/apple-touch-icon-60x60.png">
    <link rel="apple-touch-icon" sizes="72x72" href="/apple-touch-icon-72x72.png">
    <link rel="apple-touch-icon" sizes="76x76" href="/apple-touch-icon-76x76.png">
    <link rel="apple-touch-icon" sizes="114x114" href="/apple-touch-icon-114x114.png">
    <link rel="apple-touch-icon" sizes="120x120" href="/apple-touch-icon-120x120.png">
    <link rel="apple-touch-icon" sizes="144x144" href="/apple-touch-icon-144x144.png">
    <link rel="apple-touch-icon" sizes="152x152" href="/apple-touch-icon-152x152.png">
    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon-180x180.png">
    <meta property="fb:app_id" content="1401488693436528">

      <meta content="https://avatars1.githubusercontent.com/u/1227083?v=3&amp;s=400" name="twitter:image:src" /><meta content="@github" name="twitter:site" /><meta content="summary" name="twitter:card" /><meta content="sefakilic/coursera-repdata" name="twitter:title" /><meta content="coursera-repdata - Peer Assessment 1 for Reproducible Research" name="twitter:description" />
      <meta content="https://avatars1.githubusercontent.com/u/1227083?v=3&amp;s=400" property="og:image" /><meta content="GitHub" property="og:site_name" /><meta content="object" property="og:type" /><meta content="sefakilic/coursera-repdata" property="og:title" /><meta content="https://github.com/sefakilic/coursera-repdata" property="og:url" /><meta content="coursera-repdata - Peer Assessment 1 for Reproducible Research" property="og:description" />
      <meta name="browser-stats-url" content="https://api.github.com/_private/browser/stats">
    <meta name="browser-errors-url" content="https://api.github.com/_private/browser/errors">
    <link rel="assets" href="https://assets-cdn.github.com/">
    <link rel="web-socket" href="wss://live.github.com/_sockets/VjI6MTQzNjIwMzc3OmI2NWY1ODQ4N2I5ZmJmZjg0MzY1OGJjYWIzNDY4ZGQ2N2E0ZDM4MjEwZjk3N2IzODYyMDdlZjg3NTdkNzI0NjM=--ff494871766e5b119dd43dfefbabefb6db293fa2">
    <meta name="pjax-timeout" content="1000">
    <link rel="sudo-modal" href="/sessions/sudo_modal">
    <meta name="request-id" content="80547F1A:7727:1054B0E2:58642246" data-pjax-transient>

    <meta name="msapplication-TileImage" content="/windows-tile.png">
    <meta name="msapplication-TileColor" content="#ffffff">
    <meta name="selected-link" value="repo_source" data-pjax-transient>

    <meta name="google-site-verification" content="KT5gs8h0wvaagLKAVWq8bbeNwnZZK1r1XQysX3xurLU">
<meta name="google-site-verification" content="ZzhVyEFwb7w3e0-uOTltm8Jsck2F5StVihD0exw2fsA">
    <meta name="google-analytics" content="UA-3769691-2">

<meta content="collector.githubapp.com" name="octolytics-host" /><meta content="github" name="octolytics-app-id" /><meta content="80547F1A:7727:1054B0E2:58642246" name="octolytics-dimension-request_id" /><meta content="24728765" name="octolytics-actor-id" /><meta content="pw393" name="octolytics-actor-login" /><meta content="bcc02828e23f3e9189e6c63ea01888ed226c8a62f482a38986f0226fdc1162f1" name="octolytics-actor-hash" />
<meta content="/&lt;user-name&gt;/&lt;repo-name&gt;/blob/show" data-pjax-transient="true" name="analytics-location" />



  <meta class="js-ga-set" name="dimension1" content="Logged In">



        <meta name="hostname" content="github.com">
    <meta name="user-login" content="pw393">

        <meta name="expected-hostname" content="github.com">
      <meta name="js-proxy-site-detection-payload" content="ZjE0YjY1YzE4ZDZkOTc0NWY3ZDljMDdhYzliM2YyYTYwNzFlMDg4YzllY2Q3NTJjMjUyN2IzYjIzZTEzYmYzM3x7InJlbW90ZV9hZGRyZXNzIjoiMTI4Ljg0LjEyNy4yNiIsInJlcXVlc3RfaWQiOiI4MDU0N0YxQTo3NzI3OjEwNTRCMEUyOjU4NjQyMjQ2IiwidGltZXN0YW1wIjoxNDgyOTU3Mzg2LCJob3N0IjoiZ2l0aHViLmNvbSJ9">


      <link rel="mask-icon" href="https://assets-cdn.github.com/pinned-octocat.svg" color="#000000">
      <link rel="icon" type="image/x-icon" href="https://assets-cdn.github.com/favicon.ico">

    <meta name="html-safe-nonce" content="94a2a1a79cc795f5a59f61de520254d129387598">

    <meta http-equiv="x-pjax-version" content="b9f7ac0f3005268b20204004dd504175">
    

      
  <meta name="description" content="coursera-repdata - Peer Assessment 1 for Reproducible Research">
  <meta name="go-import" content="github.com/sefakilic/coursera-repdata git https://github.com/sefakilic/coursera-repdata.git">

  <meta content="1227083" name="octolytics-dimension-user_id" /><meta content="sefakilic" name="octolytics-dimension-user_login" /><meta content="19899531" name="octolytics-dimension-repository_id" /><meta content="sefakilic/coursera-repdata" name="octolytics-dimension-repository_nwo" /><meta content="true" name="octolytics-dimension-repository_public" /><meta content="true" name="octolytics-dimension-repository_is_fork" /><meta content="16709733" name="octolytics-dimension-repository_parent_id" /><meta content="rdpeng/RepData_PeerAssessment1" name="octolytics-dimension-repository_parent_nwo" /><meta content="16709733" name="octolytics-dimension-repository_network_root_id" /><meta content="rdpeng/RepData_PeerAssessment1" name="octolytics-dimension-repository_network_root_nwo" />
  <link href="https://github.com/sefakilic/coursera-repdata/commits/master.atom" rel="alternate" title="Recent Commits to coursera-repdata:master" type="application/atom+xml">


      <link rel="canonical" href="https://github.com/sefakilic/coursera-repdata/blob/master/project2/storm.analysis.md" data-pjax-transient>
  </head>


  <body class="logged-in  env-production windows vis-public fork page-blob">
    <div id="js-pjax-loader-bar" class="pjax-loader-bar"><div class="progress"></div></div>
    <a href="#start-of-content" tabindex="1" class="accessibility-aid js-skip-to-content">Skip to content</a>

    
    
    



        <div class="header header-logged-in true" role="banner">
  <div class="container clearfix">

    <a class="header-logo-invertocat" href="https://github.com/" data-hotkey="g d" aria-label="Homepage" data-ga-click="Header, go to dashboard, icon:logo">
  <svg aria-hidden="true" class="octicon octicon-mark-github" height="28" version="1.1" viewBox="0 0 16 16" width="28"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
</a>


        <div class="header-search scoped-search site-scoped-search js-site-search" role="search">
  <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/sefakilic/coursera-repdata/search" class="js-site-search-form" data-scoped-search-url="/sefakilic/coursera-repdata/search" data-unscoped-search-url="/search" method="get"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /></div>
    <label class="form-control header-search-wrapper js-chromeless-input-container">
      <div class="header-search-scope">This repository</div>
      <input type="text"
        class="form-control header-search-input js-site-search-focus js-site-search-field is-clearable"
        data-hotkey="s"
        name="q"
        placeholder="Search"
        aria-label="Search this repository"
        data-unscoped-placeholder="Search GitHub"
        data-scoped-placeholder="Search"
        autocapitalize="off">
    </label>
</form></div>


      <ul class="header-nav float-left" role="navigation">
        <li class="header-nav-item">
          <a href="/pulls" aria-label="Pull requests you created" class="js-selected-navigation-item header-nav-link" data-ga-click="Header, click, Nav menu - item:pulls context:user" data-hotkey="g p" data-selected-links="/pulls /pulls/assigned /pulls/mentioned /pulls">
            Pull requests
</a>        </li>
        <li class="header-nav-item">
          <a href="/issues" aria-label="Issues you created" class="js-selected-navigation-item header-nav-link" data-ga-click="Header, click, Nav menu - item:issues context:user" data-hotkey="g i" data-selected-links="/issues /issues/assigned /issues/mentioned /issues">
            Issues
</a>        </li>
          <li class="header-nav-item">
            <a class="header-nav-link" href="https://gist.github.com/" data-ga-click="Header, go to gist, text:gist">Gist</a>
          </li>
      </ul>

    
<ul class="header-nav user-nav float-right" id="user-links">
  <li class="header-nav-item">
    

  </li>

  <li class="header-nav-item dropdown js-menu-container">
    <a class="header-nav-link tooltipped tooltipped-s js-menu-target" href="/new"
       aria-label="Create new…"
       data-ga-click="Header, create new, icon:add">
      <svg aria-hidden="true" class="octicon octicon-plus float-left" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M12 9H7v5H5V9H0V7h5V2h2v5h5z"/></svg>
      <span class="dropdown-caret"></span>
    </a>

    <div class="dropdown-menu-content js-menu-content">
      <ul class="dropdown-menu dropdown-menu-sw">
        
<a class="dropdown-item" href="/new" data-ga-click="Header, create new repository">
  New repository
</a>

  <a class="dropdown-item" href="/new/import" data-ga-click="Header, import a repository">
    Import repository
  </a>

<a class="dropdown-item" href="https://gist.github.com/" data-ga-click="Header, create new gist">
  New gist
</a>

  <a class="dropdown-item" href="/organizations/new" data-ga-click="Header, create new organization">
    New organization
  </a>




      </ul>
    </div>
  </li>

  <li class="header-nav-item dropdown js-menu-container">
    <a class="header-nav-link name tooltipped tooltipped-sw js-menu-target" href="/pw393"
       aria-label="View profile and more"
       data-ga-click="Header, show menu, icon:avatar">
      <img alt="@pw393" class="avatar" height="20" src="https://avatars0.githubusercontent.com/u/24728765?v=3&amp;s=40" width="20" />
      <span class="dropdown-caret"></span>
    </a>

    <div class="dropdown-menu-content js-menu-content">
      <div class="dropdown-menu dropdown-menu-sw">
        <div class="dropdown-header header-nav-current-user css-truncate">
          Signed in as <strong class="css-truncate-target">pw393</strong>
        </div>

        <div class="dropdown-divider"></div>

        <a class="dropdown-item" href="/pw393" data-ga-click="Header, go to profile, text:your profile">
          Your profile
        </a>
        <a class="dropdown-item" href="/pw393?tab=stars" data-ga-click="Header, go to starred repos, text:your stars">
          Your stars
        </a>
        <a class="dropdown-item" href="/explore" data-ga-click="Header, go to explore, text:explore">
          Explore
        </a>
          <a class="dropdown-item" href="/integrations" data-ga-click="Header, go to integrations, text:integrations">
            Integrations
          </a>
        <a class="dropdown-item" href="https://help.github.com" data-ga-click="Header, go to help, text:help">
          Help
        </a>

        <div class="dropdown-divider"></div>

        <a class="dropdown-item" href="/settings/profile" data-ga-click="Header, go to settings, icon:settings">
          Settings
        </a>

        <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/logout" class="logout-form" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="xRDY9rc3NVo49gjcugkvLBsAQJOAt/ihsPQ/TfdEXwGunP+tPoLoHYUDn1XCZZA+z0dEZNGxaX5fBV6p/bZA+Q==" /></div>
          <button type="submit" class="dropdown-item dropdown-signout" data-ga-click="Header, sign out, icon:logout">
            Sign out
          </button>
</form>      </div>
    </div>
  </li>
</ul>


    
  </div>
</div>


      


    <div id="start-of-content" class="accessibility-aid"></div>

      <div id="js-flash-container">
</div>


    <div role="main">
        <div itemscope itemtype="http://schema.org/SoftwareSourceCode">
    <div id="js-repo-pjax-container" data-pjax-container>
      
<div class="pagehead repohead instapaper_ignore readability-menu experiment-repo-nav">
  <div class="container repohead-details-container">

    

<ul class="pagehead-actions">

  <li>
        <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/notifications/subscribe" class="js-social-container" data-autosubmit="true" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="0bDaEPm8wxPvwaRtx8ZewPorXD938oxUiTb4+xPcyon7Dq0kAQ5WpOO8v9dP3H9iMf1Ls6aZA0fgnTNG1dugTg==" /></div>      <input class="form-control" id="repository_id" name="repository_id" type="hidden" value="19899531" />

        <div class="select-menu js-menu-container js-select-menu">
          <a href="/sefakilic/coursera-repdata/subscription"
            class="btn btn-sm btn-with-count select-menu-button js-menu-target" role="button" tabindex="0" aria-haspopup="true"
            data-ga-click="Repository, click Watch settings, action:blob#show">
            <span class="js-select-button">
              <svg aria-hidden="true" class="octicon octicon-eye" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
              Watch
            </span>
          </a>
          <a class="social-count js-social-count"
            href="/sefakilic/coursera-repdata/watchers"
            aria-label="3 users are watching this repository">
            3
          </a>

        <div class="select-menu-modal-holder">
          <div class="select-menu-modal subscription-menu-modal js-menu-content" aria-hidden="true">
            <div class="select-menu-header js-navigation-enable" tabindex="-1">
              <svg aria-label="Close" class="octicon octicon-x js-menu-close" height="16" role="img" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"/></svg>
              <span class="select-menu-title">Notifications</span>
            </div>

              <div class="select-menu-list js-navigation-container" role="menu">

                <div class="select-menu-item js-navigation-item selected" role="menuitem" tabindex="0">
                  <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"/></svg>
                  <div class="select-menu-item-text">
                    <input checked="checked" id="do_included" name="do" type="radio" value="included" />
                    <span class="select-menu-item-heading">Not watching</span>
                    <span class="description">Be notified when participating or @mentioned.</span>
                    <span class="js-select-button-text hidden-select-button-text">
                      <svg aria-hidden="true" class="octicon octicon-eye" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                      Watch
                    </span>
                  </div>
                </div>

                <div class="select-menu-item js-navigation-item " role="menuitem" tabindex="0">
                  <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"/></svg>
                  <div class="select-menu-item-text">
                    <input id="do_subscribed" name="do" type="radio" value="subscribed" />
                    <span class="select-menu-item-heading">Watching</span>
                    <span class="description">Be notified of all conversations.</span>
                    <span class="js-select-button-text hidden-select-button-text">
                      <svg aria-hidden="true" class="octicon octicon-eye" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                      Unwatch
                    </span>
                  </div>
                </div>

                <div class="select-menu-item js-navigation-item " role="menuitem" tabindex="0">
                  <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"/></svg>
                  <div class="select-menu-item-text">
                    <input id="do_ignore" name="do" type="radio" value="ignore" />
                    <span class="select-menu-item-heading">Ignoring</span>
                    <span class="description">Never be notified.</span>
                    <span class="js-select-button-text hidden-select-button-text">
                      <svg aria-hidden="true" class="octicon octicon-mute" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8 2.81v10.38c0 .67-.81 1-1.28.53L3 10H1c-.55 0-1-.45-1-1V7c0-.55.45-1 1-1h2l3.72-3.72C7.19 1.81 8 2.14 8 2.81zm7.53 3.22l-1.06-1.06-1.97 1.97-1.97-1.97-1.06 1.06L11.44 8 9.47 9.97l1.06 1.06 1.97-1.97 1.97 1.97 1.06-1.06L13.56 8l1.97-1.97z"/></svg>
                      Stop ignoring
                    </span>
                  </div>
                </div>

              </div>

            </div>
          </div>
        </div>
</form>
  </li>

  <li>
    
  <div class="js-toggler-container js-social-container starring-container ">

    <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/sefakilic/coursera-repdata/unstar" class="starred" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="y7w/PTOOOcoAP5xawKDEW4EzkLYANF2HIC78KT46MX85oTaRchTx39NoZg18Ja7FJyI3eYCnE8TSocr97PDC3A==" /></div>
      <button
        type="submit"
        class="btn btn-sm btn-with-count js-toggler-target"
        aria-label="Unstar this repository" title="Unstar sefakilic/coursera-repdata"
        data-ga-click="Repository, click unstar button, action:blob#show; text:Unstar">
        <svg aria-hidden="true" class="octicon octicon-star" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74z"/></svg>
        Unstar
      </button>
        <a class="social-count js-social-count" href="/sefakilic/coursera-repdata/stargazers"
           aria-label="2 users starred this repository">
          2
        </a>
</form>
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/sefakilic/coursera-repdata/star" class="unstarred" data-remote="true" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="sZ+rSMafuYeAcChAWnsW/SIlhtmjKw5b1qhQf+ssnjo3SZJ0Ro61ed09rmEx1z1g877leMWY+jGEk1bTv+0UmA==" /></div>
      <button
        type="submit"
        class="btn btn-sm btn-with-count js-toggler-target"
        aria-label="Star this repository" title="Star sefakilic/coursera-repdata"
        data-ga-click="Repository, click star button, action:blob#show; text:Star">
        <svg aria-hidden="true" class="octicon octicon-star" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74z"/></svg>
        Star
      </button>
        <a class="social-count js-social-count" href="/sefakilic/coursera-repdata/stargazers"
           aria-label="2 users starred this repository">
          2
        </a>
</form>  </div>

  </li>

  <li>
          <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/sefakilic/coursera-repdata/fork" class="btn-with-count" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="iBB+bDjKvkp7W8E8gi9ZfayGN2sU0P/gm+7owjDMl80QidLt8ri8fXBpEolsbeNAoIWamNkokiUV1PFz5zkr2w==" /></div>
            <button
                type="submit"
                class="btn btn-sm btn-with-count"
                data-ga-click="Repository, show fork modal, action:blob#show; text:Fork"
                title="Fork your own copy of sefakilic/coursera-repdata to your account"
                aria-label="Fork your own copy of sefakilic/coursera-repdata to your account">
              <svg aria-hidden="true" class="octicon octicon-repo-forked" height="16" version="1.1" viewBox="0 0 10 16" width="10"><path fill-rule="evenodd" d="M8 1a1.993 1.993 0 0 0-1 3.72V6L5 8 3 6V4.72A1.993 1.993 0 0 0 2 1a1.993 1.993 0 0 0-1 3.72V6.5l3 3v1.78A1.993 1.993 0 0 0 5 15a1.993 1.993 0 0 0 1-3.72V9.5l3-3V4.72A1.993 1.993 0 0 0 8 1zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3 10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3-10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
              Fork
            </button>
</form>
    <a href="/sefakilic/coursera-repdata/network" class="social-count"
       aria-label="25928 users forked this repository">
      25,928
    </a>
  </li>
</ul>

    <h1 class="public ">
  <svg aria-hidden="true" class="octicon octicon-repo-forked" height="16" version="1.1" viewBox="0 0 10 16" width="10"><path fill-rule="evenodd" d="M8 1a1.993 1.993 0 0 0-1 3.72V6L5 8 3 6V4.72A1.993 1.993 0 0 0 2 1a1.993 1.993 0 0 0-1 3.72V6.5l3 3v1.78A1.993 1.993 0 0 0 5 15a1.993 1.993 0 0 0 1-3.72V9.5l3-3V4.72A1.993 1.993 0 0 0 8 1zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3 10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3-10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
  <span class="author" itemprop="author"><a href="/sefakilic" class="url fn" rel="author">sefakilic</a></span><!--
--><span class="path-divider">/</span><!--
--><strong itemprop="name"><a href="/sefakilic/coursera-repdata" data-pjax="#js-repo-pjax-container">coursera-repdata</a></strong>

    <span class="fork-flag">
      <span class="text">forked from <a href="/rdpeng/RepData_PeerAssessment1">rdpeng/RepData_PeerAssessment1</a></span>
    </span>
</h1>

  </div>
  <div class="container">
    
<nav class="reponav js-repo-nav js-sidenav-container-pjax"
     itemscope
     itemtype="http://schema.org/BreadcrumbList"
     role="navigation"
     data-pjax="#js-repo-pjax-container">

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a href="/sefakilic/coursera-repdata" class="js-selected-navigation-item selected reponav-item" data-hotkey="g c" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches /sefakilic/coursera-repdata" itemprop="url">
      <svg aria-hidden="true" class="octicon octicon-code" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M9.5 3L8 4.5 11.5 8 8 11.5 9.5 13 14 8 9.5 3zm-5 0L0 8l4.5 5L6 11.5 2.5 8 6 4.5 4.5 3z"/></svg>
      <span itemprop="name">Code</span>
      <meta itemprop="position" content="1">
</a>  </span>


  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a href="/sefakilic/coursera-repdata/pulls" class="js-selected-navigation-item reponav-item" data-hotkey="g p" data-selected-links="repo_pulls /sefakilic/coursera-repdata/pulls" itemprop="url">
      <svg aria-hidden="true" class="octicon octicon-git-pull-request" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M11 11.28V5c-.03-.78-.34-1.47-.94-2.06C9.46 2.35 8.78 2.03 8 2H7V0L4 3l3 3V4h1c.27.02.48.11.69.31.21.2.3.42.31.69v6.28A1.993 1.993 0 0 0 10 15a1.993 1.993 0 0 0 1-3.72zm-1 2.92c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zM4 3c0-1.11-.89-2-2-2a1.993 1.993 0 0 0-1 3.72v6.56A1.993 1.993 0 0 0 2 15a1.993 1.993 0 0 0 1-3.72V4.72c.59-.34 1-.98 1-1.72zm-.8 10c0 .66-.55 1.2-1.2 1.2-.65 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
      <span itemprop="name">Pull requests</span>
      <span class="counter">0</span>
      <meta itemprop="position" content="3">
</a>  </span>

  <a href="/sefakilic/coursera-repdata/projects" class="js-selected-navigation-item reponav-item" data-selected-links="repo_projects new_repo_project repo_project /sefakilic/coursera-repdata/projects">
    <svg aria-hidden="true" class="octicon octicon-project" height="16" version="1.1" viewBox="0 0 15 16" width="15"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 0 0-1 1v14a1 1 0 0 0 1 1h13a1 1 0 0 0 1-1V1a1 1 0 0 0-1-1z"/></svg>
    Projects
    <span class="counter">0</span>
</a>
    <a href="/sefakilic/coursera-repdata/wiki" class="js-selected-navigation-item reponav-item" data-hotkey="g w" data-selected-links="repo_wiki /sefakilic/coursera-repdata/wiki">
      <svg aria-hidden="true" class="octicon octicon-book" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M3 5h4v1H3V5zm0 3h4V7H3v1zm0 2h4V9H3v1zm11-5h-4v1h4V5zm0 2h-4v1h4V7zm0 2h-4v1h4V9zm2-6v9c0 .55-.45 1-1 1H9.5l-1 1-1-1H2c-.55 0-1-.45-1-1V3c0-.55.45-1 1-1h5.5l1 1 1-1H15c.55 0 1 .45 1 1zm-8 .5L7.5 3H2v9h6V3.5zm7-.5H9.5l-.5.5V12h6V3z"/></svg>
      Wiki
</a>

  <a href="/sefakilic/coursera-repdata/pulse" class="js-selected-navigation-item reponav-item" data-selected-links="pulse /sefakilic/coursera-repdata/pulse">
    <svg aria-hidden="true" class="octicon octicon-pulse" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M11.5 8L8.8 5.4 6.6 8.5 5.5 1.6 2.38 8H0v2h3.6l.9-1.8.9 5.4L9 8.5l1.6 1.5H14V8z"/></svg>
    Pulse
</a>
  <a href="/sefakilic/coursera-repdata/graphs" class="js-selected-navigation-item reponav-item" data-selected-links="repo_graphs repo_contributors /sefakilic/coursera-repdata/graphs">
    <svg aria-hidden="true" class="octicon octicon-graph" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M16 14v1H0V0h1v14h15zM5 13H3V8h2v5zm4 0H7V3h2v10zm4 0h-2V6h2v7z"/></svg>
    Graphs
</a>

</nav>

  </div>
</div>

<div class="container new-discussion-timeline experiment-repo-nav">
  <div class="repository-content">

    

<a href="/sefakilic/coursera-repdata/blob/887120ed7a37211dd2d2bdc05dbe0e81e0e1ae7d/project2/storm.analysis.md" class="d-none js-permalink-shortcut" data-hotkey="y">Permalink</a>

<!-- blob contrib key: blob_contributors:v21:524f3653c57e083f130da6f544a99050 -->

<div class="file-navigation js-zeroclipboard-container">
  
<div class="select-menu branch-select-menu js-menu-container js-select-menu float-left">
  <button class="btn btn-sm select-menu-button js-menu-target css-truncate" data-hotkey="w"
    
    type="button" aria-label="Switch branches or tags" tabindex="0" aria-haspopup="true">
    <i>Branch:</i>
    <span class="js-select-button css-truncate-target">master</span>
  </button>

  <div class="select-menu-modal-holder js-menu-content js-navigation-container" data-pjax aria-hidden="true">

    <div class="select-menu-modal">
      <div class="select-menu-header">
        <svg aria-label="Close" class="octicon octicon-x js-menu-close" height="16" role="img" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"/></svg>
        <span class="select-menu-title">Switch branches/tags</span>
      </div>

      <div class="select-menu-filters">
        <div class="select-menu-text-filter">
          <input type="text" aria-label="Filter branches/tags" id="context-commitish-filter-field" class="form-control js-filterable-field js-navigation-enable" placeholder="Filter branches/tags">
        </div>
        <div class="select-menu-tabs">
          <ul>
            <li class="select-menu-tab">
              <a href="#" data-tab-filter="branches" data-filter-placeholder="Filter branches/tags" class="js-select-menu-tab" role="tab">Branches</a>
            </li>
            <li class="select-menu-tab">
              <a href="#" data-tab-filter="tags" data-filter-placeholder="Find a tag…" class="js-select-menu-tab" role="tab">Tags</a>
            </li>
          </ul>
        </div>
      </div>

      <div class="select-menu-list select-menu-tab-bucket js-select-menu-tab-bucket" data-tab-filter="branches" role="menu">

        <div data-filterable-for="context-commitish-filter-field" data-filterable-type="substring">


            <a class="select-menu-item js-navigation-item js-navigation-open selected"
               href="/sefakilic/coursera-repdata/blob/master/project2/storm.analysis.md"
               data-name="master"
               data-skip-pjax="true"
               rel="nofollow">
              <svg aria-hidden="true" class="octicon octicon-check select-menu-item-icon" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5z"/></svg>
              <span class="select-menu-item-text css-truncate-target js-select-menu-filter-text">
                master
              </span>
            </a>
        </div>

          <div class="select-menu-no-results">Nothing to show</div>
      </div>

      <div class="select-menu-list select-menu-tab-bucket js-select-menu-tab-bucket" data-tab-filter="tags">
        <div data-filterable-for="context-commitish-filter-field" data-filterable-type="substring">


        </div>

        <div class="select-menu-no-results">Nothing to show</div>
      </div>

    </div>
  </div>
</div>

  <div class="BtnGroup float-right">
    <a href="/sefakilic/coursera-repdata/find/master"
          class="js-pjax-capture-input btn btn-sm BtnGroup-item"
          data-pjax
          data-hotkey="t">
      Find file
    </a>
    <button aria-label="Copy file path to clipboard" class="js-zeroclipboard btn btn-sm BtnGroup-item tooltipped tooltipped-s" data-copied-hint="Copied!" type="button">Copy path</button>
  </div>
  <div class="breadcrumb js-zeroclipboard-target">
    <span class="repo-root js-repo-root"><span class="js-path-segment"><a href="/sefakilic/coursera-repdata"><span>coursera-repdata</span></a></span></span><span class="separator">/</span><span class="js-path-segment"><a href="/sefakilic/coursera-repdata/tree/master/project2"><span>project2</span></a></span><span class="separator">/</span><strong class="final-path">storm.analysis.md</strong>
  </div>
</div>


  <div class="commit-tease">
      <span class="float-right">
        <a class="commit-tease-sha" href="/sefakilic/coursera-repdata/commit/304dacb660c525dc813d2c1728beda8d74de31a4" data-pjax>
          304dacb
        </a>
        <relative-time datetime="2014-08-19T15:47:00Z">Aug 19, 2014</relative-time>
      </span>
      <div>
        <img alt="@sefakilic" class="avatar" height="20" src="https://avatars0.githubusercontent.com/u/1227083?v=3&amp;s=40" width="20" />
        <a href="/sefakilic" class="user-mention" rel="author">sefakilic</a>
          <a href="/sefakilic/coursera-repdata/commit/304dacb660c525dc813d2c1728beda8d74de31a4" class="message" data-pjax="true" title="md added">md added</a>
      </div>

    <div class="commit-tease-contributors">
      <button type="button" class="btn-link muted-link contributors-toggle" data-facebox="#blob_contributors_box">
        <strong>1</strong>
         contributor
      </button>
      
    </div>

    <div id="blob_contributors_box" style="display:none">
      <h2 class="facebox-header" data-facebox-id="facebox-header">Users who have contributed to this file</h2>
      <ul class="facebox-user-list" data-facebox-id="facebox-description">
          <li class="facebox-user-list-item">
            <img alt="@sefakilic" height="24" src="https://avatars2.githubusercontent.com/u/1227083?v=3&amp;s=48" width="24" />
            <a href="/sefakilic">sefakilic</a>
          </li>
      </ul>
    </div>
  </div>


<div class="file">
  <div class="file-header">
  <div class="file-actions">

    <div class="BtnGroup">
      <a href="/sefakilic/coursera-repdata/raw/master/project2/storm.analysis.md" class="btn btn-sm BtnGroup-item" id="raw-url">Raw</a>
        <a href="/sefakilic/coursera-repdata/blame/master/project2/storm.analysis.md" class="btn btn-sm js-update-url-with-hash BtnGroup-item">Blame</a>
      <a href="/sefakilic/coursera-repdata/commits/master/project2/storm.analysis.md" class="btn btn-sm BtnGroup-item" rel="nofollow">History</a>
    </div>

        <a class="btn-octicon tooltipped tooltipped-nw"
           href="github-windows://openRepo/https://github.com/sefakilic/coursera-repdata?branch=master&amp;filepath=project2%2Fstorm.analysis.md"
           aria-label="Open this file in GitHub Desktop"
           data-ga-click="Repository, open with desktop, type:windows">
            <svg aria-hidden="true" class="octicon octicon-device-desktop" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M15 2H1c-.55 0-1 .45-1 1v9c0 .55.45 1 1 1h5.34c-.25.61-.86 1.39-2.34 2h8c-1.48-.61-2.09-1.39-2.34-2H15c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm0 9H1V3h14v8z"/></svg>
        </a>

        <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/sefakilic/coursera-repdata/edit/master/project2/storm.analysis.md" class="inline-form js-update-url-with-hash" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="2W9V5zSJhkVitK/NNh7aHnmjqOKN0LYo6nc/JQqmnax+0Bot25GmAbZOhgj/dM4Qxi1wfahu9Nekv/6d5b9t1w==" /></div>
          <button class="btn-octicon tooltipped tooltipped-nw" type="submit"
            aria-label="Edit the file in your fork of this project" data-hotkey="e" data-disable-with>
            <svg aria-hidden="true" class="octicon octicon-pencil" height="16" version="1.1" viewBox="0 0 14 16" width="14"><path fill-rule="evenodd" d="M0 12v3h3l8-8-3-3-8 8zm3 2H1v-2h1v1h1v1zm10.3-9.3L12 6 9 3l1.3-1.3a.996.996 0 0 1 1.41 0l1.59 1.59c.39.39.39 1.02 0 1.41z"/></svg>
          </button>
</form>        <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="/sefakilic/coursera-repdata/delete/master/project2/storm.analysis.md" class="inline-form" method="post"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /><input name="authenticity_token" type="hidden" value="tg3n6nJx5fGc9PTaofRegI2Hn8oCc+QuLHVeu/mOLwsbysA10AMYs8E3+4LJTvGz4UWYZkbS7Q0/CcpYI+rtWA==" /></div>
          <button class="btn-octicon btn-octicon-danger tooltipped tooltipped-nw" type="submit"
            aria-label="Delete the file in your fork of this project" data-disable-with>
            <svg aria-hidden="true" class="octicon octicon-trashcan" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M11 2H9c0-.55-.45-1-1-1H5c-.55 0-1 .45-1 1H2c-.55 0-1 .45-1 1v1c0 .55.45 1 1 1v9c0 .55.45 1 1 1h7c.55 0 1-.45 1-1V5c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm-1 12H3V5h1v8h1V5h1v8h1V5h1v8h1V5h1v9zm1-10H2V3h9v1z"/></svg>
          </button>
</form>  </div>

  <div class="file-info">
      321 lines (249 sloc)
      <span class="file-info-divider"></span>
    9.61 KB
  </div>
</div>

  
  <div id="readme" class="readme blob instapaper_body">
    <article class="markdown-body entry-content" itemprop="text"><h1><a id="user-content-health-and-economic-impact-of-weather-events-in-the-us" class="anchor" href="#health-and-economic-impact-of-weather-events-in-the-us" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Health and Economic Impact of Weather Events in the US</h1>

<p>Storms and other severe weather events can cause both public health and economic
problems for communities and municipalities. Many severe events can result in
fatalities, injuries, and property damage, and preventing such outcomes to the extent
possible is a key concern.</p>

<p>This project involves exploring the U.S. National Oceanic and Atmospheric
Administration's (NOAA) storm database. This database tracks characteristics of major
storms and weather events in the United States, including when and where they occur, as
well as estimates of any fatalities, injuries, and property damage.</p>

<h1><a id="user-content-synopsis" class="anchor" href="#synopsis" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Synopsis</h1>

<p>The analysis on the storm event database revealed that tornadoes are the most
dangerous weather event to the population health. The second most dangerous
event type is the excessive heat. The economic impact of weather events was
also analyzed. Flash floods and thunderstorm winds caused billions of dollars
in property damages between 1950 and 2011. The largest crop damage caused by
drought, followed by flood and hails.</p>

<h1><a id="user-content-data-processing" class="anchor" href="#data-processing" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Data Processing</h1>

<p>The analysis was performed on
<a href="http://www.ncdc.noaa.gov/stormevents/ftp.jsp">Storm Events Database</a>, provided by
<a href="http://www.ncdc.noaa.gov/">National Climatic Data Center</a>. The data is from a comma-separated-value file available
<a href="https://d396qusza40orc.cloudfront.net/repdata%2Fdata%2FStormData.csv.bz2">here</a>.
There is also some documentation of the data available
<a href="https://d396qusza40orc.cloudfront.net/repdata%2Fpeer2_doc%2Fpd01016005curr.pdf">here</a>.</p>

<p>The first step is to read the data into a data frame.</p>

<div class="highlight highlight-source-r"><pre><span class="pl-smi">storm</span> <span class="pl-k">&lt;-</span> read.csv(bzfile(<span class="pl-s"><span class="pl-pds">"</span>data/repdata-data-StormData.csv.bz2<span class="pl-pds">"</span></span>))</pre></div>

<p>Before the analysis, the data need some preprocessing. Event types don't have a
specific format. For instance, there are events with types <code>Frost/Freeze</code>,
<code>FROST/FREEZE</code> and <code>FROST\\FREEZE</code> which obviously refer to the same type of
event.</p>

<div class="highlight highlight-source-r"><pre><span class="pl-c"><span class="pl-c">#</span> number of unique event types</span>
length(unique(<span class="pl-smi">storm</span><span class="pl-k">$</span><span class="pl-smi">EVTYPE</span>))</pre></div>

<pre><code>## [1] 985
</code></pre>

<div class="highlight highlight-source-r"><pre><span class="pl-c"><span class="pl-c">#</span> translate all letters to lowercase</span>
<span class="pl-smi">event_types</span> <span class="pl-k">&lt;-</span> tolower(<span class="pl-smi">storm</span><span class="pl-k">$</span><span class="pl-smi">EVTYPE</span>)
<span class="pl-c"><span class="pl-c">#</span> replace all punct. characters with a space</span>
<span class="pl-smi">event_types</span> <span class="pl-k">&lt;-</span> gsub(<span class="pl-s"><span class="pl-pds">"</span>[[:blank:][:punct:]+]<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span> <span class="pl-pds">"</span></span>, <span class="pl-smi">event_types</span>)
length(unique(<span class="pl-smi">event_types</span>))</pre></div>

<pre><code>## [1] 874
</code></pre>

<div class="highlight highlight-source-r"><pre><span class="pl-c"><span class="pl-c">#</span> update the data frame</span>
<span class="pl-smi">storm</span><span class="pl-k">$</span><span class="pl-smi">EVTYPE</span> <span class="pl-k">&lt;-</span> <span class="pl-smi">event_types</span></pre></div>

<p>No further data preprocessing was performed although the event type field can be
processed further to merge event types such as <code>tstm wind</code> and <code>thunderstorm wind</code>. 
After the cleaning, as expected, the number of unique event types reduce
significantly. For further analysis, the cleaned event types are used.</p>

<h1><a id="user-content-dangerous-events-with-respect-to-population-health" class="anchor" href="#dangerous-events-with-respect-to-population-health" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Dangerous Events with respect to Population Health</h1>

<p>To find the event types that are most harmful to population health, the number
of casualties are aggregated by the event type.</p>

<div class="highlight highlight-source-r"><pre>library(<span class="pl-smi">plyr</span>)
<span class="pl-smi">casualties</span> <span class="pl-k">&lt;-</span> ddply(<span class="pl-smi">storm</span>, .(<span class="pl-smi">EVTYPE</span>), <span class="pl-smi">summarize</span>,
                    <span class="pl-v">fatalities</span> <span class="pl-k">=</span> sum(<span class="pl-smi">FATALITIES</span>),
                    <span class="pl-v">injuries</span> <span class="pl-k">=</span> sum(<span class="pl-smi">INJURIES</span>))

<span class="pl-c"><span class="pl-c">#</span> Find events that caused most death and injury</span>
<span class="pl-smi">fatal_events</span> <span class="pl-k">&lt;-</span> head(<span class="pl-smi">casualties</span>[order(<span class="pl-smi">casualties</span><span class="pl-k">$</span><span class="pl-smi">fatalities</span>, <span class="pl-v">decreasing</span> <span class="pl-k">=</span> <span class="pl-c1">T</span>), ], <span class="pl-c1">10</span>)
<span class="pl-smi">injury_events</span> <span class="pl-k">&lt;-</span> head(<span class="pl-smi">casualties</span>[order(<span class="pl-smi">casualties</span><span class="pl-k">$</span><span class="pl-smi">injuries</span>, <span class="pl-v">decreasing</span> <span class="pl-k">=</span> <span class="pl-c1">T</span>), ], <span class="pl-c1">10</span>)</pre></div>

<p>Top 10 events that caused largest number of deaths are</p>

<div class="highlight highlight-source-r"><pre><span class="pl-smi">fatal_events</span>[, c(<span class="pl-s"><span class="pl-pds">"</span>EVTYPE<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>fatalities<span class="pl-pds">"</span></span>)]</pre></div>

<pre><code>##             EVTYPE fatalities
## 737        tornado       5633
## 109 excessive heat       1903
## 132    flash flood        978
## 234           heat        937
## 400      lightning        816
## 760      tstm wind        504
## 148          flood        470
## 511    rip current        368
## 309      high wind        248
## 11       avalanche        224
</code></pre>

<p>Top 10 events that caused most number of injuries are</p>

<div class="highlight highlight-source-r"><pre><span class="pl-smi">injury_events</span>[, c(<span class="pl-s"><span class="pl-pds">"</span>EVTYPE<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>injuries<span class="pl-pds">"</span></span>)]</pre></div>

<pre><code>##                EVTYPE injuries
## 737           tornado    91346
## 760         tstm wind     6957
## 148             flood     6789
## 109    excessive heat     6525
## 400         lightning     5230
## 234              heat     2100
## 377         ice storm     1975
## 132       flash flood     1777
## 670 thunderstorm wind     1488
## 203              hail     1361
</code></pre>

<h1><a id="user-content-economic-effects-of-weather-events" class="anchor" href="#economic-effects-of-weather-events" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Economic Effects of Weather Events</h1>

<p>To analyze the impact of weather events on the economy, available property
damage and crop damage reportings/estimates were used.</p>

<p>In the raw data, the property damage is represented with two fields, a number
<code>PROPDMG</code> in dollars and the exponent <code>PROPDMGEXP</code>. Similarly, the crop damage
is represented using two fields, <code>CROPDMG</code> and <code>CROPDMGEXP</code>. The first step in the
analysis is to calculate the property and crop damage for each event.</p>

<div class="highlight highlight-source-r"><pre><span class="pl-en">exp_transform</span> <span class="pl-k">&lt;-</span> <span class="pl-k">function</span>(<span class="pl-smi">e</span>) {
    <span class="pl-c"><span class="pl-c">#</span> h -&gt; hundred, k -&gt; thousand, m -&gt; million, b -&gt; billion</span>
    <span class="pl-k">if</span> (<span class="pl-smi">e</span> <span class="pl-k">%in%</span> c(<span class="pl-s"><span class="pl-pds">'</span>h<span class="pl-pds">'</span></span>, <span class="pl-s"><span class="pl-pds">'</span>H<span class="pl-pds">'</span></span>))
        <span class="pl-k">return</span>(<span class="pl-c1">2</span>)
    <span class="pl-k">else</span> <span class="pl-k">if</span> (<span class="pl-smi">e</span> <span class="pl-k">%in%</span> c(<span class="pl-s"><span class="pl-pds">'</span>k<span class="pl-pds">'</span></span>, <span class="pl-s"><span class="pl-pds">'</span>K<span class="pl-pds">'</span></span>))
        <span class="pl-k">return</span>(<span class="pl-c1">3</span>)
    <span class="pl-k">else</span> <span class="pl-k">if</span> (<span class="pl-smi">e</span> <span class="pl-k">%in%</span> c(<span class="pl-s"><span class="pl-pds">'</span>m<span class="pl-pds">'</span></span>, <span class="pl-s"><span class="pl-pds">'</span>M<span class="pl-pds">'</span></span>))
        <span class="pl-k">return</span>(<span class="pl-c1">6</span>)
    <span class="pl-k">else</span> <span class="pl-k">if</span> (<span class="pl-smi">e</span> <span class="pl-k">%in%</span> c(<span class="pl-s"><span class="pl-pds">'</span>b<span class="pl-pds">'</span></span>, <span class="pl-s"><span class="pl-pds">'</span>B<span class="pl-pds">'</span></span>))
        <span class="pl-k">return</span>(<span class="pl-c1">9</span>)
    <span class="pl-k">else</span> <span class="pl-k">if</span> (<span class="pl-k">!</span>is.na(as.numeric(<span class="pl-smi">e</span>))) <span class="pl-c"><span class="pl-c">#</span> if a digit</span>
        <span class="pl-k">return</span>(as.numeric(<span class="pl-smi">e</span>))
    <span class="pl-k">else</span> <span class="pl-k">if</span> (<span class="pl-smi">e</span> <span class="pl-k">%in%</span> c(<span class="pl-s"><span class="pl-pds">'</span><span class="pl-pds">'</span></span>, <span class="pl-s"><span class="pl-pds">'</span>-<span class="pl-pds">'</span></span>, <span class="pl-s"><span class="pl-pds">'</span>?<span class="pl-pds">'</span></span>, <span class="pl-s"><span class="pl-pds">'</span>+<span class="pl-pds">'</span></span>))
        <span class="pl-k">return</span>(<span class="pl-c1">0</span>)
    <span class="pl-k">else</span> {
        stop(<span class="pl-s"><span class="pl-pds">"</span>Invalid exponent value.<span class="pl-pds">"</span></span>)
    }
}</pre></div>

<div class="highlight highlight-source-r"><pre><span class="pl-smi">prop_dmg_exp</span> <span class="pl-k">&lt;-</span> sapply(<span class="pl-smi">storm</span><span class="pl-k">$</span><span class="pl-smi">PROPDMGEXP</span>, <span class="pl-v">FUN</span><span class="pl-k">=</span><span class="pl-smi">exp_transform</span>)
<span class="pl-smi">storm</span><span class="pl-k">$</span><span class="pl-smi">prop_dmg</span> <span class="pl-k">&lt;-</span> <span class="pl-smi">storm</span><span class="pl-k">$</span><span class="pl-smi">PROPDMG</span> <span class="pl-k">*</span> (<span class="pl-c1">10</span> <span class="pl-k">**</span> <span class="pl-smi">prop_dmg_exp</span>)
<span class="pl-smi">crop_dmg_exp</span> <span class="pl-k">&lt;-</span> sapply(<span class="pl-smi">storm</span><span class="pl-k">$</span><span class="pl-smi">CROPDMGEXP</span>, <span class="pl-v">FUN</span><span class="pl-k">=</span><span class="pl-smi">exp_transform</span>)
<span class="pl-smi">storm</span><span class="pl-k">$</span><span class="pl-smi">crop_dmg</span> <span class="pl-k">&lt;-</span> <span class="pl-smi">storm</span><span class="pl-k">$</span><span class="pl-smi">CROPDMG</span> <span class="pl-k">*</span> (<span class="pl-c1">10</span> <span class="pl-k">**</span> <span class="pl-smi">crop_dmg_exp</span>)</pre></div>

<div class="highlight highlight-source-r"><pre><span class="pl-c"><span class="pl-c">#</span> Compute the economic loss by event type</span>
library(<span class="pl-smi">plyr</span>)
<span class="pl-smi">econ_loss</span> <span class="pl-k">&lt;-</span> ddply(<span class="pl-smi">storm</span>, .(<span class="pl-smi">EVTYPE</span>), <span class="pl-smi">summarize</span>,
                   <span class="pl-v">prop_dmg</span> <span class="pl-k">=</span> sum(<span class="pl-smi">prop_dmg</span>),
                   <span class="pl-v">crop_dmg</span> <span class="pl-k">=</span> sum(<span class="pl-smi">crop_dmg</span>))

<span class="pl-c"><span class="pl-c">#</span> filter out events that caused no economic loss</span>
<span class="pl-smi">econ_loss</span> <span class="pl-k">&lt;-</span> <span class="pl-smi">econ_loss</span>[(<span class="pl-smi">econ_loss</span><span class="pl-k">$</span><span class="pl-smi">prop_dmg</span> <span class="pl-k">&gt;</span> <span class="pl-c1">0</span> <span class="pl-k">|</span> <span class="pl-smi">econ_loss</span><span class="pl-k">$</span><span class="pl-smi">crop_dmg</span> <span class="pl-k">&gt;</span> <span class="pl-c1">0</span>), ]
<span class="pl-smi">prop_dmg_events</span> <span class="pl-k">&lt;-</span> head(<span class="pl-smi">econ_loss</span>[order(<span class="pl-smi">econ_loss</span><span class="pl-k">$</span><span class="pl-smi">prop_dmg</span>, <span class="pl-v">decreasing</span> <span class="pl-k">=</span> <span class="pl-c1">T</span>), ], <span class="pl-c1">10</span>)
<span class="pl-smi">crop_dmg_events</span> <span class="pl-k">&lt;-</span> head(<span class="pl-smi">econ_loss</span>[order(<span class="pl-smi">econ_loss</span><span class="pl-k">$</span><span class="pl-smi">crop_dmg</span>, <span class="pl-v">decreasing</span> <span class="pl-k">=</span> <span class="pl-c1">T</span>), ], <span class="pl-c1">10</span>)</pre></div>

<p>Top 10 events that caused most property damage (in dollars) are as follows</p>

<div class="highlight highlight-source-r"><pre><span class="pl-smi">prop_dmg_events</span>[, c(<span class="pl-s"><span class="pl-pds">"</span>EVTYPE<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>prop_dmg<span class="pl-pds">"</span></span>)]</pre></div>

<pre><code>##                 EVTYPE  prop_dmg
## 132        flash flood 6.820e+13
## 694 thunderstorm winds 2.087e+13
## 737            tornado 1.079e+12
## 203               hail 3.158e+11
## 400          lightning 1.729e+11
## 148              flood 1.447e+11
## 361  hurricane typhoon 6.931e+10
## 155           flooding 5.921e+10
## 581        storm surge 4.332e+10
## 264         heavy snow 1.793e+10
</code></pre>

<p>Similarly, the events that caused biggest crop damage are</p>

<div class="highlight highlight-source-r"><pre><span class="pl-smi">crop_dmg_events</span>[, c(<span class="pl-s"><span class="pl-pds">"</span>EVTYPE<span class="pl-pds">"</span></span>, <span class="pl-s"><span class="pl-pds">"</span>crop_dmg<span class="pl-pds">"</span></span>)]</pre></div>

<pre><code>##                EVTYPE  crop_dmg
## 77            drought 1.397e+10
## 148             flood 5.662e+09
## 515       river flood 5.029e+09
## 377         ice storm 5.022e+09
## 203              hail 3.026e+09
## 352         hurricane 2.742e+09
## 361 hurricane typhoon 2.608e+09
## 132       flash flood 1.421e+09
## 118      extreme cold 1.313e+09
## 179      frost freeze 1.094e+09
</code></pre>

<h1><a id="user-content-results" class="anchor" href="#results" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Results</h1>

<h2><a id="user-content-health-impact-of-weather-events" class="anchor" href="#health-impact-of-weather-events" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Health impact of weather events</h2>

<p>The following plot shows top dangerous weather event types.</p>

<div class="highlight highlight-source-r"><pre>library(<span class="pl-smi">ggplot2</span>)
library(<span class="pl-smi">gridExtra</span>)
<span class="pl-c"><span class="pl-c">#</span> Set the levels in order</span>
<span class="pl-smi">p1</span> <span class="pl-k">&lt;-</span> ggplot(<span class="pl-v">data</span><span class="pl-k">=</span><span class="pl-smi">fatal_events</span>,
             aes(<span class="pl-v">x</span><span class="pl-k">=</span>reorder(<span class="pl-smi">EVTYPE</span>, <span class="pl-smi">fatalities</span>), <span class="pl-v">y</span><span class="pl-k">=</span><span class="pl-smi">fatalities</span>, <span class="pl-v">fill</span><span class="pl-k">=</span><span class="pl-smi">fatalities</span>)) <span class="pl-k">+</span>
    geom_bar(<span class="pl-v">stat</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>identity<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    coord_flip() <span class="pl-k">+</span>
    ylab(<span class="pl-s"><span class="pl-pds">"</span>Total number of fatalities<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    xlab(<span class="pl-s"><span class="pl-pds">"</span>Event type<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    theme(<span class="pl-v">legend.position</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>none<span class="pl-pds">"</span></span>)

<span class="pl-smi">p2</span> <span class="pl-k">&lt;-</span> ggplot(<span class="pl-v">data</span><span class="pl-k">=</span><span class="pl-smi">injury_events</span>,
             aes(<span class="pl-v">x</span><span class="pl-k">=</span>reorder(<span class="pl-smi">EVTYPE</span>, <span class="pl-smi">injuries</span>), <span class="pl-v">y</span><span class="pl-k">=</span><span class="pl-smi">injuries</span>, <span class="pl-v">fill</span><span class="pl-k">=</span><span class="pl-smi">injuries</span>)) <span class="pl-k">+</span>
    geom_bar(<span class="pl-v">stat</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>identity<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    coord_flip() <span class="pl-k">+</span> 
    ylab(<span class="pl-s"><span class="pl-pds">"</span>Total number of injuries<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    xlab(<span class="pl-s"><span class="pl-pds">"</span>Event type<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    theme(<span class="pl-v">legend.position</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>none<span class="pl-pds">"</span></span>)

grid.arrange(<span class="pl-smi">p1</span>, <span class="pl-smi">p2</span>, <span class="pl-v">main</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Top deadly weather events in the US (1950-2011)<span class="pl-pds">"</span></span>)</pre></div>

<p><a href="/sefakilic/coursera-repdata/blob/master/project2/figure/unnamed-chunk-11.png" target="_blank"><img src="/sefakilic/coursera-repdata/raw/master/project2/figure/unnamed-chunk-11.png" alt="plot of chunk unnamed-chunk-11" style="max-width:100%;"></a> </p>

<p>Tornadoes cause most number of deaths and injuries among all event types. There 
are more than 5,000 deaths and more than 10,000 injuries in the last 60 years
in US, due to tornadoes. 
The other event types that are most dangerous with respect to population health
are excessive heat and flash floods.</p>

<h2><a id="user-content-economic-impact-of-weather-events" class="anchor" href="#economic-impact-of-weather-events" aria-hidden="true"><svg aria-hidden="true" class="octicon octicon-link" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Economic impact of weather events</h2>

<p>The following plot shows the most severe weather event types with respect to
economic cost that they have costed since 1950s.</p>

<div class="highlight highlight-source-r"><pre>library(<span class="pl-smi">ggplot2</span>)
library(<span class="pl-smi">gridExtra</span>)
<span class="pl-c"><span class="pl-c">#</span> Set the levels in order</span>
<span class="pl-smi">p1</span> <span class="pl-k">&lt;-</span> ggplot(<span class="pl-v">data</span><span class="pl-k">=</span><span class="pl-smi">prop_dmg_events</span>,
             aes(<span class="pl-v">x</span><span class="pl-k">=</span>reorder(<span class="pl-smi">EVTYPE</span>, <span class="pl-smi">prop_dmg</span>), <span class="pl-v">y</span><span class="pl-k">=</span>log10(<span class="pl-smi">prop_dmg</span>), <span class="pl-v">fill</span><span class="pl-k">=</span><span class="pl-smi">prop_dmg</span> )) <span class="pl-k">+</span>
    geom_bar(<span class="pl-v">stat</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>identity<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    coord_flip() <span class="pl-k">+</span>
    xlab(<span class="pl-s"><span class="pl-pds">"</span>Event type<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    ylab(<span class="pl-s"><span class="pl-pds">"</span>Property damage in dollars (log-scale)<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    theme(<span class="pl-v">legend.position</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>none<span class="pl-pds">"</span></span>)

<span class="pl-smi">p2</span> <span class="pl-k">&lt;-</span> ggplot(<span class="pl-v">data</span><span class="pl-k">=</span><span class="pl-smi">crop_dmg_events</span>,
             aes(<span class="pl-v">x</span><span class="pl-k">=</span>reorder(<span class="pl-smi">EVTYPE</span>, <span class="pl-smi">crop_dmg</span>), <span class="pl-v">y</span><span class="pl-k">=</span><span class="pl-smi">crop_dmg</span>, <span class="pl-v">fill</span><span class="pl-k">=</span><span class="pl-smi">crop_dmg</span>)) <span class="pl-k">+</span>
    geom_bar(<span class="pl-v">stat</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>identity<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    coord_flip() <span class="pl-k">+</span> 
    xlab(<span class="pl-s"><span class="pl-pds">"</span>Event type<span class="pl-pds">"</span></span>) <span class="pl-k">+</span>
    ylab(<span class="pl-s"><span class="pl-pds">"</span>Crop damage in dollars<span class="pl-pds">"</span></span>) <span class="pl-k">+</span> 
    theme(<span class="pl-v">legend.position</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>none<span class="pl-pds">"</span></span>)

grid.arrange(<span class="pl-smi">p1</span>, <span class="pl-smi">p2</span>, <span class="pl-v">main</span><span class="pl-k">=</span><span class="pl-s"><span class="pl-pds">"</span>Weather costs to the US economy (1950-2011)<span class="pl-pds">"</span></span>)</pre></div>

<p><a href="/sefakilic/coursera-repdata/blob/master/project2/figure/unnamed-chunk-12.png" target="_blank"><img src="/sefakilic/coursera-repdata/raw/master/project2/figure/unnamed-chunk-12.png" alt="plot of chunk unnamed-chunk-12" style="max-width:100%;"></a> </p>

<p>Property damages are given in logarithmic scale due to large range of values.
The data shows that flash floods and thunderstorm winds cost the largest
property damages among weather-related natural diseasters. Note that, due to
untidy nature of the available data, type <code>flood</code> and <code>flash flood</code> are
separate values and should be merged for more accurate data-driven conclusions.</p>

<p>The most severe weather event in terms of crop damage is the drought. In the last
half century, the drought has caused more than 10 billion dollars damage. Other
severe crop-damage-causing event types are floods and hails.</p>
</article>
  </div>

</div>

<button type="button" data-facebox="#jump-to-line" data-facebox-class="linejump" data-hotkey="l" class="d-none">Jump to Line</button>
<div id="jump-to-line" style="display:none">
  <!-- '"` --><!-- </textarea></xmp> --></option></form><form accept-charset="UTF-8" action="" class="js-jump-to-line-form" method="get"><div style="margin:0;padding:0;display:inline"><input name="utf8" type="hidden" value="&#x2713;" /></div>
    <input class="form-control linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" aria-label="Jump to line" autofocus>
    <button type="submit" class="btn">Go</button>
</form></div>

  </div>
  <div class="modal-backdrop js-touch-events"></div>
</div>


    </div>
  </div>

    </div>

        <div class="container site-footer-container">
  <div class="site-footer" role="contentinfo">
    <ul class="site-footer-links float-right">
        <li><a href="https://github.com/contact" data-ga-click="Footer, go to contact, text:contact">Contact GitHub</a></li>
      <li><a href="https://developer.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li><a href="https://training.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
      <li><a href="https://shop.github.com" data-ga-click="Footer, go to shop, text:shop">Shop</a></li>
        <li><a href="https://github.com/blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a href="https://github.com/about" data-ga-click="Footer, go to about, text:about">About</a></li>

    </ul>

    <a href="https://github.com" aria-label="Homepage" class="site-footer-mark" title="GitHub">
      <svg aria-hidden="true" class="octicon octicon-mark-github" height="24" version="1.1" viewBox="0 0 16 16" width="24"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0 0 16 8c0-4.42-3.58-8-8-8z"/></svg>
</a>
    <ul class="site-footer-links">
      <li>&copy; 2016 <span title="0.08052s from github-fe130-cp1-prd.iad.github.net">GitHub</span>, Inc.</li>
        <li><a href="https://github.com/site/terms" data-ga-click="Footer, go to terms, text:terms">Terms</a></li>
        <li><a href="https://github.com/site/privacy" data-ga-click="Footer, go to privacy, text:privacy">Privacy</a></li>
        <li><a href="https://github.com/security" data-ga-click="Footer, go to security, text:security">Security</a></li>
        <li><a href="https://status.github.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
        <li><a href="https://help.github.com" data-ga-click="Footer, go to help, text:help">Help</a></li>
    </ul>
  </div>
</div>



    

    <div id="ajax-error-message" class="ajax-error-message flash flash-error">
      <svg aria-hidden="true" class="octicon octicon-alert" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8.865 1.52c-.18-.31-.51-.5-.87-.5s-.69.19-.87.5L.275 13.5c-.18.31-.18.69 0 1 .19.31.52.5.87.5h13.7c.36 0 .69-.19.86-.5.17-.31.18-.69.01-1L8.865 1.52zM8.995 13h-2v-2h2v2zm0-3h-2V6h2v4z"/></svg>
      <button type="button" class="flash-close js-flash-close js-ajax-error-dismiss" aria-label="Dismiss error">
        <svg aria-hidden="true" class="octicon octicon-x" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"/></svg>
      </button>
      You can't perform that action at this time.
    </div>


      
      <script crossorigin="anonymous" integrity="sha256-6oyRrlVv4QXObfjQEAx3ailpVc5Wet1OIgn+eK5TbV4=" src="https://assets-cdn.github.com/assets/frameworks-ea8c91ae556fe105ce6df8d0100c776a296955ce567add4e2209fe78ae536d5e.js"></script>
      <script async="async" crossorigin="anonymous" integrity="sha256-bF2REMkhn8ABnD0dWjmB+w7m63D4BDt5YmrOGmDGnAI=" src="https://assets-cdn.github.com/assets/github-6c5d9110c9219fc0019c3d1d5a3981fb0ee6eb70f8043b79626ace1a60c69c02.js"></script>
      
      
      
      
    <div class="js-stale-session-flash stale-session-flash flash flash-warn flash-banner d-none">
      <svg aria-hidden="true" class="octicon octicon-alert" height="16" version="1.1" viewBox="0 0 16 16" width="16"><path fill-rule="evenodd" d="M8.865 1.52c-.18-.31-.51-.5-.87-.5s-.69.19-.87.5L.275 13.5c-.18.31-.18.69 0 1 .19.31.52.5.87.5h13.7c.36 0 .69-.19.86-.5.17-.31.18-.69.01-1L8.865 1.52zM8.995 13h-2v-2h2v2zm0-3h-2V6h2v4z"/></svg>
      <span class="signed-in-tab-flash">You signed in with another tab or window. <a href="">Reload</a> to refresh your session.</span>
      <span class="signed-out-tab-flash">You signed out in another tab or window. <a href="">Reload</a> to refresh your session.</span>
    </div>
    <div class="facebox" id="facebox" style="display:none;">
  <div class="facebox-popup">
    <div class="facebox-content" role="dialog" aria-labelledby="facebox-header" aria-describedby="facebox-description">
    </div>
    <button type="button" class="facebox-close js-facebox-close" aria-label="Close modal">
      <svg aria-hidden="true" class="octicon octicon-x" height="16" version="1.1" viewBox="0 0 12 16" width="12"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48z"/></svg>
    </button>
  </div>
</div>

  </body>
</html>

