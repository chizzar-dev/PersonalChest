<div align="center">

<img src="https://capsule-render.vercel.app/api?type=rect&color=0:0b1220,100:0e7490&height=110&section=header&text=PersonalChests&fontSize=42&fontColor=22d3ee&fontAlignY=54&desc=Paged%20personal%20chests&descSize=13&descColor=94a3b8&descAlignY=80" width="100%" alt="PersonalChests" />

<p>
<img src="https://img.shields.io/github/v/release/chizzar-dev/PersonalChest?style=flat&label=release&color=06b6d4&labelColor=0b1220" alt="release" />
<img src="https://img.shields.io/badge/Minecraft-1.8%20%E2%80%93%201.21.11-0891b2?style=flat&labelColor=0b1220" alt="Minecraft 1.8 - 1.21.11" />
<img src="https://img.shields.io/badge/Java-8%2B-155e75?style=flat&labelColor=0b1220&logo=openjdk&logoColor=22d3ee" alt="Java 8+" />
<a href="LICENSE"><img src="https://img.shields.io/github/license/chizzar-dev/PersonalChest?style=flat&label=license&color=0e7490&labelColor=0b1220" alt="license" /></a>
</p>

</div>

PersonalChests gives every player a set of private, paged chests, with an admin view for staff.

*PersonalChests, her oyuncuya sayfali ve kisisel sandiklar verir; yetkililer icin yonetici goruntusu icerir.*

## Features · Özellikler
- Oyuncu başına ayarlanabilir sandık sayısı (varsayılan **10**)
- `/chest <sayfa>` ile istediğin sandığı doğrudan açma
- GUI içinde ileri / geri / kapat butonları
- Yetkililer için `/chest admin <oyuncu>` — başkasının sandığını aç ve düzenle
- Başlıklar, itemler, sesler ve mesajlar tamamen configden ayarlanabilir
- Veriler oyuncu başına ayrı dosyada saklanır (`data/<uuid>.yml`)

## Installation · Kurulum
1. `PersonalChests.jar` dosyasını [Releases](https://github.com/chizzar-dev/PersonalChest/releases/latest) sayfasından indir.
2. Sunucunun `plugins/` klasörüne at.
3. Sunucuyu yeniden başlat.
4. Oluşan `plugins/PersonalChests/config.yml` dosyasını dilediğin gibi düzenle.

## Commands · Komutlar
| Komut | Açıklama | Yetki |
|-------|----------|-------|
| `/chest` | İlk sandığını açar | `chest.use` |
| `/chest <sayfa>` | Belirtilen sandığı açar | `chest.use` |
| `/chest admin <oyuncu> [sayfa]` | Başka oyuncunun sandığını açar | `chest.admin` |
| `/chest reload` | Configi yeniden yükler | `chest.admin` |

**Alias:** `/sandik` · `/pv` · `/kasa`

## Permissions · Yetkiler
| Yetki | Açıklama | Varsayılan |
|-------|----------|------------|
| `chest.use` | Komutu kullanabilir | herkes |
| `chest.admin` | Başkalarının sandıklarını yönetir, reload | op |

## Configuration · Ayarlar
| Anahtar | Açıklama |
|---------|----------|
| `total-chests` | Oyuncu başına sandık sayısı |
| `rows` | GUI satır sayısı (2–6, son satır gezinme çubuğu) |
| `titles.player` / `titles.admin` | Başlık formatları (`%page%`, `%owner%`) |
| `sound.*` | Açılış ve sayfa geçiş sesleri |
| `items.*` | Buton materyalleri, isimleri, açıklamaları |
| `messages.*` | Tüm mesajlar |

## Building · Derleme
```bash
mvn clean package
```
Çıktı · Output: `target/PersonalChests.jar`

Her push [GitHub Actions](https://github.com/chizzar-dev/PersonalChest/actions/workflows/build.yml) ile derlenir; `v*` etiketli sürümler jar'la birlikte [Releases](https://github.com/chizzar-dev/PersonalChest/releases) sayfasına eklenir.
<br><sub>Every push is built by GitHub Actions; tagged `v*` releases attach the jar.</sub>

## License · Lisans
[MIT](LICENSE) — istediğin gibi kullan, değiştir, dağıt · use, modify and distribute freely

<div align="center"><sub>chizzar-dev · Minecraft plugins for 1.8 – 1.21.11 · <a href="https://discord.gg/forges">Discord</a></sub></div>
