# Inputs
> Gamekit2D.Runtime.Utils / Inherits from Singleton / Sealed
<br>

This class is designed to override the existing InputSystem functionality. It builds onto InputSystem by automatically handling scene functionality. You should not be using this class directly unless in very specific circumstances.

```cs
using Gamekit2D.Runtime.Utils;
using UnityEngine.InputSystem;
using UnityEngine;

public class ExampleClass : MonoBehaviour
{
  private void Start()
  {
    Vector2 movementVector = Inputs.move.ReadValue<Vector2>();
  }

  private void OnEnable() => Inputs.dash += OnDash;
  private void OnDisable() => Inputs.dash -= OnDash;

  private void OnDash(InputAction.CallbackContext callbackContext) => Debug.Log("dashed!");
}
```

## Properties
Key bindings can be viewed or changed in the default InputActionAsset
| Name | Type | Description |
|-|-|-|
| move | InputAction | Movement input value. |
| dash | InputAction | Dash input value. |
| leftMouse | InputAction | Left mouse button input value. |
| reset | InputAction | Reset key input value. |
| reload | InputAction | Reload input value. |
| move | InputAction | Movement input value. |
| rightMouse | InputAction | Right mouse button input value. |
| scrollWheel | InputAction | Scroll wheel input value. |
| mousePosition | Vector3 | Position of the mouse in world coordinates. |
