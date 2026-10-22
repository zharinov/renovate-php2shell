# Renovate PHP2Shell comparison

Public reproduction for renovatebot/renovate#47283.

The same repository is processed locally with unchanged Renovate and the PHP2Shell preset. Normal PHP upgrade targets, existing groups, merge settings and Docker digest updates should remain unchanged. Qualifying patched-version updates receive a security notice and creation-time exemptions.

The fixtures cover Composer, asdf, mise, four mise lockfile selectors, official PHP Docker tags, `.php-version` and literal `setup-php` inputs. Other cases exercise separate patch/minor updates, existing groups, schedules, limits, opt-out, pinned-version freezes, approval, release age and minimum group size.

The automerge fixture enables automerge but schedules merging only during January 1, 00:00–01:00 UTC. It tests preservation of the setting without permitting a merge during this run. GitHub Actions are disabled. No PHP code, Composer scripts or workflows are executed.

The digest-refresh fixture deliberately uses a synthetic old digest. Renovate obtains the replacement digest from the real Docker registry. This tests the update path, not the contents of an old running image.
