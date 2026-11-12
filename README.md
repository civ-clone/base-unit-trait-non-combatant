# base-unit-trait-non-combatant

The `NonCombatant` unit trait: a unit type with it never fights.

A unit type with this trait takes no part in fighting: it never attacks, captures a city or pillages. A game's rules may also leave it out of whatever they count as military.

For example: Civ1: Diplomat and Caravan. Civ2: the diplomacy and trade roles.

A game declares which of its unit classes have the trait with `UnitTraits` rules from `@civ-clone/core-unit`, and its
rules ask `unit.hasTrait(NonCombatant)`:

```ts
import NonCombatant from '@civ-clone/base-unit-trait-non-combatant/NonCombatant';
import { unitTraits } from '@civ-clone/core-unit/Rules/UnitTraits';

ruleRegistry.register(...unitTraits('my-game:unit/trait', MyUnit, NonCombatant));
```

Part of the unit traits design (civ-clone/web-renderer#1008).
