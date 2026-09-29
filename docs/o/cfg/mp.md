---
description: >-
  Для обеспечения стабильной работы сервера мы ввели некие ограничения на мир
  построек. Просим заметить, что эти ограничения не действуют на мир ферм.
icon: microchip
---

# Мир Построек

***

## Ядро сервера

> В мире построек установлено ядро, базирующиеся на Paper.

***

## Основные настройки

{% tabs %}
{% tab title="bukkit.yml" %}
```yaml
spawn-limits: # Лимиты по количеству мобов на игрока
  monsters: 1
  animals: 3
  water-animals: 1
  water-ambient: 1
  water-underground-creature: 1
  axolotls: 2
  ambient: 1
ticks-per: # Время в тиках (20 тиков = 1 секунда), между спавном мобов
  monster-spawns: 400
  animal-spawns: 400
  water-spawns: 400
  water-ambient-spawns: 400
  water-underground-creature-spawns: 400
  axolotl-spawns: 400
  ambient-spawns: 400
```
{% endtab %}

{% tab title="spigot.yml" %}
```yaml
world-settings:
  default:
    mob-spawn-range: 4 # Радиус в чанках от игрока, в котором будут спавниться мобы
    entity-activation-range: # Радиус в блоках, в котором мобы будут активны
      animals: 16
      monsters: 18
      raiders: 16
      misc: 12
      water: 12
      villagers: 12
      flying-monsters: 24
    entity-tracking-range: # Радиус в блоках, в котором мобы будут прогружаться
      players: 80
      animals: 48
      monsters: 48
      misc: 32
      display: 96
      other: 48
    ticks-per: # Настройки поведения воронок
      hopper-transfer: 8
      hopper-check: 8
      hopper-amount: 1
```
{% endtab %}

{% tab title="purpur.yml" %}
```yaml
villager:
  allow-trading: false # Сделки отключены
  lobotomize: # Настройка состояния интеллекта у жителей
    enabled: true # Интеллект отключен
    check-interval: 100
```
{% endtab %}

{% tab title="paper-world-defaults.yml" %}
```yaml
despawn-range-shape: ELLIPSOID
    despawn-ranges:
      ambient:
        hard: 56
        soft: 30
      axolotls:
        hard: 56
        soft: 30
      creature:
        hard: 56
        soft: 30
      misc:
        hard: 56
        soft: 30
      monster:
        hard: 56
        soft: 30
      underground_water_creature:
        hard: 56
        soft: 30
      water_ambient:
        hard: 56
        soft: 30
      water_creature:
        hard: 56
        soft: 30
tick-rates:
  behavior:
    villager:
      acquirepoi: 120
      validatenearbypoi: 60
  container-update: 3
  dry-farmland: 4
  grass-spread: 4
  mob-spawner: 8
  sensor:
    villager:
      nearestbedsensor: 200
      nearestlivingentitysensor: 80
      playersensor: 80
      secondarypoisensor: 200
      villagerbabiessensor: 40
  wet-farmland: 4
```
{% endtab %}
{% endtabs %}

***

## Прочие настройки

* Дюп динамита, ковров, рельс выключен.
* Отключены торги у жителей.
