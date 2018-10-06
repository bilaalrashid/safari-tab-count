# Safari Tab Count

AppleScript that counts all of the tabs and windows that are open across Safari.

## Setup

Open `SafariTabCount.scpt` with Script Editor or enter the code into an Automator workflow.

## How it works

The script focuses on Safari, counts each tab in each window and then outputs the result in a dialog box.

To use use with Safari Technology Preview, replace `Safari` with `Safari Technology Preview`:
```AppleScript
tell application "Safari Technology Preview"
```

### Customise Dialog Box

`totaltabcount` stores the number of tabs, while `totalwincount` stores the number of windows. These variables are outputted in the dialog box.

Different types are dialog boxes are used depending on the number of tabs that are open. `note` displays the application icon, `caution` displays a yellow warning triagle and `stop` displays a red stop sign.

```AppleScript
if totaltabcount < 75 then
   display dialog "..." with icon note
else if totaltabcount > 74 and totaltabcount < 140 then
   display dialog "..." with icon caution
else
   display dialog "..." with icon stop
end if
```
