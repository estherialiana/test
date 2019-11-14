





<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8">
  <link rel="dns-prefetch" href="https://github.githubassets.com">
  <link rel="dns-prefetch" href="https://avatars0.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars1.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars2.githubusercontent.com">
  <link rel="dns-prefetch" href="https://avatars3.githubusercontent.com">
  <link rel="dns-prefetch" href="https://github-cloud.s3.amazonaws.com">
  <link rel="dns-prefetch" href="https://user-images.githubusercontent.com/">



  <link crossorigin="anonymous" media="all" integrity="sha512-/YEVWs7BzxfKyUd6zVxjEQcXRWsLbcEjv045Rq8DSoipySmQblhVKxlXLva2GtNd5DhwCxHwW1RM0N9I7S2Vew==" rel="stylesheet" href="https://github.githubassets.com/assets/frameworks-481a47a96965f6706fb41bae0d14b09a.css" />
  
    <link crossorigin="anonymous" media="all" integrity="sha512-UuDKgNf/5qyjHC2IFg8kEkn3j2n+D4ShuvNV5eohEqUPfuPzqAxcd98IqomrgGo/g36tB35YvxoA1CbXgE0iFg==" rel="stylesheet" href="https://github.githubassets.com/assets/github-5362384f9e2512870c388a187eaf4868.css" />
    
    
    
    

  <meta name="viewport" content="width=device-width">
  
  <title>sellfazz-backend/API.md at master · payfazz/sellfazz-backend</title>
    <meta name="description" content="The backend code for Sellfazz v2. Contribute to payfazz/sellfazz-backend development by creating an account on GitHub.">
    <link rel="search" type="application/opensearchdescription+xml" href="/opensearch.xml" title="GitHub">
  <link rel="fluid-icon" href="https://github.com/fluidicon.png" title="GitHub">
  <meta property="fb:app_id" content="1401488693436528">

    <meta name="twitter:image:src" content="https://avatars3.githubusercontent.com/u/27276028?s=400&amp;v=4" /><meta name="twitter:site" content="@github" /><meta name="twitter:card" content="summary" /><meta name="twitter:title" content="payfazz/sellfazz-backend" /><meta name="twitter:description" content="The backend code for Sellfazz v2. Contribute to payfazz/sellfazz-backend development by creating an account on GitHub." />
    <meta property="og:image" content="https://avatars3.githubusercontent.com/u/27276028?s=400&amp;v=4" /><meta property="og:site_name" content="GitHub" /><meta property="og:type" content="object" /><meta property="og:title" content="payfazz/sellfazz-backend" /><meta property="og:url" content="https://github.com/payfazz/sellfazz-backend" /><meta property="og:description" content="The backend code for Sellfazz v2. Contribute to payfazz/sellfazz-backend development by creating an account on GitHub." />

  <link rel="assets" href="https://github.githubassets.com/">
  <link rel="web-socket" href="wss://live.github.com/_sockets/VjI6NDUxMDcwNzg1OmZmNDFjMzVjZjg0ODM0M2JlZWQ3Y2ZjYWQwYWUzZTc0ODcyNTEzZDVlMGFiNjdkNTczMjYyNzcxY2U5MGQzNmY=--1ad492da331ae9efa24c7ae93e0ffb6c9a3eac2f">
  <link rel="sudo-modal" href="/sessions/sudo_modal">
  <meta name="request-id" content="C5BC:4C67:164C23:1FD0D3:5DCCD619" data-pjax-transient>


  

  <meta name="selected-link" value="repo_source" data-pjax-transient>

      <meta name="google-site-verification" content="KT5gs8h0wvaagLKAVWq8bbeNwnZZK1r1XQysX3xurLU">
    <meta name="google-site-verification" content="ZzhVyEFwb7w3e0-uOTltm8Jsck2F5StVihD0exw2fsA">
    <meta name="google-site-verification" content="GXs5KoUUkNCoaAZn7wPN-t01Pywp9M3sEjnt_3_ZWPc">

  <meta name="octolytics-host" content="collector.githubapp.com" /><meta name="octolytics-app-id" content="github" /><meta name="octolytics-event-url" content="https://collector.githubapp.com/github-external/browser_event" /><meta name="octolytics-dimension-request_id" content="C5BC:4C67:164C23:1FD0D3:5DCCD619" /><meta name="octolytics-dimension-region_edge" content="ap-southeast-1" /><meta name="octolytics-dimension-region_render" content="iad" /><meta name="octolytics-dimension-ga_id" content="" class="js-octo-ga-id" /><meta name="octolytics-dimension-visitor_id" content="8759645944188860137" /><meta name="octolytics-actor-id" content="55684684" /><meta name="octolytics-actor-login" content="estherialiana" /><meta name="octolytics-actor-hash" content="838e7bae8bdb26c640d02c2d4514c428cd56d0fce518e878b23e9149f9fb07af" />
<meta name="analytics-location" content="/&lt;user-name&gt;/&lt;repo-name&gt;/blob/show" data-pjax-transient="true" />



    <meta name="google-analytics" content="UA-3769691-2">

  <meta class="js-ga-set" name="userId" content="2276cb38ac720101ae7f73aad738e6c5">

<meta class="js-ga-set" name="dimension1" content="Logged In">



  

      <meta name="hostname" content="github.com">
    <meta name="user-login" content="estherialiana">

      <meta name="expected-hostname" content="github.com">
    <meta name="js-proxy-site-detection-payload" content="MWE0YTQ0MjFjYzAyNWQ5YjhiYjRkMDgxYjViNDhjMjhmMTYzZDA2ZTdmNDFhMzUwYzIzYTliMmYzMDk3OTQ0OXx7InJlbW90ZV9hZGRyZXNzIjoiMTEyLjIxNS4yMi4xNCIsInJlcXVlc3RfaWQiOiJDNUJDOjRDNjc6MTY0QzIzOjFGRDBEMzo1RENDRDYxOSIsInRpbWVzdGFtcCI6MTU3MzcwNTI0MiwiaG9zdCI6ImdpdGh1Yi5jb20ifQ==">

    <meta name="enabled-features" content="LAUNCH_PROJECT,ACTIONS_V2_ON_MARKETPLACE,MARKETPLACE_FEATURED_BLOG_POSTS,MARKETPLACE_INVOICED_BILLING,MARKETPLACE_SOCIAL_PROOF_CUSTOMERS,MARKETPLACE_TRENDING_SOCIAL_PROOF,MARKETPLACE_RECOMMENDATIONS,MARKETPLACE_PENDING_INSTALLATIONS,NOTIFY_ON_BLOCK,RELATED_ISSUES,GHE_CLOUD_TRIAL">

  <meta name="html-safe-nonce" content="af8d932e6ab7f58155004bd60d27461fd523fa52">

  <meta http-equiv="x-pjax-version" content="a24d82d484ab528e3f0db8bcd6034055">
  

      <link href="https://github.com/payfazz/sellfazz-backend/commits/master.atom?token=ANI24TBORZ4VK67XHWB4TW533IEJS" rel="alternate" title="Recent Commits to sellfazz-backend:master" type="application/atom+xml">

  <meta name="go-import" content="github.com/payfazz/sellfazz-backend git https://github.com/payfazz/sellfazz-backend.git">

  <meta name="octolytics-dimension-user_id" content="27276028" /><meta name="octolytics-dimension-user_login" content="payfazz" /><meta name="octolytics-dimension-repository_id" content="205763991" /><meta name="octolytics-dimension-repository_nwo" content="payfazz/sellfazz-backend" /><meta name="octolytics-dimension-repository_public" content="false" /><meta name="octolytics-dimension-repository_is_fork" content="false" /><meta name="octolytics-dimension-repository_network_root_id" content="205763991" /><meta name="octolytics-dimension-repository_network_root_nwo" content="payfazz/sellfazz-backend" /><meta name="octolytics-dimension-repository_explore_github_marketplace_ci_cta_shown" content="false" />


    <link rel="canonical" href="https://github.com/payfazz/sellfazz-backend/blob/master/docs/API.md" data-pjax-transient>


  <meta name="browser-stats-url" content="https://api.github.com/_private/browser/stats">

  <meta name="browser-errors-url" content="https://api.github.com/_private/browser/errors">

  <link rel="mask-icon" href="https://github.githubassets.com/pinned-octocat.svg" color="#000000">
  <link rel="icon" type="image/x-icon" class="js-site-favicon" href="https://github.githubassets.com/favicon.ico">

<meta name="theme-color" content="#1e2327">



  <meta name="webauthn-auth-enabled" content="true">

  <meta name="webauthn-registration-enabled" content="true">

  <link rel="manifest" href="/manifest.json" crossOrigin="use-credentials">

  </head>

  <body class="logged-in env-production page-responsive page-blob">
    

  <div class="position-relative js-header-wrapper ">
    <a href="#start-of-content" tabindex="1" class="p-3 bg-blue text-white show-on-focus js-skip-to-content">Skip to content</a>
    <span class="Progress progress-pjax-loader position-fixed width-full js-pjax-loader-bar">
      <span class="progress-pjax-loader-bar top-0 left-0" style="width: 0%;"></span>
    </span>

    
    
    


          <header class="Header js-details-container Details flex-wrap flex-lg-nowrap p-responsive" role="banner">

    <div class="Header-item d-none d-lg-flex">
      <a class="Header-link" href="https://github.com/" data-hotkey="g d" aria-label="Homepage" data-ga-click="Header, go to dashboard, icon:logo">
  <svg class="octicon octicon-mark-github v-align-middle" height="32" viewBox="0 0 16 16" version="1.1" width="32" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
</a>

    </div>

    <div class="Header-item d-lg-none">
      <button class="Header-link btn-link js-details-target" type="button" aria-label="Toggle navigation" aria-expanded="false">
        <svg height="24" class="octicon octicon-three-bars" viewBox="0 0 12 16" version="1.1" width="18" aria-hidden="true"><path fill-rule="evenodd" d="M11.41 9H.59C0 9 0 8.59 0 8c0-.59 0-1 .59-1H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1h.01zm0-4H.59C0 5 0 4.59 0 4c0-.59 0-1 .59-1H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1h.01zM.59 11H11.4c.59 0 .59.41.59 1 0 .59 0 1-.59 1H.59C0 13 0 12.59 0 12c0-.59 0-1 .59-1z"/></svg>
      </button>
    </div>

    <div class="Header-item Header-item--full flex-column flex-lg-row width-full flex-order-2 flex-lg-order-none mr-0 mr-lg-3 mt-3 mt-lg-0 Details-content--hidden">
        <div class="header-search flex-self-stretch flex-lg-self-auto mr-0 mr-lg-3 mb-3 mb-lg-0 scoped-search site-scoped-search js-site-search position-relative js-jump-to"
  role="combobox"
  aria-owns="jump-to-results"
  aria-label="Search or jump to"
  aria-haspopup="listbox"
  aria-expanded="false"
>
  <div class="position-relative">
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="js-site-search-form" role="search" aria-label="Site" data-scope-type="Repository" data-scope-id="205763991" data-scoped-search-url="/payfazz/sellfazz-backend/search" data-unscoped-search-url="/search" action="/payfazz/sellfazz-backend/search" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
      <label class="form-control input-sm header-search-wrapper p-0 header-search-wrapper-jump-to position-relative d-flex flex-justify-between flex-items-center js-chromeless-input-container">
        <input type="text"
          class="form-control input-sm header-search-input jump-to-field js-jump-to-field js-site-search-focus js-site-search-field is-clearable"
          data-hotkey="s,/"
          name="q"
          value=""
          placeholder="Search or jump to…"
          data-unscoped-placeholder="Search or jump to…"
          data-scoped-placeholder="Search or jump to…"
          autocapitalize="off"
          aria-autocomplete="list"
          aria-controls="jump-to-results"
          aria-label="Search or jump to…"
          data-jump-to-suggestions-path="/_graphql/GetSuggestedNavigationDestinations#csrf-token=7QFXcrgcFegJOu1Z4Dw7SqrTNk9kNQ9OCVelNXaFkQpvo/R3N/pmGyFCd4zLhujN1JP5AEFCECxc7bZimmYobQ=="
          spellcheck="false"
          autocomplete="off"
          >
          <input type="hidden" class="js-site-search-type-field" name="type" >
            <img src="https://github.githubassets.com/images/search-key-slash.svg" alt="" class="mr-2 header-search-key-slash">

            <div class="Box position-absolute overflow-hidden d-none jump-to-suggestions js-jump-to-suggestions-container">
              
<ul class="d-none js-jump-to-suggestions-template-container">
  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-suggestion" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 00-1 1v14a1 1 0 001 1h13a1 1 0 001-1V1a1 1 0 00-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0013 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 000-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>

</ul>

<ul class="d-none js-jump-to-no-results-template-container">
  <li class="d-flex flex-justify-center flex-items-center f5 d-none js-jump-to-suggestion p-2">
    <span class="text-gray">No suggested jump to results</span>
  </li>
</ul>

<ul id="jump-to-results" role="listbox" class="p-0 m-0 js-navigation-container jump-to-suggestions-results-container js-jump-to-suggestions-results-container">
  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-scoped-search d-none" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 00-1 1v14a1 1 0 001 1h13a1 1 0 001-1V1a1 1 0 00-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0013 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 000-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>

  

<li class="d-flex flex-justify-start flex-items-center p-0 f5 navigation-item js-navigation-item js-jump-to-global-search d-none" role="option">
  <a tabindex="-1" class="no-underline d-flex flex-auto flex-items-center jump-to-suggestions-path js-jump-to-suggestion-path js-navigation-open p-2" href="">
    <div class="jump-to-octicon js-jump-to-octicon flex-shrink-0 mr-2 text-center d-none">
      <svg height="16" width="16" class="octicon octicon-repo flex-shrink-0 js-jump-to-octicon-repo d-none" title="Repository" aria-label="Repository" viewBox="0 0 12 16" version="1.1" role="img"><path fill-rule="evenodd" d="M4 9H3V8h1v1zm0-3H3v1h1V6zm0-2H3v1h1V4zm0-2H3v1h1V2zm8-1v12c0 .55-.45 1-1 1H6v2l-1.5-1.5L3 16v-2H1c-.55 0-1-.45-1-1V1c0-.55.45-1 1-1h10c.55 0 1 .45 1 1zm-1 10H1v2h2v-1h3v1h5v-2zm0-10H2v9h9V1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-project flex-shrink-0 js-jump-to-octicon-project d-none" title="Project" aria-label="Project" viewBox="0 0 15 16" version="1.1" role="img"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 00-1 1v14a1 1 0 001 1h13a1 1 0 001-1V1a1 1 0 00-1-1z"/></svg>
      <svg height="16" width="16" class="octicon octicon-search flex-shrink-0 js-jump-to-octicon-search d-none" title="Search" aria-label="Search" viewBox="0 0 16 16" version="1.1" role="img"><path fill-rule="evenodd" d="M15.7 13.3l-3.81-3.83A5.93 5.93 0 0013 6c0-3.31-2.69-6-6-6S1 2.69 1 6s2.69 6 6 6c1.3 0 2.48-.41 3.47-1.11l3.83 3.81c.19.2.45.3.7.3.25 0 .52-.09.7-.3a.996.996 0 000-1.41v.01zM7 10.7c-2.59 0-4.7-2.11-4.7-4.7 0-2.59 2.11-4.7 4.7-4.7 2.59 0 4.7 2.11 4.7 4.7 0 2.59-2.11 4.7-4.7 4.7z"/></svg>
    </div>

    <img class="avatar mr-2 flex-shrink-0 js-jump-to-suggestion-avatar d-none" alt="" aria-label="Team" src="" width="28" height="28">

    <div class="jump-to-suggestion-name js-jump-to-suggestion-name flex-auto overflow-hidden text-left no-wrap css-truncate css-truncate-target">
    </div>

    <div class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none js-jump-to-badge-search">
      <span class="js-jump-to-badge-search-text-default d-none" aria-label="in this repository">
        In this repository
      </span>
      <span class="js-jump-to-badge-search-text-global d-none" aria-label="in all of GitHub">
        All GitHub
      </span>
      <span aria-hidden="true" class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>

    <div aria-hidden="true" class="border rounded-1 flex-shrink-0 bg-gray px-1 text-gray-light ml-1 f6 d-none d-on-nav-focus js-jump-to-badge-jump">
      Jump to
      <span class="d-inline-block ml-1 v-align-middle">↵</span>
    </div>
  </a>
</li>


    <li class="d-flex flex-justify-center flex-items-center p-0 f5 js-jump-to-suggestion">
      <img src="https://github.githubassets.com/images/spinners/octocat-spinner-128.gif" alt="Octocat Spinner Icon" class="m-2" width="28">
    </li>
</ul>

            </div>
      </label>
</form>  </div>
</div>


      <nav class="d-flex flex-column flex-lg-row flex-self-stretch flex-lg-self-auto" aria-label="Global">
    <a class="Header-link d-block d-lg-none py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-ga-click="Header, click, Nav menu - item:dashboard:user" aria-label="Dashboard" href="/dashboard">
      Dashboard
</a>
  <a class="js-selected-navigation-item Header-link  mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-hotkey="g p" data-ga-click="Header, click, Nav menu - item:pulls context:user" aria-label="Pull requests you created" data-selected-links="/pulls /pulls/assigned /pulls/mentioned /pulls" href="/pulls">
    Pull requests
</a>
  <a class="js-selected-navigation-item Header-link  mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-hotkey="g i" data-ga-click="Header, click, Nav menu - item:issues context:user" aria-label="Issues you created" data-selected-links="/issues /issues/assigned /issues/mentioned /issues" href="/issues">
    Issues
</a>
    <div class="mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15">
      <a class="js-selected-navigation-item Header-link" data-ga-click="Header, click, Nav menu - item:marketplace context:user" data-octo-click="marketplace_click" data-octo-dimensions="location:nav_bar" data-selected-links=" /marketplace" href="/marketplace">
        Marketplace
</a>      

    </div>

  <a class="js-selected-navigation-item Header-link  mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" data-ga-click="Header, click, Nav menu - item:explore" data-selected-links="/explore /trending /trending/developers /integrations /integrations/feature/code /integrations/feature/collaborate /integrations/feature/ship showcases showcases_search showcases_landing /explore" href="/explore">
    Explore
</a>


    <a class="Header-link d-block d-lg-none mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15" href="https://github.com/estherialiana">
      <img class="avatar" height="20" width="20" alt="@estherialiana" src="https://avatars1.githubusercontent.com/u/55684684?s=60&amp;v=4" />
      estherialiana
</a>
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form action="/logout" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="47MnbdwIhLWtdarC5RIGIMSAB8U4I4qoUtY3sQlonJ7RTifzURMxWoRbYjlVIO/xTjsJs1iEHEl4+WCX//dRKA==" />
      <button type="submit" class="Header-link mr-0 mr-lg-3 py-2 py-lg-0 border-top border-lg-top-0 border-white-fade-15 d-lg-none btn-link d-block width-full text-left" data-ga-click="Header, sign out, icon:logout" style="padding-left: 2px;">
        <svg class="octicon octicon-sign-out v-align-middle" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 9V7H8V5h4V3l4 3-4 3zm-2 3H6V3L2 1h8v3h1V1c0-.55-.45-1-1-1H1C.45 0 0 .45 0 1v11.38c0 .39.22.73.55.91L6 16.01V13h4c.55 0 1-.45 1-1V8h-1v4z"/></svg>
        Sign out
      </button>
</form></nav>

    </div>

    <div class="Header-item Header-item--full flex-justify-center d-lg-none position-relative">
      <div class="css-truncate css-truncate-target width-fit position-absolute left-0 right-0 text-center">
              <svg class="octicon octicon-lock" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 13H3v-1h1v1zm8-6v7c0 .55-.45 1-1 1H1c-.55 0-1-.45-1-1V7c0-.55.45-1 1-1h1V4c0-2.2 1.8-4 4-4s4 1.8 4 4v2h1c.55 0 1 .45 1 1zM3.8 6h4.41V4c0-1.22-.98-2.2-2.2-2.2-1.22 0-2.2.98-2.2 2.2v2H3.8zM11 7H2v7h9V7zM4 8H3v1h1V8zm0 2H3v1h1v-1z"/></svg>
    <a class="Header-link" href="/payfazz">payfazz</a>
    /
    <a class="Header-link" href="/payfazz/sellfazz-backend">sellfazz-backend</a>

</div>
    </div>


    <div class="Header-item mr-0 mr-lg-3 flex-order-1 flex-lg-order-none">
      

    <a aria-label="You have no unread notifications" class="Header-link notification-indicator position-relative tooltipped tooltipped-sw js-socket-channel js-notification-indicator" data-hotkey="g n" data-ga-click="Header, go to notifications, icon:read" data-channel="notification-changed:55684684" href="/notifications">
        <span class="mail-status "></span>
        <svg class="octicon octicon-bell" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 12v1H0v-1l.73-.58c.77-.77.81-2.55 1.19-4.42C2.69 3.23 6 2 6 2c0-.55.45-1 1-1s1 .45 1 1c0 0 3.39 1.23 4.16 5 .38 1.88.42 3.66 1.19 4.42l.66.58H14zm-7 4c1.11 0 2-.89 2-2H5c0 1.11.89 2 2 2z"/></svg>
</a>
    </div>


    <div class="Header-item position-relative d-none d-lg-flex">
      <details class="details-overlay details-reset">
  <summary class="Header-link"
      aria-label="Create new…"
      data-ga-click="Header, create new, icon:add">
    <svg class="octicon octicon-plus" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 9H7v5H5V9H0V7h5V2h2v5h5v2z"/></svg> <span class="dropdown-caret"></span>
  </summary>
  <details-menu class="dropdown-menu dropdown-menu-sw">
    
<a role="menuitem" class="dropdown-item" href="/new" data-ga-click="Header, create new repository">
  New repository
</a>

  <a role="menuitem" class="dropdown-item" href="/new/import" data-ga-click="Header, import a repository">
    Import repository
  </a>

<a role="menuitem" class="dropdown-item" href="https://gist.github.com/" data-ga-click="Header, create new gist">
  New gist
</a>

  <a role="menuitem" class="dropdown-item" href="/organizations/new" data-ga-click="Header, create new organization">
    New organization
  </a>


  <div role="none" class="dropdown-divider"></div>
  <div class="dropdown-header">
    <span title="payfazz/sellfazz-backend">This repository</span>
  </div>
    <a role="menuitem" class="dropdown-item" href="/payfazz/sellfazz-backend/issues/new" data-ga-click="Header, create new issue" data-skip-pjax>
      New issue
    </a>


  </details-menu>
</details>

    </div>

    <div class="Header-item position-relative mr-0 d-none d-lg-flex">
      
  <details class="details-overlay details-reset js-feature-preview-indicator-container" data-feature-preview-indicator-src="/users/estherialiana/feature_preview/indicator_check.json">

  <summary class="Header-link"
    aria-label="View profile and more"
    data-ga-click="Header, show menu, icon:avatar">
    <img alt="@estherialiana" class="avatar" src="https://avatars2.githubusercontent.com/u/55684684?s=40&amp;v=4" height="20" width="20">
      <span class="feature-preview-indicator js-feature-preview-indicator" hidden></span>
    <span class="dropdown-caret"></span>
  </summary>
  <details-menu class="dropdown-menu dropdown-menu-sw mt-2" style="width: 180px">
    <div class="header-nav-current-user css-truncate"><a role="menuitem" class="no-underline user-profile-link px-3 pt-2 pb-2 mb-n2 mt-n1 d-block" href="/estherialiana" data-ga-click="Header, go to profile, text:Signed in as">Signed in as <strong class="css-truncate-target">estherialiana</strong></a></div>
    <div role="none" class="dropdown-divider"></div>

      <div class="pl-3 pr-3 f6 user-status-container js-user-status-context pb-1" data-url="/users/status?compact=1&amp;link_mentions=0&amp;truncate=1">
        
<div class="js-user-status-container
    user-status-compact rounded-1 px-2 py-1 mt-2
    border
  " data-team-hovercards-enabled>
  <details class="js-user-status-details details-reset details-overlay details-overlay-dark">
    <summary class="btn-link btn-block link-gray no-underline js-toggle-user-status-edit toggle-user-status-edit "
      role="menuitem" data-hydro-click="{&quot;event_type&quot;:&quot;user_profile.click&quot;,&quot;payload&quot;:{&quot;profile_user_id&quot;:27276028,&quot;target&quot;:&quot;EDIT_USER_STATUS&quot;,&quot;user_id&quot;:55684684,&quot;client_id&quot;:&quot;2039514003.1569814249&quot;,&quot;originating_request_id&quot;:&quot;C5BC:4C67:164C23:1FD0D3:5DCCD619&quot;,&quot;originating_url&quot;:&quot;https://github.com/payfazz/sellfazz-backend/blob/master/docs/API.md&quot;,&quot;referrer&quot;:&quot;https://github.com/payfazz/sellfazz-backend/tree/master/docs&quot;}}" data-hydro-click-hmac="9838a0c771d30424c8e4fa9029656b12ece8882769925fe7761d22eb03025ddf">
      <div class="d-flex">
        <div class="f6 lh-condensed user-status-header
          d-inline-block v-align-middle
            user-status-emoji-only-header circle
            pr-2
"
            style="max-width: 29px"
          >
          <div class="user-status-emoji-container flex-shrink-0 mr-1 mt-1 lh-condensed-ultra v-align-bottom" style="">
            <svg class="octicon octicon-smiley" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8s3.58 8 8 8 8-3.58 8-8-3.58-8-8-8zm4.81 12.81a6.72 6.72 0 01-2.17 1.45c-.83.36-1.72.53-2.64.53-.92 0-1.81-.17-2.64-.53-.81-.34-1.55-.83-2.17-1.45a6.773 6.773 0 01-1.45-2.17A6.59 6.59 0 011.21 8c0-.92.17-1.81.53-2.64.34-.81.83-1.55 1.45-2.17.62-.62 1.36-1.11 2.17-1.45A6.59 6.59 0 018 1.21c.92 0 1.81.17 2.64.53.81.34 1.55.83 2.17 1.45.62.62 1.11 1.36 1.45 2.17.36.83.53 1.72.53 2.64 0 .92-.17 1.81-.53 2.64-.34.81-.83 1.55-1.45 2.17zM4 6.8v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2H5.2C4.53 8 4 7.47 4 6.8zm5 0v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2h-.59C9.53 8 9 7.47 9 6.8zm4 3.2c-.72 1.88-2.91 3-5 3s-4.28-1.13-5-3c-.14-.39.23-1 .66-1h8.59c.41 0 .89.61.75 1z"/></svg>
          </div>
        </div>
        <div class="
          d-inline-block v-align-middle
          
          
           css-truncate css-truncate-target 
           user-status-message-wrapper f6"
           style="line-height: 20px;" >
          <div class="d-inline-block text-gray-dark v-align-text-top text-left">
              <span class="text-gray ml-2">Set status</span>
          </div>
        </div>
      </div>
    </summary>
    <details-dialog class="details-dialog rounded-1 anim-fade-in fast Box Box--overlay" role="dialog" tabindex="-1">
      <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="position-relative flex-auto js-user-status-form" action="/users/status?compact=1&amp;link_mentions=0&amp;truncate=1" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="_method" value="put" /><input type="hidden" name="authenticity_token" value="y9wpkgZTv3Qu0xAwv3MHxf/49V3cksdKcmmFQ7/hFAnWSQWB+7RRBSPGLiAC2KJYCHYkoSmwWV55IuyyWxqw5A==" />
        <div class="Box-header bg-gray border-bottom p-3">
          <button class="Box-btn-octicon js-toggle-user-status-edit btn-octicon float-right" type="reset" aria-label="Close dialog" data-close-dialog>
            <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
          </button>
          <h3 class="Box-title f5 text-bold text-gray-dark">Edit status</h3>
        </div>
        <input type="hidden" name="emoji" class="js-user-status-emoji-field" value="">
        <input type="hidden" name="organization_id" class="js-user-status-org-id-field" value="">
        <div class="px-3 py-2 text-gray-dark">
          <div class="js-characters-remaining-container position-relative mt-2">
            <div class="input-group d-table form-group my-0 js-user-status-form-group">
              <span class="input-group-button d-table-cell v-align-middle" style="width: 1%">
                <button type="button" aria-label="Choose an emoji" class="btn-outline btn js-toggle-user-status-emoji-picker btn-open-emoji-picker p-0">
                  <span class="js-user-status-original-emoji" hidden></span>
                  <span class="js-user-status-custom-emoji"></span>
                  <span class="js-user-status-no-emoji-icon" >
                    <svg class="octicon octicon-smiley" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8s3.58 8 8 8 8-3.58 8-8-3.58-8-8-8zm4.81 12.81a6.72 6.72 0 01-2.17 1.45c-.83.36-1.72.53-2.64.53-.92 0-1.81-.17-2.64-.53-.81-.34-1.55-.83-2.17-1.45a6.773 6.773 0 01-1.45-2.17A6.59 6.59 0 011.21 8c0-.92.17-1.81.53-2.64.34-.81.83-1.55 1.45-2.17.62-.62 1.36-1.11 2.17-1.45A6.59 6.59 0 018 1.21c.92 0 1.81.17 2.64.53.81.34 1.55.83 2.17 1.45.62.62 1.11 1.36 1.45 2.17.36.83.53 1.72.53 2.64 0 .92-.17 1.81-.53 2.64-.34.81-.83 1.55-1.45 2.17zM4 6.8v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2H5.2C4.53 8 4 7.47 4 6.8zm5 0v-.59c0-.66.53-1.19 1.2-1.19h.59c.66 0 1.19.53 1.19 1.19v.59c0 .67-.53 1.2-1.19 1.2h-.59C9.53 8 9 7.47 9 6.8zm4 3.2c-.72 1.88-2.91 3-5 3s-4.28-1.13-5-3c-.14-.39.23-1 .66-1h8.59c.41 0 .89.61.75 1z"/></svg>
                  </span>
                </button>
              </span>
              <text-expander keys=": @" data-mention-url="/autocomplete/user-suggestions" data-emoji-url="/autocomplete/emoji">
                <input
                  type="text"
                  autocomplete="off"
                  data-no-org-url="/autocomplete/user-suggestions"
                  data-org-url="/suggestions?mention_suggester=1"
                  data-maxlength="80"
                  class="d-table-cell width-full form-control js-user-status-message-field js-characters-remaining-field"
                  placeholder="What's happening?"
                  name="message"
                  value=""
                  aria-label="What is your current status?">
              </text-expander>
              <div class="error">Could not update your status, please try again.</div>
            </div>
            <div style="margin-left: 53px" class="my-1 text-small label-characters-remaining js-characters-remaining" data-suffix="remaining" hidden>
              80 remaining
            </div>
          </div>
          <include-fragment class="js-user-status-emoji-picker" data-url="/users/status/emoji"></include-fragment>
          <div class="overflow-auto ml-n3 mr-n3 px-3 border-bottom" style="max-height: 33vh">
            <div class="user-status-suggestions js-user-status-suggestions collapsed overflow-hidden">
              <h4 class="f6 text-normal my-3">Suggestions:</h4>
              <div class="mx-3 mt-2 clearfix">
                  <div class="float-left col-6">
                      <button type="button" value=":palm_tree:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="palm_tree" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f334.png">🌴</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          On vacation
                        </div>
                      </button>
                      <button type="button" value=":face_with_thermometer:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="face_with_thermometer" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f912.png">🤒</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          Out sick
                        </div>
                      </button>
                  </div>
                  <div class="float-left col-6">
                      <button type="button" value=":house:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="house" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f3e0.png">🏠</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          Working from home
                        </div>
                      </button>
                      <button type="button" value=":dart:" class="d-flex flex-items-baseline flex-items-stretch lh-condensed f6 btn-link link-gray no-underline js-predefined-user-status mb-1">
                        <div class="emoji-status-width mr-2 v-align-middle js-predefined-user-status-emoji">
                          <g-emoji alias="dart" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f3af.png">🎯</g-emoji>
                        </div>
                        <div class="d-flex flex-items-center no-underline js-predefined-user-status-message ws-normal text-left" style="border-left: 1px solid transparent">
                          Focusing
                        </div>
                      </button>
                  </div>
              </div>
            </div>
            <div class="user-status-limited-availability-container">
              <div class="form-checkbox my-0">
                <input type="checkbox" name="limited_availability" value="1" class="js-user-status-limited-availability-checkbox" data-default-message="I may be slow to respond." aria-describedby="limited-availability-help-text-truncate-true-compact-true" id="limited-availability-truncate-true-compact-true">
                <label class="d-block f5 text-gray-dark mb-1" for="limited-availability-truncate-true-compact-true">
                  Busy
                </label>
                <p class="note" id="limited-availability-help-text-truncate-true-compact-true">
                  When others mention you, assign you, or request your review,
                  GitHub will let them know that you have limited availability.
                </p>
              </div>
            </div>
          </div>
            

<div class="d-inline-block f5 mr-2 pt-3 pb-2" >
  <div class="d-inline-block mr-1">
    Clear status
  </div>

  <details class="js-user-status-expire-drop-down f6 dropdown details-reset details-overlay d-inline-block mr-2">
    <summary class="f5 btn-link link-gray-dark border px-2 py-1 rounded-1" aria-haspopup="true">
      <div class="js-user-status-expiration-interval-selected d-inline-block v-align-baseline">
        Never
      </div>
      <div class="dropdown-caret"></div>
    </summary>

    <ul class="dropdown-menu dropdown-menu-se pl-0 overflow-auto" style="width: 220px; max-height: 15.5em">
      <li>
        <button type="button" class="btn-link dropdown-item js-user-status-expire-button ws-normal" title="Never">
          <span class="d-inline-block text-bold mb-1">Never</span>
          <div class="f6 lh-condensed">Keep this status until you clear your status or edit your status.</div>
        </button>
      </li>
      <li class="dropdown-divider" role="none"></li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="in 30 minutes" value="2019-11-14T11:50:42+07:00">
            in 30 minutes
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="in 1 hour" value="2019-11-14T12:20:42+07:00">
            in 1 hour
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="in 4 hours" value="2019-11-14T15:20:42+07:00">
            in 4 hours
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="today" value="2019-11-14T23:59:59+07:00">
            today
          </button>
        </li>
        <li>
          <button type="button" class="btn-link dropdown-item ws-normal js-user-status-expire-button" title="this week" value="2019-11-17T23:59:59+07:00">
            this week
          </button>
        </li>
    </ul>
  </details>
  <input class="js-user-status-expiration-date-input" type="hidden" name="expires_at" value="">
</div>

          <include-fragment class="js-user-status-org-picker" data-url="/users/status/organizations"></include-fragment>
        </div>
        <div class="d-flex flex-items-center flex-justify-between p-3 border-top">
          <button type="submit" disabled class="width-full btn btn-primary mr-2 js-user-status-submit">
            Set status
          </button>
          <button type="button" disabled class="width-full js-clear-user-status-button btn ml-2 ">
            Clear status
          </button>
        </div>
</form>    </details-dialog>
  </details>
</div>

      </div>
      <div role="none" class="dropdown-divider"></div>


    <a role="menuitem" class="dropdown-item" href="/estherialiana" data-ga-click="Header, go to profile, text:your profile">Your profile</a>

    <a role="menuitem" class="dropdown-item" href="/estherialiana?tab=repositories" data-ga-click="Header, go to repositories, text:your repositories">Your repositories</a>

    <a role="menuitem" class="dropdown-item" href="/estherialiana?tab=projects" data-ga-click="Header, go to projects, text:your projects">Your projects</a>

    <a role="menuitem" class="dropdown-item" href="/estherialiana?tab=stars" data-ga-click="Header, go to starred repos, text:your stars">Your stars</a>
      <a role="menuitem" class="dropdown-item" href="https://gist.github.com/mine" data-ga-click="Header, your gists, text:your gists">Your gists</a>





    <div role="none" class="dropdown-divider"></div>
      
<div id="feature-enrollment-toggle" class="hide-sm hide-md feature-preview-details position-relative">
  <button
    type="button"
    class="dropdown-item btn-link"
    role="menuitem"
    data-feature-preview-trigger-url="/users/estherialiana/feature_previews"
    data-feature-preview-close-details="{&quot;event_type&quot;:&quot;feature_preview.clicks.close_modal&quot;,&quot;payload&quot;:{&quot;client_id&quot;:&quot;2039514003.1569814249&quot;,&quot;originating_request_id&quot;:&quot;C5BC:4C67:164C23:1FD0D3:5DCCD619&quot;,&quot;originating_url&quot;:&quot;https://github.com/payfazz/sellfazz-backend/blob/master/docs/API.md&quot;,&quot;referrer&quot;:&quot;https://github.com/payfazz/sellfazz-backend/tree/master/docs&quot;,&quot;user_id&quot;:55684684}}"
    data-feature-preview-close-hmac="dca56f4d72fdec8e571c61d178b83cffb9f6cb40eb5951ffb073060f303c9e90"
    data-hydro-click="{&quot;event_type&quot;:&quot;feature_preview.clicks.open_modal&quot;,&quot;payload&quot;:{&quot;link_location&quot;:&quot;user_dropdown&quot;,&quot;client_id&quot;:&quot;2039514003.1569814249&quot;,&quot;originating_request_id&quot;:&quot;C5BC:4C67:164C23:1FD0D3:5DCCD619&quot;,&quot;originating_url&quot;:&quot;https://github.com/payfazz/sellfazz-backend/blob/master/docs/API.md&quot;,&quot;referrer&quot;:&quot;https://github.com/payfazz/sellfazz-backend/tree/master/docs&quot;,&quot;user_id&quot;:55684684}}"
    data-hydro-click-hmac="33af7a61792b06a7efc6ff126f80ef27d582e4b82af656ccd992c6796d3a971e"
  >
    Feature preview
  </button>
    <span class="feature-preview-indicator js-feature-preview-indicator" hidden></span>
</div>

    <a role="menuitem" class="dropdown-item" href="https://help.github.com" data-ga-click="Header, go to help, text:help">Help</a>
    <a role="menuitem" class="dropdown-item" href="/settings/profile" data-ga-click="Header, go to settings, icon:settings">Settings</a>
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="logout-form" action="/logout" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="qUCwbCoKeLF7s8/xl1xsFsmaXd7qGPHU6HqKhsqCrQKbvbDypxHNXlKdBwonboXHQyFTqIq/ZzXCVd2gPB1gtA==" />
      
      <button type="submit" class="dropdown-item dropdown-signout" data-ga-click="Header, sign out, icon:logout" role="menuitem">
        Sign out
      </button>
</form>  </details-menu>
</details>

    </div>

  </header>

      

  </div>

  <div id="start-of-content" class="show-on-focus"></div>


    <div id="js-flash-container">

</div>



  <div class="application-main " data-commit-hovercards-enabled>
        <div itemscope itemtype="http://schema.org/SoftwareSourceCode" class="">
    <main  >
      


  



  









  <div class="pagehead repohead instapaper_ignore readability-menu experiment-repo-nav pt-0 pt-lg-4 ">
    <div class="repohead-details-container clearfix container-lg p-responsive d-none d-lg-block">

      <ul class="pagehead-actions">




  <li>
    
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form data-remote="true" class="clearfix js-social-form js-social-container" action="/notifications/subscribe" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="LEjPY6xhUq/T2CuE5jjOjYhot+hB9IKhvZM6oyUMFBPfiTXvCy40BtNJU4eSUxKLgMEkbGCqgLyhOFLnwI9rcQ==" />      <input type="hidden" name="repository_id" value="205763991">

      <details class="details-reset details-overlay select-menu float-left">
        <summary class="select-menu-button float-left btn btn-sm btn-with-count" data-hydro-click="{&quot;event_type&quot;:&quot;repository.click&quot;,&quot;payload&quot;:{&quot;target&quot;:&quot;WATCH_BUTTON&quot;,&quot;repository_id&quot;:205763991,&quot;client_id&quot;:&quot;2039514003.1569814249&quot;,&quot;originating_request_id&quot;:&quot;C5BC:4C67:164C23:1FD0D3:5DCCD619&quot;,&quot;originating_url&quot;:&quot;https://github.com/payfazz/sellfazz-backend/blob/master/docs/API.md&quot;,&quot;referrer&quot;:&quot;https://github.com/payfazz/sellfazz-backend/tree/master/docs&quot;,&quot;user_id&quot;:55684684}}" data-hydro-click-hmac="6bb73442185c4a00b75127bda57f6497501bdea12994c889f5a40829510ecc86" data-ga-click="Repository, click Watch settings, action:blob#show">          <span data-menu-button>
              <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
              Watch
          </span>
</summary>        <details-menu
          class="select-menu-modal position-absolute mt-5"
          style="z-index: 99;">
          <div class="select-menu-header">
            <span class="select-menu-title">Notifications</span>
          </div>
          <div class="select-menu-list">
            <button type="submit" name="do" value="included" class="select-menu-item width-full" aria-checked="true" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Not watching</span>
                <span class="description">Be notified only when participating or @mentioned.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                  Watch
                </span>
              </div>
            </button>

            <button type="submit" name="do" value="release_only" class="select-menu-item width-full" aria-checked="false" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Releases only</span>
                <span class="description">Be notified of new releases, and when participating or @mentioned.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                  Unwatch releases
                </span>
              </div>
            </button>

            <button type="submit" name="do" value="subscribed" class="select-menu-item width-full" aria-checked="false" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Watching</span>
                <span class="description">Be notified of all conversations.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-eye v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.06 2C3 2 0 8 0 8s3 6 8.06 6C13 14 16 8 16 8s-3-6-7.94-6zM8 12c-2.2 0-4-1.78-4-4 0-2.2 1.8-4 4-4 2.22 0 4 1.8 4 4 0 2.22-1.78 4-4 4zm2-4c0 1.11-.89 2-2 2-1.11 0-2-.89-2-2 0-1.11.89-2 2-2 1.11 0 2 .89 2 2z"/></svg>
                  Unwatch
                </span>
              </div>
            </button>

            <button type="submit" name="do" value="ignore" class="select-menu-item width-full" aria-checked="false" role="menuitemradio">
              <svg class="octicon octicon-check select-menu-item-icon" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M12 5l-8 8-4-4 1.5-1.5L4 10l6.5-6.5L12 5z"/></svg>
              <div class="select-menu-item-text">
                <span class="select-menu-item-heading">Ignoring</span>
                <span class="description">Never be notified.</span>
                <span class="hidden-select-button-text" data-menu-button-contents>
                  <svg class="octicon octicon-mute v-align-text-bottom" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 2.81v10.38c0 .67-.81 1-1.28.53L3 10H1c-.55 0-1-.45-1-1V7c0-.55.45-1 1-1h2l3.72-3.72C7.19 1.81 8 2.14 8 2.81zm7.53 3.22l-1.06-1.06-1.97 1.97-1.97-1.97-1.06 1.06L11.44 8 9.47 9.97l1.06 1.06 1.97-1.97 1.97 1.97 1.06-1.06L13.56 8l1.97-1.97z"/></svg>
                  Stop ignoring
                </span>
              </div>
            </button>
          </div>
        </details-menu>
      </details>
        <a class="social-count js-social-count"
          href="/payfazz/sellfazz-backend/watchers"
          aria-label="2 users are watching this repository">
          2
        </a>
</form>
  </li>

  <li>
      <div class="js-toggler-container js-social-container starring-container ">
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="starred js-social-form" action="/payfazz/sellfazz-backend/unstar" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="tIKiS+2uE5D8Rq/cPXgEpi0zFebhdHp3xvqZ/NkxEKALCX+juaE2nYZ58Vw8hm56qdFT4hN/u0zmSpePYk5q8A==" />
      <input type="hidden" name="context" value="repository"></input>
      <button type="submit" class="btn btn-sm btn-with-count js-toggler-target" aria-label="Unstar this repository" title="Unstar payfazz/sellfazz-backend" data-hydro-click="{&quot;event_type&quot;:&quot;repository.click&quot;,&quot;payload&quot;:{&quot;target&quot;:&quot;UNSTAR_BUTTON&quot;,&quot;repository_id&quot;:205763991,&quot;client_id&quot;:&quot;2039514003.1569814249&quot;,&quot;originating_request_id&quot;:&quot;C5BC:4C67:164C23:1FD0D3:5DCCD619&quot;,&quot;originating_url&quot;:&quot;https://github.com/payfazz/sellfazz-backend/blob/master/docs/API.md&quot;,&quot;referrer&quot;:&quot;https://github.com/payfazz/sellfazz-backend/tree/master/docs&quot;,&quot;user_id&quot;:55684684}}" data-hydro-click-hmac="1cd22b070849f934418ab0aae019d72b989501d2b2f8975d2b7e6790b270b7b6" data-ga-click="Repository, click unstar button, action:blob#show; text:Unstar">        <svg class="octicon octicon-star v-align-text-bottom" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74L14 6z"/></svg>
        Unstar
</button>        <a class="social-count js-social-count" href="/payfazz/sellfazz-backend/stargazers"
           aria-label="0 users starred this repository">
           0
        </a>
</form>
    <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="unstarred js-social-form" action="/payfazz/sellfazz-backend/star" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="JC5K4J6YFDHqtrsKBH3HhLrsVTKyh9I1t2Fk8dflpfw5ChJjGn+KGbhEy+KlkGT6XAnls6g3fwQQ4WyCQ3bViw==" />
      <input type="hidden" name="context" value="repository"></input>
      <button type="submit" class="btn btn-sm btn-with-count js-toggler-target" aria-label="Unstar this repository" title="Star payfazz/sellfazz-backend" data-hydro-click="{&quot;event_type&quot;:&quot;repository.click&quot;,&quot;payload&quot;:{&quot;target&quot;:&quot;STAR_BUTTON&quot;,&quot;repository_id&quot;:205763991,&quot;client_id&quot;:&quot;2039514003.1569814249&quot;,&quot;originating_request_id&quot;:&quot;C5BC:4C67:164C23:1FD0D3:5DCCD619&quot;,&quot;originating_url&quot;:&quot;https://github.com/payfazz/sellfazz-backend/blob/master/docs/API.md&quot;,&quot;referrer&quot;:&quot;https://github.com/payfazz/sellfazz-backend/tree/master/docs&quot;,&quot;user_id&quot;:55684684}}" data-hydro-click-hmac="96c1a82132d75974c08639dab81599c4c5bbff15b339c9d2bb8a5983a3e35b4c" data-ga-click="Repository, click star button, action:blob#show; text:Star">        <svg class="octicon octicon-star v-align-text-bottom" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 6l-4.9-.64L7 1 4.9 5.36 0 6l3.6 3.26L2.67 14 7 11.67 11.33 14l-.93-4.74L14 6z"/></svg>
        Star
</button>        <a class="social-count js-social-count" href="/payfazz/sellfazz-backend/stargazers"
           aria-label="0 users starred this repository">
          0
        </a>
</form>  </div>

  </li>

  <li>
        <span class="btn btn-sm btn-with-count disabled tooltipped tooltipped-sw" aria-label="Cannot fork because forking is disabled.">
          <svg class="octicon octicon-repo-forked v-align-text-bottom" viewBox="0 0 10 16" version="1.1" width="10" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8 1a1.993 1.993 0 00-1 3.72V6L5 8 3 6V4.72A1.993 1.993 0 002 1a1.993 1.993 0 00-1 3.72V6.5l3 3v1.78A1.993 1.993 0 005 15a1.993 1.993 0 001-3.72V9.5l3-3V4.72A1.993 1.993 0 008 1zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3 10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zm3-10c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
          Fork
