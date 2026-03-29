# Add hover over add to cart system

Display product details and quick add-to-cart option on hover over menu items.

Keep any other version here as well, e.g. Show quick add button, Hover preview for food items.

## Priority: Medium 
This feature improves user experience and speeds up ordering, but is not critical for core functionality. Planned for iteration 2.

## Estimation: 2 days
Planning poker estimates:
* Nick: 2 days
* Dean: 2 days
* Gurjas: 3 days
* Nikodem: 2 days
* Dylan: 2 days

## Assumptions (if any):
- Menu items are already displayed in a grid or list format.
- Each item has enough data (image, price, name) stored in database.
- Users interact using mouse/trackpad (hover supported).
- Mobile version may require alternative (tap instead of hover).

## Description:

Description-v1:  
The website will allow users to hover over a food item to quickly view details and add the item to their cart without navigating to a separate page.

## Tasks:

1. Design hover UI effect for menu items, Estimation 0.5 days
2. Implement hover detection using CSS/JavaScript, Estimation 0.5 days
3. Add “Add to Cart” button inside hover overlay, Estimation 0.5 days
4. Connect button to cart system backend, Estimation 0.5 days
5. Test responsiveness and usability, Estimation 0.5 days


# UI Design:
* Food items displayed in cards/grid layout.
* On hover, overlay appears with:
  - Item name
  - Price
  - Quick “Add to Cart” button
* Smooth animation for better UX.

# Completed:
* Insert screenshots of hover effect working.
* Show before and after versions if updated in later iterations.
