# Overcast to Pages

A web app that syncs your Overcast listening history to automatically create a personal episodes page. It displays all the episodes you've listened to in a clean, searchable interface.

## Setup:

1. [Use this template](https://github.com/new?template_name=overcast-to-pages-template&template_owner=hbmartin)
2. Go to [overcast.fm/account](https://overcast.fm/account), sign in (if needed), and open web inspector (⌘-option-i)
3. Find your login cookie and copy the value for `o`
   1. e.g. in Chrome under `Application` > `Cookies` > `https://overcast.fm`

4. [Add your action repository secret](https://github.com/hbmartin/overcast-to-pages/settings/secrets/actions/new)
   1. Enter Name: `OVERCAST_COOKIE` and Secret: paste the `o` value from step #3
   2. Click the green button `Add secret`

5. Go to [Pages Settings](https://github.com/hbmartin/overcast-to-pages/settings/pages) > `Source` (dropdown) > Choose `GitHub Actions`
6. Start your first [scrape run](https://github.com/hbmartin/overcast-to-pages/actions/workflows/scrape.yml) > `Run workflow` (gray button) > `Run workflow` (popup green button)

After the `scrape` and `pages` workflow runs successfully complete ([watch them here](https://github.com/hbmartin/overcast-to-pages/actions)), your episodes page will be at [https://hbmartin.github.io/overcast-to-pages/](https://hbmartin.github.io/overcast-to-pages/)

Hooray! 🎉 Your episodes page will now continue to update daily.

You can also [interact with your podcast database directly using datasette](https://lite.datasette.io/?install=datasette-mp3-audio&url=https://hbmartin.github.io/overcast-to-pages/overcast.db#/overcast/)

Please report issues or feature requests [here](https://github.com/hbmartin/overcast-to-pages-template/issues)

## Legal

This project is licensed under the [Apache License Version 2.0](LICENSE.txt).

Overcast and the Overcast logo are trademarks of Overcast.fm.

All podcast content is copyright of their respective owners.

## Authors

* [Harold Martin](https://www.linkedin.com/in/harold-martin-98526971/) - harold.martin at gmail
