<!DOCTYPE html>
<!--By Divit-->
<!--I don't know how this code works 😭😭-->
<!--Before 2 people understood how this code worked... Me and God-->
<!--Now it is only god-->


<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>ClubMatcher</title>
    <style>
         :root {
            --bg: #eaf7f7;
            --panel: #ffffff;
            --primary: #2d8c8c;
            --primary-dark: #1f6f73;
            --text: #12313b;
            --muted: #5f7a7d;
            --border: #b9dfe3;
            --success: #2f8f73;
        }
        
        * {
            box-sizing: border-box;
            .box {
                border-radius: 8px;
            }
        }
        
        body {
            margin: 0;
            font-family: Arial, Helvetica, sans-serif;
            background: linear-gradient(135deg, #d7f0ee, #eef9f8);
            color: var(--text);
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            position: relative;
        }
        
        .brand {
            position: fixed;
            top: 18px;
            left: 18px;
            z-index: 10;
            width: 180px;
            max-width: calc(100vw - 36px);
        }
        
        .brand img {
            display: block;
            width: 100%;
            height: auto;
            border-radius: 8px;
        }
        
        .container {
            width: min(92vw, 700px);
            background: var(--panel);
            border: 1px solid var(--border);
            border-radius: 8px;
            box-shadow: 0 12px 30px rgba(31, 41, 55, 0.08);
            padding: 32px;
        }
        
        h1 {
            margin: 0 0 20px;
            font-size: 2rem;
        }
        
        label {
            display: block;
            margin-bottom: 10px;
            font-weight: 600;
        }
        
        select,
        button {
            width: 100%;
            padding: 12px 14px;
            border: 1px solid var(--border);
            font-size: 1rem;
        }
        
        select {
            background: #f2fbfb;
            color: var(--text);
            margin-bottom: 16px;
        }
        
        button {
            background: var(--primary);
            color: #ffffff;
            border: none;
            cursor: pointer;
            font-weight: 600;
            transition: background 0.2s ease;
        }
        
        button:hover {
            background: var(--primary-dark);
        }
        
        .results {
            margin-top: 28px;
        }
        
        .results h2 {
            font-size: 1.25rem;
            margin-bottom: 12px;
        }
        
        #club-list {
            list-style: none;
            padding: 0;
            margin: 0;
            display: grid;
            gap: 12px;
        }
        
        .club-item {
            background: #f6fbfb;
            border: 1px solid var(--border);
            border-left: 6px solid var(--success);
            padding: 14px 16px;
            font-weight: 600;
            color: var(--text);
        }
        
        .club-name {
            display: block;
        }
        
        .club-tag {
            display: inline-block;
            margin: 8px 6px 0 0;
            padding: 4px 8px;
            background: #e3f3f2;
            color: var(--primary-dark);
            font-size: 0.8rem;
            font-weight: 600;
        }
        
        .empty {
            color: var(--muted);
            font-style: italic;
        }
    </style>
</head>

