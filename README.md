# mod-installer-schema

This is a proposal for replacing the fomod file format for mod installations. Currently there are no implementations, so this schema is a theoretical option only.

To use it you would create a `mi.json` file in the root of your mod archive.

## Comparison

### FOMOD

/fomod/info.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<fomod>
    <Name>Idrinth Thalui</Name>
    <Author>Björn 'Idrinth' Büttner</Author>
    <Version MachineVersion="1.0.0">1.0.0</Version>
    <Description>This follower, trainer, questgiver and merchant is a male Altmer, focussing on Restoration magic and twohanded, elven swords. Comes with custom dialogue and patrols the world!</Description>
    <Website>https://idrinth-thalui.idrinth.de</Website>
</fomod>
```
/fomod/moduleConfig.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<config xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xsi:noNamespaceSchemaLocation="http://qconsulting.ca/fo3/ModConfig5.0.xsd">
    <moduleName>Idrinth Thalui</moduleName>
    <moduleImage showImage="true" path="/fomod/idrinth.png"/>
    <requiredInstallFiles>
        <folder source="required" destination=""/>
    </requiredInstallFiles>
    <installSteps order="Explicit">
        <installStep name="Intro">
            <optionalFileGroups order="Explicit">
                <group name="Welcome to Idrinth Thalui" type="SelectAll">
                    <plugins>
                        <plugin name="README">
                            <description>Idrinth Thalui is an ancient Altmer, or High Elf, following the warrior god Trinimac. He patrols between Solitude and Riften and visits their temples. As warrior with a two-handed sword, a mage specializing in restoration magic and a merchant trading unusual goods, he is a useful addition to any party. If you can't find him right away, there is a search quest you can enable in the MCM as well as a teleport.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
                <group name="Authors" type="SelectAll">
                    <plugins>
                        <plugin name="Björn 'Idrinth' Büttner">
                            <description>Björn is the voice actor, coder and a writer of Idrinth. Besides of a love of coding, his main focus is making Idrinth feel as alive as possible.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Shahariel">
                            <description>Shahariel is a writer of Idrinth, focussing on improving his lore friendlyness. She is always happy to write more lines where needed as well.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
                <group name="Translators" type="SelectAll">
                    <plugins>
                        <plugin name="jihan02">
                            <description>Thank you for helping out with some of the french translations in 1.0.0, they needed the extra attention.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="777Vortex777">
                            <description>Thank you a lot for improving the sometimes horrible, sometimes hilarious translations to German in version 1.0.0.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Rodocastiza">
                            <description>Thank you a lot for improving some of the sometimes horrible, sometimes hilarious translations to Spanish in version 1.0.0.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="ofuton">
                            <description>Thank you a lot for improving the japanese translations for version 1.0.0.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Elisanaere">
                            <description>Thank you a lot for improving the chinese translations for version 1.0.0 and creating them for earlier versions.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
                <group name="Artists" type="SelectAll">
                    <plugins>
                        <plugin name="Vict">
                            <description>Vict was kind enough to draw most of the custom art featuring Idrinth. She can be reached at https://twitter.com/VictMangle.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="MonaCodeLisa">
                            <description>Estee did not only create the achievement menu icon for Idrinth, she also fixed and recreated the website showing all of his texts. She has a nice Altmer preset available on Nexus as well.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="NocturnePhantom">
                            <description>Fixing a mesh issue for Idrinth's amuletts of Trinimax, they solved a long standing issue. They are a mod author themselves, so can be found on Nexusmods.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
                <group name="Testers" type="SelectAll">
                    <plugins>
                        <plugin name="MonaCodeLisa">
                            <description>Estee has been testing Idrinth 1.0.0 from when it was still thought to only be 0.58.0 and very buggy. She has a nice Altmer preset available on Nexus as well.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="petiximeni">
                            <description>Petiximeni has been heavily involved in finding and fixing bugs in version 1.0.0.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="777Vortex777">
                            <description>Vortex has been very active at finding fomod related bugs for version 1.0.0 as well as testing the mod ingame.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="FoxytheBlack">
                            <description>Foxy has been a long term support and discovered numerous bugs so they could be fixed.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Wulf">
                            <description>Wulf has been testing new dev version quickly and helped keep the quality high.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
                <group name="Additional Contributors" type="SelectAll">
                    <plugins>
                        <plugin name="Algareb">
                            <description>Thank you for helping with texts and proofreading in the early versions.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="SalemMurders">
                            <description>Thank you for helping with texts and proofreading in the early versions.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="SaintJuib">
                            <description>Thank you for helping with texts and proofreading in the early versions.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Markii">
                            <description>Thank you for helping with texts and proofreading in the early versions.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
            </optionalFileGroups>
        </installStep>
        <installStep name="Requirements">
            <optionalFileGroups>
                <group name="Requirements" type="SelectAll">
                    <plugins>
                        <plugin name="Skyrim Script Extender (SKSE64)">
                            <description>Without the script extender multiple scripts will fail to run properly. This will likely cause issues with unexpected behaviour.</description>
                            <image path="/fomod/skse64.png"/>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Spell Perk item Distributor (SPID)">
                            <description>This mod is used to provide compatibility with a number of other mods. Additionally it is required for some favor related tracking.</description>
                            <image path="/fomod/spid.png"/>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="SkyUI">
                            <description>SkyUI is required for the Mod Configuration Menu(MCM). This Menu gives you access to important information, bug workarounds and configuration options.</description>
                            <image path="/fomod/skyui.png"/>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="JContainers">
                            <description>A lot of the internal data handling is done via JContainers. Leaving this mod out will lead to issues with a couple of features, including the MCM. Potential issues include a broken MCM as well as scripts not working as expected due to dependencies on this mod's functionality.</description>
                            <image path="/fomod/jcontainers.png"/>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
            </optionalFileGroups>
        </installStep>
        <installStep name="Additional features">
            <optionalFileGroups>
                <group name="Mods enabling patchless features" type="SelectAny">
                    <plugins>
                        <plugin name="Dreams">
                            <description>Using Idrinth's Dream Framework, there are a number of dreams available, that shed some light on Idrinth Thalui's past. It is highly recommended to add a few more dream framework mods, so that you have some better selection and don't obsessively dream about Idrinth only.</description>
                            <image path="/fomod/idrinths-dream-framework.png"/>
                            <conditionFlags>
                                <flag name="idrinths-dream-framework">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Better Spell AI">
                            <description>Using NPC Spell Variance and it's dependency Keyword Item Distributor (KID) we provide keywords to make Idrinth a better, less predictable caster when he decides to cast. Some features are always handled by scripts though.</description>
                            <image path="/fomod/npc-spell-ai.png"/>
                            <conditionFlags>
                                <flag name="idrinths-dream-framework">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Interactions">
                            <description>Using Idrinth's Patchless Integration Framework (IPIF) there are reactions to and interactions with a number of other mods and creations, including other custom followers. The reason for this being it's own mod is simply reusability across mods, so that the same scripts don't have to be written multiple times.</description>
                            <image path="/fomod/comm.png"/>
                            <conditionFlags>
                                <flag name="idrinths-patchless-integration-framework">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Achievements">
                            <description>Using the Achievement Injector, a number of achievements are available related to the mod's content. Remember that achievements are tracked by character name, so that you can not re-achieve anything already done under the same name.</description>
                            <image path="/fomod/achievement-injector.png"/>
                            <conditionFlags>
                                <flag name="achievement-injector">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Translations">
                            <description>Using the Dynamic String Distributor(DSD), a language to translate texts to can be chosen in the next step. English is the base language and doesn't require this mod. The audio will always be in english.</description>
                            <image path="/fomod/dsd.png"/>
                            <conditionFlags>
                                <flag name="dynamic-string-distributor">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Show your appreciation">
                            <description>Using the mod "I'm Glad You're Here", Idrinth will react to you trying to hug him depending on his opinion about you. It being loaded adds an additional dialogue option.</description>
                            <image path="/fomod/i-m-glad-you-re-here.jpg"/>
                            <conditionFlags>
                                <flag name="i-m-glad-you-re-here">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
            </optionalFileGroups>
        </installStep>
        <installStep name="SPIDified Mod-support">
            <optionalFileGroups>
                <group name="Mods supported through SPID" type="SelectAll">
                    <plugins>
                        <plugin name="Cloaks of Skyrim">
                            <description>Idrinth will get a cloak if both mods are installed.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Ordinator">
                            <description>Idrinth will get a few additional perks to represent his experience.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Odin">
                            <description>Idrinth will get a few additional spells to represent his experience.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Awakening">
                            <description>Idrinth will be affected by the vampire improvements of this mod, making him a more dangerous foe or ally.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Wintersun">
                            <description>Fitting to his backstory, he will get an ancestor lantern added, representing his connection to Trinimac.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Idrinth's Tweaks - Beginnings">
                            <description>Idrinth gains appropriate perks from this mod, that fit his background.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Idrinth's Tweaks - Racial Skill">
                            <description>Idrinth gains all Altmer and Vampire skills from this mod, representing his age and experience.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
            </optionalFileGroups>
        </installStep>
        <installStep name="Translations">
            <visible operator="And">
                <flagDependency flag="dynamic-string-distributor" value="true"/>
            </visible>
            <optionalFileGroups>
                <group name="Text translations" type="SelectAtMostOne">
                    <plugins>
                        <plugin name="Deutsch(teilweise KI)">
                            <description>Deutsche Übersetzung aller Texte im Mod mit Dynamic String Distributor.</description>
                            <files>
                                <folder source="/dsd/de" destination="/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp"/>
                                <folder source="/dreams/de" destination="/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui"/>
                            </files>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Français(partiellement AI)">
                            <description>Traduction française de tous les textes dans le mod en utilisant Dynamic String Distributor.</description>
                            <files>
                                <folder source="/dsd/fr" destination="/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp"/>
                                <folder source="/dreams/fr" destination="/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui"/>
                            </files>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Italian(purely AI)">
                            <description>Traduzione italiana di tutti i testi del mod usando Dynamic String Distributor.</description>
                            <files>
                                <folder source="/dsd/it" destination="/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp"/>
                                <folder source="/dreams/it" destination="/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui"/>
                            </files>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Русский (чисто ИИ)">
                            <description>Русский перевод всех текстов в моде с использованием динамического дистрибутора.</description>
                            <files>
                                <folder source="/dsd/ru" destination="/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp"/>
                                <folder source="/dreams/ru" destination="/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui"/>
                            </files>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Español(púrpuramente AI)">
                            <description>Traducción al español de todos los textos en el mod usando Dynamic String Distributor.</description>
                            <files>
                                <folder source="/dsd/es" destination="/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp"/>
                                <folder source="/dreams/es" destination="/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui"/>
                            </files>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Polski (wyłącznie AI)">
                            <description>Polski tłumaczenie wszystkich tekstów w modzie za pomocą Dynamic String Distributor.</description>
                            <files>
                                <folder source="/dsd/pl" destination="/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp"/>
                                <folder source="/dreams/pl" destination="/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui"/>
                            </files>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="中文、 傳統( 纯 AI)">
                            <description>使用動態字串分配器對模組中的所有文字進行繁體中文翻譯。</description>
                            <files>
                                <folder source="/dsd/zt" destination="/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp"/>
                                <folder source="/dreams/zt" destination="/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui"/>
                            </files>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="中文,简化(纯AI)">
                            <description>使用 Dynamic String Distributor 来简化所有 Mod文本的中文翻译.</description>
                            <files>
                                <folder source="/dsd/zh" destination="/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp"/>
                                <folder source="/dreams/zh" destination="/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui"/>
                            </files>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="日本語(純粋AI)">
                            <description>動的文字列のディストリビューターを使用して、MOD内のすべてのテキストの日本語訳.</description>
                            <files>
                                <folder source="/dsd/ja" destination="/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp"/>
                                <folder source="/dreams/ja" destination="/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui"/>
                            </files>
                            <typeDescriptor>
                                <type name="Optional"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
            </optionalFileGroups>
        </installStep>
        <installStep name="Cross-Mod">
            <visible operator="And">
                <flagDependency flag="idrinths-patchless-integration-framework" value="true"/>
            </visible>
            <optionalFileGroups order="Explicit">
                <group name="Interactions" type="SelectAll">
                    <plugins>
                        <plugin name="Deimos">
                            <description>Hosted in this mod, there are currently 14 interactions with this imperial. He himself features custom voiced dialogue, a compelling backstory as well as a quest chain.</description>
                            <conditionFlags>
                                <flag name="cross-mod-deimos">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Irene Grey">
                            <description>Hosted in this mod, there are currently 19 interactions with this breton. She herself is an enchanter with an interesting backstory and custom voiced dialogue.</description>
                            <conditionFlags>
                                <flag name="cross-mod-irene">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Isadore">
                            <description>Hosted in their mod, there are currently 5 interactions with this wood elf. He himself features custom voiced dialogue and a quest chain. These interactions are not translated to other languages than english unless you patch the Isadore mod.</description>
                            <image path="/fomod/isadore.png"/>
                            <conditionFlags>
                                <flag name="cross-mod-isadore">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
                <group name="Follower Acknowledgements and Commentary" type="SelectAll">
                    <plugins>
                        <plugin name="Isadore">
                            <description>This wood elf is heavily commented on with idle chatter. He himself features custom voiced dialogue and a quest chain.</description>
                            <image path="/fomod/isadore.png"/>
                            <conditionFlags>
                                <flag name="cross-mod-isadore">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Caryalind Thallery">
                            <description>There is idle chatter acknowledging the presence of Caryalind present. He is an Altmer prince with custom voiced dialogue.</description>
                            <conditionFlags>
                                <flag name="cross-mod-caryalind">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Xelzaz">
                            <description>There is idle chatter acknowledging the presence of Xelzaz present. This argonian Alchemist is a member of house Telvanni.</description>
                            <conditionFlags>
                                <flag name="cross-mod-xelzaz">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Bowen">
                            <description>There is idle chatter acknowledging the presence of Bowen present. This traveller is a great quality of life addition to any party.</description>
                            <conditionFlags>
                                <flag name="cross-mod-bowen">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Varrik Veil">
                            <description>There is idle chatter acknowledging the presence of Varrik present. This follower of Boethiah enriches the game with his dad jokes.</description>
                            <conditionFlags>
                                <flag name="cross-mod-varrick">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Flint">
                            <description>There is idle chatter acknowledging the presence of Flint present. This minotaur is an unusual addition for any party.</description>
                            <conditionFlags>
                                <flag name="cross-mod-flint">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Lucien">
                            <description>There is idle chatter acknowledging the presence of Lucien present. This enthusiastic young scholar brings a lot of potential.</description>
                            <conditionFlags>
                                <flag name="cross-mod-lucien">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Sa'Chil">
                            <description>There is idle chatter acknowledging the presence of Sa'Chil present. This opinionated Khajiit is a good investment for future income.</description>
                            <conditionFlags>
                                <flag name="cross-mod-sa-chil">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Val Serano">
                            <description>There is idle chatter acknowledging the presence of this pirate.</description>
                            <conditionFlags>
                                <flag name="cross-mod-val-serano">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Auri">
                            <description>There is idle chatter acknowledging the presence of this wood elf archer.</description>
                            <conditionFlags>
                                <flag name="cross-mod-auri">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Aniya">
                            <description>There is idle chatter acknowledging the presence of this sweettooth.</description>
                            <conditionFlags>
                                <flag name="cross-mod-aniya">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Thogra">
                            <description>There is idle chatter acknowledging the presence of this orc widow. The intended mod variant is the custom voiced version 2.</description>
                            <conditionFlags>
                                <flag name="cross-mod-thogra">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Artigun">
                            <description>There is idle chatter acknowledging the presence of this suspicious character. His interest in dragons and their language does not go unnoticed.</description>
                            <conditionFlags>
                                <flag name="cross-mod-artigun">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
                <group name="Mod Integrations" type="SelectAll">
                    <plugins>
                        <plugin name="Survival Mode">
                            <description>Survival Mode is recognised and commented on. All three values used to track your status are considered and you get advise based on them.</description>
                            <conditionFlags>
                                <flag name="cross-mod-survival-mode">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="Skyrim's Got Talent">
                            <description>Your talent as a bard will be recognised and commented on if you play good or bad. Comments on it are randomized, so may not always fire right away - the same way that normal NPCs are not guranteed to react every time.</description>
                            <conditionFlags>
                                <flag name="cross-mod-skyrims-got-talent">true</flag>
                            </conditionFlags>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
            </optionalFileGroups>
        </installStep>
        <installStep name="Thank You">
            <optionalFileGroups order="Explicit">
                <group name="Thank You" type="SelectAll">
                    <plugins>
                        <plugin name="README">
                            <description>Thank you for trying out this mod, we hope you'll have a lot of fun with it. If you have ideas, bugs or any feedback please don't hesitate to contact us. We plan to continue working on Idrinth for the forseeable future, so we also make sure updates between versions are as painless as possible. Only if the first number in the version changes we expect any need for a new game, second digit is added features while the third digit are bugfixes.</description>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
                <group name="Feedback" type="SelectAll">
                    <plugins>
                        <plugin name="Discord">
                            <description>If you need help or assistance quickly, feel free to join the discord at https://discord.gg/idrinth - other than that it has a nice community for sharing your favourite moments.</description>
                            <image path="/fomod/discord.png"/>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="GitHub">
                            <description>Most of the development is done over at GitHub, feel free to head over to https://github.com/idrinth-thalui if you want news and  development related information ahead of time! If you want to help fix translations, this is also where you find the current ones prepared.</description>
                            <image path="/fomod/github.png"/>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                        <plugin name="NexusMods">
                            <description>This mod is only available at NexusMods, visit https://www.nexusmods.com/skyrimspecialedition/mods/69338 for the latest releases! Feedback or bug reports are of course also highly appreciated.</description>
                            <image path="/fomod/nexusmods.png"/>
                            <files></files>
                            <typeDescriptor>
                                <type name="Required"/>
                            </typeDescriptor>
                        </plugin>
                    </plugins>
                </group>
            </optionalFileGroups>
        </installStep>
    </installSteps>
</config>
```

