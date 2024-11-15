# Creating Shapes In SwiftUI

??? example "Source Code"
    [**Source Code**](../../../src/SwiftUICookbook/SwiftUICookbook/ShapesSwiftUI.swift)

SwiftUI provides a robust set of tools for creating and customizing shapes in your app. Shapes like `Circles`, `Ellipse`, `Rectangle`, `Capsule`, and `RoundedRectangle` can be easily added to your views, making it simple to create visually appealing designs. This guide will walk you through the basics of adding these shapes and customizing their appearance.

## Creating Basic Shapes

### Circle

<!-- md:version 7.1.0 -->

The `Circle` shape is straightforward to create and use. Here's an example:

```swift
import SwiftUI

struct ShapesSwiftUI: View {
    var body: some View {
        Circle()
            .frame(width: 200, height: 200)
    }
}
```

In this example, we create a `Circle` shape and set its frame to 200x200 points.

![Circle](../../assets/Screenshot%202024-06-11%20at%208.55.04%20PM.png)
![Circle](../assets/Screenshot%202024-06-11%20at%208.55.04%20PM.png)

### Ellipse

The `Ellipse` shape can be created similarly, and it automatically adjusts its aspect ratio based on the frame provided:

```swift
struct ShapesSwiftUI: View {
    var body: some View {
        Ellipse()
            .frame(width: 300, height: 200)
    }
}
```

This code snippet creates an ellipse with a width of 300 points and a height of 200 points.

![Ellipse](../assets/Screenshot%202024-06-11%20at%208.56.28%20PM.png)

### Rectangle

Creating a rectangle is just as simple:

```swift
struct ShapesSwiftUI: View {
    var body: some View {
        Rectangle()
            .frame(width: 300, height: 200)
    }
}
```

Here, a `Rectangle` shape is created with specified dimensions.

![Rectangle](../assets/Screenshot%202024-06-11%20at%208.57.35%20PM.png)

### Rounded Rectangle

A `RoundedRectangle` shape allows you to set the corner radius for rounded corners:

```swift
struct ShapesSwiftUI: View {
    var body: some View {
        RoundedRectangle(cornerRadius: 30)
             .frame(width: 300, height: 200)
    }
}
```

This creates a rectangle with rounded corners, where the corner radius is set to 30 points.

![Rounded Rectangle](../assets/Screenshot%202024-06-11%20at%208.59.28%20PM.png)

## Customizing Shapes

Shapes in SwiftUI can be customized with various modifiers to change their appearance.

### Fill

You can fill a shape with a color or add a stroke (border):

```swift
struct ShapesSwiftUI: View {
    var body: some View {
        Circle()
            .fill(.blue)
            .frame(width: 300, height: 300)
    }
}
```

![Fill](../assets/Screenshot%202024-06-11%20at%209.02.30%20PM.png)

### Stroke

```swift
struct ShapesSwiftUI: View {
     var body: some View {
         Circle()
             .stroke(.red, lineWidth: 20)
             .frame(width: 300, height: 300)
     }
}
```

The first example fills the circle with red, and the second adds a red stroke to the rectangle.

![Stroke](../assets/Screenshot%202024-06-11%20at%209.04.55%20PM.png)

### Shadow

You can adjust the opacity and add a shadow to shapes:

```swift
struct ShapesSwiftUI: View {
    var body: some View {
        Ellipse()
            .fill(Color.green)
            .frame(width: 300, height: 200)
            .shadow(color: .blue, radius: 10, x: 0, y: 15))
    }
}
```

This example creates an ellipse with blue fill, and a shadow.

![Shadow](../assets/Screenshot%202024-06-11%20at%209.07.28%20PM.png)

### Gradient Fills

SwiftUI also supports gradient fills for shapes:

```swift
struct ShapesSwiftUI: View {
    var body: some View {
        RoundedRectangle(cornerRadius: 20)
            .fill(
                LinearGradient(
                    gradient: Gradient(colors: [.blue, .orange]),
                    startPoint: .topLeading,
                    endPoint: .bottomTrailing
                )
            )
            .frame(width: 300, height: 200)
    }
}
```

Here, we apply a linear gradient to a rounded rectangle.

![Gradient Fills](../assets/Screenshot%202024-06-11%20at%209.09.22%20PM.png)
