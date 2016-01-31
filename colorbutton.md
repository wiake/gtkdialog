# colorbutton widget #

A [GtkColorButton](http://developer.gnome.org/gtk2/2.24/GtkColorButton.html)


---


## Definition ##

```
<colorbutton tag_attr="value"...>
	<default>data</default>
	<variable>varname</variable>
	<input>command</input>
	<input file>filename</input>
	<sensitive>state</sensitive>
	<action>activity</action>...
	<action signal="type">activity</action>...
	<action function="type">parameter</action>...
	<output file>filename</output>
</colorbutton>
```

"..." denotes acceptance of multiples of the same thing.

## Tag Attributes ##

See the [GtkColorButton](http://developer.gnome.org/gtk2/2.24/GtkColorButton.html#GtkColorButton.object-hierarchy) widget and ancestor class properties.

The following custom tag attributes are available:

| **Name** | **Description** | **Value** | **Since** |
|:---------|:----------------|:----------|:----------|
| space-expand | Pack widget expanding into space | `true` or `false` |  |
| space-fill | Pack widget filling space | `true` or `false` |  |
| block-function-signals | Block signal emissions from functions | `true` or `false` |  |
| file-monitor | Emit signal when input file(s) change | `true` or `false` | 0.8.1 |
| auto-refresh | Auto refresh when input file(s) change | `true` or `false` | 0.8.1 |

## Directives ##

Some of these may have tag attribute equivalents.

| **Name** | **Description** | **Contents** | **Since** |
|:---------|:----------------|:-------------|:----------|
| default | Initial data | _#rrggbb_ `|` _alpha_<sup>[1]</sup> |  |
| variable | Variable name |  |  |
| variable export="false" | Variable name, not exported to shell |  | 0.8.3 |
| input | Data input source | Shell command |  |
| input file | Data input source | Filename |  |
| sensitive | Sensitive state | `true` or `false` |  |
| action | Execute command on default signal | Shell command |  |
| action | Perform function on default signal | _function_:_parameter_ |  |
| action signal="_type_" | Execute command on signal | Shell command |  |
| action signal="_type_" | Perform function on signal | _function_:_parameter_ |  |
| action function="_type_" | Perform function on default signal | _parameter_ | 0.8.3 |
| action condition="_type_" | Execute command on default signal conditionally | Shell command | 0.8.3 |
| action condition="_type_" | Perform function on default signal conditionally | _function_:_parameter_ | 0.8.3 |
| action signal="_type_" condition="_type_" | Execute command on signal conditionally | Shell command | 0.8.3 |
| action signal="_type_" condition="_type_" | Perform function on signal conditionally | _function_:_parameter_ | 0.8.3 |
| action function="_type_" condition="_type_" | Perform function on default signal conditionally | _parameter_ | 0.8.3 |
| output file | Data output target | Filename |  |

## Signals ##

The default signal is "[color-set](http://developer.gnome.org/gtk2/2.24/GtkColorButton.html#GtkColorButton-color-set)", emitted when the user selects a colour.

The "file-changed" signal is emitted if file-monitor is true and the input file being monitored has changed.

The following signals are connected-up for all widgets:

[button-press-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-button-press-event), [button-release-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-button-release-event), [configure-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-configure-event), [enter-notify-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-enter-notify-event), [leave-notify-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-leave-notify-event), [focus-in-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-focus-in-event), [focus-out-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-focus-out-event), [hide](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-hide), [show](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-show), [realize](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-realize), [key-press-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-key-press-event), [key-release-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-key-release-event), [map-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-map-event), [unmap-event](http://developer.gnome.org/gtk2/2.24/GtkWidget.html#GtkWidget-unmap-event)

## Functions ##

The following functions can be performed upon this widget by any widget capable of emitting signals:

| **Type** | **Description** | **Parameter** | **Since** |
|:---------|:----------------|:--------------|:----------|
| enable | Sensitise widget | Variable name |  |
| disable | Desensitise widget | Variable name |  |
| show | Show widget | Variable name | 0.8.1 |
| hide | Hide widget | Variable name | 0.8.1 |
| activate | Activate widget | Variable name | 0.8.1 |
| grabfocus | Grab input focus | Variable name | 0.8.1 |
| refresh | Reload input data | Variable name |  |
| save | Save widget data | Variable name |  |

The following general functions can be performed by any widget capable of emitting signals:

| **Type** | **Description** | **Parameter** | **Since** |
|:---------|:----------------|:--------------|:----------|
| break | Break out of actions list | None | 0.8.3 |
| command | Execute command | Shell command |  |
| exit | Exit dialog | A value for the `EXIT` variable |  |
| closewindow | Close dialog | Variable name |  |
| launch | Launch dialog | Variable name |  |
| presentwindow | [Present](http://developer.gnome.org/gtk2/2.24/GtkWindow.html#gtk-window-present) dialog | Variable name | 0.8.1 |

## Conditions ##

The following conditions can be used within the condition attribute of action directives:

| **Type** | **Description** | **Argument** | **Since** |
|:---------|:----------------|:-------------|:----------|
| active\_is\_true(_argument_) | Active state of toggle widget | Variable name | 0.8.3 |
| active\_is\_false(_argument_) | Active state of toggle widget | Variable name | 0.8.3 |
| command\_is\_true(_argument_) | Output of shell command | Shell command | 0.8.3 |
| command\_is\_false(_argument_) | Output of shell command | Shell command | 0.8.3 |
| file\_is\_true(_argument_) | Contents of a file | Filename | 0.8.3 |
| file\_is\_false(_argument_) | Contents of a file | Filename | 0.8.3 |
| sensitive\_is\_true(_argument_) | Sensitive state of widget | Variable name | 0.8.3 |
| sensitive\_is\_false(_argument_) | Sensitive state of widget | Variable name | 0.8.3 |
| visible\_is\_true(_argument_) | Visible state of widget | Variable name | 0.8.3 |
| visible\_is\_false(_argument_) | Visible state of widget | Variable name | 0.8.3 |

true means "true", "yes" or a non-zero value, false means "false", "no" or zero, therefore the shell command is expected to echo one of these values to stdout.

## Notes ##

1. Setting the "[use-alpha](http://developer.gnome.org/gtk2/2.24/GtkColorButton.html#GtkColorButton--use-alpha)" tag attribute to true will enable alpha selection. Alpha can be passed in following the _#rrggbb_ value separated by a '`|`' character, or via the "[alpha](http://developer.gnome.org/gtk2/2.24/GtkColorButton.html#GtkColorButton--alpha)" tag attribute. Although the colour selection dialog displays alpha as an 8bit 0-255 value, GTK+ and Gtkdialog manage it as a 16bit 0-65535 value and therefore it'll require converting between the two formats. To convert from 8bit to 16bit use `alpha * 257` and from 16bit to 8bit use `(alpha + 257 / 2) / 257`.

This widget was introduced in version 0.7.21.


---