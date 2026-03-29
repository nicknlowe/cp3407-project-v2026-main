# Fix autofill system in cart

Ensure autofill correctly populates user details in the cart/checkout page.

Keep any other version here as well, e.g. Improve checkout autofill, Fix form autofill issues.

## Priority: High 
This directly affects checkout usability and user experience. Errors here can prevent users from completing orders.

## Estimation: 2 days
Planning poker estimates:
* Nick: 2 days
* Dean: 2 days
* Gurjas: 3 days
* Nikodem: 2 days
* Dylan: 2 days

## Assumptions (if any):
- Users have saved details (name, address, email).
- Autofill uses browser or stored account data.
- Checkout form fields are already implemented.
- Issues currently exist with incorrect or missing autofill.
- Multiple users may access the system on the same device/browser.

## Description:

Description-v1:  
The website will correctly autofill user information such as name, address, and contact details in the cart/checkout page to streamline the ordering process.

Description-v2:  
During checkout testing, a bug was discovered where the last logged-in user's details remained in the order form. This issue was missed in earlier testing and needed to be fixed immediately in iteration 2 due to privacy and usability concerns.

## Tasks:

1. Investigate current autofill issues, Estimation 0.5 days
2. Fix form field attributes (name, id, autocomplete), Estimation 0.5 days
3. Ensure user session data is cleared or correctly reassigned on logout/login, Estimation 0.5 days
4. Integrate stored user data securely for logged-in users only, Estimation 0.5 days
5. Test autofill across different browsers and multiple user sessions, Estimation 0.5 days
6. Fix edge cases and bugs, Estimation 0.5 days


# UI Design:
* Checkout form with fields:
  - Name
  - Address
  - Email
  - Phone
* Fields automatically populated only for the current logged-in user.
* No previous user data should persist after logout or session change.

# Completed:
* Screenshots showing autofill working correctly.
* Comparison of broken vs fixed version.
* Evidence of correct behaviour across multiple user sessions.
