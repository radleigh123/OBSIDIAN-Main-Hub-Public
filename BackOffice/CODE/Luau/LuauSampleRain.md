---
cssclass:
aliases:
tags:
- Luau
- 
---
**[[Luau|HOME [Luau]]]**

---
## Infinite Rain Loop
```lua
while true do

	wait()
	local Rain = Instance.new("Part", game.Workspace)
	Rain.Position = Vector3.new(0, 15, 0)
	Rain.Size = Vector3.new(0.5, 2, 0.5)
	Rain.Anchored = false
	Rain.Transparency = 0.8

end
```

```lua
--- Destroy on touched
while true do

	wait()
	local Rain = Instance.new("Part", game.Workspace)
	Rain.Position = Vector3.new(0, 15, 0)
	Rain.Size = Vector3.new(0.5, 2, 0.5)
	Rain.Anchored = false
	Rain.Transparency = 0.5
	
	Rain.Touched:Connect(function(part)
		-- check if what the droplets has touched  
		if part == game.Workspace.SpawnLocation then
			Rain:Destroy()
		end
	end)

end
```
```lua
local groundSize = Vector3.new(75, 1, 105)
local gridSize = 5
local numCells = groundSize.X /gridSize * groundSize.Z / gridSize
local rainOffset = Vector3.new(35, 16.5, -36)

local counter = 0 -- For debug purposes

while true do
	wait(0.8)
	counter = counter + 1
	for i = 1, numCells do
		local x = ((i - 1) % (groundSize.X / gridSize)) * gridSize - groundSize.X / 2 + gridSize / 2
		local z = math.floor((i - 1) / (groundSize.X / gridSize)) * gridSize - groundSize.Z / 2 + gridSize / 2
		
		local rain = Instance.new("Part", game.Workspace.Weather.Rain)
		rain.Name = "Droplet" .. tostring(counter)
		rain.Position = Vector3.new(x, 10, z) + rainOffset
		rain.Size = Vector3.new(0.2, 1, 0.2)
		rain.Anchored = false
		rain.Transparency = 0.3

		rain.Touched:Connect(function(part)
			if part == game.Workspace.Baseplate then
				rain:Destroy()
			end
		end)
	end
end
```