</span>
    <a href="/payfazz/sellfazz-backend/network/members" class="social-count"
       aria-label="0 users forked this repository">
      0
    </a>
  </li>
</ul>

      <h1 class="private ">
    <svg class="octicon octicon-lock" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 13H3v-1h1v1zm8-6v7c0 .55-.45 1-1 1H1c-.55 0-1-.45-1-1V7c0-.55.45-1 1-1h1V4c0-2.2 1.8-4 4-4s4 1.8 4 4v2h1c.55 0 1 .45 1 1zM3.8 6h4.41V4c0-1.22-.98-2.2-2.2-2.2-1.22 0-2.2.98-2.2 2.2v2H3.8zM11 7H2v7h9V7zM4 8H3v1h1V8zm0 2H3v1h1v-1z"/></svg>
  <span class="author" itemprop="author"><a class="url fn" rel="author" data-hovercard-type="organization" data-hovercard-url="/orgs/payfazz/hovercard" href="/payfazz">payfazz</a></span><!--
--><span class="path-divider">/</span><!--
--><strong itemprop="name"><a data-pjax="#js-repo-pjax-container" href="/payfazz/sellfazz-backend">sellfazz-backend</a></strong>
  <span class="Label Label--outline v-align-middle ">Private</span>

</h1>

    </div>
    
<nav class="hx_reponav reponav js-repo-nav js-sidenav-container-pjax container-lg p-responsive d-none d-lg-block"
     itemscope
     itemtype="http://schema.org/BreadcrumbList"
    aria-label="Repository"
     data-pjax="#js-repo-pjax-container">

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a class="js-selected-navigation-item selected reponav-item" itemprop="url" data-hotkey="g c" aria-current="page" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches repo_packages /payfazz/sellfazz-backend" href="/payfazz/sellfazz-backend">
      <svg class="octicon octicon-code" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M9.5 3L8 4.5 11.5 8 8 11.5 9.5 13 14 8 9.5 3zm-5 0L0 8l4.5 5L6 11.5 2.5 8 6 4.5 4.5 3z"/></svg>
      <span itemprop="name">Code</span>
      <meta itemprop="position" content="1">
</a>  </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a itemprop="url" data-hotkey="g i" class="js-selected-navigation-item reponav-item" data-selected-links="repo_issues repo_labels repo_milestones /payfazz/sellfazz-backend/issues" href="/payfazz/sellfazz-backend/issues">
        <svg class="octicon octicon-issue-opened" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7 2.3c3.14 0 5.7 2.56 5.7 5.7s-2.56 5.7-5.7 5.7A5.71 5.71 0 011.3 8c0-3.14 2.56-5.7 5.7-5.7zM7 1C3.14 1 0 4.14 0 8s3.14 7 7 7 7-3.14 7-7-3.14-7-7-7zm1 3H6v5h2V4zm0 6H6v2h2v-2z"/></svg>
        <span itemprop="name">Issues</span>
        <span class="Counter">0</span>
        <meta itemprop="position" content="2">
</a>    </span>

  <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
    <a data-hotkey="g p" itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_pulls checks /payfazz/sellfazz-backend/pulls" href="/payfazz/sellfazz-backend/pulls">
      <svg class="octicon octicon-git-pull-request" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M11 11.28V5c-.03-.78-.34-1.47-.94-2.06C9.46 2.35 8.78 2.03 8 2H7V0L4 3l3 3V4h1c.27.02.48.11.69.31.21.2.3.42.31.69v6.28A1.993 1.993 0 0010 15a1.993 1.993 0 001-3.72zm-1 2.92c-.66 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2zM4 3c0-1.11-.89-2-2-2a1.993 1.993 0 00-1 3.72v6.56A1.993 1.993 0 002 15a1.993 1.993 0 001-3.72V4.72c.59-.34 1-.98 1-1.72zm-.8 10c0 .66-.55 1.2-1.2 1.2-.65 0-1.2-.55-1.2-1.2 0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2zM2 4.2C1.34 4.2.8 3.65.8 3c0-.65.55-1.2 1.2-1.2.65 0 1.2.55 1.2 1.2 0 .65-.55 1.2-1.2 1.2z"/></svg>
      <span itemprop="name">Pull requests</span>
      <span class="Counter">3</span>
      <meta itemprop="position" content="3">
</a>  </span>


    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement" class="position-relative float-left">
      <a data-hotkey="g w" data-skip-pjax="true" class="js-selected-navigation-item reponav-item" data-selected-links="repo_actions /payfazz/sellfazz-backend/actions" href="/payfazz/sellfazz-backend/actions">
        <svg class="octicon octicon-play" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M14 8A7 7 0 110 8a7 7 0 0114 0zm-8.223 3.482l4.599-3.066a.5.5 0 000-.832L5.777 4.518A.5.5 0 005 4.934v6.132a.5.5 0 00.777.416z"/></svg>
        Actions
</a>
    </span>

    <a data-hotkey="g b" class="js-selected-navigation-item reponav-item" data-selected-links="repo_projects new_repo_project repo_project /payfazz/sellfazz-backend/projects" href="/payfazz/sellfazz-backend/projects">
      <svg class="octicon octicon-project" viewBox="0 0 15 16" version="1.1" width="15" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M10 12h3V2h-3v10zm-4-2h3V2H6v8zm-4 4h3V2H2v12zm-1 1h13V1H1v14zM14 0H1a1 1 0 00-1 1v14a1 1 0 001 1h13a1 1 0 001-1V1a1 1 0 00-1-1z"/></svg>
      Projects
      <span class="Counter" >0</span>
</a>

    <a class="js-selected-navigation-item reponav-item" data-hotkey="g w" data-selected-links="repo_wiki /payfazz/sellfazz-backend/wiki" href="/payfazz/sellfazz-backend/wiki">
      <svg class="octicon octicon-book" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M3 5h4v1H3V5zm0 3h4V7H3v1zm0 2h4V9H3v1zm11-5h-4v1h4V5zm0 2h-4v1h4V7zm0 2h-4v1h4V9zm2-6v9c0 .55-.45 1-1 1H9.5l-1 1-1-1H2c-.55 0-1-.45-1-1V3c0-.55.45-1 1-1h5.5l1 1 1-1H15c.55 0 1 .45 1 1zm-8 .5L7.5 3H2v9h6V3.5zm7-.5H9.5l-.5.5V12h6V3z"/></svg>
      Wiki
</a>
    <a data-skip-pjax="true" class="js-selected-navigation-item reponav-item" data-selected-links="security alerts policy code_scanning /payfazz/sellfazz-backend/security/advisories" href="/payfazz/sellfazz-backend/security/advisories">
      <svg class="octicon octicon-shield" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M0 2l7-2 7 2v6.02C14 12.69 8.69 16 7 16c-1.69 0-7-3.31-7-7.98V2zm1 .75L7 1l6 1.75v5.268C13 12.104 8.449 15 7 15c-1.449 0-6-2.896-6-6.982V2.75zm1 .75L7 2v12c-1.207 0-5-2.482-5-5.985V3.5z"/></svg>
      Security
</a>
    <a class="js-selected-navigation-item reponav-item" data-selected-links="repo_graphs repo_contributors dependency_graph pulse people /payfazz/sellfazz-backend/pulse" href="/payfazz/sellfazz-backend/pulse">
      <svg class="octicon octicon-graph" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M16 14v1H0V0h1v14h15zM5 13H3V8h2v5zm4 0H7V3h2v10zm4 0h-2V6h2v7z"/></svg>
      Insights
</a>

</nav>

  <div class="reponav-wrapper reponav-small d-lg-none">
  <nav class="reponav js-reponav text-center no-wrap"
       itemscope
       itemtype="http://schema.org/BreadcrumbList">

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a class="js-selected-navigation-item selected reponav-item" itemprop="url" aria-current="page" data-selected-links="repo_source repo_downloads repo_commits repo_releases repo_tags repo_branches repo_packages /payfazz/sellfazz-backend" href="/payfazz/sellfazz-backend">
        <span itemprop="name">Code</span>
        <meta itemprop="position" content="1">
</a>    </span>

      <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
        <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_issues repo_labels repo_milestones /payfazz/sellfazz-backend/issues" href="/payfazz/sellfazz-backend/issues">
          <span itemprop="name">Issues</span>
          <span class="Counter">0</span>
          <meta itemprop="position" content="2">
</a>      </span>

    <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
      <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_pulls checks /payfazz/sellfazz-backend/pulls" href="/payfazz/sellfazz-backend/pulls">
        <span itemprop="name">Pull requests</span>
        <span class="Counter">3</span>
        <meta itemprop="position" content="3">
</a>    </span>

      <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
        <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_projects new_repo_project repo_project /payfazz/sellfazz-backend/projects" href="/payfazz/sellfazz-backend/projects">
          <span itemprop="name">Projects</span>
          <span class="Counter">0</span>
          <meta itemprop="position" content="4">
</a>      </span>

      <span itemscope itemtype="http://schema.org/ListItem" itemprop="itemListElement">
        <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="repo_wiki /payfazz/sellfazz-backend/wiki" href="/payfazz/sellfazz-backend/wiki">
          <span itemprop="name">Wiki</span>
          <meta itemprop="position" content="5">
</a>      </span>

      <a itemprop="url" class="js-selected-navigation-item reponav-item" data-selected-links="security alerts policy code_scanning /payfazz/sellfazz-backend/security/advisories" href="/payfazz/sellfazz-backend/security/advisories">
        <span itemprop="name">Security</span>
        <meta itemprop="position" content="6">
</a>
      <a class="js-selected-navigation-item reponav-item" data-selected-links="pulse /payfazz/sellfazz-backend/pulse" href="/payfazz/sellfazz-backend/pulse">
        Pulse
</a>

  </nav>
</div>


  </div>
<div class="container-lg clearfix new-discussion-timeline experiment-repo-nav  p-responsive">
  <div class="repository-content ">

    
    


  


    <a class="d-none js-permalink-shortcut" data-hotkey="y" href="/payfazz/sellfazz-backend/blob/c25aaeeac970ed03439b74e876fec110c2ffc857/docs/API.md">Permalink</a>

    <!-- blob contrib key: blob_contributors:v21:2c865013564ea0a963e5b669a0592e85 -->
      

    <div class="d-flex flex-items-start flex-shrink-0 pb-3 flex-column flex-md-row">
      <span class="d-flex flex-justify-between width-full width-md-auto">
        
<details class="details-reset details-overlay select-menu branch-select-menu  hx_rsm" id="branch-select-menu">
  <summary class="btn btn-sm select-menu-button css-truncate"
           data-hotkey="w"
           title="Switch branches or tags">
    <i>Branch:</i>
    <span class="css-truncate-target" data-menu-button>master</span>
  </summary>

  <details-menu class="select-menu-modal hx_rsm-modal position-absolute" style="z-index: 99;" src="/payfazz/sellfazz-backend/ref-list/master/docs/API.md?source_action=show&amp;source_controller=blob" preload>
    <include-fragment class="select-menu-loading-overlay anim-pulse">
      <svg height="32" class="octicon octicon-octoface" viewBox="0 0 16 16" version="1.1" width="32" aria-hidden="true"><path fill-rule="evenodd" d="M14.7 5.34c.13-.32.55-1.59-.13-3.31 0 0-1.05-.33-3.44 1.3-1-.28-2.07-.32-3.13-.32s-2.13.04-3.13.32c-2.39-1.64-3.44-1.3-3.44-1.3-.68 1.72-.26 2.99-.13 3.31C.49 6.21 0 7.33 0 8.69 0 13.84 3.33 15 7.98 15S16 13.84 16 8.69c0-1.36-.49-2.48-1.3-3.35zM8 14.02c-3.3 0-5.98-.15-5.98-3.35 0-.76.38-1.48 1.02-2.07 1.07-.98 2.9-.46 4.96-.46 2.07 0 3.88-.52 4.96.46.65.59 1.02 1.3 1.02 2.07 0 3.19-2.68 3.35-5.98 3.35zM5.49 9.01c-.66 0-1.2.8-1.2 1.78s.54 1.79 1.2 1.79c.66 0 1.2-.8 1.2-1.79s-.54-1.78-1.2-1.78zm5.02 0c-.66 0-1.2.79-1.2 1.78s.54 1.79 1.2 1.79c.66 0 1.2-.8 1.2-1.79s-.53-1.78-1.2-1.78z"/></svg>
    </include-fragment>
  </details-menu>
</details>

        <div class="BtnGroup flex-shrink-0 d-md-none">
          <a href="/payfazz/sellfazz-backend/find/master"
                class="js-pjax-capture-input btn btn-sm BtnGroup-item"
                data-pjax
                data-hotkey="t">
            Find file
          </a>
          <clipboard-copy value="docs/API.md" class="btn btn-sm BtnGroup-item">
            Copy path
          </clipboard-copy>
        </div>
      </span>
      <h2 id="blob-path" class="breadcrumb flex-auto min-width-0 text-normal flex-md-self-center ml-md-2 mr-md-3 my-2 my-md-0">
        <span class="js-repo-root text-bold"><span class="js-path-segment"><a data-pjax="true" href="/payfazz/sellfazz-backend"><span>sellfazz-backend</span></a></span></span><span class="separator">/</span><span class="js-path-segment"><a data-pjax="true" href="/payfazz/sellfazz-backend/tree/master/docs"><span>docs</span></a></span><span class="separator">/</span><strong class="final-path">API.md</strong>
      </h2>

      <div class="BtnGroup flex-shrink-0 d-none d-md-inline-block">
        <a href="/payfazz/sellfazz-backend/find/master"
              class="js-pjax-capture-input btn btn-sm BtnGroup-item"
              data-pjax
              data-hotkey="t">
          Find file
        </a>
        <clipboard-copy value="docs/API.md" class="btn btn-sm BtnGroup-item">
          Copy path
        </clipboard-copy>
      </div>
    </div>



    
  <div class="Box Box--condensed d-flex flex-column flex-shrink-0">
      <div class="Box-body d-flex flex-justify-between bg-blue-light flex-column flex-md-row flex-items-start flex-md-items-center">
        <span class="pr-md-4 f6">
          <a rel="contributor" data-skip-pjax="true" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=26264682" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/faruqfadhil"><img class="avatar" src="https://avatars3.githubusercontent.com/u/26264682?s=40&amp;v=4" width="20" height="20" alt="@faruqfadhil" /></a>
          <a class="text-bold link-gray-dark lh-default v-align-middle" rel="contributor" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=26264682" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/faruqfadhil">faruqfadhil</a>
            <span class="lh-default v-align-middle">
              <a data-pjax="true" title="change view option with flag" class="link-gray" href="/payfazz/sellfazz-backend/commit/74c4cf9066c3f6fd8a536c9c7990e8cd2bf6b58c">change view option with flag</a>
            </span>
        </span>
        <span class="d-inline-block flex-shrink-0 v-align-bottom f6 mt-2 mt-md-0">
          <a class="pr-2 text-mono link-gray" href="/payfazz/sellfazz-backend/commit/74c4cf9066c3f6fd8a536c9c7990e8cd2bf6b58c" data-pjax>74c4cf9</a>
          <relative-time datetime="2019-11-13T10:55:56Z" class="no-wrap">Nov 13, 2019</relative-time>
        </span>
      </div>

    <div class="Box-body d-flex flex-items-center flex-auto f6 border-bottom-0 flex-wrap" >
      <details class="details-reset details-overlay details-overlay-dark lh-default text-gray-dark float-left mr-2" id="blob_contributors_box">
        <summary class="btn-link">
          <span><strong>4</strong> contributors</span>
        </summary>
        <details-dialog
          class="Box Box--overlay d-flex flex-column anim-fade-in fast"
          aria-label="Users who have contributed to this file"
          src="/payfazz/sellfazz-backend/contributors/master/docs/API.md/list" preload>
          <div class="Box-header">
            <button class="Box-btn-octicon btn-octicon float-right" type="button" aria-label="Close dialog" data-close-dialog>
              <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
            </button>
            <h3 class="Box-title">
              Users who have contributed to this file
            </h3>
          </div>
          <include-fragment class="octocat-spinner my-3" aria-label="Loading..."></include-fragment>
        </details-dialog>
      </details>
        <span class="">
    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=1487914" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/payfazz/sellfazz-backend/commits/master/docs/API.md?author=rickywinata">
      <img class="avatar mr-1" src="https://avatars3.githubusercontent.com/u/1487914?s=40&amp;v=4" width="20" height="20" alt="@rickywinata" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=14516660" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/payfazz/sellfazz-backend/commits/master/docs/API.md?author=chandraekap">
      <img class="avatar mr-1" src="https://avatars2.githubusercontent.com/u/14516660?s=40&amp;v=4" width="20" height="20" alt="@chandraekap" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=52452231" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/payfazz/sellfazz-backend/commits/master/docs/API.md?author=ottodanl">
      <img class="avatar mr-1" src="https://avatars3.githubusercontent.com/u/52452231?s=40&amp;v=4" width="20" height="20" alt="@ottodanl" /> 
</a>    <a class="avatar-link" data-hovercard-type="user" data-hovercard-url="/hovercards?user_id=26264682" data-octo-click="hovercard-link-click" data-octo-dimensions="link_type:self" href="/payfazz/sellfazz-backend/commits/master/docs/API.md?author=faruqfadhil">
      <img class="avatar mr-1" src="https://avatars3.githubusercontent.com/u/26264682?s=40&amp;v=4" width="20" height="20" alt="@faruqfadhil" /> 
</a>
</span>

    </div>
  </div>





    <div class="Box mt-3 position-relative">
      
<div class="Box-header py-2 d-flex flex-column flex-shrink-0 flex-md-row flex-md-items-center">
  <div class="text-mono f6 flex-auto pr-3 flex-order-2 flex-md-order-1 mt-2 mt-md-0">

      4967 lines (4237 sloc)
      <span class="file-info-divider"></span>
    123 KB
  </div>

  <div class="d-flex py-1 py-md-0 flex-auto flex-order-1 flex-md-order-2 flex-sm-grow-0 flex-justify-between">

    <div class="BtnGroup">
      <a id="raw-url" class="btn btn-sm BtnGroup-item" href="/payfazz/sellfazz-backend/raw/master/docs/API.md">Raw</a>
        <a class="btn btn-sm js-update-url-with-hash BtnGroup-item" data-hotkey="b" href="/payfazz/sellfazz-backend/blame/master/docs/API.md">Blame</a>
      <a rel="nofollow" class="btn btn-sm BtnGroup-item" href="/payfazz/sellfazz-backend/commits/master/docs/API.md">History</a>
    </div>


    <div>

            <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="inline-form js-update-url-with-hash" action="/payfazz/sellfazz-backend/edit/master/docs/API.md" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="wYQBreVWYh8QWCuaUR9tWUD+IL1otrMOg2glzbQ1f3XFu1RYNElWVlkUGU/l1sMA2BPze6RQ/XqlpkuCWz7x+w==" />
              <button class="btn-octicon tooltipped tooltipped-nw" type="submit"
                aria-label="Edit this file" data-hotkey="e" data-disable-with>
                <svg class="octicon octicon-pencil" viewBox="0 0 14 16" version="1.1" width="14" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M0 12v3h3l8-8-3-3-8 8zm3 2H1v-2h1v1h1v1zm10.3-9.3L12 6 9 3l1.3-1.3a.996.996 0 011.41 0l1.59 1.59c.39.39.39 1.02 0 1.41z"/></svg>
              </button>
</form>
          <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="inline-form" action="/payfazz/sellfazz-backend/delete/master/docs/API.md" accept-charset="UTF-8" method="post"><input name="utf8" type="hidden" value="&#x2713;" /><input type="hidden" name="authenticity_token" value="pQnqFVyfrr+hsPhfgVKeMbI4wCxyc31cyjpu+r9IaoqC+6cM473hDZbK0e59NsCx3RjsLspFRc/eDlR0eSU23Q==" />
            <button class="btn-octicon btn-octicon-danger tooltipped tooltipped-nw" type="submit"
              aria-label="Delete this file" data-disable-with>
              <svg class="octicon octicon-trashcan" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M11 2H9c0-.55-.45-1-1-1H5c-.55 0-1 .45-1 1H2c-.55 0-1 .45-1 1v1c0 .55.45 1 1 1v9c0 .55.45 1 1 1h7c.55 0 1-.45 1-1V5c.55 0 1-.45 1-1V3c0-.55-.45-1-1-1zm-1 12H3V5h1v8h1V5h1v8h1V5h1v8h1V5h1v9zm1-10H2V3h9v1z"/></svg>
            </button>
</form>    </div>
  </div>
</div>




      
  <div id="readme" class="Box-body readme blob instapaper_body js-code-block-container">
    <article class="markdown-body entry-content p-3 p-md-6" itemprop="text"><table data-table-type="yaml-metadata">
  <thead>
  <tr>
  <th>title</th>
  <th>language_tabs</th>
  </tr>
  </thead>
  <tbody>
  <tr>
  <td><div>API Reference</div></td>
  <td><div><table>
  <tbody>
  <tr>
  <td><div>shell</div></td>
  </tr>
  </tbody>
</table>
</div></td>
  </tr>
  </tbody>
</table>

