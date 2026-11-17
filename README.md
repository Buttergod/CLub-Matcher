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

Proposal:

For the CIT Project Showcase, I will develop the “Club Matcher” website which is designed to let students connect more to DRHS clubs and extracurriculars. It will take an interactive interest quiz and then generate a personalized list of top DRHS clubs. I plan to build this website independently and will attempt to finish by February 1st. Until then, I plan to get approved by Mrs. Norris, and therefore get acceptance for having my project be uploaded onto the official school platform. Once I build the website, I will refine and bug-test through multiple individuals.


# Code

###### Pseudocode python V1

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

###### Pseudocode python V2
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
###### HTML Club Format
```html

        const clubs = [{
            name: "write club name here",
            interests: ["the tags for interests", "you can add multiple"],
            activities: ["the tags for activity", "you can add multiple"],
            setting: "group setting"
        }, {
```

## Quick Start

1. Install Github (If you already have it, good)
```bash
winget install --id GitHub.cli
```
2. Check with version (Check it just in case)
```bash
gh --version
```
3. Login
```bash
gh auth login
```
4. Clone repo
```bash
gh repo clone Buttergod/CLub-Matcher
```
5. Open in VS Code
```bash
code CLub-Matcher
```
6. Open in localhost
```bash
python -m http.server 8000
```
7. Then go to:
http://localhost:8000/

```shortcut
Use CTRL + C to stop any processes in the terminal. 
```

## Github Pages

https://buttergod.github.io/CLub-Matcher/


## I am still trying to figure out how to get more clubs added
### A google form??
#### Please contact hcps-gangraded@henricostudents.org if you have any ideas
