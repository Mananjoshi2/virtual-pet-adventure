# Virtual Pet Adventure

A Tamagotchi-style desktop game built with Java Swing for CS 2212 at Western University.

## Overview

Care for a robot pet by managing its health, hunger, sleep, and happiness. Feed it, play with it, take it to the vet, and give it gifts — but watch out, its stats decay over time. Let them bottom out and your pet dies.

Three pet types offer different difficulty levels:

| Pet | Difficulty | Notes |
|---|---|---|
| RoboFriend | Easy | Forgiving stat decay |
| MechaMate | Medium | Balanced needs |
| Tech Titan | Hard | Demands constant attention |

## Features

- Pet states: Normal, Hungry, Angry, Sleeping, Dead
- Real-time stat decay with per-pet rates
- Inventory system with food and gift items
- Save/load game state per pet name
- Parental controls with session time limits and password protection
- Emergency food drop when inventory is empty and the pet goes hungry

## Requirements

- Java 21+
- Maven 3.6+

## Running

```bash
git clone https://github.com/mananjoshi211/virtual-pet-adventure.git
cd virtual-pet-adventure
mvn compile exec:java -Dexec.mainClass="com.group14.virtualpet.Main"
```

Or build a standalone JAR:

```bash
mvn package
java -jar target/virtual-pet-1.0-SNAPSHOT-jar-with-dependencies.jar
```

## Project Structure

```
src/main/java/com/group14/virtualpet/
├── Main.java                         # Entry point
├── MainFrame.java                    # Top-level window, panel switching
├── model/                            # Pet, inventory, items, state enums
├── state/                            # GameState (serialized save data)
├── ui/                               # Top-level panels (menu, selection, settings, etc.)
│   └── gameplayPanelComponents/      # Gameplay sub-panels
└── util/                             # AudioManager, SaveLoadUtil
```

## Team

Group 14 — Western University, CS 2212 (Fall 2024)

- Pragalvha Sharma
- Aaliyan Muhammad
- Athul Charanthara
- Krish Narula
- Manan Joshi
