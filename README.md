# Online Crowdfunding Platform (Java - Beginner Project)

A simple, console-based crowdfunding platform written in **core Java** (no
external libraries, no database, no frameworks). It was built as a 2nd-year
Java learning project, so the code uses only the basics: classes, objects,
`ArrayList`, `HashMap`, `Scanner`, loops and methods.

## What it does

Three types of users can log in, and each one sees a different dashboard.

### Admin
- Manage users (add / update / delete)
- Manage campaigns (approve or reject)
- Change system-wide settings
- Watch an activity log of everything that happens

### Campaign Creator
- Create a fundraising campaign (title, description, goal amount)
- See all of their campaigns with progress
- Post progress updates
- Send a message to the contributors of a campaign
- View campaign analytics (number of contributors, total raised, progress %)

### Contributor
- View all approved campaigns
- Contribute money to a campaign
- Track their own contribution history
- Read campaign updates
- Manage their profile (name / email / password)

## Files in this project

| File | What it is |
|------|------------|
| `User.java` | A single user (Admin / Creator / Contributor) |
| `Campaign.java` | A fundraising campaign |
| `Contribution.java` | One contribution made to a campaign |
| `CrowdfundingPlatform.java` | The "brain": stores all data and provides methods |
| `Main.java` | Shows the menus and reads keyboard input |

All data is kept **in memory** while the program runs. When you close the
program, the data is gone (this keeps the project simple for a beginner).

## How to run

You need Java installed (JDK 17 or newer is fine). Open a terminal in this
folder and run:

```bash
javac *.java
java Main
```

`javac` compiles all the `.java` files into `.class` files, then `java Main`
starts the program.

## Default admin account

The program creates one admin automatically so you can log in right away:

```
Email:    admin@crowd.com
Password: admin123
```

Creators and contributors can register themselves from the main menu
(option 2). Their role is chosen during registration.

## A quick try-out (in order)

1. Run the program.
2. Register as a **Campaign Creator** (choose role 1).
3. Log in as that creator and **Create a Campaign**. Note the campaign ID.
4. Log out, log in as **admin** and **approve** that campaign
   (Admin Dashboard -> Manage Campaigns).
5. Register a **Contributor**, log in, and contribute to the campaign.
6. Log back in as the creator to post a progress update and view analytics.
7. Log in as admin and open **Activity Monitoring** to see the whole history.

## Notes for the future (ideas, not required)

- Save data to a file or a database so it survives after closing.
- Add a real payment step instead of the simple "Processing payment..." line.
- Replace the console menus with a graphical (Swing/JavaFX) interface.
