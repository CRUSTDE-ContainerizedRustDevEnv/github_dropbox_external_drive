# github_dropbox_external_drive

**File Workflow for backups for CRUSTDE**  
***version: 2024.326.1347 date: 2024-03-26 author: [bestia.dev](https://bestia.dev) repository: [GitHub](https://github.com/CRUSTDE-ContainerizedRustDevEnv/github_dropbox_external_drive)***  

 ![tutorial](https://img.shields.io/badge/tutorial-yellow)
 ![License](https://img.shields.io/badge/license-MIT-blue.svg)
 ![github_dropbox_external_drive](https://bestia.dev/webpage_hit_counter/get_svg_image/1662259186.svg)

 ![logo](https://raw.githubusercontent.com/CRUSTDE-ContainerizedRustDevEnv/CRUSTDE_Containerized_Rust_DevEnv/main/images/crustde_250x250.png)
 github_dropbox_external_drive is a member of the [CRUSTDE-ContainerizedRustDevEnv](https://github.com/orgs/CRUSTDE-ContainerizedRustDevEnv/repositories?q=sort%3Aname-asc) project.

 [![Lines in md](https://img.shields.io/badge/Lines_in_markdown-136-green.svg)](https://github.com/CRUSTDE-ContainerizedRustDevEnv/github_dropbox_external_drive
)

Hashtags: #rustlang #tutorial #buildtool #developmenttool  
My projects on GitHub are more like a tutorial than a finished product: [bestia-dev tutorials](https://github.com/bestia-dev/tutorials_rust_wasm).

## CRUSTDE - Containerized Rust Development Environment

These days I mostly program with Rust on Linux.  
My primary desktop is Win10. Inside it I have WSL2, which is a Linux Virtual Machine. There I installed Debian 12 Bookworm. And now I can use a Linux container with Podman. 

I use `CRUSTDE - Containerized Rust Development Environment` described here <https://github.com/CRUSTDE-ContainerizedRustDevEnv/crustde_cnt_img_pod>.  
This CRUSTDE container is ephemeral and can be destroyed at any time. The important files inside it must be pushed to GitHub, or else they will be destroyed with the CRUSTDE container.  

[//]: # (auto_plantuml start)
<!-- markdownlint-disable MD033 -->
<details><summary>plantuml code:</summary>
<!-- markdownlint-enable MD033 -->

```plantuml
@startuml
GitHub -> CRUSTDE: clone, pull
CRUSTDE -> GitHub: push
@enduml
```

</details>

![svg_github_container](https://github.com/CRUSTDE-ContainerizedRustDevEnv/github_dropbox_external_drive/raw/main/images/svg_github_container.svg)

[//]: # (auto_plantuml end)

## GitHub backup

GitHub is great, but...  
They can cancel all my files in a second without warning. It happened to Iranian programmers when the USA imposed sanctions. It can happen to anybody anytime for any reason. GitHub is owned by Microsoft, the service is free and they don't have any obligation to the programmer whatsoever. If the service is free, you are not the customer with customer rights, you are the product with no rights whatsoever.  
I want to be sure that GitHub is not the only place where my code is stored. I will prepare a folder on my computer to have backups of all my GitHub projects. I will call the folder `github_backup`.  
Today I manually cloned all my GitHub projects. Later I can `git pull` them and have it as a backup on my notebook disk. This folder is a backup, I will not develop inside this folder.  
I prepared a utility that automates this process: <https://github.com/bestia-dev/github_readme_copy>  

[//]: # (auto_plantuml start)
<!-- markdownlint-disable MD033 -->
<details><summary>plantuml code:</summary>
<!-- markdownlint-enable MD033 -->

```plantuml
@startuml
GitHub -> github_backup: clone, pull
@enduml
```

</details>

![svg_github_backup](https://github.com/CRUSTDE-ContainerizedRustDevEnv/github_dropbox_external_drive/raw/main/images/svg_github_backup.svg)

[//]: # (auto_plantuml end)

## Dropbox

I have a 2TB storage on Dropbox for 12€/month. It is not cheap, but I had bad experiences with GoogleDrive and OneDrive in the early days. Maybe they are better now, but I don't want to retry everything. I am a paying customer, so I expect some responsibility from Dropbox. Maybe I am just delusional. They can go bankrupt in a matter of hours with modern financial games.  

## External drives

I cannot put all my eggs in the basket of Dropbox.  
Eventually, I make backups of all these files. I make backups on 2 external hard drives and I keep them in separate locations. Just for fun.  
I use my app [dropbox_backup_to_external_disk](https://github.com/bestia-dev/dropbox_backup_to_external_disk) to make backups of Dropbox, because Dropbox does not have an app for that. Shame on them.

[//]: # (auto_plantuml start)
<!-- markdownlint-disable MD033 -->
<details><summary>plantuml code:</summary>
<!-- markdownlint-enable MD033 -->

```plantuml
@startuml
github_backup -> Dropbox: automatic sync
Dropbox -> ext.hd_backup: backup
@enduml 
```

</details>

![svg_dropbox](https://github.com/CRUSTDE-ContainerizedRustDevEnv/github_dropbox_external_drive/raw/main/images/svg_dropbox.svg)

[//]: # (auto_plantuml end)

## Android Studio

When I want to make an app for Android I have to use Android Studio in Win10. All the files are pushed to GitHub. From there they are automatically synced with github_backup. The complete diagram:

[//]: # (auto_plantuml start)
<!-- markdownlint-disable MD033 -->
<details><summary>plantuml code:</summary>
<!-- markdownlint-enable MD033 -->

```plantuml
@startuml
android_studio -> GitHub: push
GitHub -> github_backup: pull
github_backup -> Dropbox: automatic sync
Dropbox -> ext.hd_backup: backup    
@enduml
```

</details>

![svg_android_studio](https://github.com/CRUSTDE-ContainerizedRustDevEnv/github_dropbox_external_drive/raw/main/images/svg_android_studio.svg)

[//]: # (auto_plantuml end)

These are usually small files and having them go up and down the internet 4 times is not a tragedy. Sure, I could save some time, by copying them from one folder to the other locally. Then the sync will just index the files and not send them over the internet.  

## Open-source and free as a beer

My open-source projects are free as a beer (MIT license).  
I just love programming.  
But I need also to drink. If you find my projects and tutorials helpful, please buy me a beer by donating to my [PayPal](https://paypal.me/LucianoBestia).  
You know the price of a beer in your local bar ;-)  
So I can drink a free beer for your health :-)  
[Na zdravje!](https://translate.google.com/?hl=en&sl=sl&tl=en&text=Na%20zdravje&op=translate) [Alla salute!](https://dictionary.cambridge.org/dictionary/italian-english/alla-salute) [Prost!](https://dictionary.cambridge.org/dictionary/german-english/prost) [Nazdravlje!](https://matadornetwork.com/nights/how-to-say-cheers-in-50-languages/) 🍻

[//bestia.dev](https://bestia.dev)  
[//github.com/bestia-dev](https://github.com/bestia-dev)  
[//bestiadev.substack.com](https://bestiadev.substack.com)  
[//youtube.com/@bestia-dev-tutorials](https://youtube.com/@bestia-dev-tutorials)  
