# Slack Night Mode
A stylesheet for the desktop Slack application. [CC BY-SA 3.0 US](https://creativecommons.org/licenses/by-sa/3.0/us/).

## Usage

Making use of this stylesheet can be achieved in two
steps. Unfortunately you'll need to do both steps each time you open
the desktop app; I currently have no effective way of persisting the
change.

1. [Opening Browser Developer Tools](#opening-developer-tools)
2. Running
```js
$.ajax({
  url: "https://cdn.rawgit.com/matthugs/slack-night-mode/master/css/black.css",
  success: function(css) {
    $("<style></style>").appendTo("head").html(css);
  }
});
```
in the javascript console (which can be brought up with the keystroke
C-`). If you don't execute any other javascript, you can easily replay
this statement later by using the up arrow, since Chromium's console
history is persistent.

### Opening Developer Tools

I've only come across ways of doing this for the Windows and Linux desktop applications, but the OSX version currently eludes me. If anyone has that solution, I would be delighted to see that pull request.

#### Linux

There's an environment variable for that! Launch slack with `SLACK_DEVELOPER_MENU=nonempty slack &`, a change persistable in any number of different ways (e.g. by writing a small shell script).

#### Windows

For reasons that are a complete mystery to me, Windows users at my
place of work have been able to open developer tools by clicking
repeatedly on empty space in the Team selection drawer on the far-left
side of the screen. This drawer is open by default for users who are a
member of multiple teams. I'm not sure if there's an easy was of
opening that drawer for users who are not members of multiple teams.

## Themes

### Supported

#### Black ([source](scss/main.scss) - [build](css/black.css))


The primary supported theme. This is an excellent theme if you use a program like f.lux or redshift.

![Black Screenshot](https://userstyles.org/style_screenshots/117475_after.png)

(Other themes are supported by laCour's version, and these are built and available to be tried out for a spin. I haven't tested them, however, and can make no guarantees about their suitability on the eyes.)

