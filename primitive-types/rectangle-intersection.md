### Rectangle Intersection

**Description/**

Judge if two rectangles have nonempty intersection.

**Variant/**

1. Given four points, check if these four points can compose a rectangle
2. Given two rectangles whose sides don't need to align with x-axis and y-axis, check if these two rectangles intersect.

-------------------------------- Leonard --------------------------

**Thoughts/**

**Code/**

```
public Rectangle intersectRect(Rectangle a, Rectangle b) {





















}
```

-------------------------------- Luckman -------------------------

**Thoughts/**

```
  ┌───┐
  │   │
  └───┘
 four sides: left , right, top, bottom
 
 bottom left (b_x, b_y)
 top right   (t_x, t_y)
 
 
 
 Overlap:
 left  = max(b_x1, b_x2) 
 right = min(t_x1, t_x2)
 
  |     |               |     |                |  |        |  | 
     |      |       |           |        |  |                    |  |
 
     l   r              l     r             r  l              r  l


 top = max(b_y1, b_y2) 
 bot = min(t_y1, t_y2)

     
```



**Code/**

```
class Rectangle{
    int[] botLeft;
    int[] topRight;
    Rectangle(int[] bLeft, int[] tRight){
        botLeft = bLeft;
        topRight = tRight;
    }
}


public Rectangle intersectRect(Rectangle a, Rectangle b) {
    int left = Math.max(a.botLeft[0], b.botLeft[0]);
    int right = Math.min(a.topRight[0], b.topRight[0]);
    int bot = Math.max(a.botLeft[1], b.botLeft[1]);
    int top = Math.min(a.topRight[1], b.topRight[1]);
    if(right <= left || top <= bot) {
        return new Rectangle(new int[]{0, 0}, new int[]{0, 0});
    } else {
        return new Rectangle(new int[]{left, bot}, new int[]{top, right});
    }
}


```

-------------------------------- Author ------------------------------

**Thoughts/**

```

```



