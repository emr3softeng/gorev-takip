# Görev Takip

**EG SOFTWARE** tarafından geliştirilmiştir.

Python ile yazılmış, harici bağımlılığı olmayan basit bir komut satırı görev yöneticisi.
Görevler kullanıcı klasöründeki `~/.gorev_takip.json` dosyasında saklanır.

## Kurulum

```bash
git clone https://github.com/KULLANICI_ADIN/gorev-takip.git
cd gorev-takip
python -m venv .venv
```

Sanal ortamı etkinleştir:

- Windows (PowerShell): `.venv\Scripts\Activate.ps1`
- macOS / Linux: `source .venv/bin/activate`

Geliştirme bağımlılıklarını kur:

```bash
pip install -r requirements-dev.txt
```

## Kullanım

```bash
python -m gorev_takip ekle "Süt al"
python -m gorev_takip ekle "Raporu bitir"
python -m gorev_takip listele
python -m gorev_takip listele --bekleyen
python -m gorev_takip tamamla 1
python -m gorev_takip sil 2
```

Örnek çıktı:

```
[x] #1 Süt al
[ ] #2 Raporu bitir
```

Farklı bir dosya kullanmak için: `python -m gorev_takip --dosya benim.json listele`

İstersen `pip install -e .` ile kurup doğrudan `gorev-takip listele` de yazabilirsin.

## Testler

```bash
python -m pytest -v
```

## VS Code

Proje klasörünü VS Code ile aç. Önerilen eklentiler otomatik önerilir, `.vscode/` içindeki ayarlar
pytest'i Test paneline bağlar ve F5 ile hazır çalıştırma/hata ayıklama yapılandırmalarını sunar.

## Lisans

MIT, telif hakkı EG SOFTWARE'e aittir. Ayrıntılar için `LICENSE` dosyasına bak.

© 2026 EG SOFTWARE
