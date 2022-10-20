# `internet-friends-gotrue-js`

This is a fork of @supabase/gotrue-js

## NOTE: THIS IS NOT SUPPORTED, AND ONLY USED BY US. DO NOT USE THIS PACKAGE UNLESS YOU WORK AT INTERNET FRIENDS, INC

The reason I had to fork was because I had to fix two bugs on v2.0.0 of supabase that were affecting my project:


1) [Requests made when a JWT token expires always fail] (https://github.com/supabase/gotrue-js/issues/487#issuecomment-1277997525)
  - Fix: [#482](https://github.com/supabase/gotrue-js/pull/482). I added this code diff to this repo

2) [Supabase kept logging my users out after they logged in after a couple of days](https://github.com/supabase/supabase/issues/9668) - This one is still unfixed
  - What I'm doing about it: adding sentry logging to try and get closer to the issue and figure out: 
    1) how often it's happening
    2) what the logs look like around it