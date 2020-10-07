# HORECA contact tracing

**Exercise:** Design, no code.

**Format**: Figma document. Starter document will be shared during the course.

**Timeframe**: 1 week after the course. Review and comments are done directly on your Figma file. Use the [board](https://github.com/HackYourFutureBelgium/class-11-12/projects/3) when ready to ping coaches for a request for review.

## Brief

You have been assigned to design an easy way to fill in customer details information for the COVID contact tracing center targeting restaurants and cafes in Brussels. (HORECA stands for Hotel, Restaurant, and Cafes. In this exercise, we will be focusing only on the restaurants and cafes establishments.) The interface should be seamless, effortless, and engaging for the customers, regardless of their devices, familiarity with technologies, and potential handicap. The interface should be frustration-free and hard to miss use. Adding the customer’s details is not the main goal of a customer coming to a restaurant or cafe, let’s not make it coming on their way of enjoying a hot beverage in a terrasse of Brussels!

- Design and define the steps that the customer will face.
- Design an interface with the requested data:
    - Name, contact email address or contact phone number, day of the visit, the hour or arrival, number of people at the table) [see requirements below]
- Make it easy to build, consistent, and logical for the development team and back end team.
- Make it engaging and appealing for the customer.

## Design Deliverables

- Flow design (steps required and content)
- Define layout and content blocks (wireframes) for mobile web
- Design reusable visual design styles for the look and feel of the brand, page, and controls. (for example: use consistent styles for headings, labels, and control types)
- States of controls and pages. (For example: Empty, filled in, errors)
- Propose multiple solutions (for example: in order of fields, number of steps, pages, design styles) and reasoning for design decisions (pros and cons)

### Go the extra mile

1. **What additional features you can think of that will enhance the user experience and/or development?**

> For example: provide a cheerful thank you page with an informative animation to explain what the next contact steps could be. And wish the customer a good stay a delicious meal!

> For example: Populate the establishment name by user search in a map, QR code, or based on the establishment wifi router.

> For example: support for voice to text input.

2. **A new feature.** The project manager is considering a feature to save the customer’s email addresses for the establishments to send updates on the opening times, new menus, and activities. What are the pros and cons of such a feature? (hint: think in terms of the end-user benefits and development implications)

## Requirements

**What are user stories?**

The purpose of user stories is to explain the roles of users in a system, their desired activities, and what they intend to accomplish by successfully completing a user story.

Format: _“As a (type of user), I want to (perform some action) so that I (can achieve some goal/result/value).”_

### Contact tracing center responsible

**Epic:**

**As a COVID contact center responsible I need to have enough customer data in order to contact that person in case of a case of COVID positive in a certain establishment.**

#### User stories:

1. I want to have access to the establishment name, date, and time of arrival, to quickly find all customers present on a certain establishment on a given date and time frame to have a list of potential customers been exposed to the COVID 19 virus after a positive case is detected.
    - **Acceptance criteria:**
    - The name of the establishment should be provided. By the user or by the establishment responsible. It needs to be part and attached to the customer data information. (hint: you can design different ways for detecting or entering an establishment name)
    - The establishment name should be in a single text string to be easy to search and sort on the back end data application at the tracking center. Images or GPS coordinates are not accepted.
    - The date provided must follow the [ISO 8601](https://en.wikipedia.org/wiki/ISO_8601) format YYYY-MM-DD (2020-09-09).
    - The date input should support any separators such as: “.”, “/”, ‘-” entered by the user or smartly adjust the format as typing.
    - The time of arrival at the establishment must follow a 24hours format. For example: “13h00” is valid, “1 pm” is not.
    - The date and time of arrival at the establishment are mandatory. The duration of the stay is irrelevant.
2. I need to have the first name and last name of the principal point of contact of a table, so I can address the person correctly and trace it back into the data back end system.
    - **Acceptance criteria**:
    - First and Last name free text fields. Fields should be separate for easy parsing and sorting in the data back end system.
    - Numbers in names are not accepted.
    - No minimum or maximum limit of characters.
    - Name and first name are mandatory.
    - Titles (prefix or suffix) are not mandatory and will not be used for contact tracking nor discrimination. (hint: you can design a solution without or without Titles (Sir, Miss, Madam, Professor, etc) as long you can argue for your design decision)
3. I need to have an email or phone contact number in order to contact back as quickly as possible the customer and its group in case of a case detected.
    - **Acceptance criteria:**
    - Only a single contact channel is required, an email address or a phone number. Allow the user to choose which one to provide. Having one contact channel is mandatory.
    - Email addresses must be valid email addresses (for example: with @ sign)
    - Phone numbers should be validated as such (for example: only numbers are accepted in the field)
    - Phone numbers from foreign countries are also accepted. A country indicative is required.
    - In the case of mobile devices, display the correct numerical keyboard for phone number input.
4. I would benefit from having an estimation of how people were sharing the table with the customer so I can evaluate the number of contacts I need to trackback.
    - **Acceptance criteria:**
    - Today a group sitting at a table is limited to 10 people. Validation should be adjustable if the legal number changes.
    - Only one customer contact per table can be provided.
    - The value of the maximum number can change if the situation evolves (for example: limit to 5 or no limit at all)
    - The number of persons per table is optional.
    - In the case of mobile devices, display the correct numerical keyboard for phone number input.

### Customer (User)

#### User stories:

5. As a non-tech savvy user, I want to be able to access the interface with my old phone.
    - **Acceptance criteria:**
    - The interface should work cross platforms, on slow internet. (hint: list the pros and cons of an app versus a website. Consider responsive states and keyboard interactions or other solutions if the user does not own a device)
6. As a non-English speaking user, I want to be able to switch the interface to a language that I am familiar with.
    - **Acceptance criteria:**
    - Users must be able to access the same interface in different languages supported: English, French, Dutch, and German (tip: you do not need to translate each screen, provide an entry point for the language switch)
    - Change of language must be present at all times.
    - The interface should support different character lengths in labels and value strings.
7. As a user, I want to effortlessly fill in my details and be able to correct if I made a mistake.
    - **Acceptance criteria:**
    - Users must be able to edit a field already filled in.
    - Users cannot enter dates in the future.
    - Validate email, phone number, date, and time fields by providing an error message clear with plain language.
    - If multiple errors occur, display a summary of the errors and indicate the errors in the specific fields that triggered an error.
    - If the user is editing the fields for the first time, no error should be triggered in line. For example: the email field should not be in error even if the user did not insert “@” yet.
8. As a user, I want to provide only the necessary information about me so I can trust the interface.
    - **Acceptance criteria:**
    - Only prompt an error on mandatory fields.
    - Provide access to data privacy terms and conditions.
    - The interface should convey a sense of modernity and security (hint: you can play with professional typography, use supporting visuals that are easily recognizable as secure items, use a human and reassuring tone of voice)



Have fun!


Bonus fun for reading: [Your Last Name Contains Invalid](https://blog.jgc.org/2010/06/your-last-name-contains-invalid.html) and [Awesome Falsehood](https://github.com/kdeldycke/awesome-falsehood)