## MI

```json
{
  "name": "Idrinth Thalui",
  "image": "/fomod/idrinth.png",
  "version": "1.0.0",
  "schemaVersion": "1.0.0",
  "authors": [
    {
      "name": "Björn 'Idrinth' Büttner",
      "roles": [
      	"voice actor",
        "writer",
        "coder",
        "translator"
      ],
      "description": "Björn is the voice actor, coder and a writer of Idrinth. Besides of a love of coding, his main focus is making Idrinth feel as alive as possible."
    },
    {
      "name": "Shahariel",
      "roles": [
        "writer"
      ],
      "description": "Shahariel is a writer of Idrinth, focussing on improving his lore friendlyness. She is always happy to write more lines where needed as well."
    },
    {
      "name": "jihan02",
      "roles": [
        "translator"
      ],
      "description": "Thank you for helping out with some of the french translations in 1.0.0, they needed the extra attention."
    },
    {
      "name": "777Vortex777",
      "roles": [
        "translator",
        "tester"
      ],
      "description": "Thank you a lot for improving the sometimes horrible, sometimes hilarious translations to German in version 1.0.0. He has been very active at finding fomod related bugs for version 1.0.0 as well as testing the mod ingame."
    },
    {
      "name": "Rodocastiza",
      "roles": [
        "translator"
      ],
      "description": "Thank you a lot for improving some of the sometimes horrible, sometimes hilarious translations to Spanish in version 1.0.0."
    },
    {
      "name": "ofuton",
      "roles": [
        "translator"
      ],
      "description": "Thank you a lot for improving the japanese translations for version 1.0.0."
    },
    {
      "name": "Elisanaere",
      "roles": [
        "translator"
      ],
      "description": "Thank you a lot for improving the chinese translations for version 1.0.0 and creating them for earlier versions."
    },
    {
      "name": "Vict",
      "roles": [
        "artist"
      ],
      "description": "Vict was kind enough to draw most of the custom art featuring Idrinth.",
      "website": "https://twitter.com/VictMangle"
    },
    {
      "name": "MonaCodeLisa",
      "roles": [
        "artist",
        "tester",
        "webdeveloper"
      ],
      "description": "Estee did not only create the achievement menu icon for Idrinth, she also fixed and recreated the website showing all of his texts. She has a nice Altmer preset available on Nexus as well. She has been testing Idrinth 1.0.0 from when it was still thought to only be 0.58.0 and very buggy."
    },
    {
      "name": "NocturnePhantom",
      "roles": [
        "artist"
      ],
      "description": "Fixing a mesh issue for Idrinth's amuletts of Trinimax, they solved a long standing issue. They are a mod author themselves, so can be found on Nexusmods."
    },
    {
      "name": "petiximeni",
      "roles": [
        "tester"
      ],
      "description": "Petiximeni has been heavily involved in finding and fixing bugs in version 1.0.0."
    },
    {
      "name": "FoxytheBlack",
      "roles": [
        "tester"
      ],
      "description": "Foxy has been a long term support and discovered numerous bugs so they could be fixed."
    },
    {
      "name": "Wulf",
      "roles": [
        "tester"
      ],
      "description": "Wulf has been testing new dev version quickly and helped keep the quality high."
    },
    {
      "name": "Algareb",
      "roles": [
        "proofreader"
      ],
      "description": "Thank you for helping with texts and proofreading in the early versions."
    },
    {
      "name": "SalemMurders",
      "roles": [
        "proofreader"
      ],
      "description": "Thank you for helping with texts and proofreading in the early versions."
    },
    {
      "name": "SaintJuib",
      "roles": [
        "proofreader"
      ],
      "description": "Thank you for helping with texts and proofreading in the early versions."
    },
    {
      "name": "Markii",
      "roles": [
        "proofreader"
      ],
      "description": "Thank you for helping with texts and proofreading in the early versions."
    }
  ],
  "websites":  [
    "https://idrinth-thalui.idrinth.de",
    "https://github.com/idrinth-thalui",
    "https://www.nexusmods.com/skyrimspecialedition/mods/69338",
    "https://discord.gg/idrinth"
  ],
  "setFileSystemFlags": {
  	"/skse64_loader.exe": "skse64-loaded",
    "/data/skse/plugins/spid.dll": "spid-loaded",
    "/data/SkyUI.esp": "skyui-loaded",
    "/data/skse/plugins/jcontainers.dll": "jcontainers-loaded",
    "/data/idrinthdreamframework.esp": "idrinth-dream-framework-loaded",
    "/data/NPC Spell Variance.esp": "npc-spell-ai-loaded",
    "/data/idrinthfollowerlike.esp": "idrinth-patchless-integration-framework-loaded",
    "/data/skse/plugins/achievementinjector.dll": "achievement-injector-loaded",
    "/data/skse/plugins/dynamicstringdistributor.dll": "dynamic-string-distributor-loaded",
    "/data/imgladyourehere.esp": "igyah-loaded"
  },
  "readme": "Idrinth Thalui is an ancient Altmer, or High Elf, following the warrior god Trinimac. He patrols between Solitude and Riften and visits their temples. As warrior with a two-handed sword, a mage specializing in restoration magic and a merchant trading unusual goods, he is a useful addition to any party. If you can't find him right away, there is a search quest you can enable in the MCM as well as a teleport.",
  "steps": [
    {
      "name": "Requirements",
      "groups":  [
        {
          "name": "Requirements",
          "mode": "SelectAll",
          "options": {
            "Skyrim Script Exteder (SKSE64)": {
              "requiredFlags": [
                "skse64-loaded"
              ],
              "description": "Without the script extender multiple scripts will fail to run properly. This will likely cause issues with unexpected behaviour.",
              "image": "/fomod/skse64.png"
            },
            "Spell Perk Item Distributor (SPID)": {
              "requiredFlags": [
                "spid-loaded"
              ],
              "description": "This mod is used to provide compatibility with a number of other mods. Additionally it is required for some favor related tracking.",
              "image": "/fomod/spid.png"
            },
            "SyUI": {
              "requiredFlags": [
                "skyui-loaded"
              ],
              "description": "SkyUI is required for the Mod Configuration Menu(MCM). This Menu gives you access to important information, bug workarounds and configuration options.",
              "image": "/fomod/skyui.png"
            },
            "JContainers": {
              "requiredFlags": [
                "jcontainers-loaded"
              ],
              "description": "A lot of the internal data handling is done via JContainers. Leaving this mod out will lead to issues with a couple of features, including the MCM. Potential issues include a broken MCM as well as scripts not working as expected due to dependencies on this mod's functionality.",
              "image": "/fomod/jcontainers.png"
            }
          }
        }
      ]
    },
    {
      "name": "Additional Features",
      "groups": [
        {
          "name": "Mods enabling patchless features",
          "mode": "SelectAny",
          "options": {
            "Dreams": {
              "requiredFlags": [
                "idrinth-dream-framework-loaded"
              ],
              "description": "Using Idrinth's Dream Framework, there are a number of dreams available, that shed some light on Idrinth Thalui's past. It is highly recommended to add a few more dream framework mods, so that you have some better selection and don't obsessively dream about Idrinth only.",
              "image": "/fomod/idrinths-dream-framework.png"
            },
            "Better Spell AI": {
              "requiredFlags": [
                "idrinth-dream-framework-loaded"
              ],
              "description": "Using NPC Spell Variance and it's dependency Keyword Item Distributor (KID) we provide keywords to make Idrinth a better, less predictable caster when he decides to cast. Some features are always handled by scripts though.",
              "image": "/fomod/npc-spell-ai.png"
            },
            "Interactions": {
              "requiredFlags": [
                "idrinth-patchless-integration-framework-loaded"
              ],
              "description": "Using Idrinth's Patchless Integration Framework (IPIF) there are reactions to and interactions with a number of other mods and creations, including other custom followers. The reason for this being it's own mod is simply reusability across mods, so that the same scripts don't have to be written multiple times.",
              "image": "/fomod/comm.png"
            },
            "Achievements": {
              "requiredFlags": [
                "achievement-injector-loaded"
              ],
              "description": "Using the Achievement Injector, a number of achievements are available related to the mod's content. Remember that achievements are tracked by character name, so that you can not re-achieve anything already done under the same name.",
              "image": "/fomod/achievement-injector.png"
            },
            "Translations": {
              "requiredFlags": [
                "dynamic-string-distributor-loaded"
              ],
              "description": "Using the Dynamic String Distributor(DSD), a language to translate texts to can be chosen in the next step. English is the base language and doesn't require this mod. The audio will always be in english.",
              "image": "/fomod/dsd.png"
            },
            "Show your appreciation": {
              "requiredFlags": [
                "igyah-loaded"
              ],
              "description": "Using the mod \"I'm Glad You're Here\", Idrinth will react to you trying to hug him depending on his opinion about you. It being loaded adds an additional dialogue option.",
              "image": "/fomod/i-m-glad-you-re-here.png"
            }
          }
        }
      ]
    },
    {
      "name": "SPIDified Mod-support",
      "groups": [
        {
          "name": "Mods supported through SPID",
          "mode": "SelectAll",
          "options": {
          	"Cloaks of Skyrim": {
              "description": "Idrinth will get a cloak if both mods are installed."
            },
          	"Ordinator": {
              "description": "Idrinth will get a few additional spells to represent his experience."
            },
          	"Awakening": {
              "description": "Idrinth will be affected by the vampire improvements of this mod, making him a more dangerous foe or ally."
            },
          	"Wintersun": {
              "description": "Fitting to his backstory, he will get an ancestor lantern added, representing his connection to Trinimac."
            },
          	"Idrinth's Tweaks - Beginnings": {
              "description": "Idrinth gains appropriate perks from this mod, that fit his background."
            },
          	"Idrinth's Tweaks - Racial Skill": {
              "description": "Idrinth gains all Altmer and Vampire skills from this mod, representing his age and experience."
            }
          }
        }
      ]
    },
    {
      "name": "Traslations",
      "requiredFlags": [
        "dynamic-string-distributor-loaded"
      ],
      "groups": [
        {
          "name": "Text translations",
          "mode": "SelectUpToOne",
          "options": {
          	"Deutsch(teilweise KI)": {
              "description": "Deutsche Übersetzung aller Texte im Mod mit Dynamic String Distributor.",
              "setFlags": [
                "translate-german"
              ]
            },
          	"Français(partiellement AI)": {
              "description": "Traduction française de tous les textes dans le mod en utilisant Dynamic String Distributor.",
              "setFlags": [
                "translate-french"
              ]
            },
          	"Italian(purely AI)": {
              "description": "Traduzione italiana di tutti i testi del mod usando Dynamic String Distributor.",
              "setFlags": [
                "translate-italian"
              ]
            },
          	"Русский (чисто ИИ)": {
              "description": "Русский перевод всех текстов в моде с использованием динамического дистрибутора.",
              "setFlags": [
                "translate-russian"
              ]
            },
          	"Español(púrpuramente AI)": {
              "description": "Traducción al español de todos los textos en el mod usando Dynamic String Distributor.",
              "setFlags": [
                "translate-spanish"
              ]
            },
          	"Polski (wyłącznie AI)": {
              "description": "Polski tłumaczenie wszystkich tekstów w modzie za pomocą Dynamic String Distributor.",
              "setFlags": [
                "translate-polish"
              ]
            },
          	"中文、 傳統( 纯 AI)": {
              "description": "使用動態字串分配器對模組中的所有文字進行繁體中文翻譯。",
              "setFlags": [
                "translate-chinese-traditional"
              ]
            },
          	"中文,简化(纯AI)": {
              "description": "使用 Dynamic String Distributor 来简化所有 Mod文本的中文翻译.",
              "setFlags": [
                "translate-chinese-simplified"
              ]
            },
          	"日本語(純粋AI)": {
              "description": "動的文字列のディストリビューターを使用して、MOD内のすべてのテキストの日本語訳.",
              "setFlags": [
                "translate-japanese"
              ]
            }
          }
        }
      ]
    }
  ],
  "installFolders": [
    {
      "from": "/required",
      "to": "/"
    },
    {
      "from": "/dsd/ja",
      "to": "/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp",
      "requiredFlags": [
        "translate-japanese"
      ]
    },
    {
      "from": "/dreams/ja",
      "to": "/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui",
      "requiredFlags": [
        "translate-japanese"
      ]
    },
    {
      "from": "/dsd/de",
      "to": "/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp",
      "requiredFlags": [
        "translate-german"
      ]
    },
    {
      "from": "/dreams/de",
      "to": "/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui",
      "requiredFlags": [
        "translate-german"
      ]
    },
    {
      "from": "/dsd/zh",
      "to": "/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp",
      "requiredFlags": [
        "translate-chinese-simplified"
      ]
    },
    {
      "from": "/dreams/zh",
      "to": "/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui",
      "requiredFlags": [
        "translate-chinese-simplified"
      ]
    },
    {
      "from": "/dsd/zt",
      "to": "/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp",
      "requiredFlags": [
        "translate-chinese-traditional"
      ]
    },
    {
      "from": "/dreams/zt",
      "to": "/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui",
      "requiredFlags": [
        "translate-chinese-traditional"
      ]
    },
    {
      "from": "/dsd/pl",
      "to": "/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp",
      "requiredFlags": [
        "translate-polish"
      ]
    },
    {
      "from": "/dreams/pl",
      "to": "/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui",
      "requiredFlags": [
        "translate-polish"
      ]
    },
    {
      "from": "/dsd/es",
      "to": "/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp",
      "requiredFlags": [
        "translate-spanish"
      ]
    },
    {
      "from": "/dreams/es",
      "to": "/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui",
      "requiredFlags": [
        "translate-spanish"
      ]
    },
    {
      "from": "/dsd/ru",
      "to": "/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp",
      "requiredFlags": [
        "translate-russian"
      ]
    },
    {
      "from": "/dreams/ru",
      "to": "/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui",
      "requiredFlags": [
        "translate-russian"
      ]
    },
    {
      "from": "/dsd/it",
      "to": "/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp",
      "requiredFlags": [
        "translate-italian"
      ]
    },
    {
      "from": "/dreams/it",
      "to": "/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui",
      "requiredFlags": [
        "translate-italian"
      ]
    },
    {
      "from": "/dsd/fr",
      "to": "/SKSE/Plugins/DynamicStringDistributor/IdrinthThalui.esp",
      "requiredFlags": [
        "translate-french"
      ]
    },
    {
      "from": "/dreams/fr",
      "to": "/SKSE/Plugins/FISS/idrinth_dream_framework/IdrinthThalui",
      "requiredFlags": [
        "translate-french"
      ]
    }
  ]
}
```