<h1><a id="user-content-introduction" class="anchor" aria-hidden="true" href="#introduction"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Introduction</h1>
<p>Welcome!</p>
<blockquote>
<p>API Endpoint:</p>
</blockquote>
<pre><code>https://staging.sellfazz.com/api/v2/
</code></pre>
<h1><a id="user-content-table-of-contents" class="anchor" aria-hidden="true" href="#table-of-contents"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Table of Contents</h1>
<ul>
<li><a href="#introduction">Introduction</a></li>
<li><a href="#user">User</a>
<ul>
<li><a href="#register">Register</a></li>
<li><a href="#login">Login</a></li>
<li><a href="#reset-password">Reset Password</a></li>
<li><a href="#users">Users</a></li>
<li><a href="#business-categories">Business Categories</a></li>
</ul>
</li>
<li><a href="#subscription">Subscription</a>
<ul>
<li><a href="#subscription-packages">Subscription Packages</a></li>
<li><a href="#subscription-payment-methods">Subscription Payment Methods</a></li>
<li><a href="#subscriptions">Subscriptions</a></li>
<li><a href="#subscription-vouchers">Subscription Vouchers</a></li>
</ul>
</li>
<li><a href="#location">Location</a>
<ul>
<li><a href="#areas">Areas</a></li>
</ul>
</li>
<li><a href="#outlet">Outlet</a>
<ul>
<li><a href="#devices">Devices</a></li>
<li><a href="#employees">Employees</a></li>
<li><a href="#shifts">Shifts</a></li>
<li><a href="#outlets">Outlets</a></li>
<li><a href="#settings">Settings</a></li>
</ul>
</li>
<li><a href="#catalog">Catalog</a>
<ul>
<li><a href="#products">Products</a></li>
<li><a href="#categories">Categories</a></li>
<li><a href="#service-types">Service Types</a></li>
</ul>
</li>
<li><a href="#order">Order</a>
<ul>
<li><a href="#orders">Orders</a></li>
<li><a href="#customers">Customers</a></li>
<li><a href="#discounts">Discounts</a></li>
<li><a href="#payment-methods">Payment Methods</a></li>
<li><a href="#charges">Charges</a></li>
</ul>
</li>
<li><a href="#reset">Reset</a>
<ul>
<li><a href="#managements">Managements</a></li>
<li><a href="#transactions">Transactions</a></li>
</ul>
</li>
<li><a href="#file">File</a></li>
</ul>
<h1><a id="user-content-user" class="anchor" aria-hidden="true" href="#user"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>User</h1>
<h1><a id="user-content-register" class="anchor" aria-hidden="true" href="#register"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Register</h1>
<h2><a id="user-content-create-a-register-token" class="anchor" aria-hidden="true" href="#create-a-register-token"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a register token</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/register-tokens \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "business_name": "Sellfazz Shop",</span>
<span class="pl-s">    "phone": "08123456789",</span>
<span class="pl-s">    "password": "Default123"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>353324b7-0004-4d9d-83ef-a0aae4991a99<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>business_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Sellfazz Shop<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>08123456789<span class="pl-pds">"</span></span>
}</pre></div>
<p>Initiate a new user registration.</p>
<h3><a id="user-content-http-request" class="anchor" aria-hidden="true" href="#http-request"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/register-tokens</code></p>
<h2><a id="user-content-resend-otp" class="anchor" aria-hidden="true" href="#resend-otp"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Resend OTP</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/register-tokens/resend-otp \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "register_token_id": "353324b7-0004-4d9d-83ef-a0aae4991a99"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Resend registration activation link.</p>
<h3><a id="user-content-http-request-1" class="anchor" aria-hidden="true" href="#http-request-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/register-tokens/resend-otp</code></p>
<h2><a id="user-content-register-1" class="anchor" aria-hidden="true" href="#register-1"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Register</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/register \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "register_token_id": "f9122cf4-88e1-4134-a093-b255d59af144",</span>
<span class="pl-s">    "otp": "123456"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>access_token<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kvDOhze6yvXERD2dZuTJdXKYBPS9q6GHJ6JHdlCm5dh063ocxsV2rknE3AGAW3Ds<span class="pl-pds">"</span></span>,    
  <span class="pl-s"><span class="pl-pds">"</span>access_type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>storeOwner<span class="pl-pds">"</span></span>    
}</pre></div>
<p>Register an user.</p>
<h3><a id="user-content-http-request-2" class="anchor" aria-hidden="true" href="#http-request-2"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/register</code></p>
<h1><a id="user-content-login" class="anchor" aria-hidden="true" href="#login"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Login</h1>
<h2><a id="user-content-create-an-access-token" class="anchor" aria-hidden="true" href="#create-an-access-token"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create an access token</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/login \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "username": "08123456777",</span>
<span class="pl-s">    "password": "Default123"    </span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>access_token<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kvDOhze6yvXERD2dZuTJdXKYBPS9q6GHJ6JHdlCm5dh063ocxsV2rknE3AGAW3Ds<span class="pl-pds">"</span></span>,    
  <span class="pl-s"><span class="pl-pds">"</span>access_type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>storeOwner<span class="pl-pds">"</span></span>    
}</pre></div>
<p>Create the token for accessing other resources.</p>
<h3><a id="user-content-http-request-3" class="anchor" aria-hidden="true" href="#http-request-3"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/login</code></p>
<h2><a id="user-content-logout" class="anchor" aria-hidden="true" href="#logout"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Logout</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/logout \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>  </pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Release the access token (Logout).</p>
<h3><a id="user-content-http-request-4" class="anchor" aria-hidden="true" href="#http-request-4"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/logout</code></p>
<h1><a id="user-content-reset-password" class="anchor" aria-hidden="true" href="#reset-password"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Reset Password</h1>
<h2><a id="user-content-create-a-reset-password-token" class="anchor" aria-hidden="true" href="#create-a-reset-password-token"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a reset password token</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/reset-password-tokens \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "username": "08123456777"    </span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2f832757-f7e1-43be-a865-8a7ba7b59f14<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>expired_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-03T11:46:54.187057Z<span class="pl-pds">"</span></span>
}</pre></div>
<p>Create the reset password resource.</p>
<h3><a id="user-content-http-request-5" class="anchor" aria-hidden="true" href="#http-request-5"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/reset-password-tokens</code></p>
<h2><a id="user-content-check-a-reset-password-token-otp" class="anchor" aria-hidden="true" href="#check-a-reset-password-token-otp"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Check a reset password token OTP</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/reset-password-tokens/{reset_password_token_id}/check-otp \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "otp": "123456"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Check a check reset password token OTP.</p>
<h3><a id="user-content-http-request-6" class="anchor" aria-hidden="true" href="#http-request-6"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/reset-password-tokens/{reset_password_token_id}/check-otp</code></p>
<h2><a id="user-content-reset-the-password" class="anchor" aria-hidden="true" href="#reset-the-password"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Reset the password</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/reset-password \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "reset_password_token_id": "2f832757-f7e1-43be-a865-8a7ba7b59f14",</span>
<span class="pl-s">    "otp": "123456",</span>
<span class="pl-s">    "new_password": "Newpassword123"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Reset the password.</p>
<h3><a id="user-content-http-request-7" class="anchor" aria-hidden="true" href="#http-request-7"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/reset-password</code></p>
<h1><a id="user-content-users" class="anchor" aria-hidden="true" href="#users"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Users</h1>
<h2><a id="user-content-get-an-user" class="anchor" aria-hidden="true" href="#get-an-user"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get an user</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/users/me</pre></div>
<p>Get current user information.</p>
<h3><a id="user-content-http-request-8" class="anchor" aria-hidden="true" href="#http-request-8"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/users/me</code></p>
<h2><a id="user-content-update-an-user" class="anchor" aria-hidden="true" href="#update-an-user"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update an user</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/users/me \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "owner_name": "BOB",</span>
<span class="pl-s">    "business_name": "Alice Shop",</span>
<span class="pl-s">    "picture_url": "http://www.example.com",</span>
<span class="pl-s">    "employee_size": "1-5 Orang karyawan",</span>
<span class="pl-s">    "outlet_size": "2-10 Outlet",</span>
<span class="pl-s">    "website": "http://www.tokomajujaya.com",</span>
<span class="pl-s">    "business_icon": "https://img.icons8.com/dusk/128/000000/money.png",</span>
<span class="pl-s">    "business_category": "Restoran",</span>
<span class="pl-s">    "business_phone": "08123456777",</span>
<span class="pl-s">    "postal_code": "123456",</span>
<span class="pl-s">    "address": "Jalan Bandung No 5 Blok B1",</span>
<span class="pl-s">    "area_id": "1",</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<p>Update current user information. You can provide partial information (<code>owner_name</code> only or <code>business_name</code> only, etc.).</p>
<h3><a id="user-content-http-request-9" class="anchor" aria-hidden="true" href="#http-request-9"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/users/me</code></p>
<h2><a id="user-content-create-a-change-password-token" class="anchor" aria-hidden="true" href="#create-a-change-password-token"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a change password token</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/users/me/change-password-tokens \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> <span class="pl-cce">\ </span> 
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>  </pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Create a change password token.</p>
<h3><a id="user-content-http-request-10" class="anchor" aria-hidden="true" href="#http-request-10"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/users/me/change-password-tokens</code></p>
<h2><a id="user-content-check-a-change-password-token-otp" class="anchor" aria-hidden="true" href="#check-a-change-password-token-otp"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Check a change password token OTP</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/users/me/change-password-tokens/{change_password_token_id}/check-otp \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "otp": "123456"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Check a change password token OTP.</p>
<h3><a id="user-content-http-request-11" class="anchor" aria-hidden="true" href="#http-request-11"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/users/me/change-password-tokens/{change_password_token_id}/check-otp</code></p>
<h2><a id="user-content-change-password" class="anchor" aria-hidden="true" href="#change-password"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Change password</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/users/me/change-password \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> <span class="pl-cce">\ </span> 
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "change_password_token_id": "dda88a68-7071-4e9c-9976-f8e30324d323",</span>
<span class="pl-s">    "otp": "758180",</span>
<span class="pl-s">    "password": "Bob12345"    </span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Change current user password.</p>
<h3><a id="user-content-http-request-12" class="anchor" aria-hidden="true" href="#http-request-12"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/users/me/change-password</code></p>
<h2><a id="user-content-create-a-change-phone-token" class="anchor" aria-hidden="true" href="#create-a-change-phone-token"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a change phone token</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/users/me/change-phone-tokens \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> <span class="pl-cce">\ </span> 
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "phone": "08123456777"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Create a change phone token.</p>
<h3><a id="user-content-http-request-13" class="anchor" aria-hidden="true" href="#http-request-13"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/users/me/change-phone-tokens</code></p>
<h2><a id="user-content-change-phone" class="anchor" aria-hidden="true" href="#change-phone"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Change phone</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/users/me/change-phone \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> <span class="pl-cce">\ </span> 
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "change_phone_token_id": "Bob12345",</span>
<span class="pl-s">    "otp": "123456"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Change current user phone number.</p>
<h3><a id="user-content-http-request-14" class="anchor" aria-hidden="true" href="#http-request-14"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/users/me/change-phone</code></p>
<h2><a id="user-content-create-a-change-email-token" class="anchor" aria-hidden="true" href="#create-a-change-email-token"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a change email token</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/users/me/change-email-tokens \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> <span class="pl-cce">\ </span> 
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "email": "alice_new@example.com"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Create a change email token.</p>
<h3><a id="user-content-http-request-15" class="anchor" aria-hidden="true" href="#http-request-15"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/users/me/change-email-tokens</code></p>
<h2><a id="user-content-check-users-password" class="anchor" aria-hidden="true" href="#check-users-password"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Check user's password</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/users/me/check-password \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> <span class="pl-cce">\ </span> 
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "password": "Default123"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Check user's password.</p>
<h3><a id="user-content-http-request-16" class="anchor" aria-hidden="true" href="#http-request-16"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/users/me/check-password</code></p>
<h2><a id="user-content-change-email" class="anchor" aria-hidden="true" href="#change-email"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Change email</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/users/me/change-email \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> <span class="pl-cce">\ </span> 
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "change_email_token_id": "Bob12345",</span>
<span class="pl-s">    "otp": "123456"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Change current user email.</p>
<h3><a id="user-content-http-request-17" class="anchor" aria-hidden="true" href="#http-request-17"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/users/me/change-email</code></p>
<h2><a id="user-content-update-a-shop" class="anchor" aria-hidden="true" href="#update-a-shop"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update a shop</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/shops/{shop_id} \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{	</span>
<span class="pl-s">    "name": "alice shop x",</span>
<span class="pl-s">    "picture_url": "abcde12345",    </span>
<span class="pl-s">    "shop_category": "grosir",</span>
<span class="pl-s">    "phone": "087878789999"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Update a shop.</p>
<h3><a id="user-content-http-request-18" class="anchor" aria-hidden="true" href="#http-request-18"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/shops/{shop_id}</code></p>
<h1><a id="user-content-business-categories" class="anchor" aria-hidden="true" href="#business-categories"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Business Categories</h1>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/business-categories  </pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    <span class="pl-s"><span class="pl-pds">"</span>Restoran<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Kafe/Toko Kopi<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Warung Makan<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Toko Roti<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Toko Kelontong<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Minimarket<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Agen Pulsa<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Apotik<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Toko Pakaian<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Toko Elektronik<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Toko Kosmetik<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Toko Bangunan<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Toko ATK<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Spa <span class="pl-cce">\u0026</span> Salon<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Barbershop<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Laundri<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>Bengkel<span class="pl-pds">"</span></span>
  ]
}</pre></div>
<p>List all business categories.</p>
<h3><a id="user-content-http-request-19" class="anchor" aria-hidden="true" href="#http-request-19"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/business-categories</code></p>
<h1><a id="user-content-subscription" class="anchor" aria-hidden="true" href="#subscription"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Subscription</h1>
<h1><a id="user-content-subscription-packages" class="anchor" aria-hidden="true" href="#subscription-packages"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Subscription Packages</h1>
<h2><a id="user-content-subscription-packages-list" class="anchor" aria-hidden="true" href="#subscription-packages-list"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Subscription Packages List</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/subscription-packages \
  -X GET \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Lite<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>features<span class="pl-pds">"</span></span>: [
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Fitur Kasir Offline untuk owner<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Jumlah kategori tak terbatas<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Jumlah produk tak terbatas<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Fitur Diskon<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Fitur Pelanggan<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Laporan keuangan dan penjualan<span class="pl-pds">"</span></span>
          }
      ],
      <span class="pl-s"><span class="pl-pds">"</span>packages<span class="pl-pds">"</span></span>: []
    },
    {
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Premium<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>features<span class="pl-pds">"</span></span>: [
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Semua Fitur SELLFAZZ Lite<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Akun karyawan tak terbatas<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Download laporan usaha<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Pengaturan multioutlet tak terbatas<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Pengaturan Struk<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>subscription_package_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Pengaturan Pajak &amp; Service Charge<span class="pl-pds">"</span></span>
          }
      ],
      <span class="pl-s"><span class="pl-pds">"</span>packages<span class="pl-pds">"</span></span>: [
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>package_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Premium<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
              <span class="pl-s"><span class="pl-pds">"</span>duration<span class="pl-pds">"</span></span>: <span class="pl-c1">30</span>,
              <span class="pl-s"><span class="pl-pds">"</span>duration_unit<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>day<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
              <span class="pl-s"><span class="pl-pds">"</span>discount_percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
              <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
              <span class="pl-s"><span class="pl-pds">"</span>voucher<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>package_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>old Premium<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100000</span>,
              <span class="pl-s"><span class="pl-pds">"</span>duration<span class="pl-pds">"</span></span>: <span class="pl-c1">1</span>,
              <span class="pl-s"><span class="pl-pds">"</span>duration_unit<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>month<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
              <span class="pl-s"><span class="pl-pds">"</span>discount_percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
              <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
              <span class="pl-s"><span class="pl-pds">"</span>voucher<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>3<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Premium 3 Bulan<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">300000</span>,
              <span class="pl-s"><span class="pl-pds">"</span>duration<span class="pl-pds">"</span></span>: <span class="pl-c1">3</span>,
              <span class="pl-s"><span class="pl-pds">"</span>duration_unit<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>month<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
              <span class="pl-s"><span class="pl-pds">"</span>discount_percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
              <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">100000</span>,
              <span class="pl-s"><span class="pl-pds">"</span>voucher<span class="pl-pds">"</span></span>: {
                  <span class="pl-s"><span class="pl-pds">"</span>code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>SFNEW100<span class="pl-pds">"</span></span>,
                  <span class="pl-s"><span class="pl-pds">"</span>start_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
                  <span class="pl-s"><span class="pl-pds">"</span>end_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-10-14T19:49:04.386957416+07:00<span class="pl-pds">"</span></span>,
                  <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                  <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">100000</span>,
                  <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
                  <span class="pl-s"><span class="pl-pds">"</span>is_auto_applied<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
              }
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>4<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Premium 6 Bulan<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">600000</span>,
              <span class="pl-s"><span class="pl-pds">"</span>duration<span class="pl-pds">"</span></span>: <span class="pl-c1">6</span>,
              <span class="pl-s"><span class="pl-pds">"</span>duration_unit<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>month<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
              <span class="pl-s"><span class="pl-pds">"</span>discount_percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
              <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">100000</span>,
              <span class="pl-s"><span class="pl-pds">"</span>voucher<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>5<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Premium 12 Bulan<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">1200000</span>,
              <span class="pl-s"><span class="pl-pds">"</span>duration<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>,
              <span class="pl-s"><span class="pl-pds">"</span>duration_unit<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>month<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
              <span class="pl-s"><span class="pl-pds">"</span>discount_percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
              <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">200000</span>,
              <span class="pl-s"><span class="pl-pds">"</span>voucher<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
          }
      ]
    }
  ]
}</pre></div>
<p>Get list of subscription packages.</p>
<h3><a id="user-content-http-request-20" class="anchor" aria-hidden="true" href="#http-request-20"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/subscription-packages</code></p>
<h1><a id="user-content-subscription-payment-methods" class="anchor" aria-hidden="true" href="#subscription-payment-methods"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Subscription Payment Methods</h1>
<h2><a id="user-content-subscription-methods-list" class="anchor" aria-hidden="true" href="#subscription-methods-list"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Subscription Methods List</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/subscription-payment-methods \
  -X GET \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>va<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Virtual Account<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Konfirmasi otomatis 24 jam<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>payment_channels<span class="pl-pds">"</span></span>: [
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>bca<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BCA<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>mandiri<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Mandiri<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>bni<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BNI<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>maybank<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Maybank<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>permata<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Bank Permata<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>hana<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Hana Bank<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>bri<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BRI<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>cimb<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>CIMB Niaga<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>danamon<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Bank Danamon<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          }
      ]
    },
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>cvs<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Gerai Minimarket<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Pembayaran 1x24 jam<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>payment_channels<span class="pl-pds">"</span></span>: [
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>lawson<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>LAWSON<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://d1mlw9qkqfqc3o.cloudfront.net/public/operator/indomaret.png<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>alfamidi<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ALFAMIDI<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://d1mlw9qkqfqc3o.cloudfront.net/public/operator/alfamidi.png<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>alfamart<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ALFAMART<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://d1mlw9qkqfqc3o.cloudfront.net/public/operator/alfamart.png<span class="pl-pds">"</span></span>
          },
          {
              <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>indomaret<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>INDOMARET<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://d1mlw9qkqfqc3o.cloudfront.net/public/operator/indomaret.png<span class="pl-pds">"</span></span>
          }
      ]
    }
  ]
}</pre></div>
<p>Get list of subscription payment methods.</p>
<h3><a id="user-content-http-request-21" class="anchor" aria-hidden="true" href="#http-request-21"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/subscription-payment-methods</code></p>
<h1><a id="user-content-subscriptions" class="anchor" aria-hidden="true" href="#subscriptions"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Subscriptions</h1>
<h2><a id="user-content-subscribe" class="anchor" aria-hidden="true" href="#subscribe"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Subscribe</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/subscriptions \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "payment_method_id": "va",</span>
<span class="pl-s">    "payment_channel_id": "bni",</span>
<span class="pl-s">    "email_address": "alice@example.com",</span>
<span class="pl-s">    "package_pricing_id": "1"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>4ce522df-a630-4c12-9ca1-058399b7e45a<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>start_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>end_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
  <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
  <span class="pl-s"><span class="pl-pds">"</span>package_pricing<span class="pl-pds">"</span></span>: {
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>package_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Premium<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
    <span class="pl-s"><span class="pl-pds">"</span>duration<span class="pl-pds">"</span></span>: <span class="pl-c1">1</span>,
    <span class="pl-s"><span class="pl-pds">"</span>duration_unit<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>month<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>discount_percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
    <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
    <span class="pl-s"><span class="pl-pds">"</span>voucher<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
  },
  <span class="pl-s"><span class="pl-pds">"</span>payment<span class="pl-pds">"</span></span>: {
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ddab538b-d44b-4840-a49f-a9e274aef8e8<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>status<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>waiting_payment<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>email_address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>alice@example.com<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>invoice_code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>INV-7286801<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>voucher_code<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>voucher_suffix<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>voucher_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_account_no<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>sellfazz12345<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-21T09:20:39.066679+07:00<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_expired_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-22T02:20:39.066678Z<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-21T09:20:39.066679+07:00<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_method<span class="pl-pds">"</span></span>: {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>va<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Virtual Account<span class="pl-pds">"</span></span>,
    },
    <span class="pl-s"><span class="pl-pds">"</span>payment_channel<span class="pl-pds">"</span></span>: {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>bni<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BNI<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://content.payfazz.com/object/88d1405e8a41134650db2e442a20674ed39ae0924a306c719591503e343d9c30<span class="pl-pds">"</span></span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>payment_instructions<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
  },
}</pre></div>
<p>Subscribe a premium package.</p>
<h3><a id="user-content-http-request-22" class="anchor" aria-hidden="true" href="#http-request-22"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/subscriptions</code></p>
<h2><a id="user-content-cancel-subscription-payment" class="anchor" aria-hidden="true" href="#cancel-subscription-payment"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Cancel Subscription Payment</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/subscriptions/e0dff58a-19e7-476f-9fcd-ff738cb4478b/cancel \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Cancel a subscription.</p>
<h3><a id="user-content-http-request-23" class="anchor" aria-hidden="true" href="#http-request-23"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/subscriptions/{subscription_id}/cancel</code></p>
<h2><a id="user-content-check-subscription-alerts" class="anchor" aria-hidden="true" href="#check-subscription-alerts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Check Subscription Alerts</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/subscriptions/check \
  -X GET \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>subscription_type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>premium<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>start_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-21T09:20:39.066679+07:00<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>end_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-10-21T09:20:39.066679+07:00<span class="pl-pds">"</span></span>
}</pre></div>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>subscription_type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>lite<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>start_date<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
  <span class="pl-s"><span class="pl-pds">"</span>end_date<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
}</pre></div>
<p>Check current subscription alerts.</p>
<h3><a id="user-content-http-request-24" class="anchor" aria-hidden="true" href="#http-request-24"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/subscriptions/check</code></p>
<h2><a id="user-content-subscription-list" class="anchor" aria-hidden="true" href="#subscription-list"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Subscription List</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/subscriptions \
  -X GET \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \</pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>4ce522df-a630-4c12-9ca1-058399b7e45a<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>start_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>end_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
      <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
      <span class="pl-s"><span class="pl-pds">"</span>package_pricing<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>package_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Premium<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
        <span class="pl-s"><span class="pl-pds">"</span>duration<span class="pl-pds">"</span></span>: <span class="pl-c1">1</span>,
        <span class="pl-s"><span class="pl-pds">"</span>duration_unit<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>month<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>discount_percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>voucher<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
      },
      <span class="pl-s"><span class="pl-pds">"</span>payment<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ddab538b-d44b-4840-a49f-a9e274aef8e8<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>status<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>waiting_payment<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>email_address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>alice@example.com<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>invoice_code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>INV-7286801<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>voucher_code<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
        <span class="pl-s"><span class="pl-pds">"</span>voucher_suffix<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
        <span class="pl-s"><span class="pl-pds">"</span>voucher_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_account_no<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>sellfazz12345<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-21T09:20:39.066679+07:00<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_expired_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-22T02:20:39.066678Z<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-21T09:20:39.066679+07:00<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_method<span class="pl-pds">"</span></span>: {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>va<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Virtual Account<span class="pl-pds">"</span></span>,
        },
        <span class="pl-s"><span class="pl-pds">"</span>payment_channel<span class="pl-pds">"</span></span>: {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>bni<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BNI<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://content.payfazz.com/object/88d1405e8a41134650db2e442a20674ed39ae0924a306c719591503e343d9c30<span class="pl-pds">"</span></span>
        },
        <span class="pl-s"><span class="pl-pds">"</span>payment_instructions<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
      }
    },
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>4ce522df-a630-4c12-058399b7-e45a9ca1<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>start_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>end_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
      <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
      <span class="pl-s"><span class="pl-pds">"</span>package_pricing<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>package_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Premium<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
        <span class="pl-s"><span class="pl-pds">"</span>duration<span class="pl-pds">"</span></span>: <span class="pl-c1">1</span>,
        <span class="pl-s"><span class="pl-pds">"</span>duration_unit<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>month<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>discount_percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>voucher<span class="pl-pds">"</span></span>: {
          <span class="pl-s"><span class="pl-pds">"</span>code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>SFNEW100<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>start_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>end_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-10-17T16:47:13.65804985+07:00<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
          <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">100000</span>,
          <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_auto_applied<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        },
      },
      <span class="pl-s"><span class="pl-pds">"</span>payment<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ab538b-d44b-4840-a4dd9f-a9e274aef8e8<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>status<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>email_address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>alice@example.com<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>invoice_code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>INV-8680172<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>voucher_code<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
        <span class="pl-s"><span class="pl-pds">"</span>voucher_suffix<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
        <span class="pl-s"><span class="pl-pds">"</span>voucher_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_account_no<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>sellfazz12345<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-21T09:20:39.066679+07:00<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_expired_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-22T02:20:39.066678Z<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-21T09:20:39.066679+07:00<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_method<span class="pl-pds">"</span></span>: {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>va<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Virtual Account<span class="pl-pds">"</span></span>,
        },
        <span class="pl-s"><span class="pl-pds">"</span>payment_channel<span class="pl-pds">"</span></span>: {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>bni<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BNI<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://content.payfazz.com/object/88d1405e8a41134650db2e442a20674ed39ae0924a306c719591503e343d9c30<span class="pl-pds">"</span></span>
        },
        <span class="pl-s"><span class="pl-pds">"</span>payment_instructions<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
      },
    }
  ]
}</pre></div>
<p>Get list of subscriptions.
Status:</p>
<ul>
<li>"waiting_payment"</li>
<li>"active"</li>
<li>"ended"</li>
<li>"cancelled"</li>
<li>"trial"</li>
</ul>
<h3><a id="user-content-http-request-25" class="anchor" aria-hidden="true" href="#http-request-25"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/subscriptions</code> <br>
<code>GET https://staging.sellfazz.com/api/v2/subscriptions?starting_after=1</code> <br>
<code>GET https://staging.sellfazz.com/api/v2/subscriptions?ending_before=2</code> \</p>
<h2><a id="user-content-subscription-details" class="anchor" aria-hidden="true" href="#subscription-details"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Subscription Details</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/subscriptions/{subscription_id} \
  -X GET \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \</pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>4ce522df-a630-4c12-9ca1-058399b7e45a<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>start_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>end_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
  <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
  <span class="pl-s"><span class="pl-pds">"</span>package_pricing<span class="pl-pds">"</span></span>: {
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>package_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Premium<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
    <span class="pl-s"><span class="pl-pds">"</span>duration<span class="pl-pds">"</span></span>: <span class="pl-c1">1</span>,
    <span class="pl-s"><span class="pl-pds">"</span>duration_unit<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>month<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>discount_percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
    <span class="pl-s"><span class="pl-pds">"</span>discount_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
    <span class="pl-s"><span class="pl-pds">"</span>voucher<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
  },
  <span class="pl-s"><span class="pl-pds">"</span>payment<span class="pl-pds">"</span></span>: {
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ddab538b-d44b-4840-a49f-a9e274aef8e8<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>status<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>waiting_payment<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>email_address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>alice@example.com<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>invoice_code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>INV-7286801<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>voucher_code<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>voucher_suffix<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>voucher_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">150000</span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_method_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>va<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_channel_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>bca<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_account_no<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>sellfazz12345<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-21T09:20:39.066679+07:00<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_expired_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-22T02:20:39.066678Z<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-09-21T09:20:39.066679+07:00<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_method<span class="pl-pds">"</span></span>: {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>va<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Virtual Account<span class="pl-pds">"</span></span>,
    },
    <span class="pl-s"><span class="pl-pds">"</span>payment_channel<span class="pl-pds">"</span></span>: {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>bni<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BNI<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>image_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://content.payfazz.com/object/88d1405e8a41134650db2e442a20674ed39ae0924a306c719591503e343d9c30<span class="pl-pds">"</span></span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>payment_instructions<span class="pl-pds">"</span></span>: [
      {
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ATM BCA<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>instructions<span class="pl-pds">"</span></span>: [
          <span class="pl-s"><span class="pl-pds">"</span>Pilih Menu &lt;b&gt;Transaksi Lainnya&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Pilih &lt;b&gt;Transfer&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Pilih &lt;b&gt;Ke rekening BCA Virtual Account&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Input Nomor Virtual Account: sellfazz12345<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Pilih &lt;b&gt;Benar&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Pilih &lt;b&gt;Ya&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Ambil bukti bayar Anda<span class="pl-pds">"</span></span>
        ]
      },
      {
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>m-BCA<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>instructions<span class="pl-pds">"</span></span>: [
          <span class="pl-s"><span class="pl-pds">"</span>Login Mobile Banking<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Pilih &lt;b&gt;m-Transfer&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Pilih &lt;b&gt;BCA Virtual Account&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Input Nomor Virtual Account: sellfazz12345<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Klik &lt;b&gt;Send&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Informasi VA akan ditampilkan<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Klik &lt;b&gt;OK&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Input PIN Mobile Banking<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Bukti bayar ditampilkan<span class="pl-pds">"</span></span>
        ]
      },
      {
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>KlikBCA<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>instructions<span class="pl-pds">"</span></span>: [
          <span class="pl-s"><span class="pl-pds">"</span>Login Internet Banking<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Pilih &lt;b&gt;Transaksi Dana&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Pilih &lt;b&gt;Transfer Ke BCA Virtual Account&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Input Nomor Virtual Account: sellfazz12345<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Klik &lt;b&gt;Lanjutkan&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Input Respon KeyBCA Appli 1<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Klik &lt;b&gt;Kirim&lt;/b&gt;<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>Bukti bayar ditampilkan<span class="pl-pds">"</span></span>
        ]
      }
    ]
  },
}</pre></div>
<p>Get subscription details.</p>
<h3><a id="user-content-http-request-26" class="anchor" aria-hidden="true" href="#http-request-26"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/subscriptions/{subscription_id}</code></p>
<h1><a id="user-content-subscription-vouchers" class="anchor" aria-hidden="true" href="#subscription-vouchers"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Subscription Vouchers</h1>
<h2><a id="user-content-voucher-list" class="anchor" aria-hidden="true" href="#voucher-list"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Voucher List</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/vouchers/DISKON50K \
  -X GET \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>DISKON50K<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>start_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>end_date<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-10-22T18:35:04.9129325+07:00<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
  <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">50000</span>,
  <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
  <span class="pl-s"><span class="pl-pds">"</span>is_auto_applied<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
}</pre></div>
<p>Get a subscription voucher by code</p>
<h3><a id="user-content-http-request-27" class="anchor" aria-hidden="true" href="#http-request-27"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/vouchers/{voucher_code}</code></p>
<h1><a id="user-content-location" class="anchor" aria-hidden="true" href="#location"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Location</h1>
<h2><a id="user-content-list-areas" class="anchor" aria-hidden="true" href="#list-areas"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List areas</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/areas</pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>[
  {
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>province<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>DKI JAKARTA<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>regency<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>JAKARTA PUSAT<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>district<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>GAMBIR<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>village<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>CIDENG<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>postalCode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>10150<span class="pl-pds">"</span></span>
  },
  {
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>province<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>JAWA BARAT<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>regency<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BANDUNG BARAT<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>district<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>CIHAMPELAS<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>village<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>MEKARMUKTI<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>postalCode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>40562<span class="pl-pds">"</span></span>
  }
  <span class="pl-ii">...</span>
]</pre></div>
<p>List all areas.</p>
<h3><a id="user-content-http-request-28" class="anchor" aria-hidden="true" href="#http-request-28"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/areas</code></p>
<h1><a id="user-content-devices" class="anchor" aria-hidden="true" href="#devices"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Devices</h1>
<h2><a id="user-content-create-a-device" class="anchor" aria-hidden="true" href="#create-a-device"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a device</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/devices \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "outlet_id": "1",</span>
<span class="pl-s">    "name": "Alice X"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>a82f226b-fd3c-4ce6-b3ca-c62154369f74<span class="pl-pds">"</span></span>, 
  <span class="pl-s"><span class="pl-pds">"</span>outlet<span class="pl-pds">"</span></span>: {
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Toko Sentosa<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
  },
  <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Alice X<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>activation_code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>J07S0SGE<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>synchronized_at<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
}</pre></div>
<p>Create a device.</p>
<h3><a id="user-content-http-request-29" class="anchor" aria-hidden="true" href="#http-request-29"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/devices</code></p>
<h2><a id="user-content-create-a-device-token" class="anchor" aria-hidden="true" href="#create-a-device-token"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a device token</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/device-tokens \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "activation_code": "J07S0SGE"    </span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>a82f226b-fd3c-4ce6-b3ca-c62154369f74<span class="pl-pds">"</span></span>  
}</pre></div>
<p>Create a device token.</p>
<h3><a id="user-content-http-request-30" class="anchor" aria-hidden="true" href="#http-request-30"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/device-tokens</code></p>
<h2><a id="user-content-list-device-employees" class="anchor" aria-hidden="true" href="#list-device-employees"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List device employees</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/device-tokens/a82f226b-fd3c-4ce6-b3ca-c62154369f74/employees  </pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>James<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>pin<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>123567<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>pin_required<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
    },
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>4<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Bob<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>pin<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>pin_required<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
    }
  ]
}</pre></div>
<p>List employees for a device.</p>
<h3><a id="user-content-http-request-31" class="anchor" aria-hidden="true" href="#http-request-31"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/device-tokens/{device_token_id}/employees</code></p>
<h2><a id="user-content-delete-a-device" class="anchor" aria-hidden="true" href="#delete-a-device"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete a device</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/devices/a82f226b-fd3c-4ce6-b3ca-c62154369f74 \
  -X DELETE \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete a device.</p>
