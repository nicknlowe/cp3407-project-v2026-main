# CP3407 Project - Testing Explanation

## Testing Approach

At the start of the project, we planned to use a structured testing strategy including:

- **Test-Driven Development (TDD)** – writing tests before implementing features  
- **Unit Testing** – testing individual functions and components  
- **Integration Testing** – verifying interaction between system components  
- **System Testing** – testing complete user workflows  
- **Acceptance Testing** – validating features against client requirements  

We also planned to use a variety of test data, including valid, invalid, and boundary inputs, to ensure reliability.

## The Testing We Performed

In practice, we partially followed our planned approach:

- TDD was used for some components, particularly smaller logic-based features, but not consistently across the entire project  
- Unit testing was applied to key functionality of the site  
- **Integration testing was performed by testing interactions between components such as the frontend, backend, and database. For example, we tested adding items to the cart, ensuring data was correctly passed and stored.**  
- **System testing was performed by manually testing complete user workflows, such as browsing products, adding items to the cart, and completing the checkout process to ensure the system worked end-to-end.**  
- Acceptance testing was conducted through client demonstrations at the end of each iteration  

## Client Feedback (Iteration 1)

During the Iteration 1 demonstration, our client identified several issues:

- Add hover-over “add to cart” functionality  
- Fix autofill bug where previous user details persisted  
- Remove redundant footer links  
- Implement a functional “Shop by Category” page  

This revealed that some issues were not detected during internal testing, particularly the autofill bug. It demonstrated the importance of acceptance testing and real user interaction.

## Improvements Based on Testing

Following testing and feedback, we:

- fixed bugs identified during client use  
- improved usability and navigation  
- ensured features aligned more closely with user expectations  

## Conclusion

While our initial testing plan was comprehensive, it was only partially implemented in practice. However, combining internal testing with client feedback allowed us to identify issues, improve the system, and better meet project requirements.
