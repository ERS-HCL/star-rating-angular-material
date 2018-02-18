# Star Rating component for Angular Material.
<p align="center">
    <img  alt="Star Rating" src="img/starRating.png" class="img-responsive">
</p>

To preview demo of star rating project, [click here](https://stackblitz.com/edit/angular-material-star-rating?embed=1&file=index.html&hideExplorer=1&hideNavigation=1&view=preview)

## Adding star rating component in your project
Download `star-rating.component` to your angular material project and include required components from angular material.

```html

<mat-star-rating [rating]="rating"  [starCount]="starCount" [color]="starColor" (ratingUpdated)="onRatingChanged($event)"></mat-star-rating>

```
## Input for star rating

```typescript

  @Input('rating') rating: number;
  @Input('starCount') starCount: number;
  @Input('color') color: string;
  
```  

Name | Description
--- | --- 
**rating** | Actual rating 
**starCount** | Maximum number of stars for rating 
**color** | Color of star in rating. Chosen from theme. `primary`, `accent` or `warn` 

### `StarRatingColor` enum from `star-rating.component`
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