<h3><a id="user-content-http-request-32" class="anchor" aria-hidden="true" href="#http-request-32"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/devices/{device_id}</code></p>
<h2><a id="user-content-release-a-device" class="anchor" aria-hidden="true" href="#release-a-device"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Release a device</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/devices/a82f226b-fd3c-4ce6-b3ca-c62154369f74/release \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>  </pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Release a device.</p>
<h3><a id="user-content-http-request-33" class="anchor" aria-hidden="true" href="#http-request-33"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/devices/{device_id}/release</code></p>
<h2><a id="user-content-get-a-device" class="anchor" aria-hidden="true" href="#get-a-device"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get a device</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/devices/a82f226b-fd3c-4ce6-b3ca-c62154369f74 \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>a82f226b-fd3c-4ce6-b3ca-c62154369f74<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>outlet<span class="pl-pds">"</span></span>: {
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Toko Sentosa<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
  },
  <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Alice X<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>activation_code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>J07S0SGE<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>synchronized_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-10-23T11:57:30.23925+07:00<span class="pl-pds">"</span></span>
}</pre></div>
<p>Get a device.</p>
<h3><a id="user-content-http-request-34" class="anchor" aria-hidden="true" href="#http-request-34"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/devices/{device_id}</code></p>
<h2><a id="user-content-list-devices" class="anchor" aria-hidden="true" href="#list-devices"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List devices</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/devices \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>outlet<span class="pl-pds">"</span></span>: {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Toko Sentosa<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>device 1<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>activation_code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ABCDEXXX<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>synchronized_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-10-23T11:57:30.23925+07:00<span class="pl-pds">"</span></span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>outlet<span class="pl-pds">"</span></span>: {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Toko Sentosa<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>device x<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>activation_code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ABCDEFGH<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>synchronized_at<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>a82f226b-fd3c-4ce6-b3ca-c62154369f74<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>outlet<span class="pl-pds">"</span></span>: {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Toko Sentosa<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
          },
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Alice X<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>activation_code<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>J07S0SGE<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>synchronized_at<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
        }
    ]
}</pre></div>
<p>List devices.</p>
<h3><a id="user-content-http-request-35" class="anchor" aria-hidden="true" href="#http-request-35"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/devices</code></p>
<h1><a id="user-content-employees" class="anchor" aria-hidden="true" href="#employees"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Employees</h1>
<h2><a id="user-content-list-employees" class="anchor" aria-hidden="true" href="#list-employees"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List employees</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/employees \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>James<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>pin<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>123567<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>pin_required<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Duke<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>pin<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>pin_required<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>3<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Anne<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>pin<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>pin_required<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        }
    ]
}</pre></div>
<p>List employees.</p>
<h3><a id="user-content-http-request-36" class="anchor" aria-hidden="true" href="#http-request-36"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/employees?limit=10</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/employees?limit=10&amp;starting_after=3</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/employees?limit=10&amp;ending_before=1</code></p>
<h2><a id="user-content-create-an-employee" class="anchor" aria-hidden="true" href="#create-an-employee"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create an employee</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/employees \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "name": "James",</span>
<span class="pl-s">    "pin": "123456",</span>
<span class="pl-s">    "pin_required": true</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>c558bf01-d0c4-4b04-88cd-31a2485b8be8<span class="pl-pds">"</span></span>,    
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>James<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>pin<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>123456<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>pin_required<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
}</pre></div>
<p>Create an employee.</p>
<h3><a id="user-content-http-request-37" class="anchor" aria-hidden="true" href="#http-request-37"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/employees</code></p>
<h2><a id="user-content-update-an-employee" class="anchor" aria-hidden="true" href="#update-an-employee"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update an employee</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/employees/c558bf01-d0c4-4b04-88cd-31a2485b8be8 \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "name": "Jamesss",</span>
<span class="pl-s">    "pin": "576819",</span>
<span class="pl-s">    "pin_required": true</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>c558bf01-d0c4-4b04-88cd-31a2485b8be8<span class="pl-pds">"</span></span>,    
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Jamesss<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>pin<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>576819<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>pin_required<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
}</pre></div>
<p>Update an employee.</p>
<h3><a id="user-content-http-request-38" class="anchor" aria-hidden="true" href="#http-request-38"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/employees/{employee_id}</code></p>
<h2><a id="user-content-delete-an-employee" class="anchor" aria-hidden="true" href="#delete-an-employee"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete an employee</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/employees/c558bf01-d0c4-4b04-88cd-31a2485b8be8 \
  -X DELETE  
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete an employee.</p>
<h3><a id="user-content-http-request-39" class="anchor" aria-hidden="true" href="#http-request-39"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/employees/{employee_id}</code></p>
<h2><a id="user-content-delete-all-employees" class="anchor" aria-hidden="true" href="#delete-all-employees"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete all employees</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/employees \
  -X DELETE  
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete all employees.</p>
<h3><a id="user-content-http-request-40" class="anchor" aria-hidden="true" href="#http-request-40"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/employees</code></p>
<h2><a id="user-content-login-an-employee" class="anchor" aria-hidden="true" href="#login-an-employee"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Login an employee</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/employees/c558bf01-d0c4-4b04-88cd-31a2485b8be8/login \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> <span class="pl-cce">\ </span> 
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "device_token_id": "a82f226b-fd3c-4ce6-b3ca-c62154369f74",</span>
<span class="pl-s">    "pin": "576819",    </span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>access_token<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Npf46wMqV3eewgaoK8RFtND6PHHzqXk6MnBCPEfzY2ppOgch9N8mlIOpGRZH0AFv<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>access_type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>employee<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>device_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1b02a560-e99d-4c02-88f7-7e754881d885<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>employee_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2b325044-8782-40be-8405-f6d1c3d97dfb<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>outlet_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>689b6d23-fa1f-4e0b-8c4b-cfa79309228b<span class="pl-pds">"</span></span>
}</pre></div>
<p>Login an employee.</p>
<h3><a id="user-content-http-request-41" class="anchor" aria-hidden="true" href="#http-request-41"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/employees/{employee_id}/login</code></p>
<h2><a id="user-content-get-an-employee-session" class="anchor" aria-hidden="true" href="#get-an-employee-session"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get an employee session</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/employees/c558bf01-d0c4-4b04-88cd-31a2485b8be8/session \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>  </pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>outlet_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Toko Sentosa<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>device_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Alice X<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-10-22T07:23:13.732619+07:00<span class="pl-pds">"</span></span>
}</pre></div>
<p>Get an employee session.</p>
<h3><a id="user-content-http-request-42" class="anchor" aria-hidden="true" href="#http-request-42"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/employees/{employee_id}/session</code></p>
<h2><a id="user-content-logout-an-employee" class="anchor" aria-hidden="true" href="#logout-an-employee"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Logout an employee</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/employees/c558bf01-d0c4-4b04-88cd-31a2485b8be8/logout \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Release an employee session.</p>
<h3><a id="user-content-http-request-43" class="anchor" aria-hidden="true" href="#http-request-43"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/employees/{employee_id}/logout</code></p>
<h1><a id="user-content-shifts" class="anchor" aria-hidden="true" href="#shifts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Shifts</h1>
<h2><a id="user-content-batch-upsert-shifts" class="anchor" aria-hidden="true" href="#batch-upsert-shifts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Batch upsert shifts</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/shifts/batch-upsert \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "data": [</span>
<span class="pl-s">      {</span>
<span class="pl-s">        "shift_id": "fgfc9UH0TonMtKrZKxOyc1Ev",</span>
<span class="pl-s">        "outlet_id": "1",</span>
<span class="pl-s">        "outlet_name": "outlet 1",</span>
<span class="pl-s">        "device_id": "1",</span>
<span class="pl-s">        "device_name": "device 1",</span>
<span class="pl-s">        "initial_cash": 500000,</span>
<span class="pl-s">        "total_cash_amount": 1500000,</span>
<span class="pl-s">        "total_non_cash_amount": 500000,</span>
<span class="pl-s">        "system_income_amount": 3500000,</span>
<span class="pl-s">        "started_at": "2019-08-20T07:00:00Z",</span>
<span class="pl-s">        "ended_at": "2019-08-20T22:00:00Z",</span>
<span class="pl-s">        "started_by_employee_id": "1",</span>
<span class="pl-s">        "started_by_employee_name": "Duke",</span>
<span class="pl-s">        "ended_by_employee_id": "2",</span>
<span class="pl-s">        "ended_by_employee_name": "James",</span>
<span class="pl-s">        "cash_flows": [</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "1",</span>
<span class="pl-s">            "shift_id": "fgfc9UH0TonMtKrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "2",</span>
<span class="pl-s">            "employee_name": "Duke",</span>
<span class="pl-s">            "cash_amount": 500000,</span>
<span class="pl-s">            "notes": "Modal awal",</span>
<span class="pl-s">            "client_created_at": "2019-08-20T07:00:15Z"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "2",</span>
<span class="pl-s">            "shift_id": "fgfc9UH0TonMtKrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "2",</span>
<span class="pl-s">            "employee_name": "Duke",</span>
<span class="pl-s">            "cash_amount": -300000,</span>
<span class="pl-s">            "notes": "Bayar listrik",</span>
<span class="pl-s">            "client_created_at": "2019-08-20T09:00:15Z"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "3",</span>
<span class="pl-s">            "shift_id": "fgfc9UH0TonMtKrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "2",</span>
<span class="pl-s">            "employee_name": "Duke",</span>
<span class="pl-s">            "cash_amount": 500000,</span>
<span class="pl-s">            "notes": "Tambahan modal",</span>
<span class="pl-s">            "client_created_at": "2019-08-20T14:00:15Z"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "4",</span>
<span class="pl-s">            "shift_id": "fgfc9UH0TonMtKrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "1",</span>
<span class="pl-s">            "employee_name": "James",</span>
<span class="pl-s">            "cash_amount": -200000,</span>
<span class="pl-s">            "notes": "Bayar air",</span>
<span class="pl-s">            "client_created_at": "2019-08-20T15:00:15Z"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "5",</span>
<span class="pl-s">            "shift_id": "fgfc9UH0TonMtKrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "1",</span>
<span class="pl-s">            "employee_name": "James",</span>
<span class="pl-s">            "cash_amount": 250000,</span>
<span class="pl-s">            "notes": "Tambahan modal 2",</span>
<span class="pl-s">            "client_created_at": "2019-08-20T20:00:15Z"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "6",</span>
<span class="pl-s">            "shift_id": "fgfc9UH0TonMtKrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "1",</span>
<span class="pl-s">            "employee_name": "James",</span>
<span class="pl-s">            "cash_amount": 750000,</span>
<span class="pl-s">            "notes": "Utang tetangga",</span>
<span class="pl-s">            "client_created_at": "2019-08-20T21:30:15Z"</span>
<span class="pl-s">          }</span>
<span class="pl-s">        ],</span>
<span class="pl-s">        "employees": [</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "employee_id": "1",</span>
<span class="pl-s">            "employee_name": "James"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "employee_id": "2",</span>
<span class="pl-s">            "employee_name": "Duke"</span>
<span class="pl-s">          }</span>
<span class="pl-s">        ]</span>
<span class="pl-s">      },</span>
<span class="pl-s">      {</span>
<span class="pl-s">        "shift_id": "TonMtfgfc9UH0KrZKxOyc1Ev",</span>
<span class="pl-s">        "outlet_id": "1",</span>
<span class="pl-s">        "outlet_name": "outlet 1",</span>
<span class="pl-s">        "device_id": "1",</span>
<span class="pl-s">        "device_name": "device 1",</span>
<span class="pl-s">        "initial_cash": 250000,</span>
<span class="pl-s">        "total_cash_amount": 3000000,</span>
<span class="pl-s">        "total_non_cash_amount": 2000000,</span>
<span class="pl-s">        "system_income_amount": 5000000,</span>
<span class="pl-s">        "started_at": "2019-08-30T14:00:00Z",</span>
<span class="pl-s">        "ended_at": "2019-08-30T22:00:00Z",</span>
<span class="pl-s">        "started_by_employee_id": "1",</span>
<span class="pl-s">        "started_by_employee_name": "Duke",</span>
<span class="pl-s">        "ended_by_employee_id": "2",</span>
<span class="pl-s">        "ended_by_employee_name": "James",</span>
<span class="pl-s">        "cash_flows": [</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "11",</span>
<span class="pl-s">            "shift_id": "TonMtfgfc9UH0KrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "2",</span>
<span class="pl-s">            "employee_name": "Duke",</span>
<span class="pl-s">            "cash_amount": 250000,</span>
<span class="pl-s">            "notes": "Modal awal",</span>
<span class="pl-s">            "client_created_at": "2019-08-30T14:00:00Z"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "12",</span>
<span class="pl-s">            "shift_id": "TonMtfgfc9UH0KrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "2",</span>
<span class="pl-s">            "employee_name": "Duke",</span>
<span class="pl-s">            "cash_amount": -250000,</span>
<span class="pl-s">            "notes": "Bayar internet",</span>
<span class="pl-s">            "client_created_at": "2019-08-30T15:00:00Z"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "13",</span>
<span class="pl-s">            "shift_id": "TonMtfgfc9UH0KrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "2",</span>
<span class="pl-s">            "employee_name": "Duke",</span>
<span class="pl-s">            "cash_amount": 1000000,</span>
<span class="pl-s">            "notes": "Tambahan modal",</span>
<span class="pl-s">            "client_created_at": "2019-08-30T20:00:00Z"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "14",</span>
<span class="pl-s">            "shift_id": "TonMtfgfc9UH0KrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "1",</span>
<span class="pl-s">            "employee_name": "James",</span>
<span class="pl-s">            "cash_amount": -500000,</span>
<span class="pl-s">            "notes": "Bayar air",</span>
<span class="pl-s">            "client_created_at": "2019-08-30T21:00:00Z"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "15",</span>
<span class="pl-s">            "shift_id": "TonMtfgfc9UH0KrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "1",</span>
<span class="pl-s">            "employee_name": "James",</span>
<span class="pl-s">            "cash_amount": 2500000,</span>
<span class="pl-s">            "notes": "Tambahan modal 2",</span>
<span class="pl-s">            "client_created_at": "2019-08-30T21:30:00Z"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "cash_flow_id": "16",</span>
<span class="pl-s">            "shift_id": "TonMtfgfc9UH0KrZKxOyc1Ev",</span>
<span class="pl-s">            "device_id": "1",</span>
<span class="pl-s">            "outlet_id": "1",</span>
<span class="pl-s">            "employee_id": "1",</span>
<span class="pl-s">            "employee_name": "James",</span>
<span class="pl-s">            "cash_amount": -500000,</span>
<span class="pl-s">            "notes": "Bayar uang keamanan",</span>
<span class="pl-s">            "client_created_at": "2019-08-30T21:45:00Z"</span>
<span class="pl-s">          }</span>
<span class="pl-s">        ],</span>
<span class="pl-s">        "employees": [</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "employee_id": "1",</span>
<span class="pl-s">            "employee_name": "James"</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "employee_id": "2",</span>
<span class="pl-s">            "employee_name": "Duke"</span>
<span class="pl-s">          }</span>
<span class="pl-s">        ]</span>
<span class="pl-s">      }</span>
<span class="pl-s">    ]</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Batch insert or update shift cash recap with operators(employees).</p>
<h3><a id="user-content-http-request-44" class="anchor" aria-hidden="true" href="#http-request-44"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/shifts/batch-upsert</code></p>
<h1><a id="user-content-outlets" class="anchor" aria-hidden="true" href="#outlets"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Outlets</h1>
<h2><a id="user-content-list-outlets" class="anchor" aria-hidden="true" href="#list-outlets"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List outlets</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/outlets \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>  </pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Toko Sentosa<span class="pl-pds">"</span></span>
    }
  ]
}</pre></div>
<p>Find all outlets. Default limit 200.</p>
<h3><a id="user-content-http-request-45" class="anchor" aria-hidden="true" href="#http-request-45"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/outlets</code></p>
<h2><a id="user-content-create-an-outlet" class="anchor" aria-hidden="true" href="#create-an-outlet"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create an outlet</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/outlets \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "name" : "Outlet 1"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>689b6d23-fa1f-4e0b-8c4b-cfa79309228b<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Outlet 1<span class="pl-pds">"</span></span>
}</pre></div>
<p>Create an outlet.</p>
<h3><a id="user-content-http-request-46" class="anchor" aria-hidden="true" href="#http-request-46"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/outlets</code></p>
<h2><a id="user-content-update-an-outlet" class="anchor" aria-hidden="true" href="#update-an-outlet"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update an outlet</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/outlets/689b6d23-fa1f-4e0b-8c4b-cfa79309228b \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "name" : "Outlet Update 1"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>689b6d23-fa1f-4e0b-8c4b-cfa79309228b<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Outlet Update 1<span class="pl-pds">"</span></span>
}</pre></div>
<p>Update an outlet.</p>
<h3><a id="user-content-http-request-47" class="anchor" aria-hidden="true" href="#http-request-47"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/outlets/{outlet_id}</code></p>
<h2><a id="user-content-delete-an-outlet" class="anchor" aria-hidden="true" href="#delete-an-outlet"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete an outlet</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/outlets/689b6d23-fa1f-4e0b-8c4b-cfa79309228b \
  -X DELETE \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete an outlet.</p>
