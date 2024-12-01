# Events and Festival Ticket Auction Website
> Built with `React`, styled with `styled-components`, fetched data with `REST API`
- [Original Repo](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-frontend)
- [Demo Video](https://youtu.be/v78D9IcYdU8)

I served as the **product manager** and **front-end developer** for a project that aimed to create a platform for purchasing events and festival tickets through an auction system. Additionally, 10% of the ticket purchase amount would automatically be donated to support cultural and artistic activities for low-income individuals. Our team consisted of three front-end developers and two back-end developers, and we completed the project in just two weeks. During the planning phase, we drew insights from auction platforms for limited products, NFT market platforms, and ticket sales websites to refine our project's details.

## Workflow

As the product manager, I wanted to maximize the completeness of our product within a short timeframe of two weeks. To work efficiently, we discussed and shared the envisioned state of our product using [**Figma**](https://www.figma.com/design/vocTAwfV7Xf1w9ByUaoFLU/Kulture-Design?m=auto&t=cUY65U21tlddJJtl-6). I also created a **Product Requirements Document (PRD)** to ensure that all team members had a precise understanding of the product's features and specifications. We managed this document collaboratively, with each team member responsible for their respective sections.

### **User Flow Chart**

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FWJt1ZaNsWD40447FOrIe%2Fimage.png?alt=media&token=d9bc2a3e-ca41-400a-b435-b69f02595275" alt="User Flow Chart" width="400" />

### **Wireframes - Figma**&#x20;

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FnyppytifYpmoSY6ORI00%2Fimage.png?alt=media&token=b7e4969f-370b-4cb6-b3db-ee04ff34d290" alt="Wireframes" width="400" />

I simplified the page layout decided upon during our meetings into wireframes. Reusable UI components were color-coded for easy identification and later conversion into components.

### **UX/UI Design -** [**Figma**](https://www.figma.com/file/gAqeaKZLItF7228PsRHKCj/Kulture-Design?type=design\&node-id=1%3A2\&mode=design\&t=jGN5WL1rQNsDmKHc-1)

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FnZaIfgUUjnQPCQzwwkEG%2Fimage.png?alt=media&token=f96701ea-b449-4372-8f7d-f5f1c3c54fe4" alt="UI Design 1" width="400" />
<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FpPtsApH2JENwKtXdYDyK%2Fimage.png?alt=media&token=2f213e72-d638-4665-ba75-4304fbc941c0" alt="UI Design 2" width="400" />

I shared the wireframes with team members, and they used them as a basis to work on specific UI elements independently. Since we didn't have a dedicated designer, this approach allowed us to allocate more time to actual development work.

### **Design System -** [**Figma**](https://www.figma.com/file/gAqeaKZLItF7228PsRHKCj/Kulture-Design?type=design\&node-id=0%3A1\&mode=design\&t=0dHAxNTIONIlXmCt-1)

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FLm6KV9oeAFPfYQcgbdRq%2FScreenshot%202023-09-17%20at%2018.24.35.png?alt=media&token=0df02236-4016-4683-9d30-93fe98d5a599" alt="Design System" width="400" />

Given that multiple front-end developers were creating a product from scratch, I believed it was essential to establish a **unified design system**. This design system proved useful during UI planning and actual code implementation. In the future, I would like to explore more advanced design systems using tools like Storybook.

## My Responsibility as a Developer

In this project, I was responsible for implementing user registration & login, purchasing prepaid tokens, user dashboard, and review functionalities.

### User Registration/Login: Using OAuth API by Kakao - [PR](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-frontend/pull/19)

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FS1EmGxxNVQBoT9YzcDKm%2Flogin-re.gif?alt=media&token=a58638d0-db77-44cf-99ac-fad0d3306dbe" alt="User Registration/Login" width="400" />

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FzT5WK2fG93mmLNRGH2Rl%2Fimage.png?alt=media&token=d7ee86a0-39eb-4822-a34e-68aee00c05e9" alt="Kakao OAuth" width="400" />

Our service aims to provide the best user experience when logged in. Therefore, we needed to minimize the hurdles of user registration and login. I implemented a simple registration and login process using Kakao accounts.

1. Authentication request to Kakao server
2. Passing the Kakao-issued token to the backend
3. Conditional rendering of navigation bar buttons based on the presence of the AccessToken issued by the backend

### Prepaid Token Purchase:  Using Payment API by Kakao - [PR](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-frontend/pull/39)

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FQ3TazOI2IV1HpcVn84L7%2Fkakaopay1.gif?alt=media&token=c5980cee-bc81-435d-b184-f4d48a2437d4" alt="Prepaid Token Purchase" width="400" />

To create a unique experience for our users and add an element of fun to the auction and ticket purchase process, we introduced payment with 'token'. This approach had benefits for both users and our service. Users could conveniently and quickly purchase tickets with prepaid tokens, while our service could secure cash upfront. We incentivized users to select charge options with larger amounts by offering additional token incentives.

Prepaid token purchase was implemented with the Payment API by Kakao for easy payments for users, using SearchParams.

1. Request payment preparation to the Kakao server
2. The user completes payment via a QR code
3. Request payment approval from the Kakao server
4. POST request to the backend

### Token Transaction History - [PR](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-frontend/pull/43)

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2F2Aqxr0yWMx8JxbImuWaX%2Fimage.png?alt=media&token=2703f400-954b-4d7a-93c5-5b36568c2f5a" alt="Token Transaction History" width="400" />

This is a feature designed to meet the needs of users who want to check where their own money has been spent. Since it involves money, we allowed users to view precise transaction details down to the second. Additionally, to intuitively distinguish between charge and usage history, different font colors have been set.

* Based on the token transaction data received from the backend, conditional rendering is done based on the type of transaction: 'charge' or 'usage'.
* The transaction type value is received as props to differentiate styling between charge and usage amounts.

### User Dashboard - [PR](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-frontend/pull/2)

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FIXK9k4BSTkgRThMOZRN4%2Fimage.png?alt=media&token=1c1b5417-4fb4-4905-bc92-f0be6d8139a5" alt="User Dashboard" width="400" />

* Sent requests to the USER, BID, and ORDER endpoints for data.
* Placed a CTA button that encourages the important conversion event, 'Token Recharge.'
* On the frontend, converted 10% of the total order amount(in tokens) into KRW and displayed the total donation amount.

### Bidding History - [PR](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-frontend/pull/30)

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FWZRXcYItcABZ7yeGcBTQ%2FMyAuction.gif?alt=media&token=d96158d3-bc62-4567-b19e-22bb36c41b59" alt="Bidding History" width="400" />

To provide clarity, I separated ongoing bids and completed bids using a tab. For completed bids, I added 'success' or 'failure' indicators, differentiating them with font colors.

### Accept the Successful Deal - [PR](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-frontend/pull/29)

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FEn6n9OHZuvCDxlQJ5Wdk%2Facceptdeal.gif?alt=media&token=6c31b103-f99a-4bc2-bdd6-75855ec2a888" alt="Accept the Successful Deal" width="400" />

When a user's bid ranked high enough at the end of the bidding period, the bid appeared in the "Waiting for Acceptance" list. Users could click the "Confirm Purchase" button to accept the deal. To ensure users were aware of token deductions, I displayed a notification if their token balance was insufficient, encouraging them to charge more tokens.

When the button was clicked, tokens were deducted, ORDER request was sent to the backend.

### Tickets in QR Codes Format - [PR](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-frontend/pull/25)

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FmUcKtyS4ADw2N7LyJZlC%2Fgrcode.gif?alt=media&token=73dab2a0-1907-4b0a-b63f-d9d3c2343f72" alt="Tickets in QR Codes Format" width="400" />

On the My Page, users can check the QR code for valid tickets. Tickets were considered valid if the event date was in the future compared to the viewing date. For past events, I provided the option to leave reviews instead of checking tickets.

* I used a QR code generation library.
* I compared the event date to the viewing date to conditionally render the buttons.

### Posting Image Reviews: Using FormData - [PR](https://github.com/wecode-bootcamp-korea/46-2nd-Kulture-frontend/pull/32)

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2F8K2bK3S2xgPekh99UYNS%2Freviewpost.gif?alt=media&token=1a267663-0531-42fd-a68a-139b1e684678" alt="Posting Image Reviews" width="400" />

For tickets with event dates in the past, I offered the option to leave reviews. When the event date had passed, the system automatically moved the event to the "Past Events" section on My Page, replacing the "Check Tickets" button with a "Leave Review" button.

* To post reviews, I created an object with the event's ID and the user's text input. I used the `type="file"` input to upload images via **FormData** and send a POST request to the backend.
* Default file upload buttons were replaced with custom button images using the `<label>` tag.

### Viewing and Deleting Reviews

<img src="https://2266874734-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2F2we7vFcb6Db4hZ3nq1Be%2Fuploads%2FRxw7QNHBt6d9mOmOyLmU%2Fdeleteee.gif?alt=media&token=c6e8183e-9a65-4979-b4cf-7c362163d678" alt="Viewing and Deleting Reviews" width="400" />

* All reviews can be accessed on the REVIEWS page, and users can delete the reviews they have posted. The UI of the review page is designed to emphasize images, which aligns with the nature of the platform.
* Render all review data using the Array.map() method.
* Compare the USER ID of the review with the logged-in user's ID, and render the delete button only if they match.
* When the delete button is clicked, send a DELETE request to the backend for removal.

## Retrospective

This project allowed me to deeply consider user experience when building a product. Based on insights gained from our other projects, our team was able to work more efficiently. We minimized trial and error and tackled more challenging technologies as a team.

As a developer, I understand that valuable experiences come from facing different issues and finding solutions, no matter the problem. If I encounter similar issues in the future, I will be able to solve them more efficiently. In the real world, I expect to encounter even more complex problems, and I'll accumulate insights and continuously improve my abilities to solve them better.
