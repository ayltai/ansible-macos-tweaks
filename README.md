# ansible-macos-tweaks

Tweak your macOS with Ansible in over 50 different ways!

## Quick start

Try it out using [BrewMyMac](https://brewmymac.sh/)!

### Installation

Make sure you have [Ansible](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html) installed on your macOS.

```bash
git clone https://github.com/ayltai/ansible-macos-tweaks.git
cd ansible-macos-tweaks
python -m pip install --upgrade pip
pip install -r requirements.txt
ansible-playbook playbook.yml --extra-vars "tweak_macos_launchpad_grid_columns_enabled=true tweak_macos_launchpad_grid_columns_value=4 tweak_macos_launchpad_grid_rows_enabled=true tweak_macos_launchpad_grid_rows_value=3"
```

## Variables

| Name | Type | Default | Description |
|------|------|---------|-------------|
| `tweak_macos_launchpad_grid_columns_enabled` | `bool` | `false` | Specify whether to enable changing the Launchpad grid layout columns. |
| `tweak_macos_launchpad_grid_columns_value` | `number` | 4 | Change the Launchpad grid layout to this many columns. By default, it displays 7 columns. |
| `tweak_macos_launchpad_grid_rows_enabled` | `bool` | `false` | Specify whether to enable changing the Launchpad grid layout rows. |
| `tweak_macos_launchpad_grid_rows_value` | `number` | 3 | Change the Launchpad grid layout to this many rows. By default, it displays 5 rows. |
| `tweak_macos_disable_disk_image_verification_enabled` | `bool` | `false` | You can skip disk image file checksum verification to speed up the mounting of disk images through this is not recommended by security experts or Apple. Specify whether to disable disk image verification. |
| `tweak_macos_disable_disk_image_verification_value` | `bool` | `true` | Specify 'true' to disable disk image verification and 'false' to enable it. |
| `tweak_macos_disable_gatekeeper_enabled` | `bool` | `false` | Gatekeeper requires applications to be signed before they can be run. However, code signing is a paid process and not all developers sign their applications. It gets annoying when it won't let you oepn an application that you know is safe. Specify whether to disable Gatekeeper. |
| `tweak_macos_disable_gatekeeper_value` | `bool` | `true` | Specify 'true' to disable Gatekeeper and 'false' to enable it. |
| `tweak_macos_disable_quarantine_enabled` | `bool` | `false` | When you download an application from the Internet, macOS will mark it as quarantined. This is to prevent you from running malicious applications. However, it gets annoying when it won't let you open an application that you know is safe. Specify whether to disable quarantine. |
| `tweak_macos_disable_quarantine_value` | `bool` | `true` | Specify 'true' to disable quarantine and 'false' to enable it. |
| `tweak_macos_disable_game_center_enabled` | `bool` | `false` | Game Center daemon continues to run even when you have disabled Game Center. Specify whether to disable Game Center. |
| `tweak_macos_disable_game_center_value` | `bool` | `true` | Specify 'true' to disable Game Center and 'false' to enable it. |
| `tweak_macos_disable_smart_quotes_enabled` | `bool` | `false` | macOS automatically converts straight quotes to smart quotes. But for developers, it's annoying to have to manually change them back. Specify whether to disable smart quotes. |
| `tweak_macos_disable_smart_quotes_value` | `bool` | `true` | Specify 'true' to disable smart quotes and 'false' to enable it. |
| `tweak_macos_disable_smart_dashes_enabled` | `bool` | `false` | macOS automatically converts two hyphens to an em dash. But for developers, it's annoying to have to manually change them back. Specify whether to disable smart dashes. |
| `tweak_macos_disable_smart_dashes_value` | `bool` | `true` | Specify 'true' to disable smart dashes and 'false' to enable it. |
| `tweak_macos_disable_auto_capitalization_enabled` | `bool` | `false` | macOS automatically capitalizes the first letter of a sentence. But for developers, it's annoying to have to manually change them back. Specify whether to disable auto capitalization. |
| `tweak_macos_disable_auto_capitalization_value` | `bool` | `true` | Specify 'true' to disable auto capitalization and 'false' to enable it. |
| `tweak_macos_disable_sudden_motion_sensor_enabled` | `bool` | `false` | The Sudden Motion Sensor is a hardware feature that detects sudden movement and can be used to protect the hard drive. However, it can also cause problems when you are using a laptop on an uneven surface and it is unnecessary if your MacBook ships with an SSD drive. Specify whether to disable Sudden Motion Sensor. |
| `tweak_macos_disable_sudden_motion_sensor_value` | `bool` | `true` | Specify 'true' to disable the Sudden Motion Sensor and 'false' to enable it. |
| `tweak_macos_disable_hibernation_enabled` | `bool` | `false` | macOS copies the current RAM contents to a file on the disk drive and then shuts down. This is useful if you want to resume your work after a power outage. However, it can cause problems to some applications and it shortens the lifespan of your SSD drive. Specify whether to disable hibernation. |
| `tweak_macos_disable_hibernation_value` | `bool` | `true` | Specify 'true' to disable hibernation and 'false' to enable it. |
| `tweak_macos_disable_photos_auto_open_enabled` | `bool` | `false` | macOS automatically opens Photos every time you insert a memory card or connect a device. Specify whether to disable Photos auto open. |
| `tweak_macos_disable_photos_auto_open_value` | `bool` | `true` | Specify 'true' to disable Photos from opening automatically and 'false' to enable it. |
| `tweak_macos_default_screenshot_location_enabled` | `bool` | `false` | Change the default location where screenshots are saved. By default, it saves screenshots to the desktop. Specify whether to change the default screenshot location. |
| `tweak_macos_default_screenshot_location_value` | `string` | `~/Desktop` | Change the default location where screenshots are saved to this path. |
| `tweak_macos_display_thumbnail_after_screenshot_enabled` | `bool` | `false` | Display a thumbnail of the screenshot after taking a screenshot. Specify whether to display a thumbnail of the screenshot after taking a screenshot. |
| `tweak_macos_display_thumbnail_after_screenshot_value` | `bool` | `true` | Specify 'true' to display a thumbnail of the screenshot after taking a screenshot and 'false' to disable it. |
| `tweak_macos_screenshots_format_enabled` | `bool` | `false` | Change the default screenshot format. By default, it saves screenshots in PNG format. Specify whether to change the default screenshot format. |
| `tweak_macos_screenshots_format_value` | `string` | `png` | By default, macOS saves screenshots in PNG format. Supported formats are 'jpg', 'tiff', 'gif', 'pdf', and 'png'. |
| `tweak_macos_disable_screenshot_shadow_enabled` | `bool` | `false` | Disable the shadow in screenshots. Specify whether to disable the shadow in screenshots. |
| `tweak_macos_disable_screenshot_shadow_value` | `bool` | `true` | Specify 'true' to disable the shadow in screenshots and 'false' to enable it. |
| `tweak_macos_include_date_in_screenshot_filenames_enabled` | `bool` | `false` | By default, macOS saves screenshots with the filename 'Screen Shot YYYY-MM-DD at HH.MM.SS AM/PM'. Specify whether to include the date in screenshot filenames. |
| `tweak_macos_include_date_in_screenshot_filenames_value` | `bool` | `true` | Specify 'true' to include the date in screenshot filenames and 'false' to disable it. |
| `tweak_macos_subpixel_font_rendering_enabled` | `bool` | `false` | If you are running macOS on a Mac without a retina display, or with an external monitor that does not have an ultra-high resolution screen, you may have noticed that some fonts and text can appear as blurry and difficult to read. This is because macOS is rendering the text using subpixel font rendering. Specify whether to enable subpixel font rendering. |
| `tweak_macos_subpixel_font_rendering_value` | `number` | 3 | Specify '1' if you want less text smoothing, '2' if you want medium-level text smoothing, and '3' if you want even more text smoothing. |
| `tweak_macos_show_file_extensions_enabled` | `bool` | `false` | By default, macOS hides file extensions in Finder. Specify whether to show file extensions. |
| `tweak_macos_show_file_extensions_value` | `bool` | `true` | Specify 'true' to show file extensions and 'false' to hide them. |
| `tweak_macos_show_hidden_files_enabled` | `bool` | `false` | By default, macOS hides hidden files in Finder. Specify whether to show hidden files. |
| `tweak_macos_show_hidden_files_value` | `bool` | `true` | Specify 'true' to show hidden files and 'false' to hide them. |
| `tweak_macos_sidebar_icon_size_enabled` | `bool` | `false` | Change the size of icons in the sidebar of Finder. Specify whether to change the size of icons in the sidebar of Finder. |
| `tweak_macos_sidebar_icon_size_value` | `number` | 2 | Change the size of the icons in the sidebar of Finder. Specify '1' (smallest), '2', or '3' (largest). |
| `tweak_macos_show_status_bar_enabled` | `bool` | `false` | By default, macOS hides the status bar in Finder. Specify whether to show the status bar. |
| `tweak_macos_show_status_bar_value` | `bool` | `true` | Specify 'true' to show the status bar in Finder and 'false' to hide it. |
| `tweak_macos_show_quit_option_enabled` | `bool` | `false` | By default, macOS hides the Quit option in Finder. Specify whether to show the Quit option. |
| `tweak_macos_show_quit_option_value` | `bool` | `true` | Specify 'true' to show the Quit option in Finder and 'false' to hide it. |
| `tweak_macos_keep_folders_on_top_enabled` | `bool` | `false` | By default, Finder sorts a directory's contents by name, with both files and folders arranged alongside one another based upon an alphabetical sorting of their names. Specify whether to keep folders on top. |
| `tweak_macos_keep_folders_on_top_value` | `bool` | `true` | Specify 'true' to keep folders on top and 'false' to disable it. |
| `tweak_macos_disable_file_extension_warning_enabled` | `bool` | `false` | macOS warns you when you change a file extension in Finder. Specify whether to disable the file extension warning. |
| `tweak_macos_disable_file_extension_warning_value` | `bool` | `true` | Specify 'true' to disable the file extension warning in Finder and 'false' to enable it. |
| `tweak_macos_default_view_style_enabled` | `bool` | `false` | Finder can display files in a variety of ways and it may open up with a different view style each time. Specify whether to change the default view style in Finder. |
| `tweak_macos_default_view_style_value` | `string` | `list` | Change the default view style in Finder. Specify 'Nlsv' for list view, 'icnv' for icon view, 'clmv' for column view, 'Flwv' for cover flow view, and 'glyv' for gallery view. |
| `tweak_macos_enable_spring_loading_enabled` | `bool` | `false` | A spring-loaded folder pops open when you drag something onto its icon while holding down the mouse button. Specify whether to enable spring loading. |
| `tweak_macos_enable_spring_loading_value` | `bool` | `true` | Specify 'true' to enable spring loading and 'false' to disable it. |
| `tweak_macos_spring_loading_delay_enabled` | `bool` | `false` | You can customize the spring-loaded folder delay to suit your preference. Specify whether to change the delay before a spring-loaded folder pops open. |
| `tweak_macos_spring_loading_delay_value` | `number` | 0.5 | Specify the delay in seconds before a spring-loaded folder pops open. |
| `tweak_macos_disable_ds_store_enabled` | `bool` | `false` | macOS creates .DS_Store files on network volumes to store custom attributes of the folder. Specify whether to disable the creation of .DS_Store files. |
| `tweak_macos_disable_ds_store_value` | `bool` | `true` | Specify 'true' to disable the creation of .DS_Store files and 'false' to enable it. |
| `tweak_macos_disable_empty_trash_warning_enabled` | `bool` | `false` | macOS warns you when you empty the Trash. Specify whether to disable the empty Trash warning. |
| `tweak_macos_disable_empty_trash_warning_value` | `bool` | `true` | Specify 'true' to disable the empty Trash warning and 'false' to enable it. |
| `tweak_macos_empty_trash_automatically_enabled` | `bool` | `false` | By default, macOS does not empty the trash automatically. Specify whether to empty the Trash automatically. |
| `tweak_macos_empty_trash_automatically_value` | `bool` | `true` | Specify 'true' to empty the trash automatically after 30 days and 'false' to disable it. |
| `tweak_macos_dock_position_enabled` | `bool` | `false` | You can change the position of the Dock to the left, bottom, or right side of the screen. Specify whether to change the position of the Dock. |
| `tweak_macos_dock_position_value` | `string` | `bottom` | Change the position of the Dock. Supported values are 'left', 'bottom', or 'right'. |
| `tweak_macos_dock_icon_size_enabled` | `bool` | `false` | You can change the size of the Dock icons to an exact number. Specify whether to change the size of the icons in the Dock. |
| `tweak_macos_dock_icon_size_value` | `number` | 32 | Change the size of the icons in the Dock. Specify a number in pixels. |
| `tweak_macos_lock_dock_icon_size_enabled` | `bool` | `false` | You can lock the size of the Dock icons to prevent them from being resized. Specify whether to lock the size of the icons in the Dock. |
| `tweak_macos_lock_dock_icon_size_value` | `bool` | `true` | Specify 'true' to lock the size of the icons in the Dock and 'false' to unlock it. |
| `tweak_macos_enable_dock_spring_loading_enabled` | `bool` | `false` | Dock icons can operate with the same spring-loaded features as folders. By default, this feature is disabled. Specify whether to enable spring loading. |
| `tweak_macos_disable_recent_apps_enabled` | `bool` | `false` | By default, macOS shows three most recent applications in the Dock. Specify whether to disable the list of recently used apps. |
| `tweak_macos_disable_recent_apps_value` | `bool` | `true` | Specify 'true' to disable the list of recently used apps and 'false' to enable it. |
| `tweak_macos_dock_animation_effect_enabled` | `bool` | `false` | macOS animates the Dock when you open or close an application. The default animation effect is 'genie'. Specify whether to change the animation effect. |
| `tweak_macos_dock_animation_effect_value` | `bool` | `true` | macOS animates the Dock when you open or close an application. The default animation effect is 'genie'. Supported values are 'genie', 'scale', or 'suck'. |
| `tweak_macos_disable_swipe_navigation_enabled` | `bool` | `false` | Even if you have disabled the system-wide 'Swipe between pages' feature, Google Chrome still allows you to swipe between pages. Specify whether to disable swipe navigation. |
| `tweak_macos_disable_swipe_navigation_value` | `bool` | `true` | Specify 'true' to disable swipe navigation in Google Chrome and 'false' to enable it. |
| `tweak_macos_dark_mode_enabled` | `bool` | `false` | Specify whether to enable changing to dark mode. |
| `tweak_macos_dark_mode_value` | `bool` | `true` | Specify 'true' to enable dark mode and 'false' to disable it. |
| `tweak_macos_disable_itunes_media_keys_enabled` | `bool` | `false` | If you have iTunes installed, when you press Play on the keyboard, or connect the headset and Bluetooth speaker, iTunes will automatically run. Specify whether to disable iTunes media keys. |
| `tweak_macos_disable_itunes_media_keys_value` | `bool` | `true` | Specify 'true' to disable iTunes media keys and 'false' to enable it. |
| `tweak_macos_disable_mouse_shake_enabled` | `bool` | `false` | By default, the mouse cursor in macOS gets really big when you shake the mouse or when you move it too quickly. Specify whether to disable mouse shake. |
| `tweak_macos_disable_mouse_shake_value` | `bool` | `true` | Specify 'true' to disable mouse shake and 'false' to enable it. |
| `tweak_macos_display_sleep_enabled` | `bool` | `false` | You can put the display to sleep for battery saving or privacy reasons. Specify whether to change the display sleep settings. |
| `tweak_macos_display_sleep_value` | `number` | 10 | Change the display sleep settings. Specify a number in minutes, and '0' to disable it. |
| `tweak_macos_computer_sleep_enabled` | `bool` | `false` | You can put the computer to sleep for battery saving or privacy reasons. Specify whether to enable changing this setting. |
| `tweak_macos_computer_sleep_value` | `number` | 0 | Change the computer sleep settings. Specify a number in minutes, and '0' to disable it. |
| `tweak_macos_disable_computer_sleep_enabled` | `bool` | `false` | You can disable the computer from sleeping. Specify whether to enable changing this setting. |
| `tweak_macos_disable_computer_sleep_value` | `bool` | `true` | Specify 'true' to disable computer sleep and 'false' to enable it. |
| `tweak_macos_keep_windows_enabled` | `bool` | `false` | macOS can remember all the tabs and windows you had open for the next time you launch it again. Specify whether to enable chaning this setting. |
| `tweak_macos_keep_windows_value` | `bool` | `true` | Specify 'true' to keep windows and 'false' to close them. |
| `tweak_macos_disable_memory_compression_enabled` | `bool` | `false` | You may want to disable memory swap to improve performance and prolong the SSD drive lifetime. However, this may cause the system to crash if you run out of memory. Specify whether to enable changing this setting. |
| `tweak_macos_disable_memory_compression_value` | `bool` | `true` | Specify 'true' to disable memory compression and 'false' to enable it. |
| `tweak_macos_disable_crash_reports_enabled` | `bool` | `false` | The crash reporter takes up a lot resources and if you are a developer, you may quickly get annoyed by the constant popups. Specify whether to enable changing this setting. |
| `tweak_macos_disable_crash_reports_value` | `bool` | `true` | Specify 'true' to disable crash reports and 'false' to enable it. |
| `tweak_macos_software_update_frequency_enabled` | `bool` | `false` | macOS automatically checks for software updates but you cannot change how often it checks in System Preferences. Specify whether to enable changing this setting. |
| `tweak_macos_software_update_frequency_value` | `number` | 1 | Change the software update frequency. Specify a number in days. |
| `tweak_macos_default_shell_enabled` | `bool` | `false` | Specify the default shell. Specify whether to change the default shell. |
| `tweak_macos_default_shell_value` | `string` | `/bin/zsh` | Specify the default shell. Supported values are 'bash', 'csh', 'dash', 'ksh', 'sh', 'tcsh', and 'zsh'. |
| `tweak_macos_disable_spelling_autocorrect_enabled` | `bool` | `false` | macOS automatically corrects your spelling mistakes. Specify whether to enable changing this setting. |
| `tweak_macos_disable_spelling_autocorrect_value` | `bool` | `true` | Specify 'true' to disable spelling autocorrect and 'false' to enable it. |
| `tweak_macos_change_computer_name_enabled` | `bool` | `false` | Specify whether to change the computer name. |
| `tweak_macos_change_computer_name_value` | `string` | `BrewMyMac` | Specify the computer name. |
| `tweak_macos_disable_boot_sound_enabled` | `bool` | `false` | macOS plays a sound when you start up your computer. Specify whether to enable changing this setting. |
| `tweak_macos_disable_boot_sound_value` | `bool` | `true` | Specify 'true' to disable boot sound and 'false' to enable it. |

## License
[MIT](/blob/master/LICENSE)
