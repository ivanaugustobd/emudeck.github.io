# Community Creations, cool things made by you! 

***

## Community Creations Table of Contents

1. [Controller Configurations](#controller-configurations)
      * [Steam Input](#steam-input)
          * [Getting Started With Steam Input](#getting-started-with-steam-input)
               * [How to Share Steam Input Layouts](#how-to-share-steam-input-layouts)
               * [How to Download Steam Input Layouts](#how-to-download-steam-input-layouts)
               * [How to use Steam Input Layouts](#how-to-use-steam-input-layouts)
          * [Community Steam Input Profiles](#community-steam-input-profiles)
               * [Nintendo 64 Controller](#nintendo-64-controller)
               * [Steam Input Layout 2](#steam-input-layout-2)
               * [Steam Input Layout 3](#steam-input-layout-3)
               * [Steam Input Layout 4](#steam-input-layout-4)
               * [Steam Input Layout 5](#steam-input-layout-5)
      * [Dolphin](#dolphin)
          * [Getting Started With Dolphin Profiles](#getting-started-with-dolphin-profiles)
               * [How to Share Dolphin Profiles](#how-to-share-dolphin-profiles)
               * [How to Download Dolphin Profiles](#how-to-download-dolphin-profiles)
          * [Community Dolphin Profiles](#community-dolphin-profiles)
               * [Wiimote Motion Controls With Nunchuck](#wiimote-motion-controls-with-nunchuck)
               * [Wiimote Motion Controls With No Attachment](#wiimote-motion-controls-with-no-attachment)
               * [Super Mario Galaxy 1 and 2](#super-mario-galaxy-1-and-2)
               * [Gyro Steam Deck on Dolphin](#dolphin-config-4)
               * [Dolphin Config 5](#dolphin-config-5)

2. [Special Game Configurations](#special-game-configurations)
      * [RPCS3 (Playstation 3)](#rpcs3-playstation-3)
          * [Metal Gear Solid 4](#metal-gear-solid-4)
      * [Yuzu (Nintendo Switch)](#yuzu-nintendo-switch)
          * [The Legend of Zelda: Link's Awakening](#the-legend-of-zelda-links-awakening)

3. [Tools and Utilities](#tools-and-utilities)
      1. [How to Set Up SyncThing](#how-to-set-up-syncthing)
      2. [How to Use ROM Hacks](#how-to-use-rom-hacks)

4. [How to Contribute to EmuDeck](#how-to-contribute-to-emudeck)
      1. [How to Submit an Emulator Package](#how-to-submit-an-emulator-package)
***

## Controller Configurations
[Back to the Top](#community-creations-table-of-contents)

***



### Steam Input
[Back to the Top](#community-creations-table-of-contents)

***

### Getting Started With Steam Input
[Back to the Top](#community-creations-table-of-contents)

***

#### How to Share Steam Input Layouts
[Back to the Top](#community-creations-table-of-contents)

This section will go over how to share and post your Steam Input Layouts on this page. 

**Tutorial**

1. Create a new Steam Input Layout in Game Mode. 
2. After you are finished, press the Gear icon on the controller layout screen, click `Export Layout`, change `Export Type` to `New Personal Save`.
    1. Visual Reference 1: <img src="https://user-images.githubusercontent.com/108900299/199400389-e35e7877-0dec-4fde-bdea-28104d981dab.png" height="300">
    2. Visual Reference 2: <img src="https://user-images.githubusercontent.com/108900299/197309794-404dbe92-6509-485a-8b1f-59f71d965584.png" height="300">
    3. Visual Reference 3: <img src="https://user-images.githubusercontent.com/108900299/199398759-7db86406-0c13-4f68-8545-4857d1a507ea.png" height="300">
3. Switch to Desktop Mode.
4. Open Konsole. 
5. In Konsole, enter: `grep --recursive "<yourprofilename>" ~/.steam/steam/userdata`
    1. Replace `<yourprofilename>` entirely with the profile name you created in Step 1. 
    2. Visual Reference (Using `Community Creations` as an example): <img src="https://user-images.githubusercontent.com/108900299/199399154-1d4a9e60-f2cd-4a13-bf89-c2fb2fb4280a.png" height="300">
6. Open the folder path outputted by the command. 
    1. `~/.steam` is an invisible folder by default, in Dolphin (File Explorer), press the hamburger button in the top right, ☰, press `Show Hidden Files`.  
7. Copy this template to another folder of your choice.
    1. Rename the copied file to something descriptive, like the profile name created in Step 1. 
8. Right click, click `Open with Kwrite` or a text editor of your choice.
9. Edit the top part of the file using the following template: 

**Template:**

```
"controller_mappings"
{
	"version"		leave this alone
	"revision"		leave this alone
	"title"		        leave this alone
	"description"		leave this alone
	"creator"		leave this alone
	"progenitor"		leave this alone
	"url"		        change to: "template://<file name>.vdf"
	"export_type"		change to:  "template"
	"controller_type"		"controller_neptune"
	"major_revision"	leave this alone
	"minor_revision"	leave this alone
	"Timestamp"		leave this alone
	"localization"
```

**Sample:**

```
"controller_mappings"
{
	"version"		"3"
	"revision"		"21"
	"title"		"EmuDeck - PPSSPP Standalone"
	"description"		"Left Touchpad quick actions. Long press to perform an action"
	"creator"		"76561198025051816"
	"progenitor"		""
	"url"		        "template://ppsspp_controller_config.vdf"
	"export_type"		"template"
	"controller_type"		"controller_neptune"
	"major_revision"		"0"
	"minor_revision"		"0"
	"Timestamp"		"4"
	"localization"
```

10. Create a new section on this page under Steam Input in the `Table of Contents`, refer to `Steam Input Layout 1` as a sample.
    1. Create a Github Account to edit this page first, if you have not done so already. 
    2. At the moment, `Steam Input Layout 4` through `Steam Input Layout 7` can be edited and replaced with your templates. 
11. Paste the contents of the file into your newly created section, include a brief description and any prerequisites. 
12. Place three \` at the top and the bottom of the pasted profile, refer to `Steam Input Layout 1` as a sample.
13. Save the page.
14. You have now successfully shared your profile. 

***

#### How to Download Steam Input Layouts
[Back to the Top](#community-creations-table-of-contents)

You may select a profile to download by choosing one from the list here: [Community Steam Input Profiles](#community-steam-input-profiles-table-of-contents).

After you have selected a profile, you may use the below tutorial to learn how to download it and use it in Steam. 


**Tutorial**

1. Copy the contents of a profile you would like to use by clicking the copy icon in the top right
   1. Visual Reference: <img src="https://user-images.githubusercontent.com/108900299/196857393-76dfa11b-ed76-464a-a665-4970505a848c.png" height="300">
2. In this folder: `/home/deck/.steam/steam/controller_base/templates`, right click, `Create New`, `Text File`
    1. `.steam` is an invisible folder by default, click the hamburger menu in the top right, click `Show Hidden Files` to un-hide it. 
3. Paste the contents of a profile you would like to use
4. Save the profile, matching the profile name in the section exactly, with a `.vdf` file extension
   1. Without the `.vdf` file extension, the profile will not work
5. You now have successfully downloaded a profile 

***

#### How to use Steam Input Layouts
[Back to the Top](#community-creations-table-of-contents)

In Game Mode, single click the game you would like to change the Steam Input Profile for, and click the `Controller Icon` on the right of the screen. Click the layout (whatever name it is currently set to) at the top, and you will see a drop-down menu. When playing a PSX, PSP, 3DS, or Wii U Game, switch to the respective Steam Input Profile.

For a visual, watch the following GIF (EmuDeck - Duckstation is being used as an example):

<img src="https://user-images.githubusercontent.com/108900299/194612525-670e56a1-a16a-4dbf-a03f-85d14e7f7b76.gif" height="300">

***

### Community Steam Input Profiles 
[Back to the Top](#community-creations-table-of-contents)

#### Community Steam Input Profiles Table of Contents

* [Nintendo 64 Controller](#nintendo-64-controller)
* [Steam Input Layout 2](#steam-input-layout-2)
* [Steam Input Layout 3](#steam-input-layout-3)
* [Steam Input Layout 4](#steam-input-layout-4)
* [Steam Input Layout 5](#steam-input-layout-5)

***

#### Nintendo 64 Controller
[Back to the Top](#community-creations-table-of-contents)

Credit: `Piximator` 

This Steam input profile is for the NSO Nintendo 64 Controller, [https://www.nintendo.com/store/products/nintendo-64-controller/](https://www.nintendo.com/store/products/nintendo-64-controller/). 

**Profile Name:** `nintendo switch online n64 controller.vdf`

```
"controller_mappings"
{
	"version"		"3"
	"revision"		"20"
	"title"		"Nintendo Switch Online N64 Controller"
	"description"		"For use with the official NSO N64 controller in RetroArch. Uses default EmuDeck bindings."
	"creator"		"76561199036238022"
	"progenitor"		""
	"url"		"template://nintendo switch online n64 controller.vdf"
	"export_type"		"template"
	"controller_type"		"controller_neptune"
	"major_revision"		"0"
	"minor_revision"		"0"
	"Timestamp"		"4"
	"localization"
	{
		"english"
		{
			"title"		"Gamepad"
			"description"		"This template is for games that already have built-in gamepad support.  Intended for dual stick games such as twin-stick shooters, side-scrollers, etc."
		}
		"czech"
		{
			"title"		"Gamepad"
			"description"		"Tato šablona je pro většinu her podporujících gamepad a byla navržena pro použití ve hrách využívajících dvě páčky, jakými jsou například plošinovky nebo automatové hry."
		}
		"danish"
		{
			"title"		"Gamepad"
			"description"		"Denne skabelon er til spil, der allerede har indbygget gamepad-understøttelse. Beregnet til spil med dobbelte styrepinde såsom twin-stick shooters, side-scrollers osv."
		}
		"dutch"
		{
			"title"		"Gamepad"
			"description"		"Deze template is voor spellen die al ingebouwde gamepadondersteuning hebben. Bedoeld voor dual-stick spellen zoals twin-stick-shooters, side-scrollers, etc."
		}
		"finnish"
		{
			"title"		"Ohjain"
			"description"		"Tämä malli on muita ohjaimia valmiiksi tukeville peleille. Se on tarkoitettu kahta sauvaa käyttäville peleille, kuten twin-stick shooterit, side-scrollerit, jne."
		}
		"french"
		{
			"title"		"Manette"
			"description"		"Ce modèle fonctionne pour les jeux conçus pour manettes à deux sticks tels que les jeux de type twin-stick shooter, à défilement horizontal (side-scrollers), etc."
		}
		"german"
		{
			"title"		"Gamepad"
			"description"		"Diese Vorlage ist für Spiele konzipiert, die bereits volle Unterstützung für Gamepads mit sich bringen. Gedacht für Zwei-Analogstick-Spiele wie Twin-Stick-Shooter, Side-Scrollers usw."
		}
		"hungarian"
		{
			"title"		"Gamepad"
			"description"		"Ez a sablon olyan játékokhoz való, melyek már rendelkeznek beépített gamepad-támogatással. Olyan két karos játékokhoz szánva, mint a kétkaros vagy oldalnézetes lövöldözős játékok stb."
		}
		"italian"
		{
			"title"		"Controller"
			"description"		"Questo modello funziona per la maggior parte dei giochi che supportano i controller in modalità nativa."
		}
		"japanese"
		{
			"title"		"ゲームパッド"
			"description"		"このテンプレートは、標準でゲームパッドをサポートしているツインスティックシューターや横スクロール等といったデュアルスティックゲームを対象としたゲーム向けです。"
		}
		"koreana"
		{
			"title"		"게임패드"
			"description"		"게임 패드를 지원하도록 설계된 게임들을 위한 설정입니다. 이중 스틱 슈팅 게임, 사이드 스크롤 게임 등 스틱을 두 개 쓰는 게임을 염두에 두고 만들어졌습니다."
		}
		"polish"
		{
			"title"		"Kontroler"
			"description"		"Ten szablon jest odpowiedni dla gier, które już mają wbudowane wsparcie dla kontrolerów. Przeznaczony dla gier obsługujących dwie gałki, m.in. twin-stick shootery, side-scrollery itp."
		}
		"portuguese"
		{
			"title"		"Comando"
			"description"		"Este modelo é indicado para jogos que já têm compatibilidade nativa com comando. Foi concebido para jogos de tiros que usam dois sticks, jogos de plataformas, de naves, etc."
		}
		"romanian"
		{
			"title"		"Gamepad"
			"description"		"Șablonul acesta este pentru jocurile care au deja suport pentru gamepad implementat. Destinat pentru jocuri dual stick, precum shooter-e twin-stick, side-scroller, etc."
		}
		"russian"
		{
			"title"		"Геймпад"
			"description"		"Этот шаблон подходит для большинства игр с поддержкой геймпада — например, для шутеров с видом сверху или сбоку."
		}
		"spanish"
		{
			"title"		"Mando"
			"description"		"Esta plantilla es para juegos que ya incluyen de serie compatibilidad con mando. Está destinada a juegos de doble stick como twin-stick shooters, side-scrollers, etc."
		}
		"swedish"
		{
			"title"		"Gamepad"
			"description"		"Denna mall är för spel som redan har inbyggt stöd för spelkontroller. Avsett för spel som använder två styrspakar, som twin-stick shooters och side-scrollers, etc."
		}
		"schinese"
		{
			"title"		"手柄"
			"description"		"该模板适用于已内置手柄支持的游戏。针对双摇杆游戏，如双摇杆射击游戏、横版过关游戏等设计。"
		}
		"thai"
		{
			"title"		"เกมแพด"
		}
		"brazilian"
		{
			"title"		"Controle padrão"
			"description"		"Este modelo é para jogos já compatíveis com controle que usam ambas as alavancas, como jogos de nave, etc."
		}
		"bulgarian"
		{
			"title"		"Геймпад"
			"description"		"Този шаблон е за игри, които вече имат вградена поддръжка на геймпад. Предназначен e за игри ползващи двата стика. Като например, екшъни за два аналогови стика, странични скролери и т.н."
		}
		"greek"
		{
			"title"		"Χειριστήριο"
			"description"		"Αυτό το πρότυπο ορίζεται για παιχνίδια τα οποία έχουν ήδη υποστήριξη χειριστηρίου. Προορίζεται για παιχνίδια dual-stick όπως twin-stick shooters, side-scrollers, κλπ."
		}
		"turkish"
		{
			"title"		"Oyun Kumandası"
			"description"		"Bu şablon hali hazırda oyun içi oyun kumandası desteği ve birincil veya üçüncü kişi kontrollü kameraya sahip oyunlar içindir. Çift çubuk kullanılan oyunlar olan ikiz çubuk nişancılık, side-scroller oyunlar vb. içindir."
		}
		"ukrainian"
		{
			"title"		"Ґеймпад"
			"description"		"Цей шаблон для більшості ігор, в яких вже вбудовано підтримку ґеймпада. Призначено для ігор з керуванням двома стіками."
		}
	}
	"group"
	{
		"id"		"0"
		"mode"		"four_buttons"
		"name"		""
		"description"		""
		"inputs"
		{
			"button_a"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button A"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"button_b"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button X"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"button_x"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button RSTICK_LEFT"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"button_y"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button RSTICK_UP"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
		}
	}
	"group"
	{
		"id"		"1"
		"mode"		"dpad"
		"name"		""
		"description"		""
		"inputs"
		{
			"dpad_north"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button dpad_up"
						}
						"settings"
						{
							"haptic_intensity"		"1"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"dpad_south"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button dpad_down"
						}
						"settings"
						{
							"haptic_intensity"		"1"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"dpad_east"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button dpad_right"
						}
						"settings"
						{
							"haptic_intensity"		"1"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"dpad_west"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button dpad_left"
						}
						"settings"
						{
							"haptic_intensity"		"1"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
		}
	}
	"group"
	{
		"id"		"2"
		"mode"		"joystick_move"
		"name"		""
		"description"		""
		"inputs"
		{
			"click"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button JOYSTICK_RIGHT"
						}
						"settings"
						{
							"haptic_intensity"		"2"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
		}
	}
	"group"
	{
		"id"		"3"
		"mode"		"joystick_move"
		"name"		""
		"description"		""
		"inputs"
		{
			"click"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button JOYSTICK_LEFT"
						}
						"settings"
						{
							"haptic_intensity"		"2"
						}
					}
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button JOYSTICK_RIGHT"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
		}
	}
	"group"
	{
		"id"		"4"
		"mode"		"trigger"
		"name"		""
		"description"		""
		"inputs"
		{
			"click"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button TRIGGER_LEFT"
						}
						"settings"
						{
							"haptic_intensity"		"2"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
		}
		"settings"
		{
			"output_trigger"		"1"
		}
	}
	"group"
	{
		"id"		"5"
		"mode"		"trigger"
		"name"		""
		"description"		""
		"inputs"
		{
			"click"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button RSTICK_DOWN"
						}
						"settings"
						{
							"haptic_intensity"		"2"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
		}
		"settings"
		{
			"output_trigger"		"2"
		}
	}
	"group"
	{
		"id"		"6"
		"mode"		"joystick_move"
		"name"		""
		"description"		""
		"inputs"
		{
			"click"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button JOYSTICK_RIGHT"
						}
						"settings"
						{
							"haptic_intensity"		"2"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
		}
	}
	"group"
	{
		"id"		"8"
		"mode"		"joystick_move"
		"name"		""
		"description"		""
		"inputs"
		{
			"click"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button JOYSTICK_RIGHT"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
		}
	}
	"group"
	{
		"id"		"9"
		"mode"		"dpad"
		"name"		""
		"description"		""
		"inputs"
		{
			"dpad_north"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button DPAD_UP"
						}
						"settings"
						{
							"haptic_intensity"		"1"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"dpad_south"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button DPAD_DOWN"
						}
						"settings"
						{
							"haptic_intensity"		"1"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"dpad_east"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button DPAD_RIGHT"
						}
						"settings"
						{
							"haptic_intensity"		"1"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"dpad_west"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button DPAD_LEFT"
						}
						"settings"
						{
							"haptic_intensity"		"1"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
		}
		"settings"
		{
			"requires_click"		"0"
			"haptic_intensity_override"		"0"
		}
	}
	"group"
	{
		"id"		"7"
		"mode"		"switches"
		"name"		""
		"description"		""
		"inputs"
		{
			"button_escape"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button start"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"button_menu"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button RSTICK_RIGHT"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"left_bumper"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button shoulder_left"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"right_bumper"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button shoulder_right"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"button_back_left"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button RSTICK_LEFT"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"button_back_right"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button A"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"button_back_left_upper"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button RSTICK_UP"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"button_back_right_upper"
			{
				"activators"
				{
					"Full_Press"
					{
						"bindings"
						{
							"binding"		"xinput_button X"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
			"button_capture"
			{
				"activators"
				{
					"release"
					{
						"bindings"
						{
							"binding"		"controller_action system_key_1"
						}
					}
				}
				"disabled_activators"
				{
				}
			}
		}
	}
	"preset"
	{
		"id"		"0"
		"name"		"Default"
		"group_source_bindings"
		{
			"7"		"switch active"
			"0"		"button_diamond active"
			"3"		"joystick active"
			"4"		"left_trigger active"
			"5"		"right_trigger active"
			"8"		"right_joystick active"
			"9"		"dpad active"
		}
	}
	"settings"
	{
		"left_trackpad_mode"		"0"
		"right_trackpad_mode"		"0"
	}
}
```

***

#### Steam Input Layout 4
[Back to the Top](#community-creations-table-of-contents)

Replace with your Steam Input Layout and a brief description. 

***

#### Steam Input Layout 5
[Back to the Top](#community-creations-table-of-contents)

Replace with your Steam Input Layout and a brief description. 

***

#### Steam Input Layout 6
[Back to the Top](#community-creations-table-of-contents)

Replace with your Steam Input Layout and a brief description. 

***

#### Steam Input Layout 7
[Back to the Top](#community-creations-table-of-contents)

Replace with your Steam Input Layout and a brief description. 

***

### Dolphin
[Back to the Top](#community-creations-table-of-contents)

* [How to create Dolphin controller profiles](../../emulators/steamos/dolphin.md#how-to-create-dolphin-controller-profiles)
* [How to Share Dolphin controller profiles](#how-to-share-dolphin-profiles). 
* [How to Download Dolphin controller profiles](#how-to-download-dolphin-profiles)
* [How to Download Dolphin controller profiles and set it for a specific game](../../emulators/steamos/dolphin.md#how-to-set-dolphin-controller-profiles-on-a-per-game-basis)


***

## Getting Started With Dolphin Profiles
[Back to the Top](#community-creations-table-of-contents)

***

### How to Share Dolphin Profiles
[Back to the Top](#community-creations-table-of-contents)

This section will go over how to share and post your Dolphin controller layouts on this page. 

To begin, locate your profile layout:

Your Gamecube controller layouts are located here: `home/deck/.var/app/org.DolphinEmu.dolphin-emu/config/dolphin-emu/Profiles/GCPad`

Your Wii controller layouts are located here: `/home/deck/.var/app/org.DolphinEmu.dolphin-emu/config/dolphin-emu/Profiles/Wiimote`

**Note:** ~/.var is an invisible folder by default. In Dolphin (file manager), click the ☰ (hamburger menu) in the top right, click view hidden files to see these folders.

**Tutorial**

1. Create a new section on this page under Dolphin in the `Table of Contents`, refer to `Dolphin Config 1` as a sample
   1. At the moment, `Dolphin Config 4` through `Dolphin Config 6` can be edited and replaced with your templates. 
2. After locating your profile layout, click `Open with Kwrite`
3. Either:
    1. Right click, click `Select All`, right click, click `Copy`
    2. Press `Ctrl` + `A`, Press `Ctrl` + `C`
4. Paste the contents of the file into your newly created section
5. Place ``` at the top and the bottom of the pasted profile, refer to `Dolphin Config 1` as a sample
6. Save the page
7. You have now successfully shared your profile

***

### How to Download Dolphin Profiles
[Back to the Top](#community-creations-table-of-contents)

You may select a profile to download by choosing one from the list here: [Community Dolphin Profiles](#community-dolphin-profiles-table-of-contents).

After you have selected a profile, you may use the below tutorial to learn how to download it and use it in Dolphin. 

**Tutorial**

1. Copy the contents of a profile you would like to use by clicking the copy icon in the top right
    1. Visual Reference: <img src="https://user-images.githubusercontent.com/108900299/196857393-76dfa11b-ed76-464a-a665-4970505a848c.png" height="300">
2. In either the `Gamecube` or the `Wii` profile folders, right click, `Create New`, `Text File`
    1. Gamecube Profile Folder: `home/deck/.var/app/org.DolphinEmu.dolphin-emu/config/dolphin-emu/Profiles/GCPad`
    2. Wii Profile Folder: `/home/deck/.var/app/org.DolphinEmu.dolphin-emu/config/dolphin-emu/Profiles/Wiimote`
3. Paste the contents of a profile you would like to use
4. Save the profile, either matching the profile name or something descriptive with an `.ini` file extension
    1. Without the `.ini` file extension, the profile will not work
5. You now have successfully downloaded a profile 

**Note:** For instructions on how to set a Dolphin controller profile for a specific game, refer to: [How to Download Dolphin controller profiles and set it for a specific game](../../emulators/steamos/dolphin.md#how-to-set-dolphin-controller-profiles-on-a-per-game-basis)

***

### Community Dolphin Profiles
[Back to the Top](#community-creations-table-of-contents)

***

#### Community Dolphin Profiles Table of Contents

* [Wiimote Motion Controls With Nunchuck](#wiimote-motion-controls-with-nunchuck)
* [Wiimote Motion Controls With No Attachment](#wiimote-motion-controls-with-no-attachment)
* [Super Mario Galaxy 1 and 2](#super-mario-galaxy-1-and-2)
* [Gyro Steam Deck on Dolphin](#dolphin-config-4)
* [Dolphin Config 5](#dolphin-config-5)

***

##### Wiimote Motion Controls With Nunchuck
[Back to the Top](#community-creations-table-of-contents)

Credit: `TrickTrigger`

**REQUIRES STEAMDECKGYRODSU TO BE INSTALLED**

[How to Install SteamDeckGyroDSU](../../emudeck-application/steamos/emudeck-application-101.md#steamdeckgyrodsu)

This config is basically the Nunchuck config, with modifications to enable proper, true motion controls. This can be easily converted into a standalone Wii Remote config with motion by simply removing the Nunchuck in the Dolphin menu, but keep in mind that I swapped some buttons around, so you might want to tweak it if you do that.

_You are advised to examine the motion inputs so you can learn how to get SDGyroDSU to work properly with Dolphin. It's kind of a pain, since Dolphin registers it as a separate controller from the buttons. This config features workarounds so the issue is resolved._

Profile Name: `Wii_base_nunchuck_with_true_motion.ini`

```
[Profile]
Device = evdev/0/Microsoft X-Box 360 pad 0
Buttons/A = SOUTH
Buttons/B = `Full Axis 5+`
Buttons/1 = EAST
Buttons/2 = WEST
Buttons/- = SELECT
Buttons/+ = START
Buttons/Home = Return
IR/Vertical Offset = 12.0
IR/Total Yaw = 19.0
IR/Total Pitch = 22.0
IR/Calibration = 100.00 101.96 108.24 112.67 116.44 114.62 108.11 101.96 100.00 101.96 108.11 113.10 115.81 113.90 108.24 101.96 100.00 101.96 108.24 114.93 115.13 115.19 108.24 101.96 100.00 101.96 108.13 112.88 112.20 110.97 108.24 101.96
Tilt/Modifier/Range = 50.0
Shake/X = NORTH
Shake/Y = NORTH
Shake/Z = NORTH
IMUAccelerometer/Up = `DSUClient/0/steamdeckgyro:Accel Up`
IMUAccelerometer/Down = `DSUClient/0/steamdeckgyro:Accel Down`
IMUAccelerometer/Left = `DSUClient/0/steamdeckgyro:Accel Left`
IMUAccelerometer/Right = `DSUClient/0/steamdeckgyro:Accel Right`
IMUAccelerometer/Forward = `DSUClient/0/steamdeckgyro:Accel Forward`
IMUAccelerometer/Backward = `DSUClient/0/steamdeckgyro:Accel Backward`
IMUGyroscope/Pitch Up = `DSUClient/0/steamdeckgyro:Gyro Pitch Up`
IMUGyroscope/Pitch Down = `DSUClient/0/steamdeckgyro:Gyro Pitch Down`
IMUGyroscope/Roll Left = `DSUClient/0/steamdeckgyro:Gyro Roll Left`
IMUGyroscope/Roll Right = `DSUClient/0/steamdeckgyro:Gyro Roll Right`
IMUGyroscope/Yaw Left = `DSUClient/0/steamdeckgyro:Gyro Yaw Left`
IMUGyroscope/Yaw Right = `DSUClient/0/steamdeckgyro:Gyro Yaw Right`
IMUIR/Recenter = THUMBR
Extension = Nunchuk
Nunchuk/Buttons/C = TL
Nunchuk/Buttons/Z = `Full Axis 2+`
Nunchuk/Stick/Up = `Axis 1-`
Nunchuk/Stick/Down = `Axis 1+`
Nunchuk/Stick/Left = `Axis 0-`
Nunchuk/Stick/Right = `Axis 0+`
Nunchuk/Stick/Modifier/Range = 50.0
Nunchuk/Stick/Calibration = 100.00 101.96 107.70 111.02 112.30 107.98 106.91 101.96 100.00 101.96 108.24 113.14 114.55 111.79 108.24 101.96 100.00 101.96 108.24 113.60 114.92 113.33 108.24 101.96 100.00 101.96 108.24 110.60 109.10 108.88 108.24 101.96
Nunchuk/Tilt/Modifier/Range = 50.0
Nunchuk/Shake/X = TR
Nunchuk/Shake/Y = TR
Nunchuk/Shake/Z = TR
Classic/Buttons/A = EAST
Classic/Buttons/B = SOUTH
Classic/Buttons/X = WEST
Classic/Buttons/Y = NORTH
Classic/Buttons/ZL = TL
Classic/Buttons/ZR = TR
Classic/Buttons/- = SELECT
Classic/Buttons/+ = START
Classic/Left Stick/Up = `Axis 1-`
Classic/Left Stick/Down = `Axis 1+`
Classic/Left Stick/Left = `Axis 0-`
Classic/Left Stick/Right = `Axis 0+`
Classic/Left Stick/Modifier/Range = 50.0
Classic/Left Stick/Calibration = 100.00 101.96 107.63 112.05 110.67 111.78 105.49 101.89 100.00 101.96 108.24 112.08 112.34 109.50 107.04 101.96 100.00 101.96 106.95 114.00 115.73 117.91 108.24 101.96 100.00 101.96 108.24 106.97 109.81 109.07 108.24 101.96
Classic/Right Stick/Up = `Axis 4-`
Classic/Right Stick/Down = `Axis 4+`
Classic/Right Stick/Left = `Axis 3-`
Classic/Right Stick/Right = `Axis 3+`
Classic/Right Stick/Modifier/Range = 50.0
Classic/Right Stick/Calibration = 100.00 101.96 107.60 112.29 113.04 111.78 108.24 101.96 100.00 101.96 108.24 109.67 111.62 109.71 104.61 101.96 100.00 101.96 108.12 116.15 116.97 117.85 107.67 101.96 100.00 101.96 108.24 107.11 107.45 110.21 108.24 101.96
Classic/Triggers/L = `Full Axis 2+`
Classic/Triggers/R = `Full Axis 5+`
Classic/Triggers/L-Analog = `Full Axis 2+`
Classic/Triggers/R-Analog = `Full Axis 5+`
Guitar/Stick/Modifier/Range = 50.0
Drums/Stick/Modifier/Range = 50.0
Turntable/Stick/Modifier/Range = 50.0
uDraw/Stylus/Modifier/Range = 50.0
Drawsome/Stylus/Modifier/Range = 50.0
Rumble/Motor = Strong
D-Pad/Up = `Axis 7-`
D-Pad/Down = `Axis 7+`
D-Pad/Left = `Axis 6-`
D-Pad/Right = `Axis 6+`
Hotkeys/Upright Toggle = SELECT&THUMBR
```

***

##### Wiimote Motion Controls With No Attachment
[Back to the Top](#community-creations-table-of-contents)

Credit: `Trick Trigger`

**REQUIRES STEAMDECKGYRODSU TO BE INSTALLED**

[How to Install SteamDeckGyroDSU](../../emudeck-application/steamos/emudeck-application-101.md#steamdeckgyrodsu)

This config is the Nunchuck config with no attachment, and modifications to enable proper, true motion controls. Keep in mind that I swapped some buttons around, so you might want to tweak it if you do that.

_You are advised to examine the motion inputs so you can learn how to get SDGyroDSU to work properly with Dolphin. It's kind of a pain, since Dolphin registers it as a separate controller from the buttons. This config features workarounds so the issue is resolved._

Profile Name: `Wii_no_attachment_with_true_motion.ini`

```
[Profile]
Device = evdev/0/Microsoft X-Box 360 pad 0
Buttons/A = SOUTH
Buttons/B = `Full Axis 5+`
Buttons/1 = EAST
Buttons/2 = NORTH
Buttons/- = SELECT
Buttons/+ = START
Buttons/Home = Return
IR/Vertical Offset = 12.0
IR/Total Yaw = 19.0
IR/Total Pitch = 22.0
IR/Auto-Hide = True
IR/Up = `Axis 4-`
IR/Down = `Axis 4+`
IR/Left = `Axis 3-`
IR/Right = `Axis 3+`
IR/Hide = THUMBR
IR/Calibration = 100.00 101.96 108.24 112.67 116.44 114.62 108.11 101.96 100.00 101.96 108.11 113.10 115.81 113.90 108.24 101.96 100.00 101.96 108.24 114.93 115.13 115.19 108.24 101.96 100.00 101.96 108.13 112.88 112.20 110.97 108.24 101.96
Tilt/Modifier/Range = 50.0
Shake/X = EAST
Shake/Y = EAST
Shake/Z = EAST
IMUAccelerometer/Up = `DSUClient/0/steamdeckgyro:Accel Up`
IMUAccelerometer/Down = `DSUClient/0/steamdeckgyro:Accel Down`
IMUAccelerometer/Left = `DSUClient/0/steamdeckgyro:Accel Left`
IMUAccelerometer/Right = `DSUClient/0/steamdeckgyro:Accel Right`
IMUAccelerometer/Forward = `DSUClient/0/steamdeckgyro:Accel Forward`
IMUAccelerometer/Backward = `DSUClient/0/steamdeckgyro:Accel Backward`
IMUGyroscope/Pitch Up = `DSUClient/0/steamdeckgyro:Gyro Pitch Up`
IMUGyroscope/Pitch Down = `DSUClient/0/steamdeckgyro:Gyro Pitch Down`
IMUGyroscope/Roll Left = `DSUClient/0/steamdeckgyro:Gyro Roll Left`
IMUGyroscope/Roll Right = `DSUClient/0/steamdeckgyro:Gyro Roll Right`
IMUGyroscope/Yaw Left = `DSUClient/0/steamdeckgyro:Gyro Yaw Left`
IMUGyroscope/Yaw Right = `DSUClient/0/steamdeckgyro:Gyro Yaw Right`
IMUIR/Recenter = TR
Nunchuk/Buttons/C = TL
Nunchuk/Buttons/Z = `Full Axis 2+`
Nunchuk/Stick/Up = `Axis 1-`
Nunchuk/Stick/Down = `Axis 1+`
Nunchuk/Stick/Left = `Axis 0-`
Nunchuk/Stick/Right = `Axis 0+`
Nunchuk/Stick/Modifier/Range = 50.0
Nunchuk/Stick/Calibration = 100.00 101.96 107.70 111.02 112.30 107.98 106.91 101.96 100.00 101.96 108.24 113.14 114.55 111.79 108.24 101.96 100.00 101.96 108.24 113.60 114.92 113.33 108.24 101.96 100.00 101.96 108.24 110.60 109.10 108.88 108.24 101.96
Nunchuk/Tilt/Modifier/Range = 50.0
Nunchuk/Shake/X = NORTH
Nunchuk/Shake/Y = NORTH
Nunchuk/Shake/Z = NORTH
Classic/Buttons/A = EAST
Classic/Buttons/B = SOUTH
Classic/Buttons/X = WEST
Classic/Buttons/Y = NORTH
Classic/Buttons/ZL = TL
Classic/Buttons/ZR = TR
Classic/Buttons/- = SELECT
Classic/Buttons/+ = START
Classic/Left Stick/Up = `Axis 1-`
Classic/Left Stick/Down = `Axis 1+`
Classic/Left Stick/Left = `Axis 0-`
Classic/Left Stick/Right = `Axis 0+`
Classic/Left Stick/Modifier/Range = 50.0
Classic/Left Stick/Calibration = 100.00 101.96 107.63 112.05 110.67 111.78 105.49 101.89 100.00 101.96 108.24 112.08 112.34 109.50 107.04 101.96 100.00 101.96 106.95 114.00 115.73 117.91 108.24 101.96 100.00 101.96 108.24 106.97 109.81 109.07 108.24 101.96
Classic/Right Stick/Up = `Axis 4-`
Classic/Right Stick/Down = `Axis 4+`
Classic/Right Stick/Left = `Axis 3-`
Classic/Right Stick/Right = `Axis 3+`
Classic/Right Stick/Modifier/Range = 50.0
Classic/Right Stick/Calibration = 100.00 101.96 107.60 112.29 113.04 111.78 108.24 101.96 100.00 101.96 108.24 109.67 111.62 109.71 104.61 101.96 100.00 101.96 108.12 116.15 116.97 117.85 107.67 101.96 100.00 101.96 108.24 107.11 107.45 110.21 108.24 101.96
Classic/Triggers/L = `Full Axis 2+`
Classic/Triggers/R = `Full Axis 5+`
Classic/Triggers/L-Analog = `Full Axis 2+`
Classic/Triggers/R-Analog = `Full Axis 5+`
Guitar/Stick/Modifier/Range = 50.0
Drums/Stick/Modifier/Range = 50.0
Turntable/Stick/Modifier/Range = 50.0
uDraw/Stylus/Modifier/Range = 50.0
Drawsome/Stylus/Modifier/Range = 50.0
Rumble/Motor = Strong
D-Pad/Up = `Axis 7-`
D-Pad/Down = `Axis 7+`
D-Pad/Left = `Axis 6-`
D-Pad/Right = `Axis 6+`
Hotkeys/Sideways Toggle = SELECT&THUMBR
```


***

##### Super Mario Galaxy 1 and 2
[Back to the Top](#community-creations-table-of-contents)

Credit: `Jigs`

***

**Tweaked Settings**

* Right bumper is duck
* Right trigger acts as secondary 'B' button, and does things like shooting star bits
* Clicking the right analog stick centers the camera
* Holding the left trigger activates "holding the wiimote up right", and turns the left analog stick into tilt controls.
* The right trackpad acts as a mouse for the wii pointer (you have to change this in Steam Input as well, by turning the trackpad into a mouse)
* The right trackpad click acts as secondary 'A' button

***

**Optional**

* Attach profile to Super Mario Galaxy 1 and 2 specifically: <img src="https://user-images.githubusercontent.com/108900299/211655773-8b315ecd-c203-4c95-be0a-09355f7d6d51.png" height="400">

***

**Download:** [https://cdn.discordapp.com/attachments/977206955871440966/977207020220448808/wiigalaxy.ini](https://cdn.discordapp.com/attachments/977206955871440966/977207020220448808/wiigalaxy.ini)

***


##### Gyro Steam Deck on Dolphin
[Back to the Top](#community-creations-table-of-contents)

Credit: [_punto16_](https://github.com/punto16)

I used the text of Trick Trigger from the profile he shared as a template so here his credits:

[Wiimote Motion Controls With Nunchuck](#wiimote-motion-controls-with-nunchuck)

[Wiimote Motion Controls With No Attachment](#wiimote-motion-controls-with-no-attachment)


**REQUIRES STEAMDECKGYRODSU TO BE INSTALLED**

[How to Install SteamDeckGyroDSU](../../emudeck-application/steamos/emudeck-application-101.md#steamdeckgyrodsu)

This config is basically the one default on dolphin when you install it with EmuDeck, but it detects as default Xbox 360 gamepad (in game it's in reality steam deck's controlls). So, this config just adds to Xbox 360 controller detected the gyro inputs of the steam deck with help of steam deck gyrodsu.

_You are advised to examine the motion inputs so you can learn how to get SDGyroDSU to work properly with Dolphin. It's kind of a pain, since Dolphin registers it as a separate controller from the buttons. This config features workarounds so the issue is resolved._

Profile Name: `Gyro_SteamDeck_on_Dolphin.ini`

```
[Profile]
Device = evdev/0/Microsoft X-Box 360 pad 0
Buttons/A = SOUTH
Buttons/B = EAST
Buttons/1 = NORTH
Buttons/2 = WEST
Buttons/- = SELECT
Buttons/+ = START
Buttons/Home = Return
D-Pad/Up = `Axis 7-`
D-Pad/Down = `Axis 7+`
D-Pad/Left = `Axis 6-`
D-Pad/Right = `Axis 6+`
IR/Vertical Offset = 12.0
IR/Total Yaw = 19.0
IR/Total Pitch = 22.0
IR/Auto-Hide = True
IR/Up = `XInput2/0/Virtual core pointer:Cursor Y-`|`Axis 4-`
IR/Down = `XInput2/0/Virtual core pointer:Cursor Y+`|`Axis 4+`
IR/Left = `XInput2/0/Virtual core pointer:Cursor X-`|`Axis 3-`
IR/Right = `XInput2/0/Virtual core pointer:Cursor X+`|`Axis 3+`
IR/Hide = THUMBR
IR/Calibration = 100.00 101.96 108.24 112.67 116.44 114.62 108.11 101.96 100.00 101.96 108.11 113.10 115.81 113.90 108.24 101.96 100.00 101.96 108.24 114.93 115.13 115.19 108.24 101.96 100.00 101.96 108.13 112.88 112.20 110.97 108.24 101.96
Shake/X = TL
Shake/Y = TL
Shake/Z = TL
Tilt/Forward = `Full Axis 2+`&`Full Axis 1-`
Tilt/Backward = `Full Axis 2+`&`Full Axis 1+`
Tilt/Left = `Full Axis 2+`&`Full Axis 0-`
Tilt/Right = `Full Axis 2+`&`Full Axis 0+`
Tilt/Modifier/Range = 50.0
IMUIR/Enabled = False
IMUAccelerometer/Up = `DSUClient/0/steamdeckgyro:Accel Up`
IMUAccelerometer/Down = `DSUClient/0/steamdeckgyro:Accel Down`
IMUAccelerometer/Left = `DSUClient/0/steamdeckgyro:Accel Left`
IMUAccelerometer/Right = `DSUClient/0/steamdeckgyro:Accel Right`
IMUAccelerometer/Forward = `DSUClient/0/steamdeckgyro:Accel Forward`
IMUAccelerometer/Backward = `DSUClient/0/steamdeckgyro:Accel Backward`
IMUGyroscope/Pitch Up = `DSUClient/0/steamdeckgyro:Gyro Pitch Up`
IMUGyroscope/Pitch Down = `DSUClient/0/steamdeckgyro:Gyro Pitch Down`
IMUGyroscope/Roll Left = `DSUClient/0/steamdeckgyro:Gyro Roll Left`
IMUGyroscope/Roll Right = `DSUClient/0/steamdeckgyro:Gyro Roll Right`
IMUGyroscope/Yaw Left = `DSUClient/0/steamdeckgyro:Gyro Yaw Left`
IMUGyroscope/Yaw Right = `DSUClient/0/steamdeckgyro:Gyro Yaw Right`
Hotkeys/Sideways Toggle = SELECT&THUMBR
Extension = Nunchuk
Nunchuk/Buttons/C = TR
Nunchuk/Buttons/Z = `Full Axis 5+`
Nunchuk/Stick/Up = `Axis 1-`
Nunchuk/Stick/Down = `Axis 1+`
Nunchuk/Stick/Left = `Axis 0-`
Nunchuk/Stick/Right = `Axis 0+`
Nunchuk/Stick/Modifier/Range = 50.0
Nunchuk/Stick/Calibration = 100.00 101.96 107.70 111.02 112.30 107.98 106.91 101.96 100.00 101.96 108.24 113.14 114.55 111.79 108.24 101.96 100.00 101.96 108.24 113.60 114.92 113.33 108.24 101.96 100.00 101.96 108.24 110.60 109.10 108.88 108.24 101.96
Nunchuk/Shake/X = `Full Axis 2+`
Nunchuk/Shake/Y = `Full Axis 2+`
Nunchuk/Shake/Z = `Full Axis 2+`
Nunchuk/Tilt/Modifier/Range = 50.0
Classic/Buttons/A = EAST
Classic/Buttons/B = SOUTH
Classic/Buttons/X = WEST
Classic/Buttons/Y = NORTH
Classic/Buttons/ZL = TL
Classic/Buttons/ZR = TR
Classic/Buttons/- = SELECT
Classic/Buttons/+ = START
Classic/Left Stick/Up = `Axis 1-`
Classic/Left Stick/Down = `Axis 1+`
Classic/Left Stick/Left = `Axis 0-`
Classic/Left Stick/Right = `Axis 0+`
Classic/Left Stick/Modifier/Range = 50.0
Classic/Left Stick/Calibration = 100.00 101.96 107.63 112.05 110.67 111.78 105.49 101.89 100.00 101.96 108.24 112.08 112.34 109.50 107.04 101.96 100.00 101.96 106.95 114.00 115.73 117.91 108.24 101.96 100.00 101.96 108.24 106.97 109.81 109.07 108.24 101.96
Classic/Right Stick/Up = `Axis 4-`
Classic/Right Stick/Down = `Axis 4+`
Classic/Right Stick/Left = `Axis 3-`
Classic/Right Stick/Right = `Axis 3+`
Classic/Right Stick/Modifier/Range = 50.0
Classic/Right Stick/Calibration = 100.00 101.96 107.60 112.29 113.04 111.78 108.24 101.96 100.00 101.96 108.24 109.67 111.62 109.71 104.61 101.96 100.00 101.96 108.12 116.15 116.97 117.85 107.67 101.96 100.00 101.96 108.24 107.11 107.45 110.21 108.24 101.96
Classic/Triggers/L = `Full Axis 2+`
Classic/Triggers/R = `Full Axis 5+`
Classic/Triggers/L-Analog = `Full Axis 2+`
Classic/Triggers/R-Analog = `Full Axis 5+`
Guitar/Stick/Modifier/Range = 50.0
Drums/Stick/Modifier/Range = 50.0
Turntable/Stick/Modifier/Range = 50.0
uDraw/Stylus/Modifier/Range = 50.0
Drawsome/Stylus/Modifier/Range = 50.0
Rumble/Motor = Strong
Options/Upright Wiimote = `Full Axis 2+`
``` 

***


##### Dolphin Config 6
[Back to the Top](#community-creations-table-of-contents)

Replace this with your controller config and a brief description. 

***

## Special Game Configurations
[Back to the Top](#community-creations-table-of-contents)

**Important:** This section is for game configurations that require elaborate setup. For minor tweaks and settings, please use Manacharge's community database. You can link back here in the community database as well. 

You can contribute to the community games database here: [https://docs.google.com/forms/d/e/1FAIpQLScavGFOuGpEVpyHdRVcPjdrCEquG9ItBaloa8Q0XaiNlu_Afg/viewform](https://docs.google.com/forms/d/e/1FAIpQLScavGFOuGpEVpyHdRVcPjdrCEquG9ItBaloa8Q0XaiNlu_Afg/viewform)

You can view the community database here: [https://docs.google.com/spreadsheets/d/1fRqvAh_wW8Ho_8i966CCSBgPJ2R_SuDFIvvKsQCv05w/edit?usp=sharing](https://docs.google.com/spreadsheets/d/1fRqvAh_wW8Ho_8i966CCSBgPJ2R_SuDFIvvKsQCv05w/edit?usp=sharing)

***

### RPCS3 (Playstation 3)
[Back to the Top](#community-creations-table-of-contents)

[How to set up and configure RPCS3](../../emulators/steamos/rpcs3.md#getting-started-with-rpcs3)

***

#### Metal Gear Solid 4
[Back to the Top](#community-creations-table-of-contents)

Credit: `AwkwaBear`

**NOTE:** This guide is just to set up MGS4 and getting it ***RUNNING WITHOUT CRASHING*** on Steam Deck, much work is still needed to get it working with an optimized playable configuration free from audio issues and framerate hitching. This page is still a work in progress and will updated as better configuration options are determined

***

**Tutorial**

MGS4 when first imported into RPCS3 will freeze natively and needs some work to get functioning.

I believe trying to patch the file using the built in RPCS3 patch manager will not fix the issue and the game needs to be patched manually to get it working. (Let me know if anyone else is able to prove otherwise)

1. If you haven't done so already, follow the PS3 setup guide from RGC to get mgs4 added and rpcs3 setup
    - [https://retrogamecorps.com/2022/10/16/steam-deck-emulation-starter-guide/](https://retrogamecorps.com/2022/10/16/steam-deck-emulation-starter-guide/)
2. Patch using the "Manually adding custom patches" section on this page and the MGS4 patch section in the second link. (You can make the patch yourself using the rpcs3 wiki link or download the one I have made from my github repo linked just below)
    - [https://wiki.rpcs3.net/index.php?title=Help:Game_Patches#Using_game_patches](https://wiki.rpcs3.net/index.php?title=Help:Game_Patches#Using_game_patches)
    - [https://wiki.rpcs3.net/index.php?title=Help:Game_Patches/Canary](https://wiki.rpcs3.net/index.php?title=Help:Game_Patches/Canary)
    - Link to premade manual patch: [https://github.com/agasbarro36/MGS4-RPCS3-Manual-Patch](https://github.com/agasbarro36/MGS4-RPCS3-Manual-Patch)
3. When the instructions say "Save the file in relevant location:" you need to navigate to save it in the flatpack location instead of the usual Linux one. _**NOTE: ~/.VAR is a hidden directory and you need to click show hidden files in dolphin file explorer to see it. **_
	- <img src="https://user-images.githubusercontent.com/19947797/207243548-ad1eb95d-3608-442a-a8de-c1008087541f.png" height="600">
    - The location is: `~/.var/app/net.rpcs3.RPCS3/config/rpcs3/patches`
4. Open RPCS3 Navigate to the Patch Manager (Select Manage > Game Patches) and tick the checkbox corresponding to the patches you wish to apply.
    - Select Metal Gear solid 4: Guns of the Patriots in the game list and click the tab to expand
    - expand both tabs for the version of the game you have
    -  select the `cellspurs urgent commands hack - 4.8x` (where 'x' is the ps3 firmware version you installed)
    -  select `Crash Fix`
    -  select `Disable Shadows`
    -  select `Disable spawned effects`
    -  select `Reduce Stage quality`
    -  select `Unlock FPS`
	- <img src="https://user-images.githubusercontent.com/19947797/196624586-81718981-902d-43f1-8a4d-28d5a718a79b.png" height="600">
5. Apply and Save your patch settings then run the game
6. Here are the current GPU settings I have tested but are still yet to be optimized 
	- <img src="https://user-images.githubusercontent.com/19947797/207242116-712babf0-ad8f-46a8-8d21-2dd24e08fc77.png" height="600">



***

The game takes ~2 hours to install initially so be ready for a long wait
	
I recommend adding all the patches to boost performance as much as possible. This game is really hard to run so you need all the help you can get.
	
These are just the settings I got to work, maybe mess around with it and let me know if something works better and I can update this guide. 
	
Good luck out there, this game will work now albeit running kinda like trash, there's a lot of frame inconsistencies and audio either cutting out or missing altogether but it is technically able to be played (though I would not consider it above the threshold of "playable") I think the results are promising and with some community tweaking we can get this masterpiece to generally playable state on steam deck.

You can find the guide here: https://github.com/dragoonDorise/EmuDeck/wiki/Metal-Gear-Solid-4---RPCS3-Setup-Guide.

***

### Yuzu (Nintendo Switch)
[Back to the Top](#community-creations-table-of-contents)

[How to set up and configure Yuzu](../../emulators/steamos/yuzu.md#getting-started-with-yuzu)

***

#### The Legend Of Zelda: Link's Awakening
[Back to the Top](#community-creations-table-of-contents)

**Credit:** `SardineCat`

**Recommended Settings**

* Yuzu on portable mode (idk if docked loses somes frames)
* accuracy on high, cpu on unsafe, 
* make sure you have powertools and then use smt off
    * [How to install Power Tools](../../emudeck-application/steamos/emudeck-application-101.md#power-tools)
* use v1.0.0 of the game 

**Recommended Mods**

* [How to install mods](../../emulators/steamos/yuzu.md#how-to-install-mods)
* This mod disables the blur effect which also increases some performance giving you some frames back: [https://cdn.discordapp.com/attachments/356187763139280896/798516893840965632/Blur_Removal.zip](https://cdn.discordapp.com/attachments/356187763139280896/798516893840965632/Blur_Removal.zip)
* The 60fps mod found here: [https://cdn.discordapp.com/attachments/356187763139280896/724250990928461834/Stable-60fps-v2.zip](https://cdn.discordapp.com/attachments/356187763139280896/724250990928461834/Stable-60fps-v2.zip)

**How well does the game perform after these tweaks?**

* This all equates to 60fps almost everywhere, I lose a couple of frames in Mabe Village and Animal Village but its not a big deal IMO.
* Fixes the invisible Chain Chomp bug

***

## Tools and Utilities
[Back to the Top](#community-creations-table-of-contents)

***

### How to Set Up SyncThing
[Back to the Top](#community-creations-table-of-contents)

[SyncThing](https://syncthing.net/) is a free self hosted "cloud" solution. There are limitations, the biggest here with the steam deck and the way EmuDeck moves/renames folders and the use of symlinks which is a “virtual file or folder” that can point to another. This is VERY nice, but due to the nature of differing filesystems, there is a reason SyncThing does not support this, and this tutorial avoids symlinks. Emudeck does make a few changes where syncing is not as straightforward as it could be, simply because the devs changed the default folder via the emulator. PCSX2 savestates and memcard folders are not only named differently from default but also moved from their default directory.
 
On the PC/Mac end, you will want to setup SynctThing to the corresponding location which will differ for each user. Just use your head, and would be wise to copy the same `Ignore Patterns`

Ryujinx and Yuzu, I find it easiest to share the entire `NAND` (Yuzu) / `User` (Ryujinx) so that the user ID is the same on your OTHER device, and if the save is locked to an ID, you still have access to it. This does mean, before setting up Syncthing, BACKUP BACKUP BACKUP! Choose your Syncthing `File Versioning` as desired. Some systems/games may save often (IE Nintendo Switch) causing more overhead or even problems with a file versioning choice. 

**Steam Deck Syncthing paths and Ignore Patterns:**

MAME SaveData:
    
    path="/home/deck/.mame"
    Ignore Patterns
    // DO NOT IGNORE
    !/nvram
    !/sta
    // IGNORE
    *
    .DS_Store

Flycast SaveData:
    
    path="/run/media/mmcblk0p1/Emulation/saves/flycast/saves"

DuckStation MemCards:
    
    path="/run/media/mmcblk0p1/Emulation/saves/duckstation/saves"

RetroArch SaveData: 
    
    path="/home/deck/.var/app/org.libretro.RetroArch/config/retroarch"
    Ignore Patterns
    // DO NOT IGNORE
    !/states
    !/saves
    // IGNORE
    *
    .DS_Store

Ryujinx SaveData:

    path="/home/deck/.config/Ryujinx/bis/user/"

RPCS3 SaveData:
    
    path="/run/media/mmcblk0p1/Emulation/saves/rpcs3/saves"

Dolphin SaveData:

    path="/home/deck/.var/app/org.DolphinEmu.dolphin-emu/data/dolphin-emu
    Ignore Patterns
    // DO NOT IGNORE
    !/GC
    !/Wii
    !/GBA
    !/states
    !/StateSaves
    // IGNORE
    *
    .DS_Store

PrimeHack SaveData:
    
    path="/home/deck/.var/app/io.github.shiiion.primehack/data/dolphin-emu"
    Ignore Patterns
    // DO NOT IGNORE
    !/GC
    !/Wii
    !/GBA
    !/states
    !/StateSaves
    // IGNORE
    *
    .DS_Store

PPSSPP SaveData

    path="/home/deck/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP"
    Ignore Patterns
    // DO NOT IGNORE
    !/PPSSPP_STATE
    !/SAVEDATA
    // IGNORE
    *
    .DS_Store

Citra SaveData:

    path="/home/deck/.var/app/org.citra_emu.citra/data/citra-emu"
    Ignore Patterns:
    // DO NOT IGNORE
    !/cheats
    !/nand
    !/sdmc
    !/sysdata
    // IGNORE
    *
    .DS_Store

PCSX2 SaveStates:

    path="/run/media/mmcblk0p1/Emulation/saves/pcsx2/states"

PCSX2 MemCards:

    path="/run/media/mmcblk0p1/Emulation/saves/pcsx2/saves"

Yuzu NAND:

    path="/run/media/mmcblk0p1/Emulation/storage/yuzu/nand/"

![Syncthing image](https://oomsgfx.com/misc/Posts%20on%20Forums/Computer/SD_Syncthing_Example.png)

**Permissions:**

Syncthing will need access to any folder in `~/.var`
Install then open *FlatSeal* (A Permissions Editor with nice GUI, can be downloaded/installed via Discover in desktop mode)

Open Flatseal and click on Synching GTK>Filesystem>Other Files

    ~/.var/app/io.github.shiion.primehack/data/dolphin-emu
    ~/.var/app/org.citra_emu.citra/data/citra-emu
    ~/.var/app/org.DolphinEmu.dolphin-emu/data/dolphin-emu
    ~/.var/app/org.libretro.RetroArch/config/retroarch
    ~/.var/app/org.ppsspp.PPSSPP/config/ppsspp/PSP

Flatseal example via Steam Deck:

![Flatseal image](https://oomsgfx.com/misc/Posts%20on%20Forums/Computer/syncthing-flatseal.png)

**Start Syncthing Automatically:**

Quit the Syncthing Daemon

Open Konsole and type 

    nano ~/.config/systemd/user/syncthing.service

Input this text:
    
    [Unit]
    Description=Syncthing

    [Service]
    Type=simple
    ExecStart=flatpak run --command=syncthing me.kozec.syncthingtk
    Restart=on-failure
    RestartSec=1
    SuccessExitStatus=3 4

    [Install]
    WantedBy=default.target

Save by typing the key command: Control O and pressing enter to confirm.

Continue in Konsole and type:

    systemctl --user enable syncthing

    systemctl --user start syncthing

If you wish to disable Syncthing starting @ launch:
   
    systemctl --user stop syncthing

    systemctl --user disable syncthing

If you use Decky, change the syncthing GUI port so it does not conflict to port 8384
![Syncthing Port](https://oomsgfx.com/misc/Posts%20on%20Forums/Computer/Syncthing%20Port%20Change.png)

**or** run this command via Konsole:

    systemctl --user stop syncthing

    sed -i 's/<address>127\.0\.0\.1:8080<\/address>/<address>127.0.0.1:8384<\/address>/' ~/.var/app/me.kozec.syncthingtk/config/syncthing/config.xml

    systemctl --user start syncthing


Anyway, now with this, you have a roadmap to sync anything else that you desire! As to other non-console saves, remember some are not compatible between systems: lookup linux Tomb Raider vs Windows Tomb Raider. Now smack the devs heads for that one.
Now if I can figure out a way to share prefixes between non-steam games so that I can sync C:Users/user/Appdata etc etc..... then all my non-steam games do not need individual Syncthing setup outside of a very convoluted Ignore Files list.

***

### How to Use ROM Hacks
[Back to the Top](#community-creations-table-of-contents)

**ROM Hack Sources**

_This list is not exhaustive_

* ROMHacking: [https://www.romhacking.net/](https://www.romhacking.net/)
* GBAtemp: [https://gbatemp.net/](https://gbatemp.net/)
* PokeCommunity: [https://www.pokecommunity.com/](https://www.pokecommunity.com/)
* Metroid Construction: [https://metroidconstruction.com/hacks.php](https://metroidconstruction.com/hacks.php)
* SegaXtreme: [https://segaxtreme.net/resources/categories/translations.9/](https://segaxtreme.net/resources/categories/translations.9/)
* GameBanana: [https://gamebanana.com/](https://gamebanana.com/)

**IMPORTANT** 

  * Everything can be done on the Steam Deck itself
  * If you plan on using Steam ROM Manager to add this ROM Hack to Steam, it may not have art yet on [https://www.steamgriddb.com/](https://www.steamgriddb.com/). If it does not have art, create a page here: [https://www.steamgriddb.com/](https://www.steamgriddb.com/) and locate some custom art for the ROM Hack so others can use it in the future as well. 
  * Not all ROM Hacks can be applied using the following method. For ROM Hacks that do not use the below method and do not have a Linux equivalent program to apply patches, you can either use Wine/Proton (through Lutris or Steam), or you can use a Windows computer to apply these patches and transfer over the patched ROM Hack. 

**Tutorial**

1. Locate a ROM Hack you would like to use and its associated game ROM
    1. Example: 
        * File 1: A clean ROM of Pokemon Emerald for the Nintendo Gameboy Advance
        * File 2: A ROM Hack that turns Pokemon Emerald into a roguelike: [https://www.pokecommunity.com/showthread.php?t=479406](https://www.pokecommunity.com/showthread.php?t=479406)
    2. Your ROM Hack patch file may end with one of the following file extensions: `IPS`, `UPS`, `APS`, `BPS`, `RUP`, `PPF`, `MOD`, `XDELTA`, `VCDIFF`
2.  (Optional) Some ROM Hacks expect a specific hash, use [https://www.romhacking.net/hash/](https://www.romhacking.net/hash/), to check the hash of your ROM
    1. You can also check hashes in the Dolphin file manager on the Steam Deck by doing the following: 
          1. Right click the ROM
          2. Click Properties
          3. Click the Checksums tab
          4. Click `Calculate` to the right of `MD5`
3. Open [https://www.romhacking.net/patch/](https://www.romhacking.net/patch/)
4. For the top field, `ROM File`, browse to your clean ROM
5. For the bottom field, `Patch File`, browse to your patch
6. Click `Apply Patch` 
7. Save this newly patched ROM, rename it to match the ROM Hack, and place it in the respective system folder within `Emulation/roms`



***

## How to Contribute to EmuDeck
[Back to the Top](#community-creations-table-of-contents)

***

### How to Submit an Emulator Package
[Back to the Top](#community-creations-table-of-contents)

To submit an emulator for integration into EmuDeck, use the following template:

**Create an issue and pull request to add an emulator to EmuDeck.**

Include the following configurations:

* Create a .sh file for the emulator in `Emulation/tools/launchers`
* Create a Steam ROM Manager Parser
* Create an emulator function, to download the emulator and configure proper permissions
* Create a storage directory, if necessary, in `Emulation/storage`
* Configure BIOS directory, if necessary, in `Emulation/bios`
    * If not doable, create a BIOS link in `Emulation/bios`
* Configure emulator saves location in `Emulation/saves`
    * If not doable, create a saves link in `Emulation/saves`
* Create a controller profile
* Configure hotkeys
    * If not doable using Steam Deck buttons, create a Steam input profile mapping keyboard keys to Steam Deck buttons
* Create controller profiles for multiplayer

For a list of standalone emulators that work on Steam Deck, refer to [https://gist.github.com/rawdatafeel/9873683285d68025846424adfd5c4296](https://gist.github.com/rawdatafeel/9873683285d68025846424adfd5c4296). 

*** 
