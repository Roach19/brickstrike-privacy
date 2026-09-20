# Privacy Policy — Brick Strike

> **Source document, not a published policy.** This is the text the hosted
> privacy policy will be built from. It is not yet published anywhere, and the
> application contains no link to it — see
> [RELEASE_CHECKLIST.md](RELEASE_CHECKLIST.md).
>
> The developer identity and contact address in §11 were supplied by the
> product owner and are filled in. **Still outstanding before publication:** a
> publicly reachable URL for this document, and the `PRIVACY_POLICY_URL`
> configuration that makes the in-app link appear.

**Last updated:** *(set on publication)*
**Russian version:** [PRIVACY_POLICY_RU.md](PRIVACY_POLICY_RU.md)

---

## 1. What this application is

Brick Strike is an Android puzzle game. You place blocks on an 8×8 board and clear
full rows and columns. It is played offline: the game itself never needs a
network connection, and no gameplay feature depends on one.

There is no account, no login, no cloud profile and no game backend. Nothing you
do in the game is associated with an identity you created.

## 2. Data stored on your device

The following is stored locally, on your device only, and is not transmitted by
the application:

| What | Why |
|---|---|
| Best score | Shown on the home screen and during play |
| Sound enabled | Your settings choice |
| Vibration enabled | Your settings choice |
| Selected theme | Your settings choice |
| Selected language | Your settings choice |
| Games played | Aggregate play statistics |
| Total score | Aggregate play statistics |
| Crystals earned and spent | The game's offline currency |
| Skins owned and selected | Which board appearance you bought and wear |
| Arcade stars per level | Which levels you finished and how well |
| Pictures revealed | Your Picture Reveal gallery |
| Advertising data-processing choice | Your privacy choice (see §6) |
| Analytics choice | Your analytics choice (see §3) |

Crystals are an **offline currency earned by playing**. They cannot be bought,
cannot be transferred, have no monetary value, and exist only in this
application on this device. There are no in-app purchases of any kind.

Your unfinished game is deliberately **not** saved. Closing the application
means the game in progress is lost; your best score and statistics are kept.

Uninstalling the application removes this data.

## 3. Analytics

Brick Strike uses **AppMetrica**, an analytics service provided by Yandex, to
understand how the game is used and to receive crash diagnostics.

When analytics is configured, the AppMetrica SDK may collect and transmit:

- application usage events, listed in §4;
- session information and technical application and device information gathered
  automatically by the SDK;
- Java/Kotlin crash diagnostics, which the SDK collects by default;
- install attribution information, where the Play Store or RuStore makes it
  available (see §8).

**You can turn analytics off.** Settings → *Share usage analytics* stops this
application sending events and instructs the AppMetrica SDK to stop sending
what it gathers on its own, including sessions and crash reports. The choice is
stored on your device and takes effect immediately. It is independent of your
advertising choice (§6): you may allow one and refuse the other.

Analytics is on by default. Turning it off never changes how the game plays.

The precise field list the SDK gathers automatically is defined by Yandex, not
by this application, and is not independently enumerated here.

The application configuration deliberately **excludes**:

- the AppMetrica advertising-identifier module;
- the AppMetrica location-collection implementation;

and sets AppMetrica location tracking to off.

This application does not send Yandex a name, an email address, a phone number,
a contact list, photos, files, messages or calendar data, because it never asks
for or holds any of those.

**This policy does not claim the analytics SDK is fully anonymous or that it
collects no device information.** It collects technical and device information
as described above.

## 4. What the game reports

Brick Strike reports gameplay and interface events. These are categories, not a
complete field specification:

- application launch;
- a game started, restarted or finished;
- a piece placed;
- lines cleared;
- a new high score;
- the settings screen opened;
- the interface language changed;
- rewarded advertisement lifecycle (offered, started, completed);
- an interstitial advertisement displayed;
- a game continued after a rewarded advertisement.

These events carry gameplay values such as a score or a piece type. They do not
carry your identity, your location, or the contents of your device.

## 5. Advertising

Brick Strike includes the **Yandex Mobile Ads** SDK.

**Production advertising is not enabled in the current release.** During
development and testing the application uses only Yandex's public demonstration
advertisement units, which serve test creatives and earn nothing.

When production advertising is eventually enabled, it is intended to consist of:

- **Rewarded advertisements** (see §5.1);
- **Interstitial advertisements** (see §5.2).

Advertising involves the advertising network receiving a request and returning a
creative. What Yandex processes as part of serving an advertisement is governed
by Yandex's own terms, not by this application.

### 5.0 Where advertising is not shown

This application **does not serve advertising in the European Economic Area,
Iceland, Liechtenstein, Norway or Switzerland.** Serving personalised
advertising there requires a consent framework that this application does not
implement, so instead of asking for consent it cannot properly record, the
application does not request advertisements at all in those countries.

The region is determined from your mobile network or SIM country. If neither is
available, the application treats the region as unknown and **does not** serve
advertising. No advertising identifier and no location data is used to make this
determination.

### 5.1 Rewarded advertisements

When a game ends, an eligible player **may choose** to watch a rewarded
advertisement to continue that same game once. If the advertisement is actually
watched and the advertising network confirms the reward, 25% of the board's
currently occupied cells are cleared and the same game resumes with its score
intact.

Watching is entirely optional. The game can always be ended or restarted without
watching anything, and declining costs nothing. A player may continue a given
game at most once this way.

### 5.2 Interstitial advertisements

Interstitial advertisements may appear only at natural breaks between games —
after a game has finally ended and you have chosen to play again or to return to
the home screen. They never interrupt play.

The current pacing rules are at most one interstitial after every third
completed game, and never less than three minutes apart. These are product
settings and may be adjusted later based on how the game is actually played;
they are described here as current behaviour, not as a permanent guarantee.

## 6. Your advertising choice

Settings → Privacy lets you allow or decline advertising data processing. Your
choice is stored on your device, can be changed at any time, and does not affect
gameplay in any way.

Until you make an explicit choice, no choice is assumed. Leaving the screen
without choosing is not treated as agreement.

**This choice does not control analytics.** AppMetrica operates independently of
it and has its own separate opt-out: Settings → *Share usage analytics*,
described in §4. The two are independent, so you may allow one and refuse the
other.

This application does **not** implement a certified Consent Management Platform,
writes no IAB TCF values, and makes no claim of TCF, IAB or GDPR compliance.

## 7. Advertising identifier

The Android advertising identifier permission
(`com.google.android.gms.permission.AD_ID`) is **removed from the current
application configuration**, and the application requests no advertising
identifier.

This describes the current configuration. It is not a permanent commitment about
every future version; a version that used an advertising identifier would say so
here first.

### App Set ID

`play-services-appset` and an AppMetrica App Set ID module are present as
dependencies of the bundled SDKs. An App Set ID is a per-developer,
user-resettable identifier; it is **not** an advertising identifier and not the
Android advertising ID.

Brick Strike's own code never requests an App Set ID. Whether the bundled SDKs read one
is determined by their vendors and is not independently verified here.

## 8. Install attribution

The Play Install Referrer library is present as a dependency of the analytics
SDK, and the application's package visibility allows the analytics SDK to see
the Google Play application and the RuStore install-referrer provider.

This can make **install attribution information** — broadly, where an install
came from — available to the SDK stack. It is not precise location data and not
an advertising identifier. Brick Strike's own code does not read it.

## 9. Location

Brick Strike does **not** request the Android precise or approximate location
permissions, and none appear in the application.

In the current technical configuration:

- the AppMetrica location-collection implementation is excluded;
- `play-services-location` is absent;
- AppMetrica location tracking is set to off;
- Yandex Mobile Ads location tracking is set to off.

This means the application does not collect device location.

It does not mean no geographic information of any kind can exist anywhere: any
network service, including the analytics and advertising services above, can
infer coarse information such as a country from the network connection itself.
That is a property of using the internet, not something this application
collects or controls.

## 10. Children

Brick Strike is a general-audience puzzle game. It is not designed for or directed at
young children, and its intended minimum audience is approximately 13 years old.

Age ranges are treated differently in different places, and some jurisdictions
treat people well above 13 as children. Nothing in this section is a legal
determination.

Brick Strike does not knowingly collect information from children. It asks for no age,
no date of birth, and no personal details of any kind.

## 11. Contact

- Developer: Гунин Иван Владимирович
- Privacy contact: bubblegu44@yandex.ru

## 12. Changes to this policy

When this policy changes, the updated version will be published at the same
address and the "last updated" date above will change.

## 13. Third-party services

- **AppMetrica** (Yandex) — analytics and crash diagnostics.
- **Yandex Mobile Ads** (Yandex) — advertising, not enabled in the current
  release.
- **Google Play services** components and the **Play Install Referrer** library,
  present as dependencies of the above.

Each is governed by its provider's own privacy terms.
