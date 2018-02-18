#Star Rating component component for Angular Material.
<p align="center">
    <img  alt="Star Rating" src="img/starRating.png" class="img-responsive">
</p>
[Click to see the demo](https://angular-material-todolist-2rug3q.stackblitz.io)


## Adding star rating component in your project

```html

<mat-star-rating [rating]="rating"  [starCount]="starCount" [color]="starColor" (ratingUpdated)="onRatingChanged($event)"></mat-star-rating>

```
## Input for star rating

```typescript

  @Input('rating') rating: number;
  @Input('starCount') starCount: number;
  @Input('color') color: string;
  
```  

Markdown | Less | Pretty
--- | --- | ---
*Still* | `renders` | **nicely**
1 | 2 | 3

## Color enum
```typescript

enum StarRatingColor {
  primary = "primary",
  accent = "accent",
  warn = "warn"
}
  
```

## Listening to events
```typescript

onRatingChanged(rating){
	console.log(rating);
	this.rating = rating;
}
  
```
