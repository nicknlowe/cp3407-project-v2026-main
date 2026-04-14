# CP3407 Project - Testing Explanation

## Initial Testing Approach

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
- Unit testing was applied to key functionality of the site using test product, business and user data to verify that components handled regular use cases
- System testing was performed by manually testing complete user workflows, such as browsing products, adding items to the cart, and completing the checkout process to ensure the system worked end-to-end
- Integration testing was performed by testing interactions between components such as the frontend, backend, and database. For example, we tested adding items to the cart, ensuring data was correctly passed and stored
- Acceptance testing was conducted through client demonstrations at the end of each iteration

Through this approach, we were able to discover issues with certain components like the payment processing early enough to address them before they affected dependent features, though some defects were identified later in development due to inconsistent TDD adoption.

## Client Feedback - Iteration 1

During the Iteration 1 demonstration, our client identified several issues:

- Autofill bug where previous user details persisted
- Redundant footer links
- Non-functional 'Shop by Category' navigation link

This revealed that some issues were not detected during internal testing, particularly the autofill bug. It demonstrated the importance of acceptance testing and real user interaction.

## Improvements Based on Testing - Iteration 1

Following testing and feedback, we:

- Fixed the autofill bug to ensure that previous user details no longer persist between sessions, preventing unintended data carryover
- Removed the redundant footer links to improve navigation clarity and reduce unncessary clutter in the UI
- Moved the submenus of the 'Shop by Catgeory' menu link to the main 'Order Now' navigation option and removed the 'Shop by Category' menu

## Testing Approach - Iteration 2

Building on the lessons learned from Iteration 1, we refined our testing approach for Iteration 2 with a greater emphasis on consistency and coverage:

- TDD was applied more consistently across new features developed in this iteration, informed by the gaps identified when the autofill bug was missed during internal testing
- Unit testing continued to be applied to key functionality, with additional test cases written to cover edge cases and scenarios that were previously overlooked
- Integration testing was performed to verify that the navigation changes, particularly the restructuring of the 'Shop by Category' menu into the 'Order Now' option, worked correctly across the site
- System testing was conducted on complete user workflows to ensure that changes made following Iteration 1 feedback did not introduce regressions
- Acceptance testing was again carried out through a client demonstration at the end of the iteration, with closer attention paid to user interaction scenarios that internal testing may not anticipate

## Conclusion

While our testing approach was not always executed as consistently as initially planned, the combination of internal testing and iterative client feedback proved effective in identifying and resolving issues throughout the project. Acceptance testing in particular demonstrated its value when client demonstrations surfaced defects that internal testing had not caught, such as the autofill bug discovered in Iteration 1. Across both iterations, our testing efforts allowed us to progressively improve the system's functionality, usability, and reliability. Each round of feedback informed targeted fixes and refinements, ensuring the product better aligned with client expectations over time.
