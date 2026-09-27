# CameraShaker

CameraShaker is a Roblox module that provides realistic and performant camera shake effects. It is a Roblox port of Unity3D's EZ Camera Shake, with permission from the original authors.

## Purpose

Easily add camera shake effects for explosions, impacts, earthquakes, movement, and other gameplay events.

## Basic Use

```lua
local function ShakeCamera(shakeCf)
    camera.CFrame = camera.CFrame * shakeCf
end

local renderPriority = Enum.RenderPriority.Camera.Value + 1
local camShake = CameraShaker.new(renderPriority, ShakeCamera)

camShake:Start()

while true do
    task.wait(5)
    camShake:Shake(CameraShaker.Presets.Explosion)
end
```

## API

**CameraShaker**

* `Start()` — Start shaking
* `Stop()` — Stop shaking
* `StopSustained()` — Stop sustained shakes
* `Shake()` — Apply a preset shake
* `ShakeSustain()` — Apply a sustained shake
* `ShakeOnce()` — Apply a custom one-time shake
* `StartShake()` — Apply a custom sustained shake

**Presets**

* `Bump`
* `Explosion`
* `Earthquake`
* `BadTrip`
* `HandheldCamera`
* `Vibration`
* `RoughDriving`

The module is designed to make camera shake easy to implement and customise in Roblox games.
