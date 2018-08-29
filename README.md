# play_games

Use Google Play Games Services on your Flutter app; this allows for signin and achievements so far, but more additions are very welcome. If you like it, give us a star and feel free to help and contribute.

## Part 1: Sign In

Call the sign in method to sign in; you must check if the login was successufully.

```dart
    SigninResult result = await PlayGames.signIn();
    if (result.success) {
      await PlayGames.setPopupOptions();
      this.account = result.account;
    } else {
      this.error = result.message;
    }
    this.loading = false;
```

But don't think it will be that easy! Actually, GPGS signin is quite a hassle to do, but [this](doc/signin.md) tutorial should help you out with this nefarious task.

Reasons for failure will be specified in the error property. Otherwhise, you can access the account property to get the account.

## Part 2: Achievements

You can both award achievements (unlock/increment) and show the Achievements screen in your game.

TODO: tutorial