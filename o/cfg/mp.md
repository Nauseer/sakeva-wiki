---
description: >-
  Для обеспечения стабильной работы сервера мы ввели некие ограничения на мир
  построек. Просим заметить, что эти ограничения не действуют на мир ферм.
icon: microchip
---

# Мир Построек

***

## Ядро сервера

> В мире построек установлено ядро [Purpur](https://purpurmc.org/).

***

## Основные настройки

{% tabs %}
{% tab title="bukkit.yml" %}
```yaml
spawn-limits: # Лимиты по количеству мобов на игрока
  monsters: 2
  animals: 5
  water-animals: 2
  water-ambient: 2
  water-underground-creature: 3
  axolotls: 3
  ambient: 1
ticks-per: # Время в тиках (20 тиков = 1 секунда), между спавном мобов
  monster-spawns: 10
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
    mob-spawn-range: 3 # Радиус в чанках от игрока, в котором будут спавниться мобы
    entity-activation-range: # Радиус в блоках, в котором мобы будут активны
      animals: 16
      monsters: 24
      raiders: 24
      misc: 8
      water: 8
      villagers: 16
      flying-monsters: 24
    entity-tracking-range: # Радиус в блоках, в котором мобы будут прогружаться
      players: 48
      animals: 48
      monsters: 48
      misc: 32
      display: 128
      other: 64
    ticks-per: # Настройки поведения воронок
      hopper-transfer: 8
      hopper-check: 8
      hopper-amount: 1
```
{% endtab %}

{% tab title="purpur.yml" %}
```yaml
villager:
  lobotomize: # Настройка состояния интеллекта у жителей
    enabled: true # Интеллект отключен
    check-interval: 100
    wait-until-trade-locked: false
```
{% endtab %}

{% tab title="paper-world-defaults.yml" %}
```yaml
despawn-range-shape: ELLIPSOID
    despawn-ranges:
      ambient:
        hard: 72
        soft: 32
      axolotls:
        hard: 72
        soft: 32
      creature:
        hard: 72
        soft: 32
      misc:
        hard: 72
        soft: 32
      monster:
        hard: 72
        soft: 32
      underground_water_creature:
        hard: 72
        soft: 32
      water_ambient:
        hard: 72
        soft: 32
      water_creature:
        hard: 72
        soft: 32
tick-rates:
  behavior:
    villager:
      acquirepoi: 120
      validatenearbypoi: 60
  container-update: 1
  dry-farmland: 1
  grass-spread: 4
  mob-spawner: 2
  sensor:
    villager:
      nearestbedsensor: 80
      nearestlivingentitysensor: 40
      playersensor: 40
      secondarypoisensor: 80
      villagerbabiessensor: 40
  wet-farmland: 1
```
{% endtab %}
{% endtabs %}

***

## Прочие настройки

* Дюп динамита, ковров, рельс выключен.
* Отключены скидки у жителей после излечения от заражения.
