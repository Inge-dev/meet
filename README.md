# Meet App

A serverless, progressive web app (PWA) built with React and integrated with the Google Calendar API. Users can filter events by location, choose how many events to display, and use the app offline.

## Features

1. Filter events by city
2. See details of each event
3. Specify number of events
4. Use the app offline
5. Add a shortcut to the home screen
6. View a chart showing the number of events by city

---

## User Stories and Scenarios

### Feature 1: Filter Events By City

**User Story:** As a user
  I want to filter events by city
  So that I can see only the events that interest me in a specific location

  **Scenario:** When user hasn’t searched for a city, show upcoming events from all cities
    Given the user has opened the app
    And has not searched for a specific city
    When the list of events is displayed
    Then upcoming events from all cities should be shown

  **Scenario:** User should see a list of suggestions when they search for a city
    Given the user is on the main page
    When the user types a city name into the search box
    Then a list of city suggestions matching the input should appear

  **Scenario:** User can select a city from the suggested list
    Given the user sees a list of city suggestions
    When the user selects a city from the list
    Then only events from the selected city should be displayed


### Feature 2: Show/Hide Event Details

**User Story:** As a user 
  I want to be able to expand and collapse event details so that I can view more or less information as needed

**Scenario:** An event element is collapsed by default
    Given the user has opened the app
    When the list of events is displayed
    Then each event element should be collapsed by default

**Scenario:** User can expand an event to see details
    Given the list of events is displayed
    When the user clicks on an event
    Then the event details should expand and be visible

**Scenario:** User can collapse an event to hide details
    Given an event’s details are expanded
    When the user clicks on the event again
    Then the event details should collapse and be hidden

### Feature 3: Specify Number of Events

**User Story:** As a user
  I want to specify how many events are shown
  So that I can control the number of events displayed on the page

  **Scenario:** When user hasn’t specified a number, 32 events are shown by default
    Given the user has not entered a number of events
    When the events are loaded
    Then 32 events should be displayed by default

  **Scenario:** User can change the number of events displayed
    Given the list of events is displayed
    When the user sets the number of events to 10
    Then only 10 events should be displayed

  ### Feature 4: Use the App When Offline

  **User Story:**  As a user
  I want to use the app offline
  So that I can still see cached events or know when features are unavailable

  **Scenario:** Show cached data when there’s no internet connection
    Given the user has previously loaded events
    And the user is now offline
    When the app is opened
    Then cached events should be displayed

  **Scenario:** Show error when user changes search settings (city,      number of events)
    Given the user is offline
    When the user changes the city or number of events
    Then an error message should be shown indicating the action cannot be completed offline

  ### Feature 5: Add an App Shortcut to the Home Screen

  **User Story:** As a user
  I want to add the app to my home screen
  So I can access it easily like a native app

  **Scenario:** User can install the meet app as a shortcut on their device home screen
    Given the user has opened the app in a supported browser
    When the browser shows the install prompt
    Then the user can add the app to their device home screen

  ### Feature 6: Display Charts Visualizing Event Details

  **User Story:** As a user
  I want to see visual data about upcoming events
  So I can understand trends and distributions easily

  **Scenario:** Show a chart with the number of upcoming events in each city
    Given the user is viewing the main page
    When the events are loaded
    Then a chart should be displayed showing the number of upcoming events in each city

## Deployment

The app is deployed on Vercel: [https://meet-rose-kappa.vercel.app](https://your-vercel-url.vercel.app)

---

## Technologies Used

- React
