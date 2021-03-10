<script>
	let game_selected = 'Birthright';
	let games = [
		"Birthright", "Conquest", "Revelations"
	]
	let boons = [
		{name: "HP", HP: 15, Def: 5, Res: 5},
		{name: "Str", Str: 15, Skl: 5, Def: 5}, 
		{name: "Mag", Mag: 20, Spd: 5, Res: 5}, 
		{name: "Skl", Str: 5, Skl: 25, Def: 5}, 
		{name: "Spd", Skl: 5, Spd: 15, Lck: 5}, 
		{name: "Lck", Str: 5, Mag: 5, Lck: 25}, 
		{name: "Def", Lck: 5, Def: 10, Res: 5}, 
		{name: "Res", Mag: 5, Spd: 5, Res: 10}
	]
	let banes = [
		{name: "HP", HP: -10, Def: -5, Res: -5},
		{name: "Str", Str: -10, Skl: -5, Def: -5}, 
		{name: "Mag", Mag: -15, Spd: -5, Res: -5}, 
		{name: "Skl", Str: -5, Skl: -20, Def: -5}, 
		{name: "Spd", Skl: -5, Spd: -10, Lck: -5}, 
		{name: "Lck", Str: -5, Mag: -5, Lck: -20}, 
		{name: "Def", Lck: -5, Def: -10, Res: -5}, 
		{name: "Res", Mag: -5, Spd: -5, Res: -10}
	]
	let talents = ["Samurai", "Oni Savage", "Spear Fighter", "Diviner", "Shrine Maiden", "Monk", "Sky Knight", "Archer", "Ninja", "Apothecary", "Cavalier", "Knight", "Fighter", "Mercenary", "Outlaw", "Wyvern Rider", "Dark Mage", "Troubadour"]
	let avatar_sex = 'M'
	let avatar_boon = boons[1]
	let avatar_bane = banes[5]
	let avatar_talent = 'Cavalier'
</script>

Game:
<select bind:value={game_selected}>
	{#each games as game}
	<option value={game}>
		{game}
	</option>
	{/each}
</select>
<br />

Avatar Sex:
<select bind:value={avatar_sex}>
	<option value="M">
		M
	</option>
	<option value="F">
		F
	</option>
</select>
<br />

Avatar Boon:
<select bind:value={avatar_boon.name}>
	{#each boons as boon}
		{#if boon.name != avatar_bane.name}
			<option value={boon.name}>
				{boon.name}
			</option>
		{/if}
	{/each}
</select>
<br />

Avatar Bane: 
<select bind:value={avatar_bane.name}>
	{#each banes as bane}
		{#if bane.name != avatar_boon.name}
			<option value={bane.name}>
				{bane.name}
			</option>
		{/if}
	{/each}
</select>
<br />

Avatar Talent:
<select bind:value={avatar_talent}>
	{#each talents as talent}
		<option value={talent}>
			{talent}
		</option>
	{/each}
</select>
<br />
