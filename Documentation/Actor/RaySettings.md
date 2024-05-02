# RaySettings
> namespace Gamekit2D.Runtime.Actor
```csharp
public record RaySettings
```

## Summary
Record that holds generic information about a raycast. Used in ground or combat checks
By itself this record does nothing. Use this record to hold data about a ray that you cast.

## Fields
| Name | Type | Description |
|------|------|-------------|
| rayLength | float | Length of the raycast |
| rayStartOffset| Vector2| The position offset to apply to the start point of the raycast |
| rayLayer | LayerMask | Layers to detect or ignore for this raycast |