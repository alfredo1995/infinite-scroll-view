# ScrollView in Unity infinite and recyclable, optimized to handle a large number of elements without compromising performance. 

<br>

![unity-infinite-reusable-scroll-view](https://github.com/alfredo1995/infinite-scroll-view/assets/71193893/6d877a7f-02d5-4911-83a3-8685e4d142da)

<br>

<h3>  Practical Implementation: Developed an infinite and recyclable ScrollView that can be used in mobile and desktop WebGL applications. </h3> 

ScrollView (Managing the content of the ScrollView, organizing the arrangement and spacing of child items within it.)

    Beginning of Logic: Getting child RectTransforms from a parent RectTransform
    Initial configuration of a flexible content layout within a RectTransform, taking into account margins and orientation (horizontal or vertical).
    Positioning of child elements within the parent object's RectTransform, maintaining an orderly and spaced arrangement according to the layout orientation (horizontal or vertical).

InfiniteScroll (Implementing infinite scroll functionality for a ScrollView, allowing items to dynamically reposition themselves when dragging or scrolling the ScrollView.)

    Beginning of Logic: Calling objects when initialized
    ScrollRect to allow scrolling and moving ("unconstrained") based on scrollContent properties, respectively.
    Determining when an object starts to be dragged. Using an OnBeginDrag(PointerEventData eventData) callback function that is part of the IBeginDragHandler interface.
    Determining while an object is being dragged (during pointer movement). Using OnDrag(PointerEventData eventData) callback function from IDragHandler interface.
    Scroll event, movement of the mouse scroll wheel. Using an OnScroll(PointerEventData eventData) callback from the IScrollHandler interface.
    OnViewScroll() function to handle scroll events in a view component.
    ReachedThreshold(Transform item) function checking whether an item has reached the limit for scrolling out of view in a ScrollView, based on the orientation (vertical or horizontal) of the ScrollView and the user's dragging direction.

ItemManager (Managing the dynamic creation of image items (Image) with specific colors, limiting the number of items created based on a color list (ColotList).

ColotList (Using ScriptableObject as a color list resource that can be created and managed in the Editor)


<strong>  Project Architecture (Component-Based Design) for each component to have a specific responsibility, such as managing game logic, the appearance of objects and user interaction.

    Content Management System: ItemManager handling dynamic creation of items in the UI based on a list of colors. Where objects are instantiated and dynamically managed at runtime.
    Factory Design Pattern: Using Instantiate to create objects from a prefab follows a simplified factory design pattern, where objects are created without the need for direct code construction, making the system more flexible and modular.
    Scriptable Objects: Using a ScriptableObject to store a list of colors (ColorList) is a common practice for maintaining data and settings that can be shared between multiple objects and instances during game execution.

This software architecture for game development follows principles of object-oriented design, modularity and component reuse. Contributing to organized, flexible, and scalable code as your game project evolves.
