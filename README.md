# RunParty: privacy policy and invite page

GitHub Pages site of the RunParty app, at https://tulgashdee.github.io/RunParty-privacy/

The app's code lives in `D:\Aaw\RunParty` (github.com/tulgashdee/RunParty).

## Files

- `index.html`: the privacy policy, one page with no scripts.
- `join/index.html`: the invite page. Party and crew QR codes and invite links point here
  (`join/?p=CODE` for a party, `join/?c=CODE` for a crew), because phone cameras open web
  links but not `runparty://` ones. On Android it opens the app with an `intent://` link
  (package `com.tulgashdee.runparty`); elsewhere with `runparty://party/CODE` or
  `runparty://crew/CODE`. It always shows the code, to type in the app if it doesn't open.
  English, Korean and Mongolian, from the phone's language. The address is
  `inviteSite` in the app's `lib/models/invite_links.dart`; change both together.
- `icon.png`, `favicon.png`: the app icon (from `brand/icon-512.png` in the app's repo).

## Publish it (first time)

1. On GitHub, create the public repository `tulgashdee/RunParty-privacy` (empty, no README).
2. In GitHub Desktop: File, Add local repository, this folder
   (`D:\Aaw\RunParty-privacy\RunParty-privacy`), then Publish / Push.
3. On GitHub: the repository's **Settings, Pages, Build and deployment**: Source "Deploy
   from a branch", branch **main**, folder **/ (root)**, Save.
4. After a minute or two, open https://tulgashdee.github.io/RunParty-privacy/join/?p=ABCDEF
   on a phone and check the page shows.

## Changing it

Edit, commit and push; Pages updates by itself. If the app ever sends anything new to the
server or another service, change the policy (and its date) and the Play Data safety answers
before that version ships.
