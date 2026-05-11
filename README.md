# Bonsai

A Windower 4 addon that automates daily tasks in the Mog Garden, such as harvesting, monster rearing pets, and furrows.

## Install

Drop the `Bonsai` folder into your Windower addons directory and then load it ingame with `lua l Bonsai`.

## Commands

To operate Bonsai, use the command `//bonsai` (or `//bon` for short).

- `//bon garden` runs all 4 garden nodes in order: Mineral Vein, Pond Dredger, Arboreal Grove, Coastal Fishing Net.
- `//bon mine`, `//bon dredger`, `//bon grove`, `//bon net` run a single garden node.
- `//bon pet` pets every breeding monster in the rearing grounds. Please use this only in the Rearing Grounds part of the Mog Garden. If used in the main Mog Garden area, it will cancel.
- `//bon all` does the garden cycle, then warps to the rearing grounds via Chacharoon, then pets all monsters.
- `//bon cancel` aborts the current run.
- `//bon furrow start` begins the Furrow loop: plant a Revival Root in each Garden Furrow, wait one hour for them to grow, harvest, repeat.
- `//bon furrow stop` stops the Furrow loop.
- `//bon furrow status` shows how long until the planted furrows are ready, or what the loop is currently doing.

## Requirements

- The garden, furrow, and `all` commands require you to be in Mog Garden.
- `//bon pet` should be ran only when you are in the Rearing Grounds part of your Mog Garden.
- `//bon all` should be ran from the main Mog Garden area and will naturally transition to the Rearing Grounds after completing the garden tasks.

### Furrow Requirements
Furrow uses Revival Roots (https://www.bg-wiki.com/ffxi/Revival_Root) specifically for planting. This means each plant cycle will be 1 hour long. 

As such, you need at least one Revival Root in your inventory for it to work. The loop will keep planting and harvesting until you run out.

## Notes

The addon walks your character to each NPC directly, so be sure to have a clear straight path between nodes when running it. The natural order defined by the addon will always have a clear pathing and should not get stuck.

## Known Bugs

When using `//bon all` and moving to the Rearing Grounds, due to the nature of the packet teleport sequence, it's possible that ghost monsters may spawn if you don't have the full 4 monster breeding slots filled. In such scenarios, the addon will skip over those monsters automatically. So far it seems to only be a visual glitch.