<body>
    <div class="brand" aria-label="ClubMatcher logo">
        <img src="https://files.smartsites.parentsquare.com/14080/_variants/contain-1440w/header_logo_img_jksgpev6io09cehdioh.png" alt="ClubMatcher logo" />
    </div>

    <main class="container">
        <h1>Welcome to ClubMatcher!</h1>
        <p>
            Check out your club at: <a href="https://docs.google.com/spreadsheets/d/1wrNmQpDBZMarfah7XkIsK_n-VAV0Rm66Eb9pWYqpUf8/edit?usp=sharing" target="_blank" rel="noopener noreferrer">Deep Run Clubs!</a>
        </p>

        <label for="interest">What is your main interest?</label>
        <select id="interest" aria-label="Select your interest">
                <option value="">Choose one...</option>
                <option value="technology">Technology</option>
                <option value="science">Science</option>
                <option value="arts">Arts and creativity</option>
                <option value="sports">Sports and fitness</option>
                <option value="community">Community service</option>
                <option value="business">Business and leadership</option>
                <option value="nature">Nature and outdoors</option>
            </select>

        <label for="activity">What would you like to do?</label>
        <select id="activity" aria-label="Choose an activity">
                <option value="">Any activity</option>
                <option value="build">Build or solve problems</option>
                <option value="create">Create or perform</option>
                <option value="compete">Compete or stay active</option>
                <option value="help">Help the community</option>
                <option value="learn">Learn and discuss</option>
            </select>

        <label for="setting">What kind of group sounds best?</label>
        <select id="setting" aria-label="Choose a group setting">
                <option value="">Any group setting</option>
                <option value="team">Collaborative team</option>
                <option value="independent">Independent projects</option>
                <option value="social">Social and welcoming</option>
            </select>

        <label for="gender">Would you like to prioritize LGBTQ+ clubs? (optional)</label>
        <select id="gender" aria-label="Choose an LGBTQ+ community preference">
                <option value="">No preference</option>
                <option value="gay">Yes, show LGBTQ+ clubs first</option>
            </select>

        <label for="race">Would you like to prioritize a cultural community? (optional)</label>
        <select id="race" aria-label="Choose a cultural community">
                <option value="">No preference</option>
                <option value="black">Black</option>
                <option value="brazilian">Brazilian</option>
                <option value="asian">Asian</option>
                <option value="desi">Desi</option>
                <option value="hispanic-latino">Hispanic or Latino</option>
                <option value="jewish">Jewish</option>
            </select>

        <label for="grade">What grade are you in?</label>
        <select id="grade" aria-label="Choose your grade">
                <option value="">Any grade / prefer not to say</option>
                <option value="9">9th grade</option>
                <option value="10">10th grade</option>
                <option value="11">11th grade</option>
                <option value="12">12th grade</option>
            </select>

        <button id="match-btn" type="button">Find clubs</button>

        <section class="results">
            <h2>Here are the clubs that match your interests:</h2>
            <ul id="club-list"></ul>
        </section>
    </main>
    <!--I had to manually do these clubs... obviously it is not all the clubs, but It is still alot-->
    <!--The place holder is baskeball so there may be some errors-->
    <script>
        const clubs = [{
            name: "ASA (Animal Shelter)",
            interests: ["community", "nature"],
            activities: ["help", "learn"],
            setting: "social"
        }, {
            name: "Academic Quiz Bowl",
            interests: ["science"],
            activities: ["compete", "learn"],
            setting: "team"
        }, {
            name: "Active Minds",
            interests: ["science", "community"],
            activities: ["learn", "help"],
            setting: "social"
        }, {
            name: "Amnesty International",
            interests: ["community"],
            activities: ["help", "learn"],
            setting: "team"
        }, {
            name: "Art Club",
            interests: ["arts"],
            activities: ["create"],
            setting: "social"
        }, {
            name: "Badminton Club",
            interests: ["sports"],
            activities: ["compete"],
            setting: "team"
        }, {
            name: "Baking Club",
            interests: ["arts"],
            activities: ["create", "learn"],
            setting: "social"
        }, {
            name: "Basketball Pep Band",
            interests: ["arts", "sports"],
            activities: ["create", "compete"],
            setting: "team"
        }, {
            name: "Better2Gether RVA",
            interests: ["community"],
            activities: ["help"],
            setting: "team"
        }, {
            name: "Black Student Union",
            interests: ["community"],
            activities: ["learn", "help"],
            setting: "social",
            race: "black"
        }, {
            name: "Brazilian Student Union",
            interests: ["community", "arts"],
            activities: ["learn", "create"],
            setting: "social",
            race: "brazilian"
        }, {
            name: "Bread Club",
            interests: ["arts"],
            activities: ["create", "learn"],
            setting: "social"
        }, {
            name: "Cards for Kids",
            interests: ["community", "arts"],
            activities: ["help", "create"],
            setting: "team"
        }, {
            name: "Chinese Student Association",
            interests: ["community"],
            activities: ["learn", "create"],
            setting: "social",
            race: "asian"
        }, {
            name: "Circle Of Friends",
            interests: ["community"],
            activities: ["help", "learn"],
            setting: "social"
        }, {
            name: "Color Guard",
            interests: ["arts", "sports"],
            activities: ["create", "compete"],
            setting: "team"
        }, {
            name: "Cancer Awareness Club",
            interests: ["science", "community"],
            activities: ["learn", "help"],
            setting: "team"
        }, {
            name: "Chess Club",
            interests: ["science"],
            activities: ["build", "compete"],
            setting: "social"
        }, {
            name: "Computer Club",
            interests: ["technology"],
            activities: ["build", "learn"],
            setting: "team"
        }, {
            name: "Computer Science Honor Society",
            interests: ["technology", "science"],
            activities: ["build", "learn"],
            setting: "team"
        }, {
            name: "Connect Me",
            interests: ["community", "technology"],
            activities: ["help", "learn"],
            setting: "team"
        }, {
            name: "Creative Writing Club",
            interests: ["arts"],
            activities: ["create", "learn"],
            setting: "social"
        }, {
            name: "Debate",
            interests: ["business", "arts"],
            activities: ["compete", "learn"],
            setting: "team"
        }, {
            name: "DECA",
            interests: ["business"],
            activities: ["compete", "learn"],
            setting: "team"
        }, {
            name: "Desi Dance Club",
            interests: ["arts", "sports"],
            activities: ["create", "compete"],
            setting: "team",
            race: "desi"
        }, {
            name: "Desi Student Association",
            interests: ["community", "arts"],
            activities: ["learn", "create"],
            setting: "social",
            race: "desi"
        }, {
            name: "Drama Club",
            interests: ["arts"],
            activities: ["create", "compete"],
            setting: "team"
        }, {
            name: "Eco Bloom Project",
            interests: ["nature", "community"],
            activities: ["help", "build"],
            setting: "team"
        }, {
            name: "Endangered Species Club",
            interests: ["nature", "science"],
            activities: ["learn", "help"],
            setting: "team"
        }, {
            name: "Educators Rising",
            interests: ["community"],
            activities: ["learn", "help"],
            setting: "team"
        }, {
            name: "Environmental Club",
            interests: ["nature", "community"],
            activities: ["help", "learn"],
            setting: "team"
        }, {
            name: "Envirothon",
            interests: ["nature", "science"],
            activities: ["learn", "compete"],
            setting: "team"
        }, {
            name: "Equity Ambassadors",
            interests: ["community", "business"],
            activities: ["help", "learn"],
            setting: "team"
        }, {
            name: "Ethics Club",
            interests: ["community", "science"],
            activities: ["learn", "discuss"],
            setting: "social"
        }, {
            name: "FBLA (Future Business Leaders of America)",
            interests: ["business"],
            activities: ["compete", "learn"],
            setting: "team"
        }, {
            name: "FCA (Fellowship of Christian Athletes)",
            interests: ["sports", "community"],
            activities: ["compete", "help"],
            setting: "social"
        }, {
            name: "FCCLA",
            interests: ["business", "community"],
            activities: ["build", "learn"],
            setting: "team"
        }, {
            name: "Finance and Economics Club",
            interests: ["business"],
            activities: ["build", "learn"],
            setting: "team"
        }, {
            name: "FORENSICS (SPEECH TEAM)",
            interests: ["arts"],
            activities: ["create", "compete"],
            setting: "team"
        }, {
            name: "French Club",
            interests: ["community", "arts"],
            activities: ["learn", "create"],
            setting: "social"
        }, {
            name: "French Honor Society",
            interests: ["community"],
            activities: ["learn", "help"],
            setting: "team"
        }, {
            name: "Future Scientists of America",
            interests: ["science"],
            activities: ["learn", "build"],
            setting: "team"
        }, {
            name: "Gender Sexuality Alliance",
            interests: ["community"],
            activities: ["help", "learn"],
            setting: "social",
            gender: "gay"
        }, {
            name: "Geography Club",
            interests: ["nature", "science"],
            activities: ["learn"],
            setting: "social"
        }, {
            name: "The Giving Oven",
            interests: ["community", "arts"],
            activities: ["help", "create"],
            setting: "team"
        }, {
            name: "Growing Beyond Earth",
            interests: ["nature", "science"],
            activities: ["build", "learn"],
            setting: "team"
        }, {
            name: "Habitat for Humanity",
            interests: ["community"],
            activities: ["help", "build"],
            setting: "team"
        }, {
            name: "Heart Club",
            interests: ["community", "science"],
            activities: ["help", "learn"],
            setting: "team"
        }, {
            name: "Helpful Hearts",
            interests: ["community"],
            activities: ["help"],
            setting: "team"
        }, {
            name: "Hispanic Heritage Society",
            interests: ["community", "arts"],
            activities: ["learn", "create"],
            setting: "social",
            race: "hispanic-latino"
        }, {
            name: "Honor Council",
            interests: ["business", "community"],
            activities: ["help", "learn"],
            setting: "team"
        }, {
            name: "International/Trivia Club",
            interests: ["science", "community"],
            activities: ["learn", "compete"],
            setting: "social"
        }, {
            name: "Jewish Student Union (JSU)",
            interests: ["community"],
            activities: ["learn", "help"],
            setting: "social",
            race: "jewish"
        }, {
            name: "Key Club",
            interests: ["community"],
            activities: ["help"],
            setting: "team"
        }, {
            name: "Kindness Club",
            interests: ["community"],
            activities: ["help"],
            setting: "social"
        }, {
            name: "Knitting Club",
            interests: ["arts"],
            activities: ["create", "learn"],
            setting: "social"
        }, {
            name: "Latin Club",
            interests: ["community", "arts"],
            activities: ["learn"],
            setting: "social"
        }, {
            name: "Latin Honor Society",
            interests: ["community"],
            activities: ["learn", "help"],
            setting: "team"
        }, {
            name: "Literary Magazine Club",
            interests: ["arts"],
            activities: ["create", "learn"],
            setting: "team"
        }, {
            name: "Marching Band",
            interests: ["arts", "sports"],
            activities: ["create", "compete"],
            setting: "team"
        }, {
            name: "Math Competition Club",
            interests: ["science"],
            activities: ["build", "compete"],
            setting: "team"
        }, {
            name: "Media/Photography Club",
            interests: ["arts", "technology"],
            activities: ["create", "learn"],
            setting: "independent"
        }, {
            name: "Medical Club",
            interests: ["science"],
            activities: ["learn", "build"],
            setting: "team"
        }, {
            name: "Medical Impact Club",
            interests: ["science", "community"],
            activities: ["learn", "help"],
            setting: "team"
        }, {
            name: "MedTech Club",
            interests: ["technology", "science"],
            activities: ["build", "learn"],
            setting: "team"
        }, {
            name: "Mentor Program",
            interests: ["community"],
            activities: ["help", "learn"],
            setting: "social"
        }, {
            name: "Mock Trial",
            interests: ["business", "arts"],
            activities: ["compete", "learn"],
            setting: "team"
        }];

        const interestSelect = document.getElementById("interest");
        const activitySelect = document.getElementById("activity");
        const settingSelect = document.getElementById("setting");
        const genderSelect = document.getElementById("gender");
        const raceSelect = document.getElementById("race");
        const gradeSelect = document.getElementById("grade");
        const matchButton = document.getElementById("match-btn");
        const clubList = document.getElementById("club-list");

        const clubDetails = {
            "Black Student Union": {
                tags: ["Black community"]
            },
            "Brazilian Student Union": {
                tags: ["Brazilian community"]
            },
            "Chinese Student Association": {
                tags: ["Chinese community"]
            },
            "Desi Dance Club": {
                tags: ["Desi community"]
            },
            "Desi Student Association": {
                tags: ["Desi community"]
            },
            "Gender Sexuality Alliance": {
                tags: ["LGBTQ+ community"]
            },
            "Hispanic Heritage Society": {
                tags: ["Hispanic and Latino community"]
            },
            "Jewish Student Union (JSU)": {
                tags: ["Jewish community"]
            }
        };

        matchButton.addEventListener("click", () => {
                    clubList.replaceChildren();

                    const answers = [
                        interestSelect.value,
                        activitySelect.value,
                        settingSelect.value
                    ].filter(Boolean);

                    const hasPreference = Boolean(genderSelect.value || raceSelect.value);

                    if (answers.length === 0 && !hasPreference && !gradeSelect.value) {
                        const message = document.createElement("li");
                        message.className = "empty";
                        message.textContent =
                            "Please answer at least one question to see your matches.";
                        clubList.appendChild(message);
                        return;
                    }

                    const rankedClubs = clubs
                        .map((club) => {
                            const details = clubDetails[club.name] || {};
                            const answerScore = answers.reduce((total, answer) => {
                                const matches =
                                    (club.interests || []).includes(answer) ||
                                    (club.activities || []).includes(answer) ||
                                    club.setting === answer;
                                return total + Number(matches);
                            }, 0);

                            const communityMatch =
                                (genderSelect.value && club.gender === genderSelect.value) ||
                                (raceSelect.value && club.race === raceSelect.value);

                            return {
                                club,
                                details,
                                score: answerScore + Number(Boolean(communityMatch))
                            };
                        })
                        .filter(({
                            club,
                            score
                        }) => {
                            const gradeMatch = !gradeSelect.value ||
                                !club.grades ||
                                club.grades.includes(gradeSelect.value);

                            return (answers.length === 0 || score > 0) && gradeMatch;
                        })
                        .sort((a, b) =>
                            b.score - a.score || a.club.name.localeCompare(b.club.name)
                        );

                    if (rankedClubs.length === 0) {
                        const item = document.createElement("li");
                        item.className = "empty";
                        item.textContent = "No clubs match those answers yet.";
                        clubList.appendChild(item);
                        return;
                    }

                    rankedClubs.forEach(({
                                club,
                                score,
                                details
                            }) => {
                                const item = document.createElement("li");
                                item.className = "club-item";

                                const name = document.createElement("span");
                                name.className = "club-name";
                                name.textContent =
                                    `${club.name}${answers.length || hasPreference
                            ? ` — ${score} matching answer${score === 1 ? "" : "s"}`
                            : ""}`;
                    item.appendChild(name);

                    (details.tags || []).forEach((tagText) => {
                        const tag = document.createElement("span");
                        tag.className = "club-tag";
                        tag.textContent = tagText;
                        item.appendChild(tag);
                    });

                    clubList.appendChild(item);
                });
            });
    </script>
</body>

</html>