<h3><a id="user-content-http-request-48" class="anchor" aria-hidden="true" href="#http-request-48"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/outlets/{outlet_id}</code></p>
<h2><a id="user-content-delete-all-outlets" class="anchor" aria-hidden="true" href="#delete-all-outlets"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete all outlets</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/outlets \
  -X DELETE \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete all outlets.</p>
<h3><a id="user-content-http-request-49" class="anchor" aria-hidden="true" href="#http-request-49"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE /outlets/</code></p>
<h1><a id="user-content-settings" class="anchor" aria-hidden="true" href="#settings"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Settings</h1>
<h2><a id="user-content-get-receipt-setting" class="anchor" aria-hidden="true" href="#get-receipt-setting"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get Receipt setting</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/settings/receipt \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>  </pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>logo_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://google.com/img1<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>footnote<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Terima kasih 1<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>is_print_logo<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
  <span class="pl-s"><span class="pl-pds">"</span>is_print_sf_logo<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
}</pre></div>
<p>Get an owner shift setting.</p>
<h3><a id="user-content-http-request-50" class="anchor" aria-hidden="true" href="#http-request-50"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/settings/receipt</code></p>
<h2><a id="user-content-save-receipt-setting" class="anchor" aria-hidden="true" href="#save-receipt-setting"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Save Receipt setting</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/settings/receipt \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "logo_url": "http://google.com/img1",</span>
<span class="pl-s">    "footnote": "Terima kasih 1",</span>
<span class="pl-s">    "is_print_logo": false,</span>
<span class="pl-s">    "is_print_sf_logo": false</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example Response:</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>logo_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://google.com/img1<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>footnote<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Terima kasih 1<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>is_print_logo<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
  <span class="pl-s"><span class="pl-pds">"</span>is_print_sf_logo<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
}</pre></div>
<p>Create/update a owner receipt setting.</p>
<h3><a id="user-content-http-request-51" class="anchor" aria-hidden="true" href="#http-request-51"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/settings/receipt</code></p>
<h2><a id="user-content-shiftsetting" class="anchor" aria-hidden="true" href="#shiftsetting"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>ShiftSetting</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/settings/shift \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example Response:</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>is_auto<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>initial_cash<span class="pl-pds">"</span></span>: <span class="pl-c1">500000</span>
}</pre></div>
<p>Get an owner shift setting.</p>
<h3><a id="user-content-http-request-52" class="anchor" aria-hidden="true" href="#http-request-52"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/settings/shift</code></p>
<h2><a id="user-content-save-user-shift-settings" class="anchor" aria-hidden="true" href="#save-user-shift-settings"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Save user shift settings</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/settings/shift \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "is_auto": true,</span>
<span class="pl-s">    "initial_cash": 500000</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example Response:</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>is_auto<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>initial_cash<span class="pl-pds">"</span></span>: <span class="pl-c1">500000</span>
}</pre></div>
<p>Create/update a device shift setting.</p>
<h3><a id="user-content-http-request-53" class="anchor" aria-hidden="true" href="#http-request-53"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/settings/shift</code></p>
<h1><a id="user-content-service-types" class="anchor" aria-hidden="true" href="#service-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Service Types</h1>
<h2><a id="user-content-create-a-service-types" class="anchor" aria-hidden="true" href="#create-a-service-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a service types</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/service-types \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    	"name":"dine in",</span>
<span class="pl-s">      "is_default": true,</span>
<span class="pl-s">      "with_service_charge": true</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
}</pre></div>
<p>Create a new service types.</p>
<h3><a id="user-content-http-request-54" class="anchor" aria-hidden="true" href="#http-request-54"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/service-types</code></p>
<h2><a id="user-content-update-a-service-types" class="anchor" aria-hidden="true" href="#update-a-service-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update a service types</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/service-types/454bbbbc-3482-4ba1-bd04-6b6da94fb9df \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">        "name": "gofood",</span>
<span class="pl-s">        "is_default": true,</span>
<span class="pl-s">        "with_service_charge": false</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>454bbbbc-3482-4ba1-bd04-6b6da94fb9df<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>gofood<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
}</pre></div>
<p>Update a service types.</p>
<h3><a id="user-content-http-request-55" class="anchor" aria-hidden="true" href="#http-request-55"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/service-types/{service_type_id}</code></p>
<h2><a id="user-content-get-a-service-types" class="anchor" aria-hidden="true" href="#get-a-service-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get a service types</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/service-types/454bbbbc-3482-4ba1-bd04-6b6da94fb9df \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>  </pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>454bbbbc-3482-4ba1-bd04-6b6da94fb9df<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
}</pre></div>
<p>Get a service types by id.</p>
<h3><a id="user-content-http-request-56" class="anchor" aria-hidden="true" href="#http-request-56"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/service-types/{service_type_id}</code></p>
<h2><a id="user-content-list-service-types" class="anchor" aria-hidden="true" href="#list-service-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List service types</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/service-types \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>  </pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        }
    ]
}</pre></div>
<p>List of service types.</p>
<h3><a id="user-content-http-request-57" class="anchor" aria-hidden="true" href="#http-request-57"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/service-types?limit=10</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/service-types?limit=10&amp;starting_after=5d51b4a-8e39-45e7-b620-38b2c0dba3f3</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/service-types?limit=10&amp;ending_before=42125ac2-2a97-4caf-a53c-f86f5928f117</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/service-types?limit=10&amp;name=grab</code></p>
<h2><a id="user-content-delete-a-service-types" class="anchor" aria-hidden="true" href="#delete-a-service-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete a service types</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/service-types/42125ac2-2a97-4caf-a53c-f86f5928f117 \
  -X DELETE
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete a service types.</p>
<h3><a id="user-content-http-request-58" class="anchor" aria-hidden="true" href="#http-request-58"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/service-types/{service_type_id}</code></p>
<h2><a id="user-content-delete-all-service-types" class="anchor" aria-hidden="true" href="#delete-all-service-types"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete all service types</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/service-types \
  -X DELETE
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete all service types.</p>
<h3><a id="user-content-http-request-59" class="anchor" aria-hidden="true" href="#http-request-59"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/service-types</code></p>
<h1><a id="user-content-categories" class="anchor" aria-hidden="true" href="#categories"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Categories</h1>
<h2><a id="user-content-create-a-category" class="anchor" aria-hidden="true" href="#create-a-category"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a category</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/categories \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "name" : "Elektronika"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>896c54e9-b85f-4efb-8b8b-afa92819b35f<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Elektronika<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
  <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
}</pre></div>
<p>Create a new category.</p>
<h3><a id="user-content-http-request-60" class="anchor" aria-hidden="true" href="#http-request-60"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/categories</code></p>
<h2><a id="user-content-update-a-category" class="anchor" aria-hidden="true" href="#update-a-category"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update a category</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/categories/896c54e9-b85f-4efb-8b8b-afa92819b35f \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "name" : "Peralatan elektronika"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>896c54e9-b85f-4efb-8b8b-afa92819b35f<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,    
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
}</pre></div>
<p>Update a category.</p>
<h3><a id="user-content-http-request-61" class="anchor" aria-hidden="true" href="#http-request-61"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/categories/{category_id}</code></p>
<h2><a id="user-content-get-a-category" class="anchor" aria-hidden="true" href="#get-a-category"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get a category</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/categories/896c54e9-b85f-4efb-8b8b-afa92819b35f \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>  </pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>896c54e9-b85f-4efb-8b8b-afa92819b35f<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,    
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
}</pre></div>
<p>Get a category by id.</p>
<h3><a id="user-content-http-request-62" class="anchor" aria-hidden="true" href="#http-request-62"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/categories/{category_id}</code></p>
<h2><a id="user-content-list-categories" class="anchor" aria-hidden="true" href="#list-categories"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List categories</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/categories \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>  </pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Example1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Example2<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>896c54e9-b85f-4efb-8b8b-afa92819b35f<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        }
    ]
}</pre></div>
<p>List of categories.</p>
<h3><a id="user-content-http-request-63" class="anchor" aria-hidden="true" href="#http-request-63"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/categories?limit=10</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/categories?limit=10&amp;starting_after=2</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/categories?limit=10&amp;ending_before=2</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/categories?limit=10&amp;name=peralatan</code></p>
<h2><a id="user-content-delete-a-category" class="anchor" aria-hidden="true" href="#delete-a-category"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete a category</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/categories/896c54e9-b85f-4efb-8b8b-afa92819b35f \
  -X DELETE
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete a category.</p>
<h3><a id="user-content-http-request-64" class="anchor" aria-hidden="true" href="#http-request-64"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/categories/{category_id}</code></p>
<h2><a id="user-content-delete-all-category" class="anchor" aria-hidden="true" href="#delete-all-category"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete all category</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/categories \
  -X DELETE
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete all category.</p>
<h3><a id="user-content-http-request-65" class="anchor" aria-hidden="true" href="#http-request-65"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/categories</code></p>
<h1><a id="user-content-products" class="anchor" aria-hidden="true" href="#products"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Products</h1>
<h2><a id="user-content-create-a-single-product" class="anchor" aria-hidden="true" href="#create-a-single-product"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a single product</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/single \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">      "name":"kipas angin",</span>
<span class="pl-s">      "description":"ini kipas angin",</span>
<span class="pl-s">      "picture_url":"shjshajhajha",</span>
<span class="pl-s">      "category_id":"9957969d-4b99-4c0b-a7cd-8d885fe7a4db",</span>
<span class="pl-s">      "barcode":"absjk",</span>
<span class="pl-s">      "combo_only":false,</span>
<span class="pl-s">      "active":true,</span>
<span class="pl-s">      "track_stock":true,</span>
<span class="pl-s">      "min_stock":1000,</span>
<span class="pl-s">      "price":11.0,</span>
<span class="pl-s">      "pricing":[{</span>
<span class="pl-s">        "service_type_id": "45d51b4a-8e39-45e7-b620-38b2c0dba3f3",</span>
<span class="pl-s">        "price": 100.0</span>
<span class="pl-s">      },</span>
<span class="pl-s">      {</span>
<span class="pl-s">        "service_type_id": "42125ac2-2a97-4caf-a53c-f86f5928f117",</span>
<span class="pl-s">        "price":10.0</span>
<span class="pl-s">      }],</span>
<span class="pl-s">      "unit_cost":10.0,</span>
<span class="pl-s">      "weight":100.0,</span>
<span class="pl-s">      "stock":1000,</span>
<span class="pl-s">      "favorite": false</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>97ba8025-97e0-4b73-817a-4eaf87f66742<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
        <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
            },
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
            }
        ],
        <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
        <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
        <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>,
        <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
}</pre></div>
<p>Create a single product.</p>
<h3><a id="user-content-http-request-66" class="anchor" aria-hidden="true" href="#http-request-66"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/products/single</code></p>
<h2><a id="user-content-create-a-variation-product" class="anchor" aria-hidden="true" href="#create-a-variation-product"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a variation product</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/variation \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    	"name":"elektronika",</span>
<span class="pl-s">      "description":"variasi elektronika",</span>
<span class="pl-s">      "picture_url":"http://...",</span>
<span class="pl-s">      "category_id":"9957969d-4b99-4c0b-a7cd-8d885fe7a4db",</span>
<span class="pl-s">      "single_product_ids":["273fcff8-aa42-4065-86cf-d05478f31ac1"],</span>
<span class="pl-s">      "active": true,</span>
<span class="pl-s">      "favorite": false</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>b60b8977-a1f8-4dfc-91dc-1a7a83a41eb9<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>elektronika<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>variasi elektronika<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://...<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>variation<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>single_product_ids<span class="pl-pds">"</span></span>: [
            <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>
        ],
        <span class="pl-s"><span class="pl-pds">"</span>single_products<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                        {
                            <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                            },
                            <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
                        },
                        {
                            <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                            },
                            <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
                        }
                    ],
                    <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
                <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
            }
        ]
    },
    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
}</pre></div>
<p>Create a variation product.</p>
<h3><a id="user-content-http-request-67" class="anchor" aria-hidden="true" href="#http-request-67"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/products/variation</code></p>
<h2><a id="user-content-create-a-combo-product" class="anchor" aria-hidden="true" href="#create-a-combo-product"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a combo product</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/combo \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    	"name":"combo 1",</span>
<span class="pl-s">      "description":"example of combo prod",</span>
<span class="pl-s">      "picture_url":"http://..",</span>
<span class="pl-s">      "category_id":"9957969d-4b99-4c0b-a7cd-8d885fe7a4db",</span>
<span class="pl-s">      "choices":[{</span>
<span class="pl-s">        "name":"choice 1",</span>
<span class="pl-s">        "options":[{</span>
<span class="pl-s">          "single_product_id":"273fcff8-aa42-4065-86cf-d05478f31ac1"</span>
<span class="pl-s">        }]</span>
<span class="pl-s">      }],</span>
<span class="pl-s">      "price":10.0,</span>
<span class="pl-s">      "pricing":[{</span>
<span class="pl-s">        "service_type_id": "45d51b4a-8e39-45e7-b620-38b2c0dba3f3",</span>
<span class="pl-s">        "price": 12.0</span>
<span class="pl-s">      }],</span>
<span class="pl-s">      "active": true,</span>
<span class="pl-s">      "favorite" : false</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>a0c2220e-6d7c-4201-9d19-7ab18af59dce<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>combo 1<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>example of combo prod<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://..<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>combo<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
        <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
            }
        ],
        <span class="pl-s"><span class="pl-pds">"</span>choices<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>choice 1<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>options<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>single_product_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>single_product<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
                            },
                            <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                                <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                                    {
                                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                                        },
                                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
                                    },
                                    {
                                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                                        },
                                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
                                    }
                                ],
                                <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
                            },
                            <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
                        }
                    }
                ]
            }
        ]
    }
}</pre></div>
<p>Create a combo product.</p>
<h3><a id="user-content-http-request-68" class="anchor" aria-hidden="true" href="#http-request-68"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/products/combo</code></p>
<h2><a id="user-content-update-a-single-product" class="anchor" aria-hidden="true" href="#update-a-single-product"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update a single product</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/273fcff8-aa42-4065-86cf-d05478f31ac1/single \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    	"name":"ddssss",</span>
<span class="pl-s">      "description":"mels",</span>
<span class="pl-s">      "picture_url":"http://....",</span>
<span class="pl-s">      "category_id":"9957969d-4b99-4c0b-a7cd-8d885fe7a4db",</span>
<span class="pl-s">      "barcode":"absjk426252",</span>
<span class="pl-s">      "combo_only":false,</span>
<span class="pl-s">      "active":true,</span>
<span class="pl-s">      "track_stock":true,</span>
<span class="pl-s">      "min_stock":1000,</span>
<span class="pl-s">      "price":11.0,</span>
<span class="pl-s">      "pricing":[{</span>
<span class="pl-s">        "service_type_id": "42125ac2-2a97-4caf-a53c-f86f5928f117",</span>
<span class="pl-s">        "price": 12.0</span>
<span class="pl-s">      }],</span>
<span class="pl-s">      "unit_cost":10.0,</span>
<span class="pl-s">      "weight":100.0,</span>
<span class="pl-s">      "stock":1000,</span>
<span class="pl-s">      "favorite": false</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ddssss<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>mels<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://....<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
        <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
            }
        ],
        <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
        <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
        <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk426252<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>,
        <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
}</pre></div>
<p>Update a single product.</p>
<h3><a id="user-content-http-request-69" class="anchor" aria-hidden="true" href="#http-request-69"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/products/{product_id}/single</code></p>
<h2><a id="user-content-update-a-variation-product" class="anchor" aria-hidden="true" href="#update-a-variation-product"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update a variation product</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/b60b8977-a1f8-4dfc-91dc-1a7a83a41eb9/variation \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    	"name":"elektronika2",</span>
<span class="pl-s">      "description":"variasi elektronika2",</span>
<span class="pl-s">      "picture_url":"http://...",</span>
<span class="pl-s">      "category_id":"9957969d-4b99-4c0b-a7cd-8d885fe7a4db",</span>
<span class="pl-s">      "single_product_ids":["273fcff8-aa42-4065-86cf-d05478f31ac1","97ba8025-97e0-4b73-817a-4eaf87f66742"],</span>
<span class="pl-s">      "active": true,</span>
<span class="pl-s">      "favorite": false</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>b60b8977-a1f8-4dfc-91dc-1a7a83a41eb9<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>elektronika2<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>variasi elektronika2<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://...<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>variation<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>single_product_ids<span class="pl-pds">"</span></span>: [
            <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>97ba8025-97e0-4b73-817a-4eaf87f66742<span class="pl-pds">"</span></span>
        ],
        <span class="pl-s"><span class="pl-pds">"</span>single_products<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>97ba8025-97e0-4b73-817a-4eaf87f66742<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                        {
                            <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                            },
                            <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
                        },
                        {
                            <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                            },
                            <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
                        }
                    ],
                    <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
                <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
            },
            {
                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ddssss<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>mels<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://....<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                        {
                            <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                            },
                            <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
                        }
                    ],
                    <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk426252<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
                <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
            }
        ]
    },
    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
}</pre></div>
<p>Update a variation product.</p>
<h3><a id="user-content-http-request-70" class="anchor" aria-hidden="true" href="#http-request-70"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/products/{product_id}/variation</code></p>
<h2><a id="user-content-update-a-combo-product" class="anchor" aria-hidden="true" href="#update-a-combo-product"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update a combo product</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/a0c2220e-6d7c-4201-9d19-7ab18af59dce/combo \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    	"name":"combo 1",</span>
<span class="pl-s">      "description":"example of combo prod",</span>
<span class="pl-s">      "picture_url":"http://..",</span>
<span class="pl-s">      "category_id":"9957969d-4b99-4c0b-a7cd-8d885fe7a4db",</span>
<span class="pl-s">      "choices":[{</span>
<span class="pl-s">        "name":"choice 1",</span>
<span class="pl-s">        "options":[{</span>
<span class="pl-s">          "single_product_id":"273fcff8-aa42-4065-86cf-d05478f31ac1"</span>
<span class="pl-s">        }]</span>
<span class="pl-s">      }],</span>
<span class="pl-s">      "price":10.0,</span>
<span class="pl-s">      "pricing":[{</span>
<span class="pl-s">        "service_type_id": "45d51b4a-8e39-45e7-b620-38b2c0dba3f3",</span>
<span class="pl-s">        "price": 12.0</span>
<span class="pl-s">      }],</span>
<span class="pl-s">      "active": true,</span>
<span class="pl-s">      "favorite" : false</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>a0c2220e-6d7c-4201-9d19-7ab18af59dce<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>combo 1<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>example of combo prod<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://..<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>combo<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
        <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
            }
        ],
        <span class="pl-s"><span class="pl-pds">"</span>choices<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>choice 1<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>options<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>single_product_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>single_product<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
                            },
                            <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                                <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                                    {
                                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                                        },
                                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
                                    },
                                    {
                                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                                        },
                                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
                                    }
                                ],
                                <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                                <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
                            },
                            <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
                        }
                    }
                ]
            }
        ]
    }
}</pre></div>
<p>Update a combo product.</p>
<h3><a id="user-content-http-request-71" class="anchor" aria-hidden="true" href="#http-request-71"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/products/{product_id}/combo</code></p>
<h2><a id="user-content-get-a-product" class="anchor" aria-hidden="true" href="#get-a-product"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get a product</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/97ba8025-97e0-4b73-817a-4eaf87f66742 <span class="pl-cce">\ </span>
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>97ba8025-97e0-4b73-817a-4eaf87f66742<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
        <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
            },
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
            }
        ],
        <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
        <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
        <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
}</pre></div>
<p>Get a product by id.</p>
<h3><a id="user-content-http-request-72" class="anchor" aria-hidden="true" href="#http-request-72"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/products/{product_id}</code></p>
<h2><a id="user-content-get-a-product-by-barcode" class="anchor" aria-hidden="true" href="#get-a-product-by-barcode"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get a product by barcode</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/absjk/barcode <span class="pl-cce">\ </span>
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>97ba8025-97e0-4b73-817a-4eaf87f66742<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
        <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
            },
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
            }
        ],
        <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
        <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
        <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
}</pre></div>
<p>Get a product by barcode.</p>
<h3><a id="user-content-http-request-73" class="anchor" aria-hidden="true" href="#http-request-73"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/products/{barcode}/barcode</code></p>
<h2><a id="user-content-product-favorite" class="anchor" aria-hidden="true" href="#product-favorite"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Product Favorite</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/97ba8025-97e0-4b73-817a-4eaf87f66742/favorite <span class="pl-cce">\ </span>
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>97ba8025-97e0-4b73-817a-4eaf87f66742<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
        <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
            },
            {
                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                },
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
            }
        ],
        <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
        <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
        <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
        <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
    },
    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
}</pre></div>
<p>Favorite Product.</p>
<h3><a id="user-content-http-request-74" class="anchor" aria-hidden="true" href="#http-request-74"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/products/{product_id}/favorite</code></p>
<h2><a id="user-content-list-products" class="anchor" aria-hidden="true" href="#list-products"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List products</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>97ba8025-97e0-4b73-817a-4eaf87f66742<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
            <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
                    },
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
                    }
                ],
                <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
            <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>a0c2220e-6d7c-4201-9d19-7ab18af59dce<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>combo 1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>example of combo prod<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://..<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>combo<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
            <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
            <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
            <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
                    }
                ],
                <span class="pl-s"><span class="pl-pds">"</span>choices<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>choice 1<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>options<span class="pl-pds">"</span></span>: [
                            {
                                <span class="pl-s"><span class="pl-pds">"</span>single_product_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>single_product<span class="pl-pds">"</span></span>: {
                                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ddssss<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>mels<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                                        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
                                    },
                                    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://....<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                                        <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                                            {
                                                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                                                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                                                },
                                                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
                                            }
                                        ],
                                        <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk426252<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
                                    },
                                    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
                                }
                            }
                        ]
                    }
                ]
            }
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>b60b8977-a1f8-4dfc-91dc-1a7a83a41eb9<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>elektronika2<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>variasi elektronika2<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://...<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>variation<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
            <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
            <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>single_product_ids<span class="pl-pds">"</span></span>: [
                    <span class="pl-s"><span class="pl-pds">"</span>97ba8025-97e0-4b73-817a-4eaf87f66742<span class="pl-pds">"</span></span>,
                    <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>
                ],
                <span class="pl-s"><span class="pl-pds">"</span>single_products<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>97ba8025-97e0-4b73-817a-4eaf87f66742<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                        <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                        <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                                {
                                    <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                                    },
                                    <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
                                },
                                {
                                    <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                                    },
                                    <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
                                }
                            ],
                            <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
                        <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
                    },
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ddssss<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>mels<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://....<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                        <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                        <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                                {
                                    <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                                    },
                                    <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
                                }
                            ],
                            <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk426252<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
                        <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
                    }
                ]
            },
            <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ddssss<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>mels<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://....<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
            <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
                    }
                ],
                <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk426252<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
            <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
        }
    ]
}</pre></div>
<p>List of products.</p>
<h3><a id="user-content-http-request-75" class="anchor" aria-hidden="true" href="#http-request-75"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/products?limit=10</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products?limit=10&amp;starting_after=273fcff8-aa42-4065-86cf-d05478f31ac1</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products?limit=10&amp;ending_before=273fcff8-aa42-4065-86cf-d05478f31ac1</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products?limit=10?product_name=kipas</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products?limit=10&amp;product_category=9957969d-4b99-4c0b-a7cd-8d885fe7a4db</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products?limit=10&amp;product_category=9957969d-4b99-4c0b-a7cd-8d885fe7a4db&amp;starting_after=273fcff8-aa42-4065-86cf-d05478f31ac1</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products?limit=10&amp;product_category=9957969d-4b99-4c0b-a7cd-8d885fe7a4db&amp;ending_before=273fcff8-aa42-4065-86cf-d05478f31ac1</code></p>
<h2><a id="user-content-list-products-for-combo" class="anchor" aria-hidden="true" href="#list-products-for-combo"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List products for combo</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/combo \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>97ba8025-97e0-4b73-817a-4eaf87f66742<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>kipas angin<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ini kipas angin<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>shjshajhajha<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>
                    },
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>
                    }
                ],
                <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
            <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>a0c2220e-6d7c-4201-9d19-7ab18af59dce<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>combo 1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>example of combo prod<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://..<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>combo<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
            <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
            <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
            <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>45d51b4a-8e39-45e7-b620-38b2c0dba3f3<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine in<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
                    }
                ],
                <span class="pl-s"><span class="pl-pds">"</span>choices<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>choice 1<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>options<span class="pl-pds">"</span></span>: [
                            {
                                <span class="pl-s"><span class="pl-pds">"</span>single_product_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                                <span class="pl-s"><span class="pl-pds">"</span>single_product<span class="pl-pds">"</span></span>: {
                                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ddssss<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>mels<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                                        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
                                    },
                                    <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://....<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                                        <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                                            {
                                                <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                                <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                                                    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                                                    <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                                                    <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                                                    <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                                                },
                                                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
                                            }
                                        ],
                                        <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk426252<span class="pl-pds">"</span></span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                                        <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
                                    },
                                    <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
                                    <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
                                }
                            }
                        ]
                    }
                ]
            }
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>273fcff8-aa42-4065-86cf-d05478f31ac1<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ddssss<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>mels<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>9957969d-4b99-4c0b-a7cd-8d885fe7a4db<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>category<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Peralatan elektronika<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://....<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>single<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
            <span class="pl-s"><span class="pl-pds">"</span>favorite<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
            <span class="pl-s"><span class="pl-pds">"</span>single_data<span class="pl-pds">"</span></span>: {
                <span class="pl-s"><span class="pl-pds">"</span>combo_only<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">11</span>,
                <span class="pl-s"><span class="pl-pds">"</span>pricing<span class="pl-pds">"</span></span>: [
                    {
                        <span class="pl-s"><span class="pl-pds">"</span>service_type_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                        <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: {
                            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>42125ac2-2a97-4caf-a53c-f86f5928f117<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>grabfood<span class="pl-pds">"</span></span>,
                            <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
                            <span class="pl-s"><span class="pl-pds">"</span>with_service_charge<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
                        },
                        <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">12</span>
                    }
                ],
                <span class="pl-s"><span class="pl-pds">"</span>unit_cost<span class="pl-pds">"</span></span>: <span class="pl-c1">10</span>,
                <span class="pl-s"><span class="pl-pds">"</span>weight<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
                <span class="pl-s"><span class="pl-pds">"</span>barcode<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>absjk426252<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>track_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>,
                <span class="pl-s"><span class="pl-pds">"</span>stock<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
                <span class="pl-s"><span class="pl-pds">"</span>min_stock<span class="pl-pds">"</span></span>: <span class="pl-c1">1000</span>
            },
            <span class="pl-s"><span class="pl-pds">"</span>variation_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
            <span class="pl-s"><span class="pl-pds">"</span>combo_data<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
        }
    ]
}</pre></div>
<p>List of products for combo.</p>
<h3><a id="user-content-http-request-76" class="anchor" aria-hidden="true" href="#http-request-76"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/products/combo?limit=10</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products/combo?limit=10&amp;starting_after=273fcff8-aa42-4065-86cf-d05478f31ac1</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products/combo?limit=10&amp;ending_before=273fcff8-aa42-4065-86cf-d05478f31ac1</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products/combo?limit=10?product_name=kipas</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products/combo?limit=10&amp;product_category=9957969d-4b99-4c0b-a7cd-8d885fe7a4db</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products/combo?limit=10&amp;product_category=9957969d-4b99-4c0b-a7cd-8d885fe7a4db&amp;starting_after=273fcff8-aa42-4065-86cf-d05478f31ac1</code></p>
<p><code>GET https://staging.sellfazz.com/api/v2/products/combo?limit=10&amp;product_category=9957969d-4b99-4c0b-a7cd-8d885fe7a4db&amp;ending_before=273fcff8-aa42-4065-86cf-d05478f31ac1</code></p>
<h2><a id="user-content-delete-a-product" class="anchor" aria-hidden="true" href="#delete-a-product"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete a product</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products/273fcff8-aa42-4065-86cf-d05478f31ac1 \
  -X DELETE
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete a product.</p>
<h3><a id="user-content-http-request-77" class="anchor" aria-hidden="true" href="#http-request-77"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/products/{product_id}</code></p>
<h2><a id="user-content-delete-all-product" class="anchor" aria-hidden="true" href="#delete-all-product"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete all product</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/products \
  -X DELETE
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete all product.</p>
<h3><a id="user-content-http-request-78" class="anchor" aria-hidden="true" href="#http-request-78"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/products</code></p>
<h1><a id="user-content-orders" class="anchor" aria-hidden="true" href="#orders"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Orders</h1>
<h2><a id="user-content-list-orders" class="anchor" aria-hidden="true" href="#list-orders"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List orders</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/orders \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>
  
