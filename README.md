# ClubMatcher
# WIP

Ovr:
ClubMatcher is a website that is made for DRHS students. It takes an interactive quiz which then lets the student get a personalized list of top matching clubs at DRHs. This makes it easy for students to discover extracurriculars that they enjoy

Feat:
Interactive quiz: Students input main intreasts
Automatic club matchinfg: Filters and finds diffrent clubs and displays the matching clubs to the students
UI: Clean and friendly UI

Goals:

Created as an individual project and will be using Scrum methodology
Developed to meet the deadline(Feburary 1st)

# Pseudocode

Pseudocode python V1
```python
import ClubDatabaseModule  # Placeholder for the actual module that contains club data

print("Welcome to ClubMatcher!")

print("What is your main interest? Tech, arts, sports, science")  # Placeholder for user input (Will be actual cards for user to select)
userInterest = input()

matchingClubs = []
for club in ClubDatabaseModule.getAllClubs():
    if club.matches(userInterest):
        matchingClubs.append(club)

print("Here are the clubs that match your interests:")
print(matchingClubs)
```

Pseudocode python V2
```python
try:
    import ClubDatabaseModule  # type: ignore[import-not-found]
except ImportError:
    class _Club:
        def matches(self, _interest):
            return False

    class _ClubDatabaseModule:
        @staticmethod
        def getAllClubs():
            return []

    ClubDatabaseModule = _ClubDatabaseModule()

print("Welcome to ClubMatcher!")

print("What is your main interest? Tech, arts, sports, science")  # Placeholder for user input (Will be actual cards for user to select)
userInterest = input()

matchingClubs = []
for club in ClubDatabaseModule.getAllClubs():
    if club.matches(userInterest):
        matchingClubs.append(club)

print("Here are the clubs that match your interests:")
print(matchingClubs)
```
## I am still trying to figure out how to get more clubs added
### A google form??
#### Please contact hcps-gangraded@henricostudents.org if you have any ideas
