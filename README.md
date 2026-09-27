<div align="center">

<img src="docs/logo.png" alt="DanLauncher" width="128" height="128">

# 🎮 DanLauncher

**Современный лаунчер Minecraft с мод-менеджером, автообновлением и приятным интерфейсом**

[![Version](https://img.shields.io/badge/version-5.0.1-8b5cf6?style=for-the-badge)](https://github.com/daanilll/DanLauncher/releases)
[![License](https://img.shields.io/badge/license-MIT-10b981?style=for-the-badge)](LICENSE)
[![Python](https://img.shields.io/badge/python-3.10+-3b82f6?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Platform](https://img.shields.io/badge/platform-Linux-f59e0b?style=for-the-badge&logo=linux&logoColor=white)](https://fedoraproject.org/)

[![GitHub Stars](https://img.shields.io/github/stars/daanilll/DanLauncher?style=for-the-badge&color=fbbf24)](https://github.com/daanilll/DanLauncher/stargazers)
[![GitHub Issues](https://img.shields.io/github/issues/daanilll/DanLauncher?style=for-the-badge&color=ef4444)](https://github.com/daanilll/DanLauncher/issues)
[![Downloads](https://img.shields.io/github/downloads/daanilll/DanLauncher/total?style=for-the-badge&color=22c55e)](https://github.com/daanilll/DanLauncher/releases)

[🚀 Установка](#-установка) • [✨ Возможности](#-возможности) • [📸 Скриншоты](#-скриншоты) • [🛠 Разработка](#-разработка)

</div>

---

## 🎯 Что такое DanLauncher?

**DanLauncher** — это красивый и лёгкий лаунчер Minecraft, написанный на Python. Он создан для тех, кто устал от громоздких решений и хочет получить всё необходимое в одном месте: установку модов в один клик, поиск контента прямо в лаунчере, автоматические обновления и приятный глазу интерфейс в стиле **Aurora Glass**.

> 💡 **Почему DanLauncher?** Потому что остальные лаунчеры либо перегружены, либо не работают на Linux «из коробки». DanLauncher — лёгкий, нативный, и делает ровно то, что нужно.

---

## ✨ Возможности

### 🎨 Интерфейс
- 🌌 Тёмная тема **Aurora Glass**
- ✨ Плавные анимации и glass-эффекты
- 🖼 Кастомная иконка и фон
- 🎯 Нативная интеграция с GNOME
- 🌐 Двуязычный интерфейс (RU / EN)

### ⚙️ Управление версиями
- 🚀 Установка **Fabric / Forge / NeoForge / Quilt**
- ☕ Автоматическая загрузка **Java Runtime**
- 📋 Список всех установленных версий

### 📦 Моды
- 📦 **Мод-менеджер** с поиском и включением/выключением
- 🔍 Поиск модов на **Modrinth** и **CurseForge**
- 🗂 Сортировка модов по версии Minecraft
- 🎯 **Drag & Drop** модов, ресурспаков и шейдеров
- ➕ Установка **Fabric API** в один клик

### 🔧 Технические
- 🔄 **Автообновление** через GitHub Releases
- 🛡 Умная обработка ошибок
- 🌍 Поддержка зеркала **BMCLAPI** для СНГ
- ⚙️ Прокси для обхода блокировок

---

## 📸 Скриншоты

<div align="center">

### 🖥 Главное окно
![Main Window](docs/screenshots/main.png)

### 📦 Мод-менеджер
![Mod Manager](docs/screenshots/mods.png)

### 🔍 Поиск модов
![Mod Search](docs/screenshots/search.png)

### ⚙️ Настройки
![Settings](docs/screenshots/settings.png)

</div>

---

## 🚀 Установка

### 🐧 Linux (Fedora / RHEL)

```bash
# Скачай .rpm из последнего релиза
wget https://github.com/daanilll/DanLauncher/releases/latest/download/danlauncher-5.0.1-1.fc44.noarch.rpm

# Установи через dnf
sudo dnf install ./danlauncher-5.0.1-1.fc44.noarch.rpm
После установки запусти из меню приложений DanLauncher или командой:

bash
danlauncher
🛠 Установка из исходников
bash
git clone https://github.com/daanilll/DanLauncher.git
cd DanLauncher

sudo dnf install python3 python3-tkinter python3-pillow python3-pillow-tk python3-requests
pip install --user minecraft_launcher_lib tkinterdnd2

python3 main.py
📋 Требования
Компонент	Минимум	Рекомендуется
ОС	Fedora 40+	Fedora 44+
Python	3.10	3.12+
RAM	4 ГБ	8 ГБ+
Место на диске	2 ГБ	10 ГБ+ (с модами)
🎮 Как пользоваться
1️⃣ Выбор версии
Открой DanLauncher → выбери версию в выпадающем списке.

2️⃣ Установка модлоадера
Выбери Fabric / Forge / NeoForge / Quilt → нажми «⤓ Установить».

3️⃣ Установка модов
Из Modrinth: кнопка «🔍 Найти мод» → введи название → «⤓ Установить»

Локально: перетащи .jar прямо в окно DanLauncher

Вручную: положи .jar в ~/.minecraft/mods/

4️⃣ Запуск
Жми большую зелёную кнопку «▶ ИГРАТЬ».

🛠 Разработка
Структура проекта
text
DanLauncher/
├── main.py                    # Основной файл
├── black.png                  # Иконка приложения
├── image.jpg                  # Фоновое изображение
├── danlauncher.desktop        # Ярлык для меню
├── danlauncher.spec           # Spec-файл для .rpm
├── docs/
│   ├── logo.png
│   └── screenshots/
└── README.md
Сборка .rpm
bash
sudo dnf install rpm-build rpmdevtools
rpmdev-setuptree

mkdir -p ~/danlauncher-5.0.1
cp main.py black.png danlauncher.desktop ~/danlauncher-5.0.1/
tar -czf ~/rpmbuild/SOURCES/danlauncher-5.0.1.tar.gz -C ~ danlauncher-5.0.1

rpmbuild -ba danlauncher.spec
Версионирование
Мелкая правка: 5.0.1 → 5.0.2 … 5.0.9

Крупное обновление: 5.0.9 → 5.9.0

Следующий мажор: 5.9.9 → 6.0.0

🤝 Вклад
🐛 Нашёл баг? → Создай Issue

💡 Есть идея? → Открой обсуждение

📝 Pull Request — приветствуется

🗺 Дорожная карта
☑ Базовый функционал
☑ Установка Fabric / Forge / Quilt
☑ Мод-менеджер
☑ Поиск модов
☑ Переход на Linux и .rpm
☑ Автообновление через GitHub Releases
□ Менеджер модпаков (Modrinth Modpacks)
□ Менеджер аккаунтов со скинами
□ Discord Rich Presence
□ Сборка для .deb
□ Дизайн на GTK4
❓ FAQ
<details> <summary><b>DanLauncher не запускается, что делать?</b></summary>
Проверь зависимости:

bash
python3 -c "import tkinter, PIL, requests"
Если что-то падает:

bash
sudo dnf install python3-tkinter python3-pillow python3-pillow-tk python3-requests
</details><details> <summary><b>Как обновить DanLauncher?</b></summary>
Запусти — он сам проверит обновления. Или нажми 🔄 в топбаре.

</details><details> <summary><b>Где хранятся настройки и логи?</b></summary>
Настройки: ~/.config/danlauncher/settings.json

Лог: ~/.config/danlauncher/last_run.log

Игра: ~/.minecraft/

</details><details> <summary><b>Работает ли на Windows?</b></summary>
Сейчас проект ориентирован на Linux. Windows-версия — в планах.

</details>
📄 Лицензия
Проект распространяется под лицензией MIT. См. LICENSE.

<div align="center">
🌟 Понравился проект? Поставь звезду!
https://api.star-history.com/svg?repos=daanilll/DanLauncher&type=Date

Сделано с ❤️ на Fedora Linux

</div> ```