curl https://staging.sellfazz.com/api/v2/orders<span class="pl-k">?</span>outlet_id=1<span class="pl-k">&amp;</span>query=aaa<span class="pl-k">&amp;</span>order_no=111<span class="pl-k">&amp;</span>starting_after=1 \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span>
  
curl https://staging.sellfazz.com/api/v2/orders<span class="pl-k">?</span>from_date=2019-10-01T11%3A57%3A30.23925%2B07%3A00<span class="pl-cce">\&amp;</span>to_date=2019-11-01T11%3A57%3A30.23925%2B07%3A00<span class="pl-k">&amp;</span>ending_before=4<span class="pl-k">&amp;</span>limit=10 \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dfe941a7-893a-492b-9531-90902afa0a7c<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>outlet_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>11<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>outlet_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Toko Budi<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>employee_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Employee 1<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>employee_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>54321<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>customer_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>12345<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>employee_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Employee XX<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>customer_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Customer XX<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>customer_phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0812345689111<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>customer_email<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>order_no<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ORD00000<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>order_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>status<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>paid<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>order_items<span class="pl-pds">"</span></span>: [
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>123<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>product_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Product X<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>product_picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>quantity<span class="pl-pds">"</span></span>: <span class="pl-c1">1</span>,
          <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10000</span>,
          <span class="pl-s"><span class="pl-pds">"</span>product_unit_cost<span class="pl-pds">"</span></span> : <span class="pl-c1">5000</span>,
          <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine_in<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>discounts<span class="pl-pds">"</span></span>: [
              {
                <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span> : <span class="pl-c1">10</span>,
                <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span> : <span class="pl-c1">0</span>
              },
              <span class="pl-ii">...</span> 
          ],
          <span class="pl-s"><span class="pl-pds">"</span>combo_items<span class="pl-pds">"</span></span>: [
              {
                <span class="pl-s"><span class="pl-pds">"</span>product_name<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>Product XX<span class="pl-pds">"</span></span>,
                <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>
              },
              <span class="pl-ii">...</span>
          ],
          <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
        }
      ],
      <span class="pl-s"><span class="pl-pds">"</span>payment<span class="pl-pds">"</span></span>: {
        <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>11<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>payment_method<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>cash<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">10000</span>,
        <span class="pl-s"><span class="pl-pds">"</span>discounts<span class="pl-pds">"</span></span>: [
            {
             <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span> : <span class="pl-c1">0</span>,
             <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span> : <span class="pl-c1">5000</span>
            },
            <span class="pl-ii">...</span> 
        ],
        <span class="pl-s"><span class="pl-pds">"</span>extra_charges<span class="pl-pds">"</span></span>: [
            {
              <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>pajak<span class="pl-pds">"</span></span>,
              <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span> : <span class="pl-c1">5000</span>,
              <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span> : <span class="pl-c1">0</span>
            }
        ],
        <span class="pl-s"><span class="pl-pds">"</span>due_date<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
        <span class="pl-s"><span class="pl-pds">"</span>initial_payment<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>order_repayments<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
      },
      <span class="pl-s"><span class="pl-pds">"</span>metadata<span class="pl-pds">"</span></span>: {},
      <span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>
    }
  ]
}</pre></div>
<p>List of orders. Default limit 20. Max limit 100.</p>
<h3><a id="user-content-http-request-79" class="anchor" aria-hidden="true" href="#http-request-79"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/orders</code></p>
<h2><a id="user-content-get-an-order" class="anchor" aria-hidden="true" href="#get-an-order"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get an order</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/orders/dfe941a7-893a-492b-9531-90902afa0a7c \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dfe941a7-893a-492b-9531-90902afa0a7c<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>outlet_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>11<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>outlet_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Toko Budi<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>employee_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Employee 1<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>employee_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>54321<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>customer_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>12345<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>employee_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Employee XX<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>customer_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Customer XX<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>customer_phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0812345689111<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>customer_email<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>order_no<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ORD00000<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>order_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>status<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>paid<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>order_items<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>123<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>product_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Product X<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>product_picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>quantity<span class="pl-pds">"</span></span>: <span class="pl-c1">1</span>,
      <span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">10000</span>,
      <span class="pl-s"><span class="pl-pds">"</span>product_unit_cost<span class="pl-pds">"</span></span> : <span class="pl-c1">5000</span>,
      <span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine_in<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>discounts<span class="pl-pds">"</span></span>: [
        {
          <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span> : <span class="pl-c1">10</span>,
          <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span> : <span class="pl-c1">0</span>
        },
        <span class="pl-ii">...</span> 
      ],
      <span class="pl-s"><span class="pl-pds">"</span>combo_items<span class="pl-pds">"</span></span>: [
        {
          <span class="pl-s"><span class="pl-pds">"</span>product_name<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>Product XX<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>
        },
        <span class="pl-ii">...</span>
      ],
    <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
    }
  ],
  <span class="pl-s"><span class="pl-pds">"</span>payment<span class="pl-pds">"</span></span>: {
    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>11<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>payment_method<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>cash<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">10000</span>,
    <span class="pl-s"><span class="pl-pds">"</span>discounts<span class="pl-pds">"</span></span>: [
      {
        <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span> : <span class="pl-c1">0</span>,
        <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span> : <span class="pl-c1">5000</span>
      },
      <span class="pl-ii">...</span> 
    ],
      <span class="pl-s"><span class="pl-pds">"</span>extra_charges<span class="pl-pds">"</span></span>: [
      {
        <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>pajak<span class="pl-pds">"</span></span>,
        <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span> : <span class="pl-c1">5000</span>,
        <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span> : <span class="pl-c1">0</span>
      }
    ],
    <span class="pl-s"><span class="pl-pds">"</span>due_date<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>,
    <span class="pl-s"><span class="pl-pds">"</span>initial_payment<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
    <span class="pl-s"><span class="pl-pds">"</span>order_repayments<span class="pl-pds">"</span></span>: <span class="pl-c1">null</span>
  },
  <span class="pl-s"><span class="pl-pds">"</span>metadata<span class="pl-pds">"</span></span>: {},
  <span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0001-01-01T00:00:00Z<span class="pl-pds">"</span></span>
}</pre></div>
<p>Get an order.</p>
<h3><a id="user-content-http-request-80" class="anchor" aria-hidden="true" href="#http-request-80"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/orders/{order_id}</code></p>
<h2><a id="user-content-create-an-order" class="anchor" aria-hidden="true" href="#create-an-order"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create an order</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/orders \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "id": "b1c3ad3f-b840-40d3-8d18-ccef95822477",</span>
<span class="pl-s">    "outlet_id": "11",</span>
<span class="pl-s">    "outlet_name": "Toko Budi",</span>
<span class="pl-s">    "employee_name": "Employee 1",</span>
<span class="pl-s">    "employee_id": "54321",</span>
<span class="pl-s">    "customer_id": "12345",</span>
<span class="pl-s">    "employee_name": "Employee 1",</span>
<span class="pl-s">    "customer_name": "Customer 1",</span>
<span class="pl-s">    "customer_phone": "08123456789",</span>
<span class="pl-s">    "customer_email": "customer1@example.com",</span>
<span class="pl-s">    "order_no": "ABCD1234",</span>
<span class="pl-s">    "order_name": "Table 1",</span>
<span class="pl-s">    "status": "paid",</span>
<span class="pl-s">    "notes": "", </span>
<span class="pl-s">    "order_items": [{</span>
<span class="pl-s">      "id" : "123",</span>
<span class="pl-s">      "product_name": "Product X",</span>
<span class="pl-s">      "product_picture_url": "",</span>
<span class="pl-s">      "quantity": 1,</span>
<span class="pl-s">      "price": 100000,</span>
<span class="pl-s">      "product_unit_cost" : 5000,</span>
<span class="pl-s">      "discounts": [</span>
<span class="pl-s">        {</span>
<span class="pl-s">          "percentage" : 10,</span>
<span class="pl-s">          "amount" : 0</span>
<span class="pl-s">        },</span>
<span class="pl-s">        ... </span>
<span class="pl-s">      ],</span>
<span class="pl-s">      "combo_items": [</span>
<span class="pl-s">        {</span>
<span class="pl-s">          "product_name" : "Product XX",</span>
<span class="pl-s">          "notes" : "notes"</span>
<span class="pl-s">        },</span>
<span class="pl-s">        ...</span>
<span class="pl-s">      ],      </span>
<span class="pl-s">      "notes": ""</span>
<span class="pl-s">    }],</span>
<span class="pl-s">    "payment_id" : "11",</span>
<span class="pl-s">    "payment_method": "cash",</span>
<span class="pl-s">    "payment_discounts": [</span>
<span class="pl-s">      {</span>
<span class="pl-s">        "percentage" : 0,</span>
<span class="pl-s">        "amount" : 5000</span>
<span class="pl-s">      },</span>
<span class="pl-s">      ... </span>
<span class="pl-s">    ],</span>
<span class="pl-s">    "payment_extra_charges": [</span>
<span class="pl-s">      { </span>
<span class="pl-s">        "name" : "pajak",</span>
<span class="pl-s">        "amount" : 5000,</span>
<span class="pl-s">        "percentage" : 0</span>
<span class="pl-s">      }</span>
<span class="pl-s">    ],</span>
<span class="pl-s">    "payment_notes": "",</span>
<span class="pl-s">    "payment_amount": 100000,</span>
<span class="pl-s">    "initiat_payment": 0,</span>
<span class="pl-s">    "metadata": {},</span>
<span class="pl-s">    "created_at": "2019-12-01T00:00:00Z"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
	<span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>b1c3ad3f-b840-40d3-8d18-ccef95822477<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>outlet_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>11<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>outlet_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Toko Budi<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>employee_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Employee 1<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>employee_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>54321<span class="pl-pds">"</span></span>,
    <span class="pl-s"><span class="pl-pds">"</span>customer_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>12345<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>employee_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Employee 1<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>customer_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Customer 1<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>customer_phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>08123456789<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>customer_email<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>customer1@example.com<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>order_no<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ABCD1234<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>order_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Table 1<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>status<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>paid<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,	
	<span class="pl-s"><span class="pl-pds">"</span>order_items<span class="pl-pds">"</span></span>: [{
	    <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>123<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>product_name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Product X<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>product_picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>quantity<span class="pl-pds">"</span></span>: <span class="pl-c1">1</span>,
		<span class="pl-s"><span class="pl-pds">"</span>price<span class="pl-pds">"</span></span>: <span class="pl-c1">100000</span>,
        <span class="pl-s"><span class="pl-pds">"</span>product_unit_cost<span class="pl-pds">"</span></span> : <span class="pl-c1">5000</span>,
		<span class="pl-s"><span class="pl-pds">"</span>service_type<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>dine_in<span class="pl-pds">"</span></span>,
		<span class="pl-s"><span class="pl-pds">"</span>discounts<span class="pl-pds">"</span></span>: [
          {
            <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span> : <span class="pl-c1">10</span>,
            <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span> : <span class="pl-c1">0</span>
          },
          <span class="pl-ii">...</span> 
        ],
        <span class="pl-s"><span class="pl-pds">"</span>combo_items<span class="pl-pds">"</span></span>: [
          {
            <span class="pl-s"><span class="pl-pds">"</span>product_name<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>Product XX<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>
          },
          <span class="pl-ii">...</span>
        ],		
		<span class="pl-s"><span class="pl-pds">"</span>notes<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>
	}],
	<span class="pl-s"><span class="pl-pds">"</span>payment<span class="pl-pds">"</span></span> : {
	  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>11<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>payment_method<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>cash<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>payment_discounts<span class="pl-pds">"</span></span>: [
        {
          <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span> : <span class="pl-c1">0</span>,
          <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span> : <span class="pl-c1">5000</span>
        }
      ],
      <span class="pl-s"><span class="pl-pds">"</span>payment_extra_charges<span class="pl-pds">"</span></span>: [
        { 
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span> : <span class="pl-s"><span class="pl-pds">"</span>pajak<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span> : <span class="pl-c1">5000</span>,
          <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span> : <span class="pl-c1">0</span>
        }
      ],
      <span class="pl-s"><span class="pl-pds">"</span>payment_notes<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>payment_amount<span class="pl-pds">"</span></span>: <span class="pl-c1">100000</span>,
      <span class="pl-s"><span class="pl-pds">"</span>initiat_payment<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
      <span class="pl-s"><span class="pl-pds">"</span>order_repayment<span class="pl-pds">"</span></span> : []
	},
	<span class="pl-s"><span class="pl-pds">"</span>metadata<span class="pl-pds">"</span></span>: {},
	<span class="pl-s"><span class="pl-pds">"</span>created_at<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2019-12-01T00:00:00Z<span class="pl-pds">"</span></span>
}</pre></div>
<p>Create an order.</p>
<h3><a id="user-content-http-request-81" class="anchor" aria-hidden="true" href="#http-request-81"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/orders</code></p>
<h1><a id="user-content-customers" class="anchor" aria-hidden="true" href="#customers"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Customers</h1>
<h2><a id="user-content-list-customers" class="anchor" aria-hidden="true" href="#list-customers"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List customers</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/customers \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>area_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Customer 1<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0812345678999<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>email<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>customer1@example.com<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
      <span class="pl-s"><span class="pl-pds">"</span>address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Jalan Kuningan Barat No. 78999<span class="pl-pds">"</span></span>
    },
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>278bf81b-b100-40d1-b9f7-4c8eee772c2c<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>area_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ABC<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0812345666666<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://example.com/example.jpg<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>email<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>abc@example.com<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
      <span class="pl-s"><span class="pl-pds">"</span>address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Jalan Kuningan Timur No. 78999<span class="pl-pds">"</span></span>
    }
  ]
}</pre></div>
<p>List of customers. Default limit 200.</p>
<h3><a id="user-content-http-request-82" class="anchor" aria-hidden="true" href="#http-request-82"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/customers</code></p>
<h2><a id="user-content-get-a-customer" class="anchor" aria-hidden="true" href="#get-a-customer"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get a customer</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/customers/278bf81b-b100-40d1-b9f7-4c8eee772c2c \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>278bf81b-b100-40d1-b9f7-4c8eee772c2c<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>area_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ABC<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0812345666666<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://example.com/example.jpg<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>email<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>abc@example.com<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
  <span class="pl-s"><span class="pl-pds">"</span>address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Jalan Kuningan Barat No. 78999<span class="pl-pds">"</span></span>
}</pre></div>
<p>Get customer by id.</p>
<h3><a id="user-content-http-request-83" class="anchor" aria-hidden="true" href="#http-request-83"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/customers/{customer_id}</code></p>
<h2><a id="user-content-create-a-customer" class="anchor" aria-hidden="true" href="#create-a-customer"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a customer</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/customers \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "area_id": "1",</span>
<span class="pl-s">    "name": "XYZ",</span>
<span class="pl-s">    "phone": "0812345666666",</span>
<span class="pl-s">    "picture_url": "http://example.com/example.jpg",</span>
<span class="pl-s">    "email": "",</span>
<span class="pl-s">    "address": "Jalan Kuningan Barat No. 78999"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>area_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>XYZ<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0812345666666<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://example.com/example.jpg<span class="pl-pds">"</span></span>,
	<span class="pl-s"><span class="pl-pds">"</span>email<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span><span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Jalan Kuningan Barat No. 78999<span class="pl-pds">"</span></span>
}</pre></div>
<p>Create a customer.</p>
<h3><a id="user-content-http-request-84" class="anchor" aria-hidden="true" href="#http-request-84"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/customers</code></p>
<h2><a id="user-content-update-a-customer" class="anchor" aria-hidden="true" href="#update-a-customer"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update a customer</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/customers \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "area_id": "100",</span>
<span class="pl-s">    "name": "ABC",</span>
<span class="pl-s">    "phone": "0812345666666",</span>
<span class="pl-s">    "picture_url": "http://example.com/example.jpg",</span>
<span class="pl-s">    "email": "abc@example.com",</span>
<span class="pl-s">    "address": "Jalan Kuningan Timur No. 78999"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>278bf81b-b100-40d1-b9f7-4c8eee772c2c<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>area_id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>100<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ABC<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>phone<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>0812345666666<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>picture_url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>http://example.com/example.jpg<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>email<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>abc@example.com<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>is_default<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>,
  <span class="pl-s"><span class="pl-pds">"</span>address<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Jalan Kuningan Timur No. 78999<span class="pl-pds">"</span></span>
}</pre></div>
<p>Update a customer.</p>
<h3><a id="user-content-http-request-85" class="anchor" aria-hidden="true" href="#http-request-85"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/customers/{customer_id}</code></p>
<h2><a id="user-content-delete-a-customer" class="anchor" aria-hidden="true" href="#delete-a-customer"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete a customer</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/customers/278bf81b-b100-40d1-b9f7-4c8eee772c2c \
  -X DELETE \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete a customer.</p>
