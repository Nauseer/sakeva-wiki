---
description: >-
  Для поддерживания стабильного, а самое главное большого значения спавн рейта
  мобов на игрока, мы изменили некие настройки появления мобов.
icon: microchip
---

# Мир Ферм

***

## Ядро сервера

> В мире ферм установлено ядро [Purpur](https://purpurmc.org/).

***

## Основные настройки

{% tabs %}
{% tab title="bukkit.yml" %}
```yaml
spawn-limits: # Лимиты по количеству мобов на игрока
  monsters: 35
  animals: 8
  water-animals: 15
  water-ambient: 5
  water-underground-creature: 5
  axolotls: 5
  ambient: 15
ticks-per: # Время в тиках (20 тиков = 1 секунда), между спавном мобов
  monster-spawns: 6
  animal-spawns: 400
  water-spawns: 12
  water-ambient-spawns: 12
  water-underground-creature-spawns: 12
  axolotl-spawns: 12
  ambient-spawns: 12
```
{% endtab %}

{% tab title="spigot.yml" %}
```yaml
world-settings:
  default:
    mob-spawn-range: 3 # Радиус в чанках от игрока, в котором будут спавниться мобы
    entity-activation-range: # Радиус в блоках, в котором мобы будут активны
      animals: 32
      monsters: 32
      raiders: 12
      misc: 16
      water: 16
      villagers: 32
      flying-monsters: 32
    entity-tracking-range: # Радиус в блоках, в котором мобы будут прогружаться
      players: 48
      animals: 48
      monsters: 48
      misc: 32
      display: 128
      other: 64
    ticks-per: # Настройки поведения воронок
      hopper-transfer: 8
      hopper-check: 1
      hopper-amount: 1
```
{% endtab %}

{% tab title="purpur.yml" %}
```yaml
villager:
  lobotomize: # Настройка состояния интеллекта у жителей
    enabled: false # Интеллект включен
    check-interval: 100
    wait-until-trade-locked: false
```
{% endtab %}

{% tab title="paper-world-defaults.yml" %}
```yaml
despawn-range-shape: ELLIPSOID
    despawn-ranges:
      ambient:
        hard:
          horizontal: 56
          vertical: 128
        soft: 32
      axolotls:
        hard:
          horizontal: 56
          vertical: 128
        soft: 32
      creature:
        hard:
          horizontal: 56
          vertical: 128
        soft: 32
      misc:
        hard:
          horizontal: 56
          vertical: 128
        soft: 32
      monster:
        hard:
          horizontal: 56
          vertical: 128
        soft: 32
      underground_water_creature:
        hard:
          horizontal: 56
          vertical: 128
        soft: 32
      water_ambient:
        hard:
          horizontal: 56
          vertical: 128
        soft: 32
      water_creature:
        hard:
          horizontal: 56
          vertical: 128
        soft: 32
tick-rates:
  behavior:
    villager:
      acquirepoi: 120
      validatenearbypoi: 60
  container-update: 1
  dry-farmland: 1
  grass-spread: 8
  mob-spawner: 4
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

* Дюп динамита включен, максимальное количество взрывов динамита на тик неограниченно.
* Отключены скидки у жителей после излечения от заражения.
