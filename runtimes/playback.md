---
description: Playing and pausing animations
---

# Playback

Rive lets you specify what artboard to use, what animations and state machines to mix and play, and to control the play/pause state of each animation.

## Choosing an artboard

When a Rive object is instantiated, the artboard to use can be specified. If no artboard is given, the default artboard is used. Only one artboard can be used at a time.

{% tabs %}
{% tab title="web" %}
```javascript
new rive.Rive({
    src: 'https://cdn.rive.app/animations/vehicles.riv',
    canvas: document.getElementById('canvas'),
    artboard: 'Truck',
    autoplay: true
});
```
{% endtab %}

{% tab title="Flutter" %}
```dart
RiveAnimation.network(
    'https://cdn.rive.app/animations/vehicles.riv',
    artboard: 'Truck'
);
```
{% endtab %}
{% endtabs %}

## Choosing starting animations

Starting animations can also be chosen when Rive is instantiated. A list of animation names can be provided.

{% tabs %}
{% tab title="web" %}
```javascript
// Play the idle animation
new rive.Rive({
    src: 'https://cdn.rive.app/animations/vehicles.riv',
    canvas: document.getElementById('canvas'),
    animations: ['idle', 'curves'],
    autoplay: true
});

// play and mix the idle and curves animations
new rive.Rive({
    src: 'https://cdn.rive.app/animations/vehicles.riv',
    canvas: document.getElementById('canvas'),
    animations: ['idle', 'curves'],
    autoplay: true
});
```
{% endtab %}

{% tab title="Flutter" %}
```dart
// Play the curves animation
RiveAnimation.network(
    'https://cdn.rive.app/animations/vehicles.riv',
    animations: ['curves'],
);

// Play and mix both the idle and curves animations
RiveAnimation.network(
    'https://cdn.rive.app/animations/vehicles.riv',
    animations: ['idle', 'curves'],
),
```
{% endtab %}
{% endtabs %}

## Choosing starting state machines

A starting state machine can be specified when Rive is instantiated. A state machine name can be provided.

{% tabs %}
{% tab title="web" %}
```javascript
new rive.Rive({
    src: 'https://cdn.rive.app/animations/vehicles.riv',
    canvas: document.getElementById('canvas'),
    stateMachines: 'weather',
    autoplay: true
});
```
{% endtab %}

{% tab title="Flutter" %}
```dart
RiveAnimation.network(
    'https://cdn.rive.app/animations/vehicles.riv',
    stateMachines: ['weather'],
)
```
{% endtab %}
{% endtabs %}