<h3><a id="user-content-http-request-86" class="anchor" aria-hidden="true" href="#http-request-86"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/customers/{customer_id}</code></p>
<h1><a id="user-content-discounts" class="anchor" aria-hidden="true" href="#discounts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Discounts</h1>
<h2><a id="user-content-list-discounts" class="anchor" aria-hidden="true" href="#list-discounts"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List discounts</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/discounts \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>1<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>label<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>DISKON10<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
      <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">10000</span>,
      <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Diskon 10 ribu<span class="pl-pds">"</span></span>
    },
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>label<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>DISKON20<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
      <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">20000</span>,
      <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Diskon 20 ribu<span class="pl-pds">"</span></span>
    },
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>243cf21c-4976-427f-99e2-e2c721dc5d3a<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>label<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>MANTAP<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
      <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
      <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>discount all items 100%<span class="pl-pds">"</span></span>
    }
  ]
}</pre></div>
<p>List of discounts. Default limit is 200.</p>
<h3><a id="user-content-http-request-87" class="anchor" aria-hidden="true" href="#http-request-87"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/discounts</code></p>
<h2><a id="user-content-get-a-discount" class="anchor" aria-hidden="true" href="#get-a-discount"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get a discount</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/discounts/243cf21c-4976-427f-99e2-e2c721dc5d3a \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>243cf21c-4976-427f-99e2-e2c721dc5d3a<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>label<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>MANTAP<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>discount all items 100%<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
  <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>
}</pre></div>
<p>Get discount by id.</p>
<h3><a id="user-content-http-request-88" class="anchor" aria-hidden="true" href="#http-request-88"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/discounts/{discount_id}</code></p>
<h2><a id="user-content-create-a-discount" class="anchor" aria-hidden="true" href="#create-a-discount"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Create a discount</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/discounts \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "label": "Discount100",</span>
<span class="pl-s">    "description": "discount all items 100%",</span>
<span class="pl-s">    "percentage": 100,</span>
<span class="pl-s">    "amount": 0</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>243cf21c-4976-427f-99e2-e2c721dc5d3a<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>label<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Discount100<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>discount all items 100%<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
  <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>
}</pre></div>
<p>Create a discount.</p>
<h3><a id="user-content-http-request-89" class="anchor" aria-hidden="true" href="#http-request-89"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/discounts</code></p>
<h2><a id="user-content-update-a-discount" class="anchor" aria-hidden="true" href="#update-a-discount"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update a discount</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/discounts/243cf21c-4976-427f-99e2-e2c721dc5d3a \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "label": "MANTAP",</span>
<span class="pl-s">    "description": "discount all items 100%",</span>
<span class="pl-s">    "percentage": 100,</span>
<span class="pl-s">    "amount": 0</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>243cf21c-4976-427f-99e2-e2c721dc5d3a<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>label<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>MANTAP<span class="pl-pds">"</span></span>,
  <span class="pl-s"><span class="pl-pds">"</span>percentage<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
  <span class="pl-s"><span class="pl-pds">"</span>amount<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
  <span class="pl-s"><span class="pl-pds">"</span>description<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>discount all items 100%<span class="pl-pds">"</span></span>
}</pre></div>
<p>Update a discount.</p>
<h3><a id="user-content-http-request-90" class="anchor" aria-hidden="true" href="#http-request-90"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/discounts/{discount_id}</code></p>
<h2><a id="user-content-delete-a-discount" class="anchor" aria-hidden="true" href="#delete-a-discount"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Delete a discount</h2>
<blockquote>
<p>Example request&gt;</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/discounts/243cf21c-4976-427f-99e2-e2c721dc5d3a \
  -X DELETE \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Delete a discount.</p>
<h3><a id="user-content-http-request-91" class="anchor" aria-hidden="true" href="#http-request-91"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>DELETE https://staging.sellfazz.com/api/v2/discounts/{discount_id}</code></p>
<h1><a id="user-content-payment-methods" class="anchor" aria-hidden="true" href="#payment-methods"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Payment Methods</h1>
<h2><a id="user-content-list-payment-methods" class="anchor" aria-hidden="true" href="#list-payment-methods"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>List payment methods</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/payment-methods \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>4923e736-cfe1-4348-9633-35fab310631a<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>E-Wallet<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>options<span class="pl-pds">"</span></span>: [
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>49bef999-a0b6-46cb-afdd-826fb4358d80<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>OVO<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>31810f95-2f06-424f-90a1-bf7c7a0e185a<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>DANA<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>740859bd-bff5-45b0-b1cd-cef36850c6ef<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>GOPAY<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>f62fb548-1550-4d3b-9c8a-230ef5d8c257<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>LINK AJA<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ca5f180b-9927-4d63-98d3-0f1729c6d724<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Lainnya<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        }
      ]
    },
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ee5c9b37-bc4a-4f95-8f2b-9ad4330125b1<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Kartu<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>options<span class="pl-pds">"</span></span>: [
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2a012a0d-6f3b-4985-8358-cc40ea4ff4e2<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>MANDIRI<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>a6fb43d1-c9f1-427b-99d9-1a394c43b5e5<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BCA<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>e3b16912-ba10-42ec-a3a3-09d31511053c<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BNI<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>c0c85961-abe3-4868-a012-d558d0119984<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BRI<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>614e9a20-4d41-4412-ba3f-f559f5bbfb46<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Lainnya<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        }
      ]
    }
  ]
}</pre></div>
<p>List user's payment methods.</p>
<h3><a id="user-content-http-request-92" class="anchor" aria-hidden="true" href="#http-request-92"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/payment-methods</code></p>
<h2><a id="user-content-batch-update-payment-methods" class="anchor" aria-hidden="true" href="#batch-update-payment-methods"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Batch update payment methods</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/payment-methods/batch-update
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "data": [</span>
<span class="pl-s">      {</span>
<span class="pl-s">        "id": "4923e736-cfe1-4348-9633-35fab310631a",</span>
<span class="pl-s">        "options": [</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "id": "49bef999-a0b6-46cb-afdd-826fb4358d80",</span>
<span class="pl-s">            "is_active": true</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "id": "740859bd-bff5-45b0-b1cd-cef36850c6ef",</span>
<span class="pl-s">            "is_active": true</span>
<span class="pl-s">          }</span>
<span class="pl-s">        ]</span>
<span class="pl-s">      },</span>
<span class="pl-s">      {</span>
<span class="pl-s">        "id": "ee5c9b37-bc4a-4f95-8f2b-9ad4330125b1",</span>
<span class="pl-s">        "options": [</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "id": "2a012a0d-6f3b-4985-8358-cc40ea4ff4e2",</span>
<span class="pl-s">            "is_active": true</span>
<span class="pl-s">          },</span>
<span class="pl-s">          {</span>
<span class="pl-s">            "id": "614e9a20-4d41-4412-ba3f-f559f5bbfb46",</span>
<span class="pl-s">            "is_active": true</span>
<span class="pl-s">          }</span>
<span class="pl-s">        ]</span>
<span class="pl-s">      }</span>
<span class="pl-s">    ]</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
  <span class="pl-s"><span class="pl-pds">"</span>data<span class="pl-pds">"</span></span>: [
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>4923e736-cfe1-4348-9633-35fab310631a<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>E-Wallet<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>options<span class="pl-pds">"</span></span>: [
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>49bef999-a0b6-46cb-afdd-826fb4358d80<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>OVO<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>31810f95-2f06-424f-90a1-bf7c7a0e185a<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>DANA<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>740859bd-bff5-45b0-b1cd-cef36850c6ef<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>GOPAY<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>f62fb548-1550-4d3b-9c8a-230ef5d8c257<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>LINK AJA<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ca5f180b-9927-4d63-98d3-0f1729c6d724<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Lainnya<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        }
      ]
    },
    {
      <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>ee5c9b37-bc4a-4f95-8f2b-9ad4330125b1<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Kartu<span class="pl-pds">"</span></span>,
      <span class="pl-s"><span class="pl-pds">"</span>options<span class="pl-pds">"</span></span>: [
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>2a012a0d-6f3b-4985-8358-cc40ea4ff4e2<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>MANDIRI<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>a6fb43d1-c9f1-427b-99d9-1a394c43b5e5<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BCA<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>e3b16912-ba10-42ec-a3a3-09d31511053c<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BNI<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>c0c85961-abe3-4868-a012-d558d0119984<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>BRI<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
          <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>614e9a20-4d41-4412-ba3f-f559f5bbfb46<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Lainnya<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>image<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>https://img.icons8.com/dusk/128/000000/money.png<span class="pl-pds">"</span></span>,
          <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        }
      ]
    }
  ]
}</pre></div>
<p>Batch update user's payment methods.</p>
<h3><a id="user-content-http-request-93" class="anchor" aria-hidden="true" href="#http-request-93"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/payment-methods/batch-update</code></p>
<h1><a id="user-content-charges" class="anchor" aria-hidden="true" href="#charges"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Charges</h1>
<h2><a id="user-content-get-charges" class="anchor" aria-hidden="true" href="#get-charges"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get charges</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/settings/charge \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>charges<span class="pl-pds">"</span></span>: [
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>tax<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Pajak<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>value<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
            <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>service<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Service Charge<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>value<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
            <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        }
    ],
    <span class="pl-s"><span class="pl-pds">"</span>is_extra_charge_included<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
}</pre></div>
<p>get user charges.</p>
<h3><a id="user-content-http-request-94" class="anchor" aria-hidden="true" href="#http-request-94"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>GET https://staging.sellfazz.com/api/v2/settings/charge</code></p>
<h2><a id="user-content-update-charges" class="anchor" aria-hidden="true" href="#update-charges"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Update charges</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/settings/charge
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">	"charge_setting":{</span>
<span class="pl-s">	    "charges": [</span>
<span class="pl-s">	        {</span>
<span class="pl-s">	            "id": "tax",</span>
<span class="pl-s">	            "value": 100,</span>
<span class="pl-s">	            "is_active": true</span>
<span class="pl-s">	        },</span>
<span class="pl-s">	        {</span>
<span class="pl-s">	            "id": "service",</span>
<span class="pl-s">	            "value": 0,</span>
<span class="pl-s">	            "is_active": false</span>
<span class="pl-s">	        }</span>
<span class="pl-s">	    ],</span>
<span class="pl-s">	    "is_extra_charge_included": true</span>
<span class="pl-s">	}</span>
<span class="pl-s">}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Example response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>charges<span class="pl-pds">"</span></span>: [
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>tax<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Pajak<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>value<span class="pl-pds">"</span></span>: <span class="pl-c1">100</span>,
            <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
        },
        {
            <span class="pl-s"><span class="pl-pds">"</span>id<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>service<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>name<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>Service Charge<span class="pl-pds">"</span></span>,
            <span class="pl-s"><span class="pl-pds">"</span>value<span class="pl-pds">"</span></span>: <span class="pl-c1">0</span>,
            <span class="pl-s"><span class="pl-pds">"</span>is_active<span class="pl-pds">"</span></span>: <span class="pl-c1">false</span>
        }
    ],
    <span class="pl-s"><span class="pl-pds">"</span>is_extra_charge_included<span class="pl-pds">"</span></span>: <span class="pl-c1">true</span>
}</pre></div>
<p>Update user's charge setting.</p>
<h3><a id="user-content-http-request-95" class="anchor" aria-hidden="true" href="#http-request-95"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/settings/charge</code></p>
<h1><a id="user-content-reset" class="anchor" aria-hidden="true" href="#reset"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Reset</h1>
<h1><a id="user-content-managements" class="anchor" aria-hidden="true" href="#managements"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Managements</h1>
<h2><a id="user-content-reset-management-data" class="anchor" aria-hidden="true" href="#reset-management-data"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Reset management data</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/reset-managements \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Reset managements data (products, service types, product categories, devices, employees, shift setting, outlets, customers, discounts, order payment methods, order charges)</p>
<h3><a id="user-content-http-request-96" class="anchor" aria-hidden="true" href="#http-request-96"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/reset-managements</code></p>
<h1><a id="user-content-transactions" class="anchor" aria-hidden="true" href="#transactions"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Transactions</h1>
<h2><a id="user-content-reset-transaction-data" class="anchor" aria-hidden="true" href="#reset-transaction-data"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Reset transaction data</h2>
<blockquote>
<p>Example request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/reset-transactions \
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: application/json<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (204 No Content)</p>
</blockquote>
<p>Reset transactions data (orders and shifts)</p>
<h3><a id="user-content-http-request-97" class="anchor" aria-hidden="true" href="#http-request-97"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/reset-transactions</code></p>
<h1><a id="user-content-file" class="anchor" aria-hidden="true" href="#file"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>File</h1>
<h2><a id="user-content-upload" class="anchor" aria-hidden="true" href="#upload"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Upload</h2>
<p>Upload image</p>
<blockquote>
<p>Example Request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/files
  -X POST \
  -H <span class="pl-s"><span class="pl-pds">'</span>Content-Type: multipart/form-data<span class="pl-pds">'</span></span> \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span> \
  -d <span class="pl-s"><span class="pl-pds">'</span>{</span>
<span class="pl-s">    "file": "@/path/to/a/file.jpg"</span>
<span class="pl-s">  }<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response</p>
</blockquote>
<div class="highlight highlight-source-json"><pre>{
    <span class="pl-s"><span class="pl-pds">"</span>url<span class="pl-pds">"</span></span>: <span class="pl-s"><span class="pl-pds">"</span>localhost:8080/v2/files/20191029162810_ccc1ef0051142f7b.jpeg<span class="pl-pds">"</span></span>
}</pre></div>
<h3><a id="user-content-http-request-98" class="anchor" aria-hidden="true" href="#http-request-98"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>HTTP Request</h3>
<p><code>POST https://staging.sellfazz.com/api/v2/files</code></p>
<h2><a id="user-content-get" class="anchor" aria-hidden="true" href="#get"><svg class="octicon octicon-link" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M4 9h1v1H4c-1.5 0-3-1.69-3-3.5S2.55 3 4 3h4c1.45 0 3 1.69 3 3.5 0 1.41-.91 2.72-2 3.25V8.59c.58-.45 1-1.27 1-2.09C10 5.22 8.98 4 8 4H4c-.98 0-2 1.22-2 2.5S3 9 4 9zm9-3h-1v1h1c1 0 2 1.22 2 2.5S13.98 12 13 12H9c-.98 0-2-1.22-2-2.5 0-.83.42-1.64 1-2.09V6.25c-1.09.53-2 1.84-2 3.25C6 11.31 7.55 13 9 13h4c1.45 0 3-1.69 3-3.5S14.5 6 13 6z"></path></svg></a>Get</h2>
<p>Get image</p>
<blockquote>
<p>Example Request</p>
</blockquote>
<div class="highlight highlight-source-shell"><pre>curl https://staging.sellfazz.com/api/v2/files/{filename}/contents \
  -H <span class="pl-s"><span class="pl-pds">'</span>Authorization: Bearer {{accessToken}}<span class="pl-pds">'</span></span></pre></div>
<blockquote>
<p>Response (200 Ok With Image)</p>
</blockquote>
<p><code>GET https://staging.sellfazz.com/api/v2/files/{filename}/contents</code></p>
</article>
  </div>

    </div>

  

  <details class="details-reset details-overlay details-overlay-dark">
    <summary data-hotkey="l" aria-label="Jump to line"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast linejump" aria-label="Jump to line">
      <!-- '"` --><!-- </textarea></xmp> --></option></form><form class="js-jump-to-line-form Box-body d-flex" action="" accept-charset="UTF-8" method="get"><input name="utf8" type="hidden" value="&#x2713;" />
        <input class="form-control flex-auto mr-3 linejump-input js-jump-to-line-field" type="text" placeholder="Jump to line&hellip;" aria-label="Jump to line" autofocus>
        <button type="submit" class="btn" data-close-dialog>Go</button>
</form>    </details-dialog>
  </details>

    <div class="Popover anim-scale-in js-tagsearch-popover"
     hidden
     data-tagsearch-url="/payfazz/sellfazz-backend/find-symbols"
     data-tagsearch-ref="master"
     data-tagsearch-path="docs/API.md"
     data-tagsearch-lang="Markdown"
     data-hydro-click="{&quot;event_type&quot;:&quot;code_navigation.click_on_symbol&quot;,&quot;payload&quot;:{&quot;action&quot;:&quot;click_on_symbol&quot;,&quot;repository_id&quot;:205763991,&quot;ref&quot;:&quot;master&quot;,&quot;language&quot;:&quot;Markdown&quot;,&quot;client_id&quot;:&quot;2039514003.1569814249&quot;,&quot;originating_request_id&quot;:&quot;C5BC:4C67:164C23:1FD0D3:5DCCD619&quot;,&quot;originating_url&quot;:&quot;https://github.com/payfazz/sellfazz-backend/blob/master/docs/API.md&quot;,&quot;referrer&quot;:&quot;https://github.com/payfazz/sellfazz-backend/tree/master/docs&quot;,&quot;user_id&quot;:55684684}}"
     data-hydro-click-hmac="ea6ef097b8d48149d069fd339b564eeffffa9440ea2cedb3c5f9c325c7243f27">
  <div class="Popover-message Popover-message--large Popover-message--top-left TagsearchPopover mt-1 mb-4 mx-auto Box box-shadow-large">
    <div class="TagsearchPopover-content js-tagsearch-popover-content overflow-auto" style="will-change:transform;">
    </div>
  </div>
</div>



  </div>
</div>

    </main>
  </div>
  

  </div>

        
<div class="footer container-lg width-full p-responsive" role="contentinfo">
  <div class="position-relative d-flex flex-row-reverse flex-lg-row flex-wrap flex-lg-nowrap flex-justify-center flex-lg-justify-between pt-6 pb-2 mt-6 f6 text-gray border-top border-gray-light ">
    <ul class="list-style-none d-flex flex-wrap col-12 col-lg-5 flex-justify-center flex-lg-justify-between mb-2 mb-lg-0">
      <li class="mr-3 mr-lg-0">&copy; 2019 <span title="0.49563s from unicorn-c78988749-h8gl2">GitHub</span>, Inc.</li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to terms, text:terms" href="https://github.com/site/terms">Terms</a></li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to privacy, text:privacy" href="https://github.com/site/privacy">Privacy</a></li>
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to security, text:security" href="https://github.com/security">Security</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://githubstatus.com/" data-ga-click="Footer, go to status, text:status">Status</a></li>
        <li><a data-ga-click="Footer, go to help, text:help" href="https://help.github.com">Help</a></li>
    </ul>

    <a aria-label="Homepage" title="GitHub" class="footer-octicon d-none d-lg-block mx-lg-4" href="https://github.com">
      <svg height="24" class="octicon octicon-mark-github" viewBox="0 0 16 16" version="1.1" width="24" aria-hidden="true"><path fill-rule="evenodd" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/></svg>
</a>
   <ul class="list-style-none d-flex flex-wrap col-12 col-lg-5 flex-justify-center flex-lg-justify-between mb-2 mb-lg-0">
        <li class="mr-3 mr-lg-0"><a data-ga-click="Footer, go to contact, text:contact" href="https://github.com/contact">Contact GitHub</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://github.com/pricing" data-ga-click="Footer, go to Pricing, text:Pricing">Pricing</a></li>
      <li class="mr-3 mr-lg-0"><a href="https://developer.github.com" data-ga-click="Footer, go to api, text:api">API</a></li>
      <li class="mr-3 mr-lg-0"><a href="https://training.github.com" data-ga-click="Footer, go to training, text:training">Training</a></li>
        <li class="mr-3 mr-lg-0"><a href="https://github.blog" data-ga-click="Footer, go to blog, text:blog">Blog</a></li>
        <li><a data-ga-click="Footer, go to about, text:about" href="https://github.com/about">About</a></li>

    </ul>
  </div>
  <div class="d-flex flex-justify-center pb-6">
    <span class="f6 text-gray-light"></span>
  </div>
</div>



  <div id="ajax-error-message" class="ajax-error-message flash flash-error">
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.893 1.5c-.183-.31-.52-.5-.887-.5s-.703.19-.886.5L.138 13.499a.98.98 0 000 1.001c.193.31.53.501.886.501h13.964c.367 0 .704-.19.877-.5a1.03 1.03 0 00.01-1.002L8.893 1.5zm.133 11.497H6.987v-2.003h2.039v2.003zm0-3.004H6.987V5.987h2.039v4.006z"/></svg>
    <button type="button" class="flash-close js-ajax-error-dismiss" aria-label="Dismiss error">
      <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
    </button>
    You can’t perform that action at this time.
  </div>


    <script crossorigin="anonymous" integrity="sha512-mRSqIFCwTq2GWoxlcJsfkCaJBbjKYs1nP66S6f2/tCb6Fkkew4DsnmhVETA4NfO6mM64NiwslbrTzmQYkUeRAA==" type="application/javascript" src="https://github.githubassets.com/assets/compat-bootstrap-d6aa8981.js"></script>
    <script crossorigin="anonymous" integrity="sha512-hcybWmnZc/MmTSqQy1XHK+BnCKGf74XHXtSJUqDjQbGCitPaKuZomLtzEnWzud5zyr0Cx5cowKxapak6m711cg==" type="application/javascript" src="https://github.githubassets.com/assets/frameworks-fcbb97e8.js"></script>
    
    <script crossorigin="anonymous" async="async" integrity="sha512-mEhViOqajTVIWIt8vaNeZgWVSKFCUJuydMJcDSsZGeWRk/vg1IodwsjZNLW6zpqHESnkvCRcBkYkF1oGf0uMeQ==" type="application/javascript" src="https://github.githubassets.com/assets/github-bootstrap-f844e701.js"></script>
    
    
    
  <div class="js-stale-session-flash flash flash-warn flash-banner" hidden
    >
    <svg class="octicon octicon-alert" viewBox="0 0 16 16" version="1.1" width="16" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M8.893 1.5c-.183-.31-.52-.5-.887-.5s-.703.19-.886.5L.138 13.499a.98.98 0 000 1.001c.193.31.53.501.886.501h13.964c.367 0 .704-.19.877-.5a1.03 1.03 0 00.01-1.002L8.893 1.5zm.133 11.497H6.987v-2.003h2.039v2.003zm0-3.004H6.987V5.987h2.039v4.006z"/></svg>
    <span class="js-stale-session-flash-signed-in" hidden>You signed in with another tab or window. <a href="">Reload</a> to refresh your session.</span>
    <span class="js-stale-session-flash-signed-out" hidden>You signed out in another tab or window. <a href="">Reload</a> to refresh your session.</span>
  </div>
  <template id="site-details-dialog">
  <details class="details-reset details-overlay details-overlay-dark lh-default text-gray-dark hx_rsm" open>
    <summary role="button" aria-label="Close dialog"></summary>
    <details-dialog class="Box Box--overlay d-flex flex-column anim-fade-in fast hx_rsm-dialog hx_rsm-modal">
      <button class="Box-btn-octicon m-0 btn-octicon position-absolute right-0 top-0" type="button" aria-label="Close dialog" data-close-dialog>
        <svg class="octicon octicon-x" viewBox="0 0 12 16" version="1.1" width="12" height="16" aria-hidden="true"><path fill-rule="evenodd" d="M7.48 8l3.75 3.75-1.48 1.48L6 9.48l-3.75 3.75-1.48-1.48L4.52 8 .77 4.25l1.48-1.48L6 6.52l3.75-3.75 1.48 1.48L7.48 8z"/></svg>
      </button>
      <div class="octocat-spinner my-6 js-details-dialog-spinner"></div>
    </details-dialog>
  </details>
</template>

  <div class="Popover js-hovercard-content position-absolute" style="display: none; outline: none;" tabindex="0">
  <div class="Popover-message Popover-message--bottom-left Popover-message--large Box box-shadow-large" style="width:360px;">
  </div>
</div>

  <div aria-live="polite" class="js-global-screen-reader-notice sr-only"></div>

  </body>
</html>

