[index.html](https://github.com/user-attachments/files/33616027/index.html)
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>MCM 100L Self-Test — Weeks 1-6</title>
<meta property="og:title" content="MCM 100L Self-Test — Weeks 1-6">
<meta property="og:description" content="Self-test portal covering all 8 Mass Communication courses, Weeks 1-6. Multiple choice, fill-in-the-blank, and short answer questions.">
<meta property="og:type" content="website">
<meta name="description" content="Self-test portal covering all 8 Mass Communication courses, Weeks 1-6. Multiple choice, fill-in-the-blank, and short answer questions.">
<style>
  :root {
    --navy: #13294B;
    --navy-light: #1E3A66;
    --gold: #A8825A;
    --gold-light: #C9A876;
    --cream: #F6F1E7;
    --paper: #FFFDF9;
    --text: #201C16;
    --muted: #6B6459;
    --good: #3E6B52;
    --good-bg: #E7F0EA;
    --bad: #9B3B32;
    --bad-bg: #F6E7E4;
    --border: #DCD3C2;
  }
  * { box-sizing: border-box; }
  html, body {
    margin: 0; padding: 0;
    background: var(--cream);
    color: var(--text);
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
    line-height: 1.5;
  }
  h1, h2, h3, .serif { font-family: Georgia, 'Times New Roman', serif; }
  .app { max-width: 760px; margin: 0 auto; padding: 32px 20px 80px; }

  /* Header */
  .masthead {
    border-bottom: 3px solid var(--navy);
    padding-bottom: 18px;
    margin-bottom: 32px;
  }
  .masthead .kicker {
    font-size: 13px;
    color: var(--gold);
    font-weight: 600;
    letter-spacing: 0.02em;
    margin-bottom: 6px;
  }
  .masthead h1 {
    font-size: 28px;
    font-weight: 700;
    color: var(--navy);
    margin: 0 0 4px;
  }
  .masthead p {
    margin: 0;
    color: var(--muted);
    font-size: 15px;
  }

  /* Home: course grid */
  .course-list { display: flex; flex-direction: column; gap: 10px; }
  .course-row {
    display: flex;
    align-items: center;
    gap: 16px;
    background: var(--paper);
    border: 1px solid var(--border);
    border-left: 4px solid var(--navy);
    padding: 16px 18px;
    cursor: pointer;
    transition: border-left-color 0.15s ease, transform 0.1s ease;
    text-align: left;
    width: 100%;
    font-family: inherit;
  }
  .course-row:hover { border-left-color: var(--gold); }
  .course-row:active { transform: scale(0.995); }
  .course-code {
    font-family: Georgia, 'Times New Roman', serif;
    font-weight: 600;
    font-size: 16px;
    color: var(--navy);
    min-width: 108px;
    flex-shrink: 0;
  }
  .course-meta { flex: 1; }
  .course-title { font-size: 15px; font-weight: 500; color: var(--text); }
  .course-topic { font-size: 13px; color: var(--muted); margin-top: 2px; }
  .course-arrow { color: var(--gold); font-size: 18px; }
  .course-progress {
    font-size: 12px;
    color: var(--good);
    font-weight: 600;
    background: var(--good-bg);
    padding: 3px 8px;
    border-radius: 3px;
    white-space: nowrap;
  }

  /* Test view */
  .back-link {
    background: none; border: none; cursor: pointer;
    color: var(--navy); font-size: 14px; font-weight: 600;
    padding: 0; margin-bottom: 20px; font-family: inherit;
    display: flex; align-items: center; gap: 6px;
  }
  .back-link:hover { color: var(--gold); }

  .section-header {
    margin: 36px 0 16px;
    display: flex;
    align-items: baseline;
    gap: 12px;
  }
  .section-header:first-of-type { margin-top: 0; }
  .section-header h2 {
    font-size: 18px;
    color: var(--navy);
    margin: 0;
  }
  .section-header .count {
    font-size: 13px;
    color: var(--muted);
  }
  .section-note {
    font-size: 13px;
    color: var(--muted);
    margin: -10px 0 18px;
  }

  .q-block {
    background: var(--paper);
    border: 1px solid var(--border);
    padding: 18px 20px;
    margin-bottom: 12px;
  }
  .q-text {
    font-size: 15px;
    font-weight: 500;
    margin-bottom: 12px;
  }
  .q-num { color: var(--gold); font-weight: 700; margin-right: 6px; }

  .opt {
    display: flex;
    align-items: center;
    gap: 10px;
    padding: 8px 10px;
    margin-bottom: 6px;
    border: 1px solid var(--border);
    cursor: pointer;
    font-size: 14px;
    background: var(--cream);
  }
  .opt:hover { border-color: var(--gold); }
  .opt input { accent-color: var(--navy); }
  .opt.selected { border-color: var(--navy); background: #EDE7D8; }

  .fib-input, .short-input {
    width: 100%;
    border: 1px solid var(--border);
    background: var(--cream);
    padding: 10px 12px;
    font-family: inherit;
    font-size: 14px;
    color: var(--text);
  }
  .fib-input:focus, .short-input:focus {
    outline: none;
    border-color: var(--navy);
  }
  .short-input { min-height: 70px; resize: vertical; }

  .submit-bar {
    margin-top: 32px;
    padding-top: 24px;
    border-top: 2px solid var(--navy);
    display: flex;
    justify-content: flex-end;
  }
  .btn {
    background: var(--navy);
    color: #fff;
    border: none;
    padding: 13px 28px;
    font-size: 15px;
    font-weight: 600;
    font-family: inherit;
    cursor: pointer;
  }
  .btn:hover { background: var(--navy-light); }
  .btn.secondary {
    background: transparent;
    color: var(--navy);
    border: 1.5px solid var(--navy);
  }
  .btn.secondary:hover { background: #EDE7D8; }

  /* Results view */
  .score-card {
    background: var(--navy);
    color: #fff;
    padding: 28px 26px;
    margin-bottom: 32px;
    text-align: center;
  }
  .score-card .big {
    font-family: Georgia, 'Times New Roman', serif;
    font-size: 44px;
    font-weight: 700;
    color: var(--gold-light);
  }
  .score-card .label {
    font-size: 14px;
    color: #D9D2C2;
    margin-top: 4px;
  }
  .score-card .sub {
    font-size: 13px;
    color: #B9B2A2;
    margin-top: 10px;
  }

  .review-block {
    background: var(--paper);
    border: 1px solid var(--border);
    padding: 16px 18px;
    margin-bottom: 10px;
  }
  .review-block.correct { border-left: 4px solid var(--good); }
  .review-block.incorrect { border-left: 4px solid var(--bad); }
  .review-q { font-size: 14.5px; font-weight: 500; margin-bottom: 8px; }
  .review-row { font-size: 13.5px; margin-top: 4px; }
  .review-row .tag {
    font-weight: 600;
    font-size: 11px;
    text-transform: uppercase;
    letter-spacing: 0.03em;
    margin-right: 6px;
  }
  .your-ans { color: var(--text); }
  .your-ans.wrong { color: var(--bad); }
  .correct-ans { color: var(--good); font-weight: 600; }
  .suggested-box {
    background: var(--good-bg);
    border: 1px solid var(--good);
    padding: 10px 12px;
    margin-top: 8px;
    font-size: 13.5px;
    color: #294536;
  }
  .suggested-box .tag { color: var(--good); }

  .unanswered { color: var(--muted); font-style: italic; }

  /* Week picker */
  .week-row {
    display: flex;
    align-items: center;
    gap: 16px;
    background: var(--paper);
    border: 1px solid var(--border);
    border-left: 4px solid var(--gold);
    padding: 16px 18px;
    cursor: pointer;
    width: 100%;
    font-family: inherit;
    text-align: left;
    margin-bottom: 10px;
  }
  .week-row:hover { border-left-color: var(--navy); }
  .week-label {
    font-family: 'Georgia', serif;
    font-weight: 600;
    font-size: 16px;
    color: var(--navy);
    min-width: 90px;
    flex-shrink: 0;
  }
  .week-topic { font-size: 14px; color: var(--text); flex: 1; }
  .week-arrow { color: var(--gold); font-size: 18px; }

  /* Stage progress track */
  .stage-track {
    display: flex;
    align-items: center;
    gap: 6px;
    margin-bottom: 20px;
  }
  .stage-step {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 13px;
    font-weight: 600;
    color: var(--muted);
  }
  .stage-step .dot {
    width: 22px; height: 22px;
    border-radius: 50%;
    border: 1.5px solid var(--border);
    display: flex; align-items: center; justify-content: center;
    font-size: 11px;
    background: var(--paper);
    color: var(--muted);
    flex-shrink: 0;
  }
  .stage-step.active .dot { border-color: var(--navy); background: var(--navy); color: #fff; }
  .stage-step.active { color: var(--navy); }
  .stage-step.done .dot { border-color: var(--good); background: var(--good); color: #fff; }
  .stage-step.done { color: var(--good); }
  .stage-line {
    flex: 1;
    height: 1.5px;
    background: var(--border);
    min-width: 16px;
  }

  /* Game HUD */
  .hud {
    display: flex;
    gap: 10px;
    margin-bottom: 22px;
    flex-wrap: wrap;
  }
  .hud-pill {
    display: flex;
    align-items: center;
    gap: 6px;
    background: var(--navy);
    color: #fff;
    padding: 8px 14px;
    font-size: 13px;
    font-weight: 600;
    border-radius: 2px;
  }
  .hud-pill.gold { background: var(--gold); color: #fff; }
  .hud-pill .n { font-family: 'Georgia', serif; font-size: 15px; }
  .device-note {
    font-size: 11.5px;
    color: var(--muted);
    background: var(--cream);
    border: 1px dashed var(--border);
    padding: 8px 12px;
    margin-bottom: 20px;
    line-height: 1.4;
  }
  .device-note button {
    background: none; border: none; color: var(--navy);
    font-weight: 600; cursor: pointer; font-size: 11.5px;
    text-decoration: underline; padding: 0; margin-left: 6px;
  }

  /* Badges on week rows */
  .badge-icon { font-size: 18px; margin-right: 4px; }
  .review-due {
    font-size: 11px;
    font-weight: 700;
    color: var(--bad);
    background: var(--bad-bg);
    padding: 3px 8px;
    border-radius: 3px;
    white-space: nowrap;
    margin-right: 6px;
  }

  /* Streak reveal on results */
  .streak-banner {
    background: var(--gold);
    color: #fff;
    text-align: center;
    padding: 14px;
    margin-bottom: 20px;
    font-weight: 700;
    font-size: 15px;
  }
  .xp-summary {
    display: flex;
    justify-content: space-around;
    background: var(--paper);
    border: 1px solid var(--border);
    padding: 14px;
    margin-bottom: 20px;
    text-align: center;
  }
  .xp-summary .stat-num {
    font-family: 'Georgia', serif;
    font-size: 22px;
    color: var(--navy);
    font-weight: 700;
  }
  .xp-summary .stat-label {
    font-size: 11px;
    color: var(--muted);
    text-transform: uppercase;
    letter-spacing: 0.03em;
  }
  .new-badge-toast {
    background: var(--good-bg);
    border: 1px solid var(--good);
    color: #294536;
    padding: 12px 14px;
    text-align: center;
    font-weight: 600;
    font-size: 14px;
    margin-bottom: 20px;
  }
  .q-block.streak-correct { border-left: 4px solid var(--good); }
  .q-block.streak-wrong { border-left: 4px solid var(--bad); }
  .streak-fire { font-size: 12px; color: var(--gold); font-weight: 700; margin-left: 8px; }

  .results-actions {
    display: flex;
    gap: 12px;
    flex-wrap: wrap;
    margin-top: 32px;
    padding-top: 24px;
    border-top: 2px solid var(--navy);
  }

  @media (max-width: 520px) {
    .course-row { flex-wrap: wrap; }
    .course-code { min-width: auto; }
  }
</style>
</head>
<body>
<div class="app" id="app"></div>

<script>
/* ---------------- DATA ---------------- */
const courses = [
{
  code: "GST 111",
  title: "Communication in English Language I",
  weeks: [
    {
      week: 1,
      topic: "The Hierarchical Nature of English Grammar",
      mcq: [

    {q:"What are the five major units of English grammar, from largest to smallest?", opts:["Sentence, clause, phrase, word, morpheme","Paragraph, sentence, clause, phrase, word","Clause, sentence, word, phrase, morpheme","Sentence, phrase, clause, morpheme, word"], a:0},
    {q:"Which unit represents a complete thought, and which is the smallest indivisible unit?", opts:["Clause is complete thought; word is smallest","Sentence is complete thought; morpheme is smallest","Phrase is complete thought; sentence is smallest","Sentence is complete thought; word is smallest"], a:1},
    {q:"How are nouns defined in this week's material?", opts:["Words that show action","Words that describe verbs","Names of things, animals, persons, ideas, and places","Words that connect clauses"], a:2},
    {q:"Besides type, what two features can nouns indicate?", opts:["Tense and mood","Number and gender","Case and voice","Person and aspect"], a:1},
    {q:"Which of these is NOT one of the noun types listed this week?", opts:["Collective noun","Abstract noun","Conjunctive noun","Countable noun"], a:2},
    {q:"How many key grammatical functions can a noun perform in a sentence, per this week's material?", opts:["Four","Five","Six","Eight"], a:2},
    {q:"Which of these is one of the six noun functions covered this week?", opts:["Modifier of the adjective","Complement of a preposition","Head of the clause","Anchor of the sentence"], a:1},
    {q:"What distinguishes a regular plural noun from an irregular one?", opts:["Regular plurals are always capitalized","Regular plurals follow standard rules (e.g. add -s); irregular ones don't","Irregular plurals only apply to proper nouns","There is no meaningful difference"], a:1},
    {q:"What does a \"gender-neutral noun\" mean, as referenced this week?", opts:["A noun used only for objects","A noun that doesn't specify masculine or feminine","A noun with no plural form","A noun that changes meaning by context only"], a:1},
    {q:"Why does the hierarchical structure of grammar (sentence → morpheme) matter?", opts:["It has no practical use beyond spelling","It shows how meaning builds from the smallest units up to complete thought","It only applies to written, not spoken, English","It replaces the need to learn vocabulary"], a:1},
    {q:"What is the title of this week's case study?", opts:["Analysing Social Media Posts for Sentiment Analysis","Reviewing Grammar in Academic Journals","The History of the English Language","Comparing British and American English"], a:0},
    {q:"What is the objective of this week's case study?", opts:["To teach spelling rules","To analyse social media posts to determine sentiment toward a brand or product using grammar principles","To translate posts into other languages","To count the number of nouns in a post"], a:1},
    {q:"Which methods are used in this week's case study?", opts:["Only manual reading, no technology","Collecting posts, preprocessing data, analysing at different grammar levels, applying sentiment analysis","Interviewing brand executives only","Surveying only offline customers"], a:1},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Identification and differentiation of the five major units of grammar","Improved writing and speaking abilities","Ability to identify and categorise nouns","Financial forecasting"], a:3},
    {q:"Who are the authors of \"A Comprehensive Grammar of the English Language,\" a key reference this week?", opts:["Todd, J.","Quirk, Greenbaum, Leech, & Svartvik","Baran & Davis","McQuail, D."], a:1}
      ],
      fib: [

    {q:"The five major units of English grammar, from largest to smallest, are sentence, clause, phrase, word, and __________.", a:"morpheme"},
    {q:"A __________ represents the highest level in the grammatical hierarchy, representing a complete thought.", a:"sentence"},
    {q:"Nouns are the names of things, animals, __________, ideas, and places.", a:"persons"},
    {q:"Nouns can indicate __________ (singular or plural) and gender (masculine, feminine, or neuter).", a:"number"},
    {q:"A __________ noun refers to a specific, named entity, while a __________ noun refers to a general class of entity.", a:"proper; common"},
    {q:"Plural nouns can be either regular or __________.", a:"irregular"},
    {q:"A noun that does not specify masculine or feminine is described as __________.", a:"gender-neutral"},
    {q:"There are __________ key functions of nouns in English grammar covered this week.", a:"six"},
    {q:"One of the six noun functions is \"complement of a __________.\"", a:"preposition"},
    {q:"Studying the hierarchical nature of grammar improves __________ and speaking abilities.", a:"writing"},
    {q:"This week's case study title is \"Analysing __________ Posts for Sentiment Analysis.\"", a:"social media"},
    {q:"The case study's objective is to analyse social media posts to determine __________ expressed by users toward a brand or product.", a:"sentiment"},
    {q:"The case study uses machine learning or __________ for sentiment classification.", a:"NLP"},
    {q:"One skill gained this week is the ability to identify and __________ nouns.", a:"categorise"},
    {q:"Quirk, Greenbaum, Leech, and Svartvik wrote \"A Comprehensive __________ of the English Language.\"", a:"grammar"}
      ],
      short: [

    {q:"What are the five major units of English grammar, listed from largest to smallest?", a:"Sentence, clause, phrase, word, and morpheme."},
    {q:"Which grammatical unit represents a complete thought, and which is the smallest indivisible unit?", a:"Sentence is the complete thought; morpheme is the smallest unit."},
    {q:"Give the definition of a noun as covered this week.", a:"A noun names things, animals, persons, ideas, and places."},
    {q:"What two features can nouns indicate regarding \"nature\" (besides type)?", a:"Number (singular/plural) and gender (masculine/feminine/neuter)."},
    {q:"Name three of the seven noun types covered this week.", a:"Any 3 of: proper, common, collective, abstract, concrete, countable, non-countable."},
    {q:"List the six key grammatical functions a noun can perform in a sentence.", a:"Subject of the verb, object of the verb, complement of the verb, complement of a preposition, complement of the object, appositive element."},
    {q:"Give an example of a function a noun can serve involving a preposition.", a:"Complement of a preposition."},
    {q:"What's the difference between a regular and an irregular plural noun?", a:"Regular plurals follow standard rules (e.g. add -s); irregular plurals don't follow a standard pattern."},
    {q:"What does \"gender-neutral noun\" mean, as referenced this week?", a:"A noun that doesn't specify masculine or feminine."},
    {q:"Why does understanding the hierarchy (sentence → clause → phrase → word → morpheme) matter for language analysis?", a:"It shows how meaning is built up from the smallest units into complete thoughts, aiding grammatical analysis."},
    {q:"What is the title and objective of this week's case study?", a:"\"Analysing Social Media Posts for Sentiment Analysis\" — to determine the sentiment expressed by users toward a brand or product using grammar principles."},
    {q:"Name two methods used in the case study on analysing social media posts.", a:"Any 2 of: collecting social media posts, preprocessing data, analysing at different grammar levels, applying sentiment analysis."},
    {q:"Name three skills/competencies gained this week beyond noun identification.", a:"Any 3 of: identification and differentiation of the five major units of grammar, understanding of hierarchical order, analysis and deconstruction of words/phrases, improved writing and speaking abilities, critical thinking skills."},
    {q:"What does the personal reflection this week focus on regarding nouns?", a:"How exploring the meaning and nature of nouns expands understanding of how they name entities and their categories within sentences."},
    {q:"Name the two key references cited this week.", a:"Todd, J. (2010) Communication in English: Course Handbook; Quirk, Greenbaum, Leech, & Svartvik (1985) A Comprehensive Grammar of the English Language."}
      ]
    },
    {
      week: 2,
      topic: "The English Articles, Quantifiers, Pre-determiners, and Demonstratives",
      mcq: [
    {q:"What do English articles precede, to indicate familiarity, quantity, and specificity?", opts:["Verbs only","Nouns or noun phrases","Adjectives only","Prepositions"], a:1},
    {q:"How many types of articles are there, and what are they called?", opts:["Three: definite, indefinite, zero","Two: definite and indefinite","Four: a, an, the, some","One: the definite article"], a:1},
    {q:"Definite articles are used for ___ nouns, while indefinite articles are used for ___ nouns.", opts:["plural; singular","specific; nonspecific","countable; uncountable","formal; informal"], a:1},
    {q:"What determines the choice between \"a\" and \"an\"?", opts:["The length of the word","The initial sound of the following word","Whether the noun is plural","The speaker's accent"], a:1},
    {q:"Besides specificity, what do articles help distinguish, per this week's material?", opts:["Verb tense","Countable and non-countable nouns","Active and passive voice","Direct and indirect speech"], a:1},
    {q:"What do articles indicate regarding mention, per this week's material?", opts:["Only plural forms","First vs. subsequent mention, and general vs. specific reference","Only past tense","Only formal register"], a:1},
    {q:"Which of these is an example of a quantifier mentioned this week?", opts:["Some, many, few","Quickly, slowly","Red, blue","Walk, run"], a:0},
    {q:"Where can quantifiers occur, per this week's material?", opts:["Only at the end of a sentence","Before nouns, adjective+noun, or adverb+adjective+noun","Only before verbs","Only in questions"], a:1},
    {q:"What does the choice of quantifier depend on?", opts:["The speaker's mood","The type of noun (singular, plural, or uncountable)","The length of the sentence","The time of day"], a:1},
    {q:"What are pre-determiners, and what is one example type mentioned this week?", opts:["Verbs that precede adjectives; e.g. run, jump","Words that modify plural or singular count nouns; e.g. multipliers like double, twice","Punctuation marks; e.g. commas","Suffixes; e.g. -ing, -ed"], a:1},
    {q:"What do intensifiers do, per this week's material?", opts:["Replace nouns entirely","Strengthen adjectives or nouns","Indicate past tense","Form questions"], a:1},
    {q:"Which of these is an example of an intensifier mentioned this week?", opts:["Rather, such","The, a, an","This, that","And, but"], a:0},
    {q:"What do demonstratives describe, per this week's material?", opts:["The tense of a verb","The position of objects from the speaker's viewpoint","The gender of a noun","The subject of a sentence"], a:1},
    {q:"Which four words are given as demonstratives this week?", opts:["This, that, these, those","Here, there, where, when","Some, many, few, several","My, your, his, her"], a:0},
    {q:"Who wrote \"The Cambridge Grammar of the English Language,\" this week's key reference?", opts:["Todd, J.","Huddleston, R., & Pullum, G.K.","Quirk, R.","Svartvik, J."], a:1}
      ],
      fib: [
    {q:"English articles are __________ that precede nouns or noun phrases to indicate familiarity, quantity, and specificity.", a:"determiners"},
    {q:"The two types of articles are definite and __________.", a:"indefinite"},
    {q:"The definite article is \"__________,\" used for specific nouns.", a:"the"},
    {q:"The choice between \"a\" and \"an\" depends on the initial __________ of the following word.", a:"sound"},
    {q:"Articles are important for distinguishing between countable and __________ nouns.", a:"non-countable"},
    {q:"Quantifiers such as some, many, and few provide information about __________.", a:"quantity"},
    {q:"The choice of quantifiers depends on the type of nouns being referred to: singular, plural, or __________.", a:"uncountable"},
    {q:"Pre-determiners, including multipliers and __________ expressions, modify plural or singular count nouns.", a:"fractional"},
    {q:"An example of a multiplier pre-determiner is \"double\" or \"__________.\"", a:"twice"},
    {q:"An example of a fractional expression pre-determiner is \"one-third\" or \"__________.\"", a:"half"},
    {q:"Intensifiers like \"rather\" and \"such\" strengthen __________ or nouns.", a:"adjectives"},
    {q:"Demonstratives describe the position of objects from the speaker's __________.", a:"viewpoint"},
    {q:"The four demonstratives covered this week are this, that, these, and __________.", a:"those"},
    {q:"This week's case study is titled \"Effective Use of __________ in English Writing.\"", a:"Articles"},
    {q:"__________, R., & Pullum, G.K. (2002) wrote \"The Cambridge Grammar of the English Language,\" this week's key reference.", a:"Huddleston"}
      ],
      short: [
    {q:"What do English articles precede, and what do they indicate?", a:"Nouns or noun phrases, to indicate familiarity, quantity, and specificity."},
    {q:"Name the two types of articles covered this week.", a:"Definite (the) and indefinite (a, an)."},
    {q:"What is the difference between definite and indefinite articles?", a:"Definite articles are used for specific nouns; indefinite articles are used for nonspecific nouns."},
    {q:"What determines whether \"a\" or \"an\" is used?", a:"The initial sound of the following word."},
    {q:"Besides specificity, what else do articles help distinguish?", a:"Countable and non-countable nouns, and first vs. subsequent mention."},
    {q:"Give three examples of quantifiers mentioned this week.", a:"Any 3 of: some, many, few."},
    {q:"What does the choice of quantifier depend on?", a:"The type of noun being referred to (singular, plural, or uncountable)."},
    {q:"What are pre-determiners, and name the two types mentioned?", a:"Words that modify plural or singular count nouns — multipliers (e.g. double, twice) and fractional expressions (e.g. one-third, half)."},
    {q:"What do intensifiers do, and give an example?", a:"Strengthen adjectives or nouns; examples include \"rather\" and \"such.\""},
    {q:"What do demonstratives describe, and name the four demonstratives.", a:"The position of objects from the speaker's viewpoint; this, that, these, those."},
    {q:"What is the title and objective of this week's case study?", a:"\"Effective Use of Articles in English Writing\" — to examine how knowledge and application of articles enhance written English."},
    {q:"Name two methods used in this week's case study.", a:"Any 2 of: assessing learners' understanding, conducting a training session, post-assessment, analysing written texts, group discussion."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: understanding the role of articles, proper article usage, noun modification, differentiating countable/non-countable nouns, quantifier usage, pre-determiner understanding, demonstrative comprehension."},
    {q:"What question does this week's 'Questions to ponder' ask about learner challenges?", a:"What common challenges or mistakes English language learners face when using articles, and how these can be addressed."},
    {q:"Name this week's key reference and its authors.", a:"The Cambridge Grammar of the English Language, by Huddleston, R., & Pullum, G.K. (2002)."}
      ]
    },
    {
      week: 3,
      topic: "The Nature of Pronoun, Types of Pronoun",
      mcq: [
    {q:"What do pronouns do, per this week's material?", opts:["Replace or are used in place of nouns","Replace verbs","Replace adjectives only","Form questions only"], a:0},
    {q:"How many types of pronouns are covered this week?", opts:["Five","Seven","Nine","Twelve"], a:2},
    {q:"What do personal pronouns refer to?", opts:["Nonspecific persons or things","Specific individuals, and express numbers","Only objects, never people","Only plural groups"], a:1},
    {q:"What do possessive pronouns indicate?", opts:["Ownership, replacing possessive forms of nouns","Location","Time","Questions"], a:0},
    {q:"What do relative pronouns do?", opts:["Form questions","Introduce dependent clauses and refer to people and things","Indicate ownership","Emphasise another pronoun"], a:1},
    {q:"What do demonstrative pronouns do?", opts:["Point to the nouns they replace","Form questions","Reflect back to the subject","Indicate relationships between nouns"], a:0},
    {q:"What do interrogative pronouns do?", opts:["Form questions","Indicate ownership","Emphasise a noun","Refer to nonspecific things"], a:0},
    {q:"What do intensive pronouns do, per this week's material?", opts:["Change the sentence's meaning when removed","Emphasise a noun or pronoun without changing the sentence's meaning when removed","Form questions","Indicate possession"], a:1},
    {q:"What do reflexive pronouns do?", opts:["Reflect back to the subject","Form questions","Point to objects","Indicate quantity"], a:0},
    {q:"What do indefinite pronouns refer to?", opts:["Specific named individuals","Nonspecific persons or things","Only plural objects","Only questions"], a:1},
    {q:"What do reciprocal pronouns indicate?", opts:["The relationship between two or more nouns","Ownership of an object","The tense of a sentence","A question being asked"], a:0},
    {q:"In the possessive pronoun table shown this week, what is the plural form of \"mine\"?", opts:["Ours","Yours","Theirs","Hers"], a:0},
    {q:"What is important for correct pronoun usage, besides case, per this week's material?", opts:["Agreement between pronouns and their antecedents, and clear reference","Using only personal pronouns","Avoiding all plural pronouns","Using pronouns only in questions"], a:0},
    {q:"What is the title of this week's case study?", opts:["Effective Use of Pronouns in Business Communication","The History of Pronouns","Pronouns in Fiction Writing","Grammar Rules for Beginners"], a:0},
    {q:"What is the objective of this week's case study?", opts:["To eliminate pronoun use in writing","To demonstrate how proper pronoun usage improves business communication by reducing redundancy and enhancing readability","To teach only possessive pronouns","To analyse pronouns in poetry"], a:1}
      ],
      fib: [
    {q:"Pronouns replace or are used in place of __________.", a:"nouns"},
    {q:"There are __________ types of pronouns covered this week.", a:"nine"},
    {q:"Personal pronouns refer to specific individuals and express __________.", a:"numbers"},
    {q:"Possessive pronouns indicate __________ and replace possessive forms of nouns.", a:"ownership"},
    {q:"Relative pronouns introduce __________ clauses and refer to people and things.", a:"dependent"},
    {q:"Demonstrative pronouns point to the __________ they replace.", a:"nouns"},
    {q:"Interrogative pronouns form __________.", a:"questions"},
    {q:"Intensive pronouns emphasise a noun or pronoun without changing the sentence's __________ when removed.", a:"meaning"},
    {q:"Reflexive pronouns reflect back to the __________.", a:"subject"},
    {q:"Indefinite pronouns refer to __________ persons or things.", a:"nonspecific"},
    {q:"Reciprocal pronouns indicate the __________ between two or more nouns.", a:"relationship"},
    {q:"Correct pronoun usage requires agreement between pronouns and their __________.", a:"antecedents"},
    {q:"This week's case study is titled \"Effective Use of Pronouns in __________ Communication.\"", a:"Business"},
    {q:"The case study's objective is to show how proper pronoun usage can reduce __________ in business communication.", a:"redundancy"},
    {q:"In the possessive pronoun table, the plural form of \"his/hers\" is \"__________.\"", a:"their"}
      ],
      short: [
    {q:"What do pronouns do, per this week's material?", a:"They replace or are used in place of nouns."},
    {q:"How many types of pronouns are covered this week?", a:"Nine."},
    {q:"What do personal pronouns refer to?", a:"Specific individuals, and they express numbers."},
    {q:"What do possessive pronouns indicate?", a:"Ownership, replacing possessive forms of nouns."},
    {q:"What do relative pronouns do?", a:"Introduce dependent clauses and refer to people and things."},
    {q:"What do demonstrative and interrogative pronouns do, respectively?", a:"Demonstrative pronouns point to the nouns they replace; interrogative pronouns form questions."},
    {q:"What do intensive and reflexive pronouns do, respectively?", a:"Intensive pronouns emphasise a noun/pronoun without changing meaning when removed; reflexive pronouns reflect back to the subject."},
    {q:"What do indefinite and reciprocal pronouns do, respectively?", a:"Indefinite pronouns refer to nonspecific persons or things; reciprocal pronouns indicate the relationship between two or more nouns."},
    {q:"Besides correct case usage, what two things matter for correct pronoun use?", a:"Agreement between pronouns and their antecedents, and clear reference."},
    {q:"Give the plural possessive pronoun forms for \"mine,\" \"yours,\" and \"his/hers.\"", a:"Ours, yours, their(s)."},
    {q:"What is the title and objective of this week's case study?", a:"\"Effective Use of Pronouns in Business Communication\" — to show how proper pronoun usage improves business communication by reducing redundancy and enhancing readability."},
    {q:"Name two methods used in this week's case study.", a:"Any 2 of: collecting business communication samples, analysing pronoun usage, evaluating clarity/professionalism, conducting training, providing feedback."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: knowledge of different types of pronouns, understanding of pronoun usage, ability to ensure pronoun-antecedent agreement, enhanced communication skills, improved grammar proficiency."},
    {q:"What two questions does this week's 'Question to ponder' raise?", a:"How understanding pronoun types contributes to effective communication, and why pronoun-antecedent agreement matters in writing and speaking."},
    {q:"Name this week's key references.", a:"Todd, J. (2010) Communication in English: Course Handbook; Quirk, Greenbaum, Leech, & Svartvik (1985) A Comprehensive Grammar of the English Language."}
      ]
    },
    {
      week: 4,
      topic: "The Nature of Verb/Auxiliary Verb, Tense, and Aspect",
      mcq: [
        {q:"What is the topic of Week 4 in this course?", opts:["The Nature of Adjective","The Nature of Adverb","The Nature of Noun","The Nature of Verb/Auxiliary Verb, Tense, and Aspect"], a:3},
        {q:"According to Week 4, what do verbs denote?", opts:["Actions or states","Feelings or places","Qualities or sounds","Actions or objects"], a:0},
        {q:"Which part of a sentence do verbs form, according to Week 4?", opts:["The predicate","The subject","The adjective phrase","The object only"], a:0},
        {q:"According to Week 4, which statement is true about verbs and nouns?", opts:["Neither verbs nor nouns can form a sentence alone","Both verbs and nouns can never stand alone","Verbs can stand alone as sentences, while nouns require a verb to form a complete sentence","Nouns can stand alone as sentences, while verbs require a noun"], a:2},
        {q:"What is the role of auxiliary verbs, according to Week 4?", opts:["They assist main verbs in conveying their meanings","They describe nouns","They replace main verbs entirely","They only appear in questions"], a:0},
        {q:"Into how many groups are auxiliary verbs categorised in Week 4?", opts:["Five","Three","Two","Four"], a:1},
        {q:"Which of the following is NOT one of the three groups of auxiliary verbs mentioned in Week 4?", opts:["Descriptive auxiliary","\"Be\" auxiliary","\"Do\" auxiliary","Modal auxiliary"], a:0},
        {q:"What does tense refer to, according to Week 4?", opts:["The mood of the speaker","How an action is performed","The time of an action or condition","The number of verbs in a sentence"], a:2},
        {q:"Which three tenses are identified in Week 4?", opts:["Present, perfect, and continuous","Active, passive, and modal","Present, past, and future","Simple, complex, and compound"], a:2},
        {q:"What does aspect describe, according to Week 4?", opts:["How time is conveyed in a sentence","The number of auxiliary verbs used","The gender of a noun","Subject-verb agreement"], a:0},
        {q:"Which four aspects are listed in Week 4?", opts:["Simple, progressive, perfect, and perfect-continuous","Simple, compound, complex, and perfect","Active, passive, modal, and simple","Present, past, future, and conditional"], a:0},
        {q:"What is the title of the Week 4 case study?", opts:["Enhancing Grammar Skills through Tense Mastery","Enhancing Business Communication Skills through Effective Verb and Auxiliary Verb Usage","Improving Descriptive Writing through Adjective Usage","Enhancing Public Speaking Skills through Effective Adverb Usage"], a:1},
        {q:"What is the objective of the Week 4 case study?", opts:["To assess participants' spelling accuracy","To equip participants with knowledge and skills to use verbs and auxiliary verbs effectively in business communication","To teach participants how to write business reports","To train participants in public speaking"], a:1},
        {q:"According to the Week 4 case study methods, what does the training cover?", opts:["Noun and pronoun usage","Public speaking techniques","Verb nature, forms, tenses, and aspects","Only verb tenses"], a:2},
        {q:"Who are given as the authors of 'A Comprehensive Grammar of the English Language' (1985), a key reference for Week 4?", opts:["Todd, J.","Crystal, David","Eyisi, Joy","Quirk, Greenbaum, Leech, and Svartvik"], a:3}
      ],
      fib: [
        {q:"Verbs denote actions or __________.", a:"states"},
        {q:"Verbs form the __________ of a sentence.", a:"predicate"},
        {q:"__________ verbs can stand alone as sentences, while nouns require a verb to form a complete sentence.", a:"Verbs"},
        {q:"__________ verbs assist main verbs in conveying their meanings.", a:"Auxiliary"},
        {q:"Auxiliary verbs are categorised into three groups: \"be\" auxiliary, \"do\" auxiliary, and __________ auxiliary.", a:"modal"},
        {q:"__________ refers to the time of an action or condition, including present, past, and future.", a:"Tense"},
        {q:"__________ describes how time is conveyed and includes the simple, progressive, perfect, and perfect-continuous aspects.", a:"Aspect"},
        {q:"The three tenses identified in Week 4 are present, past, and __________.", a:"future"},
        {q:"The four aspects identified in Week 4 are the simple, progressive, perfect, and __________ aspects.", a:"perfect-continuous"},
        {q:"The Week 4 case study is titled \"Enhancing Business Communication Skills through Effective __________ Usage.\"", a:"Verb and Auxiliary Verb"},
        {q:"The Week 4 case study methods include training that covers verb nature, forms, tenses, and __________.", a:"aspects"},
        {q:"Among the skills acquired in Week 4 are verb identification, tense awareness, aspect comprehension, auxiliary verb usage, sentence construction, and __________.", a:"communication clarity"},
        {q:"One key reference for Week 4 is Todd, J. (2010), titled Communication in English: __________.", a:"Course Handbook"},
        {q:"A Comprehensive Grammar of the English Language (1985) was written by __________, Greenbaum, Leech, and Svartvik.", a:"Quirk"},
        {q:"According to the Week 4 personal reflection, applying verb and auxiliary verb skills improves language __________ in daily conversations and writing.", a:"proficiency"}
      ],
      short: [
        {q:"What is the topic of Week 4?", a:"The Nature of Verb/Auxiliary Verb, Tense, and Aspect"},
        {q:"According to Week 4, what do verbs denote?", a:"Actions or states"},
        {q:"What part of a sentence do verbs form, according to Week 4?", a:"The predicate of a sentence"},
        {q:"How do verbs differ from nouns in their ability to form a sentence, according to Week 4?", a:"Verbs can stand alone as sentences, while nouns require a verb to form a complete sentence"},
        {q:"What is the function of auxiliary verbs, according to Week 4?", a:"They assist main verbs in conveying their meanings"},
        {q:"List the three groups into which auxiliary verbs are categorised in Week 4.", a:"\"Be\" auxiliary, \"do\" auxiliary, and modal auxiliary"},
        {q:"Define tense as presented in Week 4.", a:"Tense refers to the time of an action or condition, including present, past, and future"},
        {q:"Define aspect as presented in Week 4.", a:"Aspect describes how time is conveyed in a sentence"},
        {q:"Name the four aspects covered in Week 4.", a:"Simple, progressive, perfect, and perfect-continuous aspects"},
        {q:"What is the title of the Week 4 case study?", a:"Enhancing Business Communication Skills through Effective Verb and Auxiliary Verb Usage"},
        {q:"What is the objective of the Week 4 case study?", a:"To equip participants with the knowledge and skills to use verbs and auxiliary verbs effectively in their business communication"},
        {q:"What does the Week 4 case study's training method cover?", a:"Verb nature, forms, tenses, and aspects, through interactive activities, feedback, and assignments"},
        {q:"State one of the questions to ponder posed in Week 4.", a:"How does a clear understanding of verb tenses and aspects enhance communication effectiveness in various contexts? (or: What are some common challenges or misconceptions that learners may face when using verbs and auxiliary verbs, and how can these be overcome to improve proficiency?)"},
        {q:"List three skills or competencies acquired in Week 4.", a:"Any three of: verb identification, tense awareness, aspect comprehension, auxiliary verb usage, sentence construction, communication clarity"},
        {q:"According to the Week 4 personal reflection, how does understanding tenses and aspects affect communication?", a:"It enables effective use of tenses and aspects, enhancing precision and clarity in communication"}
      ]
    },
    {
      week: 5,
      topic: "The Nature of Adjective",
      mcq: [
        {q:"What is the topic of Week 5?", opts:["The Nature of Adjective","The Nature of Adverb","The Nature of Noun","The Nature of Verb/Auxiliary Verb, Tense, and Aspect"], a:0},
        {q:"According to Week 5, what do adjectives do?", opts:["Replace nouns in a sentence","Modify only verbs","Describe or modify a person or thing (noun) in a statement","Connect two independent clauses"], a:2},
        {q:"According to Week 5, what effect do adjectives have on sentences?", opts:["They shorten sentences for clarity","They add vividness and depth, transforming ordinary nouns into captivating descriptions","They replace the need for nouns","They remove ambiguity from verbs"], a:1},
        {q:"How does Week 5 distinguish adjectives from adverbs?", opts:["Both adjectives and adverbs modify only nouns","Adjectives modify verbs while adverbs modify nouns","Adverbs modify verbs, adjectives, and other adverbs, while adjectives modify only nouns","Adverbs and adjectives are presented as the same word class"], a:2},
        {q:"According to Week 5, where do adjectives appear when describing a noun before the verb \"to be\"?", opts:["Before the verb \"to be\"","At the end of the sentence only","Immediately after the verb \"to be\"","Immediately before the subject"], a:2},
        {q:"Week 5 states that adjectives also appear immediately after verbs that depict the senses. Which of these is listed as one such sense verb?", opts:["Write","Smell","Think","Run"], a:1},
        {q:"How does Week 5 define an adjective clause?", opts:["A clause that replaces the subject of a sentence","A phrase that only modifies verbs","A dependent clause that begins with relative pronouns and provides more information about a noun or noun phrase","An independent clause that stands alone as a sentence"], a:2},
        {q:"Which skill, listed among those acquired in Week 5, involves recognising and utilising clauses that provide additional information about a noun?", opts:["Auxiliary verb usage","Tense awareness","Sentence punctuation","Recognising and utilising adjective clauses"], a:3},
        {q:"In the Week 5 case study methods, what does the process involve selecting?", opts:["A range of products, forming control and test groups","A group of student essays","A sample of public speakers","A set of grammar textbooks"], a:0},
        {q:"In the Week 5 case study methods, what is optimised with adjectives for the test group?", opts:["Public speeches","Business emails","Customer complaint forms","Product descriptions"], a:3},
        {q:"How does the Week 5 case study collect data, according to its methods?", opts:["Through audience applause","Through classroom observation only","Through exam scores","Through website analytics and customer feedback"], a:3},
        {q:"What is the final step of the Week 5 case study methods?", opts:["Repeating the experiment indefinitely","Publishing the results in an academic journal","Summarising the findings to provide actionable insights for businesses","Awarding certificates to participants"], a:2},
        {q:"Which question to ponder is posed in Week 5?", opts:["How can appropriate adverb usage change the impact of a spoken message?","How do adjectives contribute to effective communication and descriptive writing?","How does understanding verb tenses enhance communication?","What is the role of nouns in a sentence?"], a:1},
        {q:"Which of the following is listed as a skill/competency acquired in Week 5?", opts:["Differentiating between adjectives and adverbs","Identifying auxiliary verbs","Analysing public speakers","Recognising verb tense"], a:0},
        {q:"Which reference, cited for Week 5, is titled 'A Grammar of English: the Student's Companion'?", opts:["Todd, J. (2010)","Eyisi, Joy (2011)","Crystal, David (2010)","Quirk, R. et al. (1985)"], a:1}
      ],
      fib: [
        {q:"__________ are words that describe or modify a person or thing in a statement.", a:"Adjectives"},
        {q:"Adjectives add vividness and depth to sentences, transforming ordinary nouns into __________ descriptions.", a:"captivating"},
        {q:"Adverbs modify verbs, adjectives, and other adverbs, while adjectives modify only __________.", a:"nouns"},
        {q:"Adjectives appear immediately after the verb \"__________\" when describing nouns before the verb.", a:"to be"},
        {q:"Adjectives also appear immediately after verbs that depict the senses, such as taste, feel, smell, appear, look, and __________.", a:"seem"},
        {q:"An adjective __________ is a dependent clause that begins with relative pronouns and provides more information about a noun or noun phrase.", a:"clause"},
        {q:"Adjective __________ provide additional information about nouns and pronouns.", a:"phrases"},
        {q:"The Week 5 case study methods involve forming __________ and test groups.", a:"control"},
        {q:"In the Week 5 case study, product descriptions are optimised with __________ for the test group.", a:"adjectives"},
        {q:"The Week 5 case study collects data through website analytics and __________.", a:"customer feedback"},
        {q:"The final step of the Week 5 case study methods is summarising the findings to provide __________ for businesses.", a:"actionable insights"},
        {q:"Among the skills acquired in Week 5 is understanding the __________ of adjectives in relation to verbs.", a:"placement"},
        {q:"One of the Week 5 questions to ponder asks about common mistakes or challenges people face when using __________.", a:"adjectives"},
        {q:"According to the Week 5 personal reflection, proper use of adjectives aids effective __________.", a:"writing"},
        {q:"The reference by Eyisi, Joy (2011) is titled A Grammar of English: the Student's __________.", a:"Companion"}
      ],
      short: [
        {q:"What is the topic of Week 5?", a:"The Nature of Adjective"},
        {q:"According to Week 5, what do adjectives do to a sentence?", a:"They describe or modify a person or thing (noun), adding vividness and depth, and transforming ordinary nouns into captivating descriptions"},
        {q:"How are adjectives distinct from adverbs, according to Week 5?", a:"Adverbs modify verbs, adjectives, and other adverbs, while adjectives modify only nouns"},
        {q:"Where do adjectives appear in relation to the verb 'to be', according to Week 5?", a:"Immediately after the verb 'to be' when describing nouns before the verb"},
        {q:"Name the sense verbs after which adjectives can appear, according to Week 5.", a:"Taste, feel, smell, appear, look, and seem"},
        {q:"What is an adjective clause, according to Week 5?", a:"A dependent clause that begins with relative pronouns and provides more information about a noun or noun phrase"},
        {q:"What is the purpose of adjective phrases, according to Week 5?", a:"To describe nouns and pronouns accurately and provide additional information about nouns"},
        {q:"What does the Week 5 case study method involve regarding products?", a:"Selecting a range of products and forming control and test groups"},
        {q:"How are product descriptions treated for the test group in the Week 5 case study?", a:"They are optimised with adjectives"},
        {q:"How is data collected in the Week 5 case study?", a:"Through website analytics and customer feedback"},
        {q:"What is the goal of analysing the data in the Week 5 case study?", a:"To identify patterns and differences between the control and test groups"},
        {q:"State one of the Week 5 questions to ponder.", a:"How do adjectives contribute to effective communication and descriptive writing? (or: What are some common mistakes or challenges that people face when using adjectives, and how can they be overcome?)"},
        {q:"List three skills or competencies acquired in Week 5.", a:"Any three of: differentiating between adjectives and adverbs, modifying nouns effectively with appropriate adjectives, using adjectives correctly in writing and communication, understanding the placement of adjectives in relation to verbs, recognising and utilising adjective clauses, employing adjective phrases"},
        {q:"According to the Week 5 personal reflection, what does proper use of adjectives aid?", a:"Effective writing"},
        {q:"Name the two key references cited for Week 5.", a:"Todd, J. (2010), Communication in English: Course Handbook; and Eyisi, Joy (2011), A Grammar of English: the Student's Companion"}
      ]
    },
    {
      week: 6,
      topic: "The Nature of Adverb",
      mcq: [
        {q:"What is the topic of Week 6?", opts:["The Nature of Adjective","The Nature of Adverb","The Nature of Pronoun","The Nature of Verb/Auxiliary Verb, Tense, and Aspect"], a:1},
        {q:"According to Week 6, what can adverbs modify?", opts:["Only nouns","Verbs, adjectives, other adverbs, or entire sentences","Only pronouns","Only prepositions"], a:1},
        {q:"Which questions do adverbs answer, according to Week 6?", opts:["How, when, where, and why an action occurs","Who and what","Why only","Which and whose"], a:0},
        {q:"Which example of comparative and superlative adverb forms is given in Week 6?", opts:["Quick, quicker, quickest","Good, better, best","Quickly, more quickly, most quickly","Fast, faster, fastest-ly"], a:2},
        {q:"According to Week 6, what caveat is given about words ending in \"-ly\"?", opts:["All words ending in \"-ly\" are adverbs","Words ending in \"-ly\" are always verbs","\"-ly\" endings only apply to nouns","Not all words ending in \"-ly\" are adverbs (e.g., \"friendly\" is an adjective)"], a:3},
        {q:"What do adverbs of manner describe, according to Week 6?", opts:["Why an action occurs","How an action is performed","Where an action occurs","When an action occurs"], a:1},
        {q:"Which of these is given in Week 6 as an example of an adverb of manner?", opts:["Yesterday","Here","Often","Quietly"], a:3},
        {q:"According to Week 6, in which positions can adverbs appear in a sentence?", opts:["Only at the end","Only immediately before the verb","Front, mid, and end positions","Only at the beginning"], a:2},
        {q:"According to Week 6, what does understanding adverbs improve?", opts:["Sentence length","Spelling accuracy only","Vocabulary size only","Clarity and precision in both speech and writing"], a:3},
        {q:"What is the title of the Week 6 case study?", opts:["Improving Descriptive Writing through Adjective Usage","Enhancing Business Communication Skills through Effective Verb and Auxiliary Verb Usage","Developing Listening Skills through Tense Awareness","Enhancing Public Speaking Skills through Effective Adverb Usage"], a:3},
        {q:"What is the objective of the Week 6 case study?", opts:["To explore how the strategic use of adverbs can improve public speaking by adding clarity, emphasis, and nuance","To analyse the use of adjectives in product descriptions","To teach participants how to write formal business letters","To assess participants' grammar test scores"], a:0},
        {q:"Which types of adverbs are identified in the Week 6 case study methods?", opts:["Adverbs of place and size only","Adverbs of manner, time, place, frequency, and degree","Adverbs of number and gender","Adverbs of colour and shape"], a:1},
        {q:"According to the Week 6 case study methods, what do the observers assess?", opts:["The number of words per sentence","The length of the speech","The effect of adverb usage on audience engagement","The speaker's accent only"], a:2},
        {q:"Which of the following is listed as a skill/competency acquired in Week 6?", opts:["Auxiliary verb usage","Paragraph structuring","Adjective clause recognition","Critical listening"], a:3},
        {q:"Which two authors/references are cited as key references for Week 6?", opts:["Todd, J. (2010) and Crystal, David","Eyisi, Joy (2011) and Crystal, David","Todd, J. (2010) and Eyisi, Joy (2011)","Quirk et al. (1985) and Todd, J. (2010)"], a:2}
      ],
      fib: [
        {q:"Adverbs modify verbs, adjectives, other adverbs, or entire __________.", a:"sentences"},
        {q:"Adverbs answer questions such as how, when, __________, and why an action occurs.", a:"where"},
        {q:"Adverbs can have comparative and superlative forms, such as quickly, more quickly, and __________ quickly.", a:"most"},
        {q:"Not all words ending in \"__________\" are adverbs; for example, \"friendly\" is an adjective.", a:"-ly"},
        {q:"Adverbs of __________ describe how an action is performed, e.g., quickly, quietly, slowly, eventually.", a:"manner"},
        {q:"Adverbs can appear in different positions in a sentence: front, mid, and __________.", a:"end"},
        {q:"Understanding adverbs improves clarity and __________ in both speech and writing.", a:"precision"},
        {q:"The Week 6 case study is titled \"Enhancing Public Speaking Skills through Effective __________ Usage.\"", a:"Adverb"},
        {q:"The objective of the Week 6 case study is to explore how the strategic use of adverbs can add clarity, __________, and nuance to spoken communication.", a:"emphasis"},
        {q:"The Week 6 case study methods involve observing __________ and analysing their use of adverbs.", a:"public speakers"},
        {q:"The Week 6 case study identifies adverbs of manner, time, place, frequency, and __________.", a:"degree"},
        {q:"The Week 6 case study assesses the effect of adverb usage on __________ engagement.", a:"audience"},
        {q:"Among the skills acquired in Week 6 are public speaking proficiency, grammatical accuracy, effective communication, critical listening, language analysis, and __________ engagement.", a:"audience"},
        {q:"One Week 6 question to ponder asks about the risks of overusing or __________ adverbs in public speaking.", a:"misusing"},
        {q:"A key reference for Week 6 is Eyisi, Joy (2011), titled A Grammar of English: The Student's __________.", a:"Companion"}
      ],
      short: [
        {q:"What is the topic of Week 6?", a:"The Nature of Adverb"},
        {q:"According to Week 6, what can adverbs modify?", a:"Verbs, adjectives, other adverbs, or entire sentences"},
        {q:"Which questions do adverbs answer, according to Week 6?", a:"How, when, where, and why an action occurs"},
        {q:"Give the example of comparative and superlative adverb forms provided in Week 6.", a:"Quickly, more quickly, most quickly"},
        {q:"What caveat does Week 6 give about words ending in '-ly'?", a:"Not all words ending in '-ly' are adverbs; some, like 'friendly', are adjectives"},
        {q:"What do adverbs of manner describe, and give two examples from Week 6.", a:"They describe how an action is performed; examples include quickly, quietly, slowly, and eventually"},
        {q:"Where can adverbs appear in a sentence, according to Week 6?", a:"In front, mid, or end positions, depending on emphasis"},
        {q:"What does understanding adverbs improve, according to Week 6?", a:"Clarity and precision in both speech and writing"},
        {q:"What is the title of the Week 6 case study?", a:"Enhancing Public Speaking Skills through Effective Adverb Usage"},
        {q:"What is the objective of the Week 6 case study?", a:"To explore how the strategic use of adverbs can improve public speaking by adding clarity, emphasis, and nuance to spoken communication"},
        {q:"Which types of adverbs does the Week 6 case study method identify in public speakers' speech?", a:"Adverbs of manner, time, place, frequency, and degree"},
        {q:"State one of the Week 6 questions to ponder.", a:"How can appropriate adverb usage change the impact of a spoken message? (or: What are the risks of overusing or misusing adverbs in public speaking?)"},
        {q:"List three skills or competencies acquired in Week 6.", a:"Any three of: public speaking proficiency, grammatical accuracy, effective communication, critical listening, language analysis, audience engagement"},
        {q:"According to the Week 6 personal reflection, what does adverb choice affect?", a:"The clarity and persuasiveness of one's own speech"},
        {q:"Name the two key references cited for Week 6.", a:"Todd, J. (2010), Communication in English: Course Handbook; and Eyisi, Joy (2011), A Grammar of English: The Student's Companion"}
      ]
    }
  ]
},
{
  code: "MCM 101",
  title: "Foundations of Broadcasting and Film",
  weeks: [
    {
      week: 1,
      topic: "Overview of Radio and Television Broadcasting",
      mcq: [

    {q:"What two 19th-century inventions set the stage for broadcasting?", opts:["Radio and television","The telegraph and telephone","The camera and phonograph","The printing press and newspaper"], a:1},
    {q:"Who are named as pioneers of radio communication, and when was the first audio broadcast?", opts:["Edison and Bell; 1876","Marconi and Tesla; 1906","Gutenberg and Marconi; 1920","Tesla and Bell; 1899"], a:1},
    {q:"Which decade marked the start of commercial radio, and which station is given as an example?", opts:["1910s; BBC","1920s; KDKA","1930s; NBC","1940s; CBS"], a:1},
    {q:"What happened to radio's role during the 1930s–40s?", opts:["It declined as newspapers took over","It became the primary source of entertainment and information","It was replaced almost immediately by television","It became government-restricted worldwide"], a:1},
    {q:"What did television introduce that radio could not offer?", opts:["Faster news delivery","Visual storytelling, combining audio and visual elements","Lower production costs","Wider international reach than radio"], a:1},
    {q:"What two developments expanded broadcasting content in the late 20th century?", opts:["FM radio and colour print","Cable and satellite TV","Streaming and podcasts","3D printing and VR"], a:1},
    {q:"What does \"media convergence\" refer to in the 21st-century context?", opts:["Merging of competing broadcast companies","Integration of traditional broadcasting with online and mobile platforms","Combining radio and print journalism only","The decline of television viewership"], a:1},
    {q:"Which of the following is NOT listed as a core function of broadcasting?", opts:["Informing","Educating","Entertaining","Manufacturing"], a:3},
    {q:"Why is radio considered effective for social mobilisation in areas with high illiteracy?", opts:["It requires expensive equipment, ensuring quality control","It doesn't require reading ability to access information","It's the only medium regulated by governments","It has no competition from other media"], a:1},
    {q:"What is the correct order of stages in producing a radio/TV programme, per this week's material?", opts:["Production, conceptualisation, post-production, quality assurance","Conceptualisation, content development, production, post-production, quality assurance","Quality assurance, conceptualisation, production, content development","Content development, quality assurance, production, conceptualisation"], a:1},
    {q:"Which innovations are named as having enhanced broadcasting's quality and reach?", opts:["3D printing and holograms","Digital radio, FM, and digital TV standards","Satellite phones only","Analog-only signal boosters"], a:1},
    {q:"Besides providing information, what has broadcasting been crucial in shaping/fostering?", opts:["Only advertising revenue","Public opinion and cultural exchange","Only government policy","Only entertainment ratings"], a:1},
    {q:"What does television's combination of audio and visual elements do, per this week's material?", opts:["Reduces its impact compared to radio","Delivers impactful communication, influencing public opinion and cultural norms","Has no effect on public opinion","Only works for entertainment, not news"], a:1},
    {q:"Who wrote \"Radio-TV Production,\" a key reference cited this week?", opts:["Akpan S. Church","Onabajo, Olufemi","Owuamalam, E.O.","Sambe, J.A."], a:2},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Historical knowledge","Technical understanding","Content production","Financial auditing"], a:3}
      ],
      fib: [

    {q:"Broadcasting began with the invention of the __________ and telephone in the 19th century.", a:"telegraph"},
    {q:"__________ and Tesla are credited as pioneers in developing radio communication.", a:"Marconi"},
    {q:"The first audio broadcast is dated to the year __________.", a:"1906"},
    {q:"The __________ marked the start of commercial radio, with stations like KDKA offering regular programming.", a:"1920s"},
    {q:"Television emerged in the __________ century, revolutionising broadcasting with visual storytelling.", a:"mid-20th"},
    {q:"The late 20th century saw the introduction of __________ and satellite TV.", a:"cable"},
    {q:"The 21st century features media __________, integrating traditional broadcasting with online and mobile platforms.", a:"convergence"},
    {q:"Broadcasting stations can be owned by the __________ or private entities.", a:"government"},
    {q:"Producing a radio/TV programme involves conceptualisation, content development, production, __________, and quality assurance.", a:"post-production"},
    {q:"Radio is especially effective in social mobilisation in areas with high __________.", a:"illiteracy"},
    {q:"Innovations such as digital radio, FM, and digital __________ standards have enhanced broadcasting's quality and reach.", a:"TV"},
    {q:"Broadcasting has been crucial in shaping public opinion and fostering cultural __________.", a:"exchange"},
    {q:"Television combines audio and visual elements to deliver impactful communication, influencing public opinion and cultural __________.", a:"norms"},
    {q:"__________, E.O. (2007) wrote \"Radio-TV Production,\" a key reference this week.", a:"Owuamalam"},
    {q:"One skill gained this week is media __________.", a:"literacy"}
      ],
      short: [

    {q:"What two 19th-century inventions set the stage for broadcasting?", a:"The telegraph and telephone."},
    {q:"Name two pioneers credited with developing radio communication, and the year of the first audio broadcast.", a:"Marconi and Tesla; 1906."},
    {q:"What decade marked the start of commercial radio, and which station is cited as an example?", a:"The 1920s; KDKA."},
    {q:"What major shift happened to radio's role during the 1930s–40s?", a:"It became the primary source of entertainment and information."},
    {q:"What did television introduce that radio couldn't offer?", a:"Visual storytelling, combining audio and visual elements."},
    {q:"What two developments expanded channel/content availability in the late 20th century?", a:"Cable and satellite TV."},
    {q:"What is \"media convergence,\" as it applies to 21st-century broadcasting?", a:"Integration of traditional broadcasting with online and mobile platforms."},
    {q:"Name three core functions broadcasting serves in society, beyond entertainment.", a:"Any 3 of: informs, educates, shapes opinion/propaganda, commercial purposes."},
    {q:"Why is radio described as effective for social mobilisation in areas with high illiteracy?", a:"Because it's accessible without reading ability and reaches wide audiences."},
    {q:"List the stages involved in producing a radio or TV programme.", a:"Conceptualisation, content development, production, post-production, quality assurance."},
    {q:"Name two innovations credited with enhancing broadcasting's quality and reach.", a:"Any 2 of: digital radio, FM, digital TV standards."},
    {q:"What two things has broadcasting been crucial in shaping/fostering, beyond entertainment?", a:"Public opinion and cultural exchange."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: historical knowledge, technical understanding, media literacy, critical thinking, content production, communication skills."},
    {q:"Name the two key references given on the second page of this week's material.", a:"Sambe, J.A. (2008) Introduction to Mass Communication Practice in Nigeria; Owuamalam, E.O. (2007) Radio-TV Production."},
    {q:"What does the Call to Action for this week ask students to do?", a:"Explore the history of broadcasting, consider its impact on society, and engage critically with various forms of media."}
      ]
    },
    {
      week: 2,
      topic: "Natural Laws and Scientists that Make Broadcasting Possible",
      mcq: [
    {q:"Who formulated the 19th-century equations that established the theoretical foundation for electromagnetism?", opts:["James Clerk Maxwell","Heinrich Hertz","Guglielmo Marconi","Nikola Tesla"], a:0},
    {q:"Who confirmed the existence of electromagnetic waves through experiments in the late 19th century?", opts:["Edwin Armstrong","Heinrich Hertz","Lee de Forest","Claude Shannon"], a:1},
    {q:"Who developed practical wireless telegraphy systems, laying the groundwork for modern radio broadcasting?", opts:["Guglielmo Marconi","Philo Farnsworth","Thomas Stockham","A.J. Goldsmith"], a:0},
    {q:"What was the first method of modulating radio signals for transmission, developed in the early 20th century?", opts:["FM radio","AM radio","Digital radio","Satellite radio"], a:1},
    {q:"Who invented FM radio, and what advantage did it offer over AM?", opts:["Edwin Armstrong; superior sound quality and resistance to noise","Nikola Tesla; lower cost","Marconi; longer range only","Hertz; no real advantage"], a:0},
    {q:"Who developed essential components of early television systems, including the CRT and image dissector?", opts:["Vladimir Zworykin and Philo Farnsworth","Maxwell and Hertz","Shannon and Tesla","Armstrong and de Forest"], a:0},
    {q:"Whose work on information theory laid the groundwork for digital communication systems?", opts:["Claude Shannon","Reginald Fessenden","Lee de Forest","James Clerk Maxwell"], a:0},
    {q:"Who conducted the first known audio radio broadcast in 1906?", opts:["Reginald Fessenden","Guglielmo Marconi","Edwin Armstrong","Nikola Tesla"], a:0},
    {q:"Who invented the Audion vacuum tube, which improved the efficiency and amplification of radio signals?", opts:["Lee de Forest","Vladimir Zworykin","Claude Shannon","Thomas Stockham"], a:0},
    {q:"Whose innovations in AC electrical systems were crucial for the infrastructure needed for radio and television transmission?", opts:["Nikola Tesla","Heinrich Hertz","Philo Farnsworth","A.J. Goldsmith"], a:0},
    {q:"What are the three major functions broadcasting performs, per this week's material?", opts:["Informing, educating, entertaining","Selling, taxing, regulating","Recording, archiving, broadcasting","Producing, directing, editing"], a:0},
    {q:"What is the key difference between radio and television broadcasting, per this week's material?", opts:["Radio transmits audio signals only; television transmits both audio and visual signals","Radio is newer than television","Television cannot transmit audio","There is no meaningful difference"], a:0},
    {q:"Who developed algorithms for audio and video compression, per this week's material?", opts:["Engineers like A.J. Goldsmith and Thomas Stockham","Maxwell and Hertz","Marconi and Tesla","Zworykin and Farnsworth"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Analytical Thinking","Historical Knowledge","Technical Comprehension of Radio and TV Systems","Financial Accounting"], a:3},
    {q:"Who wrote \"Pillars of Broadcasting,\" a key reference cited again this week?", opts:["Akpan S. Church","Kovach & Rosenstiel","Pat Weaver","Russell B."], a:0}
      ],
      fib: [
    {q:"__________, who formulated key 19th-century equations, established the theoretical foundation for electromagnetism.", a:"Maxwell"},
    {q:"Heinrich __________ confirmed the existence of electromagnetic waves through experiments.", a:"Hertz"},
    {q:"Guglielmo __________ developed practical wireless telegraphy systems.", a:"Marconi"},
    {q:"__________ radio, developed in the early 20th century, was the first method of modulating radio signals for transmission.", a:"AM"},
    {q:"Edwin __________ invented FM radio, which offered superior sound quality and noise resistance.", a:"Armstrong"},
    {q:"Vladimir Zworykin and Philo __________ developed essential components of early television systems.", a:"Farnsworth"},
    {q:"Claude __________'s work on information theory laid the groundwork for digital communication systems.", a:"Shannon"},
    {q:"Reginald __________ conducted the first known audio radio broadcast in 1906.", a:"Fessenden"},
    {q:"Lee de __________ invented the Audion vacuum tube.", a:"Forest"},
    {q:"Nikola __________'s innovations in AC electrical systems were crucial for radio and television infrastructure.", a:"Tesla"},
    {q:"Broadcasting performs three major functions: informing, educating, and __________.", a:"entertaining"},
    {q:"Radio broadcasting involves the transmission of __________ signals through electromagnetic waves.", a:"audio"},
    {q:"Television broadcasting includes the transmission of both audio and __________ signals.", a:"visual"},
    {q:"Broadcasting has significantly influenced public opinion, cultural exchange, and social __________.", a:"mobilisation"},
    {q:"A.J. Goldsmith and Thomas Stockham developed algorithms for audio and video __________.", a:"compression"}
      ],
      short: [
    {q:"Who formulated the equations describing electric and magnetic fields, establishing the foundation for electromagnetism?", a:"James Clerk Maxwell."},
    {q:"What significant contribution did Heinrich Hertz make to electromagnetism?", a:"He confirmed the existence of electromagnetic waves through experiments."},
    {q:"Who is credited with developing practical wireless telegraphy systems?", a:"Guglielmo Marconi."},
    {q:"What invention is Edwin Armstrong known for, and what advantage did it offer?", a:"FM radio, which offered superior sound quality and resistance to noise compared to AM."},
    {q:"How did Reginald Fessenden contribute to the development of radio broadcasting?", a:"He conducted the first known audio radio broadcast in 1906, demonstrating the feasibility of voice transmission via radio waves."},
    {q:"Who developed essential components of early television systems, and what were they?", a:"Vladimir Zworykin and Philo Farnsworth; the CRT and the image dissector."},
    {q:"Whose work laid the groundwork for digital communication systems?", a:"Claude Shannon, through his work on information theory."},
    {q:"What did Lee de Forest invent, and what did it improve?", a:"The Audion vacuum tube, which improved the efficiency and amplification of radio signals."},
    {q:"Why was Nikola Tesla's work important to broadcasting?", a:"His innovations in AC electrical systems were crucial for the infrastructure needed for radio and television transmission."},
    {q:"What are the three major functions broadcasting performs?", a:"Informing, educating, and entertaining the audience."},
    {q:"What is the key difference between radio and television broadcasting?", a:"Radio transmits audio signals only; television transmits both audio and visual signals."},
    {q:"What does this week's Call to Action ask students to do?", a:"Explore the history and evolution of broadcasting technologies and their impact on society."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: analytical thinking, historical knowledge, awareness of technological advancements, societal impact, technical comprehension of radio and TV systems."},
    {q:"What three questions does this week's Personal Reflection raise?", a:"The role of inventors like Maxwell, Hertz, and Marconi today; broadcasting's societal impact on public opinion and cultural exchange; and which technological advancements are most fascinating."},
    {q:"Name two key references cited this week.", a:"Akpan S. Church (2006) Pillars of Broadcasting; Kovach & Rosenstiel (2007) The Elements of Journalism."}
      ]
    },
    {
      week: 3,
      topic: "Legal Framework and Codes of Ethics of Broadcasting",
      mcq: [
    {q:"What governs the practice of occupations and professions, per this week's material?", opts:["Professional ethics, referred to as codes of ethics","Government subsidies","Trade unions only","Advertising budgets"], a:0},
    {q:"Who describes the National Broadcasting Code as a roadmap for free and responsible broadcasting?", opts:["Dr. Tom Adaba","Akpan S. Church","Olufemi Onabajo","Liad Tella"], a:0},
    {q:"What must journalists strive for, per this week's material?", opts:["Accuracy, verifying information from multiple sources before broadcasting","Speed over accuracy","Avoiding verification to save time","Publishing unverified claims first"], a:0},
    {q:"How should broadcast journalists present news, per this week's material?", opts:["With personal opinions included","Without bias, giving balanced representation of different perspectives","Favouring one perspective only","Only from government sources"], a:1},
    {q:"What should journalists avoid, regarding individuals' feelings and dignity?", opts:["Sensationalism and offensive content","Using any images at all","Reporting on sensitive topics entirely","Interviewing the public"], a:0},
    {q:"What is crucial regarding personal information or images in broadcasting?", opts:["Respecting privacy and seeking consent before use","Publishing them without restriction","Avoiding all personal stories","Using them only for entertainment"], a:0},
    {q:"What should journalists do regarding conflicts of interest?", opts:["Ignore them if the story is important enough","Avoid them, disclose any potential conflicts, and maintain integrity","Only disclose conflicts if asked","Resolve them privately without disclosure"], a:1},
    {q:"What should journalists be, regarding their actions?", opts:["Accountable, and open to public criticism and feedback","Immune from criticism","Anonymous at all times","Free from any oversight"], a:0},
    {q:"What is essential for maintaining journalistic independence, per this week's material?", opts:["Editorial independence from outside influences like advertisers or political interests","Full dependence on advertiser funding","Government ownership of all outlets","Avoiding all sources of funding"], a:0},
    {q:"What is important for credibility in news gathering and reporting?", opts:["Being transparent about methods and processes","Keeping sources and methods entirely secret","Avoiding transparency to protect sources always","Publishing without any process"], a:0},
    {q:"What do laws, regulations, policies, and guidelines govern, per this week's material?", opts:["Broadcast media operations, content, and licensing","Only print journalism","Only social media platforms","Only advertising content"], a:0},
    {q:"What do regulatory bodies do, per this week's material?", opts:["Oversee and enforce broadcast laws, issue licenses, monitor compliance, and investigate complaints","Only collect broadcasting fees","Have no role in broadcasting","Only produce content"], a:0},
    {q:"What does this week's Call to Action ask students to foster?", opts:["A culture of ethical journalism by holding broadcasters accountable","Competition between news outlets only","Avoidance of all media engagement","Reduced transparency in reporting"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Ethical Decision-Making","Accuracy in Reporting","Understanding of Legal Frameworks","Software Development"], a:3},
    {q:"Who wrote \"Media Ethics and Moral Reasoning,\" a key reference cited this week?", opts:["Clifford, G.C. et al.","Akpan S. Church","Liad Tella","The Associated Press"], a:0}
      ],
      fib: [
    {q:"Professional ethics govern the practice of occupations and professions, and are referred to as codes of __________.", a:"ethics"},
    {q:"Dr. Tom __________ describes the National Broadcasting Code as a roadmap for free and responsible broadcasting.", a:"Adaba"},
    {q:"Journalists must strive for __________, verifying information from multiple sources before broadcasting.", a:"accuracy"},
    {q:"Broadcast journalists should present news without __________, giving balanced representation of different perspectives.", a:"bias"},
    {q:"Journalists should be sensitive to individuals' feelings and dignity, avoiding sensationalism and __________ content.", a:"offensive"},
    {q:"Respecting privacy and seeking __________ before using personal information or images is crucial in broadcasting.", a:"consent"},
    {q:"Journalists should avoid conflicts of interest, disclose any potential conflicts, and maintain __________ in reporting.", a:"integrity"},
    {q:"Journalists should be accountable for their actions and open to public criticism and __________.", a:"feedback"},
    {q:"Maintaining editorial __________ from outside influences like advertisers or political interests is essential.", a:"independence"},
    {q:"Being transparent about methods and processes in news gathering and reporting is important for __________.", a:"credibility"},
    {q:"__________ bodies oversee and enforce broadcast laws, issue licenses, monitor compliance, and investigate complaints.", a:"Regulatory"},
    {q:"This week's Call to Action asks students to foster a culture of __________ journalism.", a:"ethical"},
    {q:"Clifford, G.C. et al. (2020) wrote \"Media Ethics and Moral __________,\" a key reference this week.", a:"Reasoning"},
    {q:"One skill gained this week is __________ decision-making.", a:"ethical"},
    {q:"The Associated Press __________ 2017 is cited as a key reference this week.", a:"Stylebook"}
      ],
      short: [
    {q:"What governs the practice of occupations and professions, per this week's material?", a:"Professional ethics, referred to as codes of ethics."},
    {q:"Who describes the National Broadcasting Code as a roadmap for free and responsible broadcasting?", a:"Dr. Tom Adaba."},
    {q:"What must journalists strive for, and how?", a:"Accuracy, by verifying information from multiple sources before broadcasting and correcting errors promptly."},
    {q:"How should broadcast journalists present news, per this week's material?", a:"Without bias, giving balanced representation of different perspectives, and maintaining objectivity."},
    {q:"What should journalists be sensitive to, per this week's material?", a:"Individuals' feelings and dignity, avoiding sensationalism and offensive content."},
    {q:"What is crucial regarding personal information or images in broadcasting?", a:"Respecting privacy and seeking consent before using them."},
    {q:"How should journalists handle conflicts of interest?", a:"Avoid them, disclose any potential conflicts, and maintain integrity in reporting."},
    {q:"What should journalists be accountable for, per this week's material?", a:"Their actions, and they should be open to public criticism and feedback."},
    {q:"What is essential for maintaining journalistic independence?", a:"Editorial independence from outside influences like advertisers or political interests."},
    {q:"What do regulatory bodies do in the broadcasting industry?", a:"Oversee and enforce broadcast laws, issue licenses, monitor compliance, and investigate complaints."},
    {q:"What does this week's Call to Action ask students to do?", a:"Foster a culture of ethical journalism, advocate for transparency and fairness, and support outlets with high ethical standards."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: ethical decision-making, accuracy in reporting, objectivity and impartiality, respect for privacy and consent, accountability and transparency, understanding of legal frameworks."},
    {q:"What three questions does this week's Personal Reflection raise?", a:"Reflecting on biased reporting encountered; a situation where privacy/consent was violated; and the role of ethics in shaping responsible journalism."},
    {q:"Name two key references cited this week.", a:"Akpan S. Church (2006) Pillars of Broadcasting; Clifford, G.C. et al. (2020) Media Ethics and Moral Reasoning."},
    {q:"What does broadcasting's legal framework include, per this week's material?", a:"Laws, regulations, policies, and guidelines governing broadcast media operations, content, and licensing."}
      ]
    },
    {
      week: 4,
      topic: "Individual Items or Equipment Used in Radio and Television Broadcast",
      mcq: [
        {q:"According to the material, radio station equipment includes hardware and software for which types of broadcasting?", opts:["Television broadcasting exclusively","FM, AM, internet, satellite, and digital radio broadcasting","Film production exclusively","Only AM and shortwave radio"], a:1},
        {q:"What is a broadcast studio described as being essential for?", opts:["Producing and transmitting audiovisual content for radio, TV, or online platforms","Training radio presenters only","Storing archived newspapers","Manufacturing transmission antennas"], a:0},
        {q:"Which of the following are features of television studios, as described in the material?", opts:["Sound stages and lighting grids only","VR and AR immersive environments only","Multiple sets, professional cameras, lighting, and control rooms","Soundproofing materials and ribbon microphones only"], a:2},
        {q:"Radio studios are equipped with which of the following, according to the material?", opts:["Professional cameras and control rooms","Video servers and broadcast monitors","Sound stages and post-production facilities","Microphones, mixing consoles, and soundproofing materials"], a:3},
        {q:"Film studios, as described in the material, include which facilities?", opts:["Mixing consoles and soundproofing materials only","Virtual reality headsets only","Transmitters and antennas only","Sound stages, lighting grids, and post-production facilities"], a:3},
        {q:"What technologies do virtual studios use for creating immersive broadcasting environments?", opts:["Ribbon microphones","Analog mixing consoles","VR and AR technologies","Satellite and shortwave transmitters"], a:2},
        {q:"Online streaming studios, as described in the material, range from professional setups to what?", opts:["Radar transmission facilities","Film sound stages","DIY home offices tailored for internet content creation","Large-scale national broadcast towers"], a:2},
        {q:"What is the primary function of transmitters in broadcasting?", opts:["Converting electrical signals into radio waves for broadcasting","Combining audio sources and adjusting levels","Capturing visual images and converting them into electronic signals","Storing and managing digital video content"], a:0},
        {q:"Which type of transmitter is NOT mentioned among the types listed in the material?", opts:["VHF/UHF transmitters","Bluetooth transmitters","Satellite transmitters","Shortwave transmitters"], a:1},
        {q:"Which of the following is listed in the material as a type of microphone?", opts:["Bluetooth microphone","Infrared microphone","USB microphone","Ribbon microphone"], a:3},
        {q:"What is the main function of a mixing console, according to the material?", opts:["To create on-screen graphics such as titles and logos","To combine audio sources and adjust levels","To capture visual images and convert them into electronic signals","To store digital video content for playback"], a:1},
        {q:"Mixing consoles can be which of the following types, as described in the material?", opts:["Analog, digital, software-based, or portable","Only portable or fixed","Only analog or digital","Only wireless or satellite-based"], a:0},
        {q:"What do television cameras do, according to the material?", opts:["Capture visual images and convert them into electronic signals","Enable seamless transitions between video sources","Convert electrical signals into radio waves","Combine multiple audio sources"], a:0},
        {q:"What is another name given to video switchers in the material?", opts:["Production switchers","Video servers","Graphics generators","Broadcast monitors"], a:0},
        {q:"What is the function of graphics generators, as described in the material?", opts:["To convert electrical signals into radio waves","To provide real-time video and audio signal monitoring","To store and manage digital video content","To create on-screen graphics like titles, logos, and animations"], a:3}
      ],
      fib: [
        {q:"Radio station equipment can overlap with television broadcasting, involving audio and __________ production tools.", a:"video"},
        {q:"Television studios have multiple sets, professional cameras, lighting, and __________ rooms.", a:"control"},
        {q:"Film studios include sound stages, lighting grids, and __________ facilities.", a:"post-production"},
        {q:"Virtual studios use __________ and __________ technologies for creating immersive broadcasting environments.", a:"VR; AR"},
        {q:"Transmitters convert electrical signals into __________ for broadcasting.", a:"radio waves"},
        {q:"Microphones capture __________ signals.", a:"audio"},
        {q:"Video servers store and manage __________ video content, facilitating playback during live or pre-recorded broadcasts.", a:"digital"},
        {q:"Broadcast monitors provide real-time video and audio signal __________.", a:"monitoring"},
        {q:"Types of broadcast monitors include reference monitors, production monitors, client monitors, field monitors, multiview monitors, and __________ monitors.", a:"portable video assist"},
        {q:"Transmission equipment such as amplifiers, transmitters, and __________ ensure reliable broadcasting of television signals to viewers.", a:"antennas"},
        {q:"Towolawi, N. authored \"Microphone Appreciation\" as part of the Basic Production Course Manual at the __________ Training School, Shogunle, Lagos State.", a:"FRCN"},
        {q:"Chan, R. (2023) wrote \"Radio Station Equipment: Full List for Studio & __________\".", a:"Transmission"},
        {q:"One of the skills and competencies listed for this lesson is __________ Selection Skills.", a:"Microphone"},
        {q:"One of the skills and competencies listed for this lesson is Broadcast __________ Setup.", a:"Studio"},
        {q:"One of the discussion questions asks: \"What are the advantages of using __________ mixing consoles over analog ones?\"", a:"digital"}
      ],
      short: [
        {q:"What types of broadcasting does radio station equipment support, according to the material?", a:"FM, AM, internet, satellite, and digital radio broadcasting."},
        {q:"Why is a broadcast studio considered essential?", a:"It is essential for producing and transmitting audiovisual content for radio, TV, or online platforms."},
        {q:"List the equipment typically found in a radio studio.", a:"Microphones, mixing consoles, and soundproofing materials."},
        {q:"What facilities are included in a film studio?", a:"Sound stages, lighting grids, and post-production facilities."},
        {q:"Describe the function of virtual studios.", a:"They use VR and AR technologies for creating immersive broadcasting environments."},
        {q:"What range of setups do online streaming studios cover?", a:"They range from professional setups to DIY home offices, tailored for internet content creation."},
        {q:"List the types of transmitters mentioned in the material.", a:"AM, FM, shortwave, VHF/UHF, digital, satellite, and radar transmitters."},
        {q:"List the types of microphones mentioned in the material.", a:"Dynamic, condenser, shotgun, lavalier, headset, boundary, and ribbon microphones."},
        {q:"What are the possible types of mixing consoles according to the material?", a:"Analog, digital, software-based, or portable."},
        {q:"What do video switchers (production switchers) enable during live broadcasts?", a:"They enable seamless transitions between multiple video sources during live broadcasts."},
        {q:"What is the function of graphics generators in television broadcasts?", a:"They create on-screen graphics like titles, logos, and animations to enhance television broadcasts."},
        {q:"What is the role of video servers in broadcasting?", a:"They store and manage digital video content, facilitating playback during live or pre-recorded broadcasts."},
        {q:"Name the types of broadcast monitors listed in the material.", a:"Reference monitors, production monitors, client monitors, field monitors, multiview monitors, and portable video assist monitors."},
        {q:"What does transmission equipment such as amplifiers, transmitters, and antennas ensure?", a:"Reliable broadcasting of television signals to viewers."},
        {q:"Name two skills and competencies students should have acquired after this lesson.", a:"Any two of: Broadcast Studio Setup, Microphone Selection Skills, Broadcast Equipment Knowledge, Broadcast Monitoring, Camera Operation."}
      ]
    },
    {
      week: 5,
      topic: "Diverse Environment of Broadcasting Stations and Networks",
      mcq: [
        {q:"Which of the following does the material list as part of broadcasting stations?", opts:["Only film and print media","Television, radio, internet, streaming services, and social media","Only television and radio","Only internet and social media"], a:1},
        {q:"How is television described in the material?", opts:["A dominant medium that delivers diverse content directly to homes","A purely local medium","A declining medium with little audience reach","A medium used only for advertising"], a:0},
        {q:"How is radio described in the material?", opts:["An outdated medium no longer in use","A medium primarily for visual content","A niche medium with minimal engagement","A cherished medium that engages listeners through sound"], a:3},
        {q:"What role does the internet play in broadcasting, according to the material?", opts:["It only supports radio broadcasting","It revolutionises broadcasting, offering vast digital platforms for content creation","It has no significant role in broadcasting","It replaced television entirely"], a:1},
        {q:"What do streaming services provide, according to the material?", opts:["Live-only broadcasting with no replay","Government-funded educational content only","Local community programming only","On-demand access to extensive libraries of media content"], a:3},
        {q:"What do social media platforms enable, according to the material?", opts:["Only local community engagement","Real-time interaction and information sharing globally","Only one-way broadcasting with no interaction","Only pre-recorded video content"], a:1},
        {q:"How are commercial broadcasting stations sustained, according to the material?", opts:["They are funded entirely by government grants","They operate for profit, sustained by advertising revenue","They rely solely on viewer donations","They are funded by international organisations"], a:1},
        {q:"What type of programming do commercial broadcasting stations produce?", opts:["Only educational and cultural content","Only hyper-local community content","Only international news content","A mix of entertainment, news, and other programmes for broad audiences"], a:3},
        {q:"How are public broadcasting stations funded, according to the material?", opts:["Exclusively by international investors","By government, viewer donations, and sponsorships","Exclusively by advertising revenue","Exclusively by subscription fees"], a:1},
        {q:"What type of content do public broadcasting stations prioritise?", opts:["Educational, informative, and culturally enriching content","Purely entertainment content for profit","Purely international sports content","Purely local community content"], a:0},
        {q:"What type of communities do community broadcasting stations serve?", opts:["International audiences with global content","Only commercial advertisers","Local or niche communities with hyper-local content","National audiences with country-wide programming"], a:2},
        {q:"What do community broadcasting stations focus on promoting, according to the material?", opts:["Diversity, inclusion, and civic engagement within their communities","International trade relations","Profit maximisation through advertising","National political agendas"], a:0},
        {q:"How do national broadcasting networks operate, according to the material?", opts:["On a country-wide scale with varied programming","On a global scale exclusively","On a purely local scale with niche content","On an international scale with no local content"], a:0},
        {q:"What do global broadcasting networks do, according to the material?", opts:["Reach international audiences with diverse, global content","Focus solely on specialised demographics","Serve only local or niche communities","Operate only within a single country"], a:0},
        {q:"What do specialised networks cater to, according to the material?", opts:["Niche interests or demographics with targeted programming","Only international news audiences","Broad general audiences with mixed programming","Only government-funded educational content"], a:0}
      ],
      fib: [
        {q:"Broadcasting stations encompass television, radio, internet, __________ services, and social media.", a:"streaming"},
        {q:"Television remains a __________ medium, delivering diverse content directly to homes.", a:"dominant"},
        {q:"Radio persists as a __________ medium, engaging listeners through sound.", a:"cherished"},
        {q:"The internet __________ broadcasting, offering vast digital platforms for content creation.", a:"revolutionises"},
        {q:"Commercial broadcasting stations operate for __________, sustained by advertising revenue.", a:"profit"},
        {q:"Public broadcasting stations are funded by government, viewer donations, and __________.", a:"sponsorships"},
        {q:"Community broadcasting stations serve local or niche communities with __________ content.", a:"hyper-local"},
        {q:"Community broadcasting stations focus on promoting diversity, inclusion, and __________ engagement within their communities.", a:"civic"},
        {q:"National broadcasting networks operate on a __________ scale with varied programming.", a:"country-wide"},
        {q:"Global broadcasting networks reach __________ audiences with diverse, global content.", a:"international"},
        {q:"Specialised networks cater to niche interests or demographics with __________ programming.", a:"targeted"},
        {q:"Tella, L. (2019) wrote \"Basic Elements and techniques of News Reporting and Writing\", published by __________ Press.", a:"Unilorin"},
        {q:"Kovach, B. & Rosenstiel, T. (2014) wrote \"Elements of __________\" (E-Book), Penguin Random House.", a:"Journalism"},
        {q:"One of the skills and competencies listed for this lesson is Media __________.", a:"Literacy"},
        {q:"One of the skills and competencies listed for this lesson is __________ Awareness.", a:"Cultural"}
      ],
      short: [
        {q:"List the types of broadcasting stations and networks mentioned in the material.", a:"Television, radio, internet, streaming services, social media, commercial, public, community, national, global, and specialised broadcasting stations/networks."},
        {q:"How is television described in the material?", a:"As a dominant medium that delivers diverse content directly to homes."},
        {q:"How is radio described in the material?", a:"As a cherished medium that engages listeners through sound."},
        {q:"What impact has the internet had on broadcasting, according to the material?", a:"It has revolutionised broadcasting, offering vast digital platforms for content creation."},
        {q:"What do streaming services offer, according to the material?", a:"On-demand access to extensive libraries of media content."},
        {q:"What do social media platforms enable in broadcasting?", a:"Real-time interaction and information sharing globally."},
        {q:"How do commercial broadcasting stations generate revenue, and what do they produce?", a:"They operate for profit, sustained by advertising revenue, and produce a mix of entertainment, news, and other programmes for broad audiences."},
        {q:"How are public broadcasting stations funded, and what content do they prioritise?", a:"They are funded by government, viewer donations, and sponsorships, and prioritise educational, informative, and culturally enriching content."},
        {q:"What is the role of community broadcasting stations?", a:"They serve local or niche communities with hyper-local content and focus on promoting diversity, inclusion, and civic engagement."},
        {q:"Describe the scale and programming of national broadcasting networks.", a:"They operate on a country-wide scale with varied programming."},
        {q:"Describe the scale and content of global broadcasting networks.", a:"They reach international audiences with diverse, global content."},
        {q:"What do specialised networks cater to?", a:"Niche interests or demographics with targeted programming."},
        {q:"Name a key reference cited in the Week 5 material relating to news reporting.", a:"Tella, L. (2019). Basic Elements and techniques of News Reporting and Writing. Ilorin: Unilorin Press."},
        {q:"Name two skills and competencies students should have acquired after this lesson.", a:"Any two of: Media Literacy, Analytical Skills, Critical Thinking, Civic Engagement, Cultural Awareness, Communication Skills."},
        {q:"According to the discussion questions, how do public broadcasting stations differ from commercial ones?", a:"They differ in terms of funding (government, donations, sponsorships vs advertising revenue) and content priorities (educational/cultural vs profit-driven entertainment and news)."}
      ]
    },
    {
      week: 6,
      topic: "Overview of Kinds of Film",
      mcq: [
        {q:"According to the material, what role can film serve in society?", opts:["A tool used only for advertising products","A medium exclusively for historical documentation","A purely entertainment medium with no social role","A development communication tool to promote social and economic development"], a:3},
        {q:"What does content analysis of Kannada films, as discussed in the material, reveal?", opts:["Their focus on special effects only","Their lack of any social themes","Their exclusive focus on international audiences","Their use in addressing societal concerns"], a:3},
        {q:"Which two Kannada films are named in the material as emphasising agriculture and social change?", opts:["\"Lagaan\" and \"Swades\"","\"Bangarada Manushya\" and \"Boothayyana Maga Ayyu\"","\"Sholay\" and \"Mughal-E-Azam\"","\"Pather Panchali\" and \"Mother India\""], a:1},
        {q:"How does the material define film?", opts:["A purely digital format with no physical medium","A written script with no visual component","A physical medium for recording images and a creative product combining moving images, sound, and storytelling","A type of radio broadcast"], a:2},
        {q:"How is cinema described in the material?", opts:["The entire process of filmmaking, from concept to distribution","Only the technical editing stage of filmmaking","Only the act of watching a film in a theatre","Only the marketing of a film"], a:0},
        {q:"What is the origin and meaning of the term \"genre\", according to the material?", opts:["A German term meaning \"sound\"","An English term meaning \"story\"","A Latin term meaning \"image\"","A French term meaning \"type\", used to classify films"], a:3},
        {q:"How does the material describe the definition of genre?", opts:["It is no longer used in filmmaking","It applies only to documentaries","It is precisely and universally agreed upon","It remains elusive despite being used to classify films"], a:3},
        {q:"What is the purpose of documentaries, according to the material?", opts:["To replace scripted drama films","To prioritise artistic experimentation over facts","To create entirely fictional narratives","To provide factual accounts of real-life subjects and inform and raise awareness"], a:3},
        {q:"Which of the following is listed in the material as a form documentaries can take?", opts:["Musical","Animated-only","Melodramatic","Observational"], a:3},
        {q:"What do avant-garde films prioritise, according to the material?", opts:["Commercial success and mass-market appeal","Documentary-style factual accuracy","Artistic expression and formal experimentation over traditional storytelling","Strict adherence to traditional narrative structure"], a:2},
        {q:"Which characteristics are associated with avant-garde films in the material?", opts:["Factual reporting and journalistic interviews","Heavy use of traditional theatrical staging","Abstract narratives, unconventional editing, and minimal dialogue","Linear plots, conventional editing, and extensive dialogue"], a:2},
        {q:"What are the stages of producing a film, as listed in the material?", opts:["Idea generation, scriptwriting, pre-production, production, post-production, and distribution","Casting, marketing, release, and archiving only","Pre-production and post-production only","Scriptwriting and distribution only"], a:0},
        {q:"Which tasks are part of pre-production, according to the material?", opts:["Casting, location scouting, and developing a production schedule","Capturing scenes with cameras and lighting","Editing, sound design, and visual effects","Distribution and marketing of the finished film"], a:0},
        {q:"What does the production stage of filmmaking involve, according to the material?", opts:["Idea generation and scriptwriting","Casting and location scouting","Editing and visual effects","Capturing scenes with cameras, lighting, and sound equipment"], a:3},
        {q:"What does the post-production stage include, according to the material?", opts:["Editing, sound design, and visual effects to refine the film","Casting and location scouting","Distribution to theatres only","Idea generation and scriptwriting"], a:0}
      ],
      fib: [
        {q:"Film serves as a __________ communication tool to promote social and economic development.", a:"development"},
        {q:"\"Bangarada Manushya\" and \"Boothayyana Maga Ayyu\" emphasise __________ and social change.", a:"agriculture"},
        {q:"Film is both a physical medium for recording images and a creative product combining moving images, sound, and __________.", a:"storytelling"},
        {q:"Cinema includes the entire process of filmmaking, from __________ to distribution.", a:"concept"},
        {q:"Genre, a French term for \"__________\", is used to classify films but remains elusive in its definition.", a:"type"},
        {q:"Documentaries provide factual accounts of real-life subjects and aim to inform and raise __________.", a:"awareness"},
        {q:"Documentaries can take various forms, such as expository, observational, and __________.", a:"participatory"},
        {q:"Avant-garde films prioritise artistic expression and formal __________ over traditional storytelling.", a:"experimentation"},
        {q:"Avant-garde films often feature abstract narratives, unconventional editing, and minimal __________.", a:"dialogue"},
        {q:"Producing a film involves stages such as idea generation, scriptwriting, pre-production, production, post-production, and __________.", a:"distribution"},
        {q:"Pre-production includes casting, location scouting, and developing a __________ schedule.", a:"production"},
        {q:"Production involves capturing scenes with cameras, lighting, and __________ equipment.", a:"sound"},
        {q:"Post-production includes editing, sound design, and __________ effects to refine the film.", a:"visual"},
        {q:"Sachin N J (2023) published \"Film as a Development Communication Medium: An Analytical Study of Selected __________ Movies\".", a:"Kannada"},
        {q:"Langford, B. (2005) wrote \"Hollywood and Beyond\", published by __________ University Press.", a:"Edinburgh"}
      ],
      short: [
        {q:"How can film be used as a tool for development communication, according to the material?", a:"Film serves as a development communication tool to promote social and economic development."},
        {q:"What does the content analysis of Kannada films reveal, according to the material?", a:"It reveals their use in addressing societal concerns."},
        {q:"Name the two Kannada films mentioned in the material and what they emphasise.", a:"\"Bangarada Manushya\" and \"Boothayyana Maga Ayyu\", which emphasise agriculture and social change."},
        {q:"How does the material define film as both a medium and a product?", a:"Film is both a physical medium for recording images and a creative product combining moving images, sound, and storytelling."},
        {q:"What does the term \"cinema\" encompass, according to the material?", a:"The entire process of filmmaking, from concept to distribution."},
        {q:"What is the origin of the term \"genre\" and why is it described as elusive?", a:"Genre is a French term for \"type\" used to classify films, but its definition remains elusive."},
        {q:"What is the purpose of documentaries, according to the material?", a:"To provide factual accounts of real-life subjects and aim to inform and raise awareness."},
        {q:"List the forms documentaries can take, according to the material.", a:"Expository, observational, and participatory."},
        {q:"What do avant-garde films prioritise, and what features do they often have?", a:"They prioritise artistic expression and formal experimentation over traditional storytelling, often featuring abstract narratives, unconventional editing, and minimal dialogue."},
        {q:"List the stages involved in producing a film, according to the material.", a:"Idea generation, scriptwriting, pre-production, production, post-production, and distribution."},
        {q:"What tasks are involved in the pre-production stage of filmmaking?", a:"Casting, location scouting, and developing a production schedule."},
        {q:"What does the production stage of filmmaking involve?", a:"Capturing scenes with cameras, lighting, and sound equipment."},
        {q:"What does the post-production stage involve?", a:"Editing, sound design, and visual effects to refine the film."},
        {q:"Name two skills and competencies students should have acquired after this lesson.", a:"Any two of: Critical analysis, Creative adaptation, Visual storytelling, Film production, Narrative development, Audience engagement."},
        {q:"Name a key reference cited in the Week 6 material relating to Kannada films.", a:"Sachin N J (2023) Film as a Development Communication Medium: An Analytical Study of Selected Kannada Movies. UGC Care Group 1 Journal, Mumbai."}
      ]
    }
  ]
},
{
  code: "MIVA-MCM 109",
  title: "History and Development of Mass Communication",
  weeks: [
    {
      week: 1,
      topic: "Introduction to Mass Communication",
      mcq: [

    {q:"How is mass communication defined this week?", opts:["Private exchange of messages between two people","Transmitting information to a large, diverse audience via various channels","Communication limited to written text only","A process exclusive to broadcast journalism"], a:1},
    {q:"Which of these is NOT listed as a channel of mass communication?", opts:["Newspapers","Social media","Private letters","Television"], a:2},
    {q:"Which of these is NOT listed as a discipline involved in mass communication?", opts:["Journalism","Public relations","Digital media","Astronomy"], a:3},
    {q:"What three roles does mass communication play for audiences, per this week's material?", opts:["Informing, entertaining, persuading","Selling, taxing, regulating","Translating, archiving, encrypting","Debating, voting, legislating"], a:0},
    {q:"Which three methods are named as early, pre-writing forms of communication?", opts:["Telegrams, letters, newspapers","Cave paintings, hieroglyphics, oral storytelling","Radio, television, film","Printing press, telephone, telegraph"], a:1},
    {q:"What effect did the printing press have on society, per this week's summary?", opts:["It had minimal effect on literacy","It revolutionised information dissemination and literacy","It slowed the spread of written material","It was primarily used for private letters"], a:1},
    {q:"Which two inventions enabled long-distance communication before radio and TV?", opts:["Camera and phonograph","Telegraph and telephone","Fax machine and pager","Printing press and newspaper"], a:1},
    {q:"What is the correct order of the mass communication process, per this week's material?", opts:["Reception, production, distribution","Production, distribution, reception","Distribution, reception, production","Production, reception, distribution"], a:1},
    {q:"Which of these is described as a benefit of mass communication beyond informing/persuading?", opts:["It eliminates the need for personal communication","It fosters cultural exchange and social cohesion","It reduces the diversity of audience opinions","It replaces journalism entirely"], a:1},
    {q:"What made the internet distinct in transforming mass communication in the 21st century?", opts:["It made mass communication a one-way process only","It transformed communication broadly, alongside digital media","It eliminated the role of television","It had no impact on journalism practices"], a:1},
    {q:"What does mass communication provide insight into, per this week's material?", opts:["Only advertising budgets","Media production and consumption","Only government regulation","Only historical dates"], a:1},
    {q:"How is the interaction between senders and receivers in mass communication described?", opts:["Static and one-directional","Dynamic","Irrelevant to the process","Entirely automated"], a:1},
    {q:"What does this week's Call to Action ask students to do?", opts:["Memorise dates only","Create a timeline of key milestones in mass communication history and discuss ethical responsibilities","Avoid discussing ethics","Write a private journal entry"], a:1},
    {q:"Who wrote \"McQuail's Mass Communication Theory,\" a key reference this week?", opts:["Baran, S.J.","Davis, D.K.","McQuail, D.","Thompson, J.B."], a:2},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Critical Thinking","Media Literacy","Ethical Awareness","Financial Modelling"], a:3}
      ],
      fib: [

    {q:"Mass communication transmits information to a large, __________ audience via various channels.", a:"diverse"},
    {q:"Disciplines involved in mass communication include journalism, broadcasting, advertising, public relations, and __________ media.", a:"digital"},
    {q:"Early communication methods included cave paintings, hieroglyphics, and __________ storytelling.", a:"oral"},
    {q:"The __________ press revolutionised information dissemination and literacy.", a:"printing"},
    {q:"The __________ and telephone enabled long-distance communication.", a:"telegraph"},
    {q:"Radio and television became dominant mass communication forms in the __________ century.", a:"20th"},
    {q:"The mass communication process includes production, __________, and reception of messages.", a:"distribution"},
    {q:"Mass communication fosters cultural exchange and social __________.", a:"cohesion"},
    {q:"The __________ and digital media have transformed communication in the 21st century.", a:"internet"},
    {q:"Mass communication has been a driver of societal __________ and progress.", a:"change"},
    {q:"Mass communication influences __________ of the world.", a:"perceptions"},
    {q:"There is a dynamic __________ between senders and receivers of information.", a:"interaction"},
    {q:"Audience __________ and response are integral to the communication process.", a:"interpretation"},
    {q:"Mass communication __________ civic engagement and facilitates the exchange of ideas.", a:"promotes"},
    {q:"__________, D. (2010) wrote \"McQuail's Mass Communication Theory,\" a key reference this week.", a:"McQuail"}
      ],
      short: [

    {q:"Give the definition of mass communication as covered this week.", a:"Transmitting information to a large, diverse audience via various channels."},
    {q:"Name four channels through which mass communication occurs.", a:"Any 4 of: newspapers, television, radio, internet, social media."},
    {q:"Name four disciplines involved in mass communication.", a:"Any 4 of: journalism, broadcasting, advertising, public relations, digital media."},
    {q:"What three core roles does mass communication play for audiences?", a:"Informing, entertaining, persuading."},
    {q:"What three early communication methods are named as predating writing?", a:"Cave paintings, hieroglyphics, oral storytelling."},
    {q:"What effect did the printing press have on society, per this week's material?", a:"It revolutionised information dissemination and literacy."},
    {q:"What two inventions enabled long-distance communication before radio/TV?", a:"The telegraph and telephone."},
    {q:"What are the three stages in the mass communication process?", a:"Production, distribution, reception."},
    {q:"Name two ways mass communication contributes to society beyond informing/persuading.", a:"Fosters cultural exchange/social cohesion; promotes civic engagement."},
    {q:"What made the internet's role in the 21st century different from earlier mass media?", a:"It transformed communication broadly and interactively, alongside digital media."},
    {q:"What does this week's material say about the interaction between senders and receivers?", a:"It is a dynamic interaction between senders and receivers of information."},
    {q:"What role does audience interpretation play in the mass communication process?", a:"Audience interpretation and response are integral to the communication process."},
    {q:"What does the Call to Action ask students to create and discuss this week?", a:"A timeline of key milestones in mass communication history, and a discussion on ethical responsibilities of professionals."},
    {q:"Name the two key references cited on the second page of this week's material.", a:"Baran, S.J. & Davis, D.K. (2015) Mass Communication Theory; McQuail, D. (2010) McQuail's Mass Communication Theory."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: critical thinking, media literacy, cultural awareness, communication skills, ethical awareness, research skills."}
      ]
    },
    {
      week: 2,
      topic: "Evolution of Printing",
      mcq: [
    {q:"Printing traces back to which ancient civilisations, per this week's material?", opts:["Mesopotamia and China","Greece and Rome","Egypt and India","Persia and Japan"], a:0},
    {q:"What did Mesopotamians use for imprints on clay or wax?", opts:["Cylinder seals","Movable type","Lithography stones","Offset plates"], a:0},
    {q:"What did cylinder seals in Mesopotamia ensure, per this week's material?", opts:["The authenticity of documents and items, for record-keeping","Faster printing speeds","Colour accuracy","Mass distribution"], a:0},
    {q:"What did woodblock printing in China involve?", opts:["Carving characters or images onto wooden blocks","Using movable metal type","Digital scanning of documents","Lithography on stone"], a:0},
    {q:"How were ink-coated wooden blocks used in early Chinese printing?", opts:["Pressed onto materials like paper or fabric","Melted down for reuse","Used only for sculpture","Buried as historical records"], a:0},
    {q:"What did woodblock printing in China help to do, per this week's material?", opts:["Preserve cultural heritage and share knowledge","Eliminate the need for written records","Replace oral storytelling entirely","Prevent the spread of literature"], a:0},
    {q:"Whose 15th-century movable type press revolutionised the printing process?", opts:["Johannes Gutenberg","James Clerk Maxwell","Claude Shannon","Heinrich Hertz"], a:0},
    {q:"What effect did Gutenberg's press have on book production, per this week's material?", opts:["Made printing faster, more efficient, and reduced production costs","Made books more expensive","Slowed down the spread of ideas","Had no effect on affordability"], a:0},
    {q:"What did the printing press facilitate, beyond book production?", opts:["The spread of ideas, contributing to historical movements","The decline of literacy","The end of oral traditions","Isolation between cultures"], a:0},
    {q:"What spurred innovations like lithography and offset printing, per this week's material?", opts:["Competition in the printing industry","Government regulation alone","A lack of demand for printed material","The invention of the internet"], a:0},
    {q:"What did lithography allow, per this week's material?", opts:["Detailed images and text on flat surfaces","Only black-and-white text printing","3D printed objects","Digital-only publishing"], a:0},
    {q:"What did offset printing improve, per this week's material?", opts:["Print quality and speed, revolutionising mass media","Only the cost of ink","Only the size of newspapers","Nothing significant"], a:0},
    {q:"What have digital printing and the internet done, per this week's material?", opts:["Transformed printing in the digital age","Eliminated all printing entirely","Had no impact on mass media","Only affected photography"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Historical knowledge","Cultural awareness","Creative design","Financial auditing"], a:3},
    {q:"Who wrote \"The Gutenberg Revolution: The Story of a Genius and an Invention that Changed the World,\" a key reference this week?", opts:["Man, J. (2002)","Seiter, E., & Waisbord, S.","Febvre, L., & Martin, H.-J.","Carter, J."], a:0}
      ],
      fib: [
    {q:"Printing traces back to ancient civilisations like Mesopotamia and __________.", a:"China"},
    {q:"Mesopotamians used cylinder __________ for imprints on clay or wax.", a:"seals"},
    {q:"Woodblock printing in China involved carving characters or images on wooden __________.", a:"blocks"},
    {q:"Woodblock printing in China helped preserve cultural heritage and share __________.", a:"knowledge"},
    {q:"Ancient printing made written records more accessible, spreading laws and __________.", a:"literature"},
    {q:"Gutenberg's __________-century movable type press revolutionised the printing process.", a:"15th"},
    {q:"Gutenberg's press made printing faster, more efficient, and reduced production __________.", a:"costs"},
    {q:"Books became more affordable and accessible due to Gutenberg's __________.", a:"press"},
    {q:"Competition in the printing industry spurred innovations like lithography and __________ printing.", a:"offset"},
    {q:"__________ allowed detailed images and text on flat surfaces.", a:"Lithography"},
    {q:"Offset printing improved print quality and speed, revolutionising mass __________.", a:"media"},
    {q:"Consolidation in the industry led to __________ of printing practices.", a:"standardisation"},
    {q:"Digital printing and the internet have transformed printing in the digital __________.", a:"age"},
    {q:"One skill gained this week is __________ design.", a:"creative"},
    {q:"Man, J. (2002) wrote \"The Gutenberg __________: The Story of a Genius and an Invention that Changed the World.\"", a:"Revolution"}
      ],
      short: [
    {q:"Which ancient civilisations does printing trace back to, per this week's material?", a:"Mesopotamia and China."},
    {q:"What did Mesopotamians use cylinder seals for?", a:"Imprints on clay or wax, to authenticate documents and goods, and for record-keeping."},
    {q:"What did woodblock printing in China involve, and what did it help achieve?", a:"Carving characters/images onto wooden blocks, pressed onto paper or fabric; it helped preserve cultural heritage and share knowledge."},
    {q:"What effect did ancient printing methods have on written records, per this week's material?", a:"They made written records more accessible, spreading laws and literature, and facilitated cultural exchange."},
    {q:"Whose press revolutionised printing in the 15th century, and what effect did it have?", a:"Gutenberg's movable type press — it made printing faster, more efficient, reduced production costs, and made books more affordable."},
    {q:"What broader historical effect did the printing press have, beyond book production?", a:"It facilitated the spread of ideas, contributing to historical movements."},
    {q:"What spurred innovations like lithography and offset printing?", a:"Competition in the printing industry."},
    {q:"What did lithography and offset printing each contribute, per this week's material?", a:"Lithography allowed detailed images and text on flat surfaces; offset printing improved print quality and speed, revolutionising mass media."},
    {q:"What has transformed printing in the digital age, per this week's material?", a:"Digital printing and the internet."},
    {q:"What does this week's Call to Action ask students to compare?", a:"The societal impacts of Gutenberg's printing press with those of digital printing technologies, and to investigate printing's role in preserving local cultural heritage."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: historical knowledge, analytical thinking, cultural awareness, technological understanding, creative design, research skills."},
    {q:"What three questions does this week's Personal Reflection raise?", a:"A time printed material influenced your understanding; how life might differ without modern printing; the role of printed materials in preserving cultural heritage."},
    {q:"Name two key references cited this week.", a:"Seiter, E., & Waisbord, S. (2020) The Routledge Handbook of Media and Gender; Man, J. (2002) The Gutenberg Revolution."},
    {q:"What consolidation effect occurred in the printing industry, per this week's material?", a:"It led to standardisation of printing practices."},
    {q:"How did cylinder seals in Mesopotamia contribute to record-keeping and authenticity?", a:"They were used to authenticate documents and goods and ensure accurate record-keeping."}
      ]
    },
    {
      week: 3,
      topic: "Development of Newspapers",
      mcq: [
    {q:"How did newspapers originate, per this week's material?", opts:["As handwritten newsletters in small communities","As digital publications","As government decrees only","As radio transcripts"], a:0},
    {q:"What transformed newspapers into mass-produced publications?", opts:["The printing press in the 15th century","The invention of the telegraph","The internet","Television broadcasting"], a:0},
    {q:"What did early newspapers include, per this week's material?", opts:["Broadsheets and pamphlets","Only digital files","Only radio scripts","Only government bulletins"], a:0},
    {q:"When did the first printed newspapers appear?", opts:["The 17th century","The 12th century","The 20th century","The 21st century"], a:0},
    {q:"Which newspaper marked the beginning of newspapers in Nigeria, and when?", opts:["Lagos Times, in 1880","Daily Times, in 1925","West African Pilot, in 1937","Nigerian Chronicle, in 1901"], a:0},
    {q:"Which newspapers are named as prominent early Nigerian publications?", opts:["Nigerian Chronicle (1901) and Nigerian Pioneer (1914)","Daily Times (1925) only","The Guardian (1983) only","Vanguard (1984) only"], a:0},
    {q:"What did post-independence Nigerian newspapers promote, per this week's material?", opts:["Nationalist ideals and social change","Only colonial interests","Only entertainment content","Only sports coverage"], a:0},
    {q:"Which newspapers were influential in Nigerian journalism, per this week's material?", opts:["The Daily Times (1925) and West African Pilot (1937)","Only the Lagos Times","Only the Nigerian Chronicle","Only foreign-owned papers"], a:0},
    {q:"What characterised Nigerian journalism in the 1980s and 1990s, per this week's material?", opts:["Vibrant investigative journalism","A complete absence of newspapers","Only state-controlled media","A shift entirely to radio"], a:0},
    {q:"What enabled newspapers to publish daily editions in the 19th and 20th centuries?", opts:["Steam-powered printing presses and improved paper manufacturing","Only government funding","Only increased literacy","Only reduced printing costs"], a:0},
    {q:"What does the editorial process of a newspaper involve, per this week's material?", opts:["Journalists sourcing news and editors refining content","Only automated content generation","Only advertising sales","Only distribution logistics"], a:0},
    {q:"What do journalistic ethics focus on, per this week's material?", opts:["Truthfulness, accuracy, objectivity, and impartiality","Maximising advertising revenue only","Publishing speed above all else","Avoiding all investigative reporting"], a:0},
    {q:"What ethical challenges does journalism face, per this week's material?", opts:["Conflicts of interest and privacy concerns","A lack of available news stories","Excessive government support","Too much reader engagement"], a:0},
    {q:"What role do newspapers play in democratic societies, per this week's material?", opts:["Informing and engaging the public","Only generating advertising revenue","Only entertaining readers","Only supporting government policy"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Historical Insight","Editorial Knowledge","Media Literacy","Software Engineering"], a:3}
      ],
      fib: [
    {q:"Newspapers originated as handwritten newsletters in small __________.", a:"communities"},
    {q:"The printing press in the __________ century transformed newspapers into mass-produced publications.", a:"15th"},
    {q:"The first printed newspapers appeared in the __________ century.", a:"17th"},
    {q:"Newspapers in Nigeria began during the colonial era with the Lagos __________ in 1880.", a:"Times"},
    {q:"The Nigerian Chronicle (1901) and the Nigerian __________ (1914) were prominent early Nigerian newspapers.", a:"Pioneer"},
    {q:"Post-independence, Nigerian newspapers promoted __________ ideals and social change.", a:"nationalist"},
    {q:"The Daily Times (1925) and West African __________ (1937) were influential in Nigerian journalism.", a:"Pilot"},
    {q:"The 1980s and 1990s saw vibrant __________ journalism in Nigeria.", a:"investigative"},
    {q:"__________-powered printing presses and improved paper manufacturing enabled frequent publication.", a:"Steam"},
    {q:"The editorial process involves journalists sourcing news and editors __________ content.", a:"refining"},
    {q:"Journalistic ethics focus on truthfulness, accuracy, objectivity, and __________.", a:"impartiality"},
    {q:"__________ and accountability are essential in journalistic practices.", a:"Transparency"},
    {q:"Ethical challenges in journalism include conflicts of interest and __________ concerns.", a:"privacy"},
    {q:"Newspapers play a vital role in democratic societies by informing and __________ the public.", a:"engaging"},
    {q:"One skill gained this week is __________ insight.", a:"historical"}
      ],
      short: [
    {q:"How did newspapers originate, per this week's material?", a:"As handwritten newsletters in small communities."},
    {q:"What transformed newspapers into mass-produced publications, and when did the first printed newspapers appear?", a:"The 15th-century printing press; the first printed newspapers appeared in the 17th century."},
    {q:"Which newspaper marked the beginning of Nigerian newspapers, and when?", a:"The Lagos Times, in 1880."},
    {q:"Name two newspapers influential in Nigerian journalism, per this week's material.", a:"Any 2 of: Nigerian Chronicle (1901), Nigerian Pioneer (1914), Daily Times (1925), West African Pilot (1937)."},
    {q:"What did post-independence Nigerian newspapers promote?", a:"Nationalist ideals and social change."},
    {q:"What characterised Nigerian journalism in the 1980s and 1990s?", a:"Vibrant investigative journalism."},
    {q:"What enabled newspapers to publish daily editions in the 19th and 20th centuries?", a:"Steam-powered printing presses and improved paper manufacturing."},
    {q:"What does the editorial process of a newspaper involve?", a:"Journalists sourcing news and editors refining content, with visual elements designed by layout artists."},
    {q:"What do journalistic ethics focus on, per this week's material?", a:"Truthfulness, accuracy, objectivity, and impartiality, with transparency and accountability as essential."},
    {q:"What ethical challenges does journalism face, per this week's material?", a:"Conflicts of interest and privacy concerns."},
    {q:"What role do newspapers play in democratic societies?", a:"Informing and engaging the public."},
    {q:"What does this week's Call to Action ask students to do?", a:"Organise a debate on ethical challenges journalists face, and keep a journal reflecting on current news articles."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: historical insight, editorial knowledge, ethical understanding, critical thinking, research skills, media literacy."},
    {q:"What three questions does this week's Personal Reflection raise?", a:"A time a newspaper article influenced your opinion; the role of newspapers in your community; and your preference for digital vs. printed newspapers."},
    {q:"Name two key references cited this week.", a:"Kovach, B., & Rosenstiel, T. (2014) The Elements of Journalism; Zinsser, W. (2006) On Writing Well."}
      ]
    },
    {
      week: 4,
      topic: "The Magazine Industry (Emergence and Growth)",
      mcq: [
        {q:"According to the summary, magazines are key platforms for storytelling, information, and what else?", opts:["Scientific research","Legal regulation","Cultural expression","Military strategy"], a:2},
        {q:"Which two 17th-century publications set the precedent for modern magazines with diverse content?", opts:["The Gentleman's Magazine and The Review","The Economist and Vogue","Time and Newsweek","National Geographic and Life"], a:0},
        {q:"What two factors boosted magazine production in the 19th and 20th centuries?", opts:["Advances in printing technology and rising literacy rates","Decline of newspapers and books","Government subsidies and tax breaks","The invention of television and radio"], a:0},
        {q:"What role did magazines play regarding information and entertainment?", opts:["Replacing radio entirely","Restricting access to elite readers only","Eliminating local journalism","Democratising information and entertainment"], a:3},
        {q:"What did investigative journalism in magazines achieve, per the summary?", opts:["Reduced advertising revenue","Discouraged social reform","Exposed corruption and promoted accountability","Increased subscription prices"], a:2},
        {q:"Magazines advocated for social reforms in which areas, according to the text?", opts:["Taxation, trade, and banking regulation","Sports governance only","Civil rights, environmental sustainability, and public health","Military policy only"], a:2},
        {q:"What have fashion magazines influenced, per the summary?", opts:["Agricultural subsidies","Television ratings","Interest rates and monetary policy","Style choices and personal expression"], a:3},
        {q:"What have lifestyle magazines shaped, according to the material?", opts:["Consumer behaviour and daily life decisions","Court rulings","International trade agreements","Radio frequencies"], a:0},
        {q:"What role do magazines serve as, according to the text?", opts:["Political parties","Regulatory bodies for broadcasting","Cultural archives, preserving history and traditions","Licensing authorities"], a:2},
        {q:"What do niche publications cater to, per the summary?", opts:["Specialised interests and foster community among enthusiasts","Mass general audiences exclusively","Advertisers exclusively","Government agencies only"], a:0},
        {q:"What helps publishers tailor content to specific demographics and interests?", opts:["Advertising bans","Printing technology alone","Investigative journalism","Audience segmentation"], a:3},
        {q:"What is described as a crucial revenue source for magazines?", opts:["Newsstand returns","Advertising","Government grants","Subscriptions alone"], a:1},
        {q:"What must publishers balance, per the text?", opts:["Local content with global content","Commercial interests with editorial integrity","Print costs with digital costs","Fashion content with political content"], a:1},
        {q:"Despite digital age challenges, how does the magazine industry fare according to the summary?", opts:["It exists only in print now","It has merged entirely with radio","It continues to thrive","It has completely disappeared"], a:2},
        {q:"Which of the following is listed as a skill/competency for Week 4?", opts:["Research skills","Technological awareness","Audience segmentation","Ethical Awareness"], a:2}
      ],
      fib: [
        {q:"Magazines are key platforms for storytelling, information, and __________.", a:"cultural expression"},
        {q:"Magazines offer in-depth analysis, captivating visuals, and __________.", a:"expert commentary"},
        {q:"Early magazines like __________ and The Review emerged in the 17th century.", a:"The Gentleman's Magazine"},
        {q:"The 19th and __________ centuries saw significant growth in magazine popularity.", a:"20th"},
        {q:"Advances in printing technology and rising __________ rates boosted magazine production.", a:"literacy"},
        {q:"Diverse publications emerged, covering topics from __________ to politics.", a:"fashion"},
        {q:"Magazines played a role in __________ information and entertainment.", a:"democratising"},
        {q:"Investigative journalism in magazines exposed __________ and promoted accountability.", a:"corruption"},
        {q:"Magazines advocated for social reforms in civil rights, environmental sustainability, and __________.", a:"public health"},
        {q:"Fashion magazines influenced __________ choices and personal expression.", a:"style"},
        {q:"Lifestyle magazines shaped consumer behaviour and __________ decisions.", a:"daily life"},
        {q:"Magazines serve as cultural __________, preserving history and traditions.", a:"archives"},
        {q:"Niche publications cater to specialised interests and foster __________ among enthusiasts.", a:"community"},
        {q:"__________ is a crucial revenue source for magazines.", a:"Advertising"},
        {q:"Publishers must balance commercial interests with editorial __________.", a:"integrity"}
      ],
      short: [
        {q:"What are magazines described as key platforms for?", a:"Storytelling, information, and cultural expression."},
        {q:"Name two 17th-century magazines mentioned as pioneering publications.", a:"The Gentleman's Magazine and The Review."},
        {q:"What two factors boosted magazine production in the 19th and 20th centuries?", a:"Advances in printing technology and rising literacy rates."},
        {q:"How did magazines contribute to democratisation, per the summary?", a:"They played a role in democratising information and entertainment."},
        {q:"What did investigative journalism in magazines accomplish?", a:"It exposed corruption and promoted accountability."},
        {q:"List three social reform areas magazines advocated for.", a:"Civil rights, environmental sustainability, and public health."},
        {q:"How have fashion magazines influenced readers?", a:"They influenced style choices and personal expression."},
        {q:"What role do lifestyle magazines play, according to the text?", a:"They shape consumer behaviour and daily life decisions."},
        {q:"In what sense do magazines function as cultural archives?", a:"They preserve history and traditions."},
        {q:"What do niche publications provide for their readers?", a:"They cater to specialised interests and foster community among enthusiasts."},
        {q:"What is audience segmentation used for in the magazine industry?", a:"It helps publishers tailor content to specific demographics and interests."},
        {q:"What is described as a crucial revenue source for magazines?", a:"Advertising."},
        {q:"What tension must publishers manage, per the summary?", a:"Balancing commercial interests with editorial integrity."},
        {q:"Despite digital age challenges, what is the state of the magazine industry?", a:"It continues to thrive."},
        {q:"Name three skills or competencies listed for Week 4.", a:"Critical thinking, content analysis, and historical context (also: audience segmentation, advertising strategies, cultural awareness)."}
      ]
    },
    {
      week: 5,
      topic: "Radio (Early Operations and Development Across Decades)",
      mcq: [
        {q:"Whose late-19th-century experiments are credited with the origins of radio?", opts:["Thomas Edison and Nikola Tesla","Alexander Graham Bell and Samuel Morse","Heinrich Hertz and Guglielmo Marconi","Philo Farnsworth and John Logie Baird"], a:2},
        {q:"Who is known as the \"father of radio\" and invented the Audion vacuum tube?", opts:["Reginald Fessenden","Heinrich Hertz","Lee de Forest","Guglielmo Marconi"], a:2},
        {q:"Whose experiments led to the successful transmission of voice and music over radio waves in 1900?", opts:["Lee de Forest","Heinrich Hertz","Reginald Fessenden","Guglielmo Marconi"], a:2},
        {q:"What was the first commercial radio station, and where did it begin broadcasting in 1920?", opts:["KDKA in Pittsburgh","RCA in Chicago","BBC in London","WABC in New York"], a:0},
        {q:"Which period is known as the \"golden age of radio\"?", opts:["The 1950s and 1960s","The 1890s","The 1920s and 1930s","The 1970s"], a:2},
        {q:"During which events did radio become a central household fixture for entertainment and information?", opts:["World War I and the Spanish Flu","The Industrial Revolution","The Great Depression and World War II","The Cold War and Vietnam War"], a:2},
        {q:"Which innovations are named as following radio post-World War II?", opts:["Television and cable","FM radio, stereo broadcasting, and transistor radios","Satellite radio and podcasts","The internet and streaming"], a:1},
        {q:"What has radio been a potent tool for, particularly in underserved communities and developing regions?", opts:["Military strategy","Stock trading","Sports betting","Education"], a:3},
        {q:"Which subjects do educational radio programmes cover, per the summary?", opts:["Law, finance, and engineering","Art history and music theory","Health, agriculture, literacy, and civic education","Mathematics, physics, and chemistry"], a:2},
        {q:"What issues does radio raise public awareness on, according to the text?", opts:["Stock market trends","Space exploration","International trade policy","Public health, environmental conservation, and human rights"], a:3},
        {q:"What are named as key components of radio programming in the summary?", opts:["Satellite uplinks","Paid subscriptions only","Public service announcements and community outreach initiatives","Closed-caption services"], a:2},
        {q:"What has radio significantly influenced, shaping musical trends and genres?", opts:["Judicial systems","Popular culture","Agricultural policy","Urban planning"], a:1},
        {q:"What did a radio broadcast mentioned in the summary cause by blurring the lines between fiction and reality?", opts:["Widespread panic","A decline in listenership","A government shutdown","Increased literacy"], a:0},
        {q:"What did that incident highlight about media, per the summary?", opts:["The potential dangers of sensationalism and misinformation","The benefits of live broadcasting","The need for more music programming","The importance of advertising"], a:0},
        {q:"What does radio continue to serve as, according to the summary?", opts:["A platform used exclusively for advertising","Primarily a military communication tool","A declining medium with no modern relevance","A primary source of news and information, delivering real-time updates"], a:3}
      ],
      fib: [
        {q:"The origins of radio trace back to the late 19th century with experiments by Heinrich Hertz and __________.", a:"Guglielmo Marconi"},
        {q:"__________, known as the \"father of radio,\" invented the Audion vacuum tube.", a:"Lee de Forest"},
        {q:"Reginald Fessenden's experiments led to the successful transmission of voice and music over radio waves in __________.", a:"1900"},
        {q:"The first commercial radio station, __________, began broadcasting in 1920.", a:"KDKA in Pittsburgh"},
        {q:"The 1920s and 1930s are known as the __________ of radio.", a:"golden age"},
        {q:"Radio became a central fixture in households during the Great Depression and __________.", a:"World War II"},
        {q:"Post-World War II innovations included FM radio, stereo broadcasting, and __________ radios.", a:"transistor"},
        {q:"__________ formats emerged to cater to diverse audience interests and demographics.", a:"Niche"},
        {q:"Radio has been a potent tool for education, particularly in underserved communities and __________.", a:"developing regions"},
        {q:"Educational radio programmes cover subjects such as health, agriculture, literacy, and __________.", a:"civic education"},
        {q:"Radio raises public awareness on issues like public health, environmental conservation, and __________.", a:"human rights"},
        {q:"__________ and community outreach initiatives are key components of radio programming.", a:"Public service announcements"},
        {q:"Radio has significantly influenced popular culture, shaping musical trends and __________.", a:"genres"},
        {q:"The broadcast mentioned in the summary blurred the lines between fiction and __________, causing widespread panic.", a:"reality"},
        {q:"Radio serves as a primary source of news and information, delivering real-time updates and __________.", a:"analysis"}
      ],
      short: [
        {q:"Who conducted the early experiments credited with the origins of radio in the late 19th century?", a:"Heinrich Hertz and Guglielmo Marconi."},
        {q:"What invention is Lee de Forest credited with?", a:"The Audion vacuum tube, which amplified radio signals."},
        {q:"What did Reginald Fessenden's experiments achieve in 1900?", a:"The successful transmission of voice and music over radio waves."},
        {q:"Identify the first commercial radio station and when it began broadcasting.", a:"KDKA in Pittsburgh, which began broadcasting in 1920."},
        {q:"What characterized radio programming during the golden age of radio?", a:"A proliferation of programming including news, music, and dramas."},
        {q:"Why was radio central to households during the Great Depression and World War II?", a:"It provided entertainment and information during those periods."},
        {q:"What technological developments followed radio after World War II?", a:"FM radio, stereo broadcasting, and transistor radios."},
        {q:"What role has radio played in underserved communities and developing regions?", a:"It has been a potent tool for education."},
        {q:"What subjects do educational radio programmes typically cover?", a:"Health, agriculture, literacy, and civic education."},
        {q:"What kinds of public awareness issues does radio address, per the summary?", a:"Public health, environmental conservation, and human rights."},
        {q:"What are two key components of radio programming mentioned in the text?", a:"Public service announcements and community outreach initiatives."},
        {q:"How has radio influenced popular culture?", a:"By shaping musical trends and genres."},
        {q:"What effect did a particular radio broadcast have, according to the summary?", a:"It blurred the lines between fiction and reality, causing widespread panic."},
        {q:"What danger did that incident highlight?", a:"The potential dangers of sensationalism and misinformation in media."},
        {q:"What role does radio continue to serve today, per the summary?", a:"A primary source of news and information, delivering real-time updates and analysis."}
      ]
    },
    {
      week: 6,
      topic: "Evolution of Television Programming",
      mcq: [
        {q:"Who demonstrated the first successful television transmission in the early 1920s?", opts:["Philo Farnsworth","Guglielmo Marconi","John Logie Baird","Vladimir Zworykin"], a:2},
        {q:"Who transmitted the first electronic television image in 1927?", opts:["Lee de Forest","John Logie Baird","Philo Farnsworth","Vladimir Zworykin"], a:2},
        {q:"What two tubes did Vladimir Zworykin invent, advancing TV technology?", opts:["The iconoscope and kinescope","The magnetron and klystron","The cathode and anode","The Audion and triode"], a:0},
        {q:"What characterized early television sets, according to the summary?", opts:["Small screens, limited resolution, and mechanical scanning systems","High-definition colour displays","Large flat screens and digital tuners","Wireless remote controls"], a:0},
        {q:"By what decade had television broadcasting become a reality with regular programming?", opts:["The 1900s","The 1950s","The 1930s","The 1970s"], a:2},
        {q:"What did early television programming include, per the summary?", opts:["Only political debates","Only sitcoms","News, sports, and experimental entertainment","Only advertisements"], a:2},
        {q:"What happened to TV broadcasting after World War II?", opts:["A shift exclusively to radio","A complete shutdown","A decline in viewership","Rapid expansion with technological advancements"], a:3},
        {q:"Which decades mark the golden age of television in the USA?", opts:["The 1980s and 1990s","The 2000s and 2010s","The 1920s and 1930s","The 1950s and 1960s"], a:3},
        {q:"When did television begin in Nigeria, and with which station?", opts:["Early 1920s, with NTA","1977, with NTA","1990s, with WNTV","Late 1950s, with Western Nigeria Television"], a:3},
        {q:"When was the Nigerian Television Authority (NTA) launched?", opts:["1959","1927","1950","1977"], a:3},
        {q:"What does television in Nigeria promote, per the summary?", opts:["Regional division","Military propaganda","Exclusively foreign programming","Cultural diversity and national unity"], a:3},
        {q:"What is described as the primary revenue model for television networks?", opts:["Advertising","Subscription fees exclusively","Government subsidies","Viewer donations"], a:0},
        {q:"What has the rise of digital media led to in television audiences?", opts:["Audience fragmentation","Elimination of advertising","A return to radio","Audience consolidation"], a:0},
        {q:"Which of the following is listed as a future trend in television?", opts:["Mechanical scanning","Vacuum tube amplification","Wireless telegraphy","Virtual reality"], a:3},
        {q:"Which professionals are described as collaborating in TV production?", opts:["Only engineers","Only government regulators","Only advertisers","Writers, directors, producers, and actors"], a:3}
      ],
      fib: [
        {q:"__________ demonstrated the first successful television transmission in the early 1920s.", a:"John Logie Baird"},
        {q:"Philo Farnsworth transmitted the first __________ television image in 1927.", a:"electronic"},
        {q:"Vladimir Zworykin invented the \"iconoscope\" and \"__________\" tubes.", a:"kinescope"},
        {q:"Early television sets featured small screens, limited resolution, and __________ scanning systems.", a:"mechanical"},
        {q:"By the __________, television broadcasting had become a reality with regular programming.", a:"1930s"},
        {q:"Post-WWII saw rapid expansion in TV broadcasting with __________ advancements.", a:"technological"},
        {q:"The 1950s and 1960s marked the __________ of television in the USA.", a:"golden age"},
        {q:"Television in Nigeria began in the late 1950s with __________.", a:"Western Nigeria Television"},
        {q:"The __________ was launched in 1977, expanding TV reach in Nigeria.", a:"Nigerian Television Authority (NTA)"},
        {q:"Television in Nigeria promotes cultural diversity and __________.", a:"national unity"},
        {q:"Television influences popular culture through scripted dramas, sitcoms, and __________.", a:"live events"},
        {q:"__________ is the primary revenue model for television networks.", a:"Advertising"},
        {q:"The rise of digital media has led to audience __________.", a:"fragmentation"},
        {q:"Future trends in TV include interactive programming, virtual reality, and __________ content recommendations.", a:"personalised"},
        {q:"TV production involves collaboration between writers, directors, producers, and __________.", a:"actors"}
      ],
      short: [
        {q:"Who demonstrated the first successful television transmission, and when?", a:"John Logie Baird, in the early 1920s."},
        {q:"What achievement is Philo Farnsworth credited with?", a:"Transmitting the first electronic television image in 1927."},
        {q:"What two technologies did Vladimir Zworykin invent?", a:"The iconoscope and kinescope tubes."},
        {q:"Describe the characteristics of early television sets.", a:"Small screens, limited resolution, and mechanical scanning systems."},
        {q:"By what point had television broadcasting become a reality with regular programming?", a:"By the 1930s."},
        {q:"What did early television programming consist of?", a:"News, sports, and experimental entertainment."},
        {q:"What happened to TV broadcasting after World War II?", a:"Rapid expansion with technological advancements."},
        {q:"What is the golden age of television, and when did it occur?", a:"The 1950s and 1960s in the USA, marked by iconic shows."},
        {q:"When and with which station did television begin in Nigeria?", a:"In the late 1950s, with Western Nigeria Television."},
        {q:"What was launched in 1977 in Nigeria, and what did it do?", a:"The Nigerian Television Authority (NTA), which expanded TV reach."},
        {q:"What does television in Nigeria promote, per the summary?", a:"Cultural diversity and national unity."},
        {q:"What role does TV serve as a conduit for, according to the summary?", a:"Disseminating information, news, and educational content."},
        {q:"Who collaborates in TV production, per the summary?", a:"Writers, directors, producers, and actors."},
        {q:"What is the primary revenue model for television networks?", a:"Advertising."},
        {q:"What are some future trends in television mentioned in the summary?", a:"Interactive programming, virtual reality, and personalised content recommendations."}
      ]
    }
  ]
},
{
  code: "MCM 103",
  title: "Introduction to Advertising",
  weeks: [
    {
      week: 1,
      topic: "Introduction to Advertising",
      mcq: [

    {q:"Which four features define advertising, per this week's summary?", opts:["Free, personal, factual, anonymous","Paid, non-personal, persuasive intent, identified sponsorship","Informal, private, neutral, unsponsored","Regulated, personal, factual, government-owned"], a:1},
    {q:"Which of these is NOT listed as a media channel advertising uses?", opts:["Print","Broadcast","Digital","Personal diaries"], a:3},
    {q:"How did ancient Egyptians and Romans advertise goods and services?", opts:["Through television and radio","Via hieroglyphics, papyrus scrolls, town criers, and handbills","Through email and social media","Only through word of mouth, with no visual materials"], a:1},
    {q:"What did Gutenberg's printing press enable for advertising?", opts:["The decline of print advertising","Mass production of advertisements, including classified and display ads","The end of advertising agencies","A shift entirely to broadcast media"], a:1},
    {q:"What two tools emerged during the later print era, enhancing advertising's visual reach?", opts:["Lithography and photography","Radio jingles and slogans","Digital printing and AI","Social media and mobile apps"], a:0},
    {q:"How did radio and television change advertising, per this week's material?", opts:["They eliminated the need for creative messaging","They offered personal, immersive experiences, enhanced by colour TV","They reduced advertising's reach significantly","They made print advertising obsolete immediately"], a:1},
    {q:"Which of these is NOT listed as a digital-era advertising innovation?", opts:["Search engine marketing","Programmatic advertising","Mobile apps","Cuneiform tablets"], a:3},
    {q:"Which of these is NOT listed as an objective of advertising this week?", opts:["Building brand loyalty","Educating consumers","Eliminating competition through legal means","Creating emotional connections"], a:2},
    {q:"What distinguishes advertising from public relations, per this week's material?", opts:["Advertising has no persuasive intent, unlike PR","Advertising is paid, commercial, and has identified sponsorship; PR does not share these traits","PR is always more expensive than advertising","There is no meaningful distinction between them"], a:1},
    {q:"Which technologies are named as reshaping modern advertising practices?", opts:["Augmented reality, virtual reality, and artificial intelligence","Telegraph and telephone","Cuneiform and papyrus","Radio and print only"], a:0},
    {q:"What does advertising's evolution from ancient practices to digital campaigns reflect, per this week's material?", opts:["A decline in creativity","Adapting to changes in consumer behaviour and technology","A return to purely print media","No meaningful change over time"], a:1},
    {q:"What does this week's Call to Action ask students to explore?", opts:["Only advertisements from one company","Various advertisements around them, on TV, online, in print, or outdoor displays","Only historical advertisements","Only advertisements they created themselves"], a:1},
    {q:"Who wrote \"Advertising, Promotion, and Other Aspects of Integrated Marketing Communications,\" a key reference this week?", opts:["Bovee, C.L.","Shimp, T.A.","Wells, W.D.","Moriarty, S.E."], a:1},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Critical analysis","Strategic thinking","Consumer insight","Structural engineering"], a:3},
    {q:"Besides informing and persuading, what else does advertising do, per this week's summary?", opts:["Eliminates the need for branding","Reminds, reinforces brand image, and generates sales/revenue","Removes all competitor products","Only targets new customers"], a:1}
      ],
      fib: [

    {q:"Advertising is defined by its paid nature, non-personal presentation, persuasive intent, and identified __________.", a:"sponsorship"},
    {q:"Ancient Egyptians and Romans used hieroglyphics, papyrus scrolls, town criers, inscriptions, and __________ to advertise goods and services.", a:"handbills"},
    {q:"The invention of the printing press by __________ allowed mass production of advertisements.", a:"Gutenberg"},
    {q:"The advertising era that followed the printing press saw the emergence of advertising __________, lithography, and photography.", a:"agencies"},
    {q:"__________ commercials and television advertisements transformed advertising by offering personal and immersive experiences.", a:"Radio"},
    {q:"The internet and digital technologies introduced websites, search engine marketing, and __________ advertising.", a:"social media"},
    {q:"Innovations like digital printing, augmented reality, virtual reality, and __________ intelligence have opened new avenues for advertisers.", a:"artificial"},
    {q:"Advertising objectives include promoting awareness, driving sales, building brand __________, and educating consumers.", a:"loyalty"},
    {q:"Advertising differs from public relations through its paid promotion, commercial intent, and identified __________.", a:"sponsorship"},
    {q:"Advertising informs, persuades, __________, reinforces brand image, and generates sales and revenue.", a:"reminds"},
    {q:"Advertising has evolved from ancient practices to sophisticated __________ campaigns.", a:"digital"},
    {q:"This week's Call to Action asks students to explore advertisements around them — on TV, online, in print, or __________ displays.", a:"outdoor"},
    {q:"__________, T.A. (2020) wrote \"Advertising, Promotion, and Other Aspects of Integrated Marketing Communications.\"", a:"Shimp"},
    {q:"One skill gained this week is consumer __________.", a:"insight"},
    {q:"Advertising informs, persuades, reminds, and reinforces brand __________.", a:"image"}
      ],
      short: [

    {q:"What four features define advertising, according to this week's material?", a:"Paid nature, non-personal presentation, persuasive intent, identified sponsorship."},
    {q:"Name three media channels advertising uses to reach audiences.", a:"Any 3 of: print, broadcast, digital, outdoor."},
    {q:"Give two examples of how ancient civilizations advertised goods/services.", a:"Hieroglyphics/papyrus scrolls (Egyptians); town criers/inscriptions/handbills (Romans)."},
    {q:"What did Gutenberg's printing press enable for advertising specifically?", a:"Mass production of advertisements (classified ads, display ads, advertorials)."},
    {q:"What two new tools appeared during the print era's later evolution?", a:"Lithography and photography."},
    {q:"How did radio and TV change the advertising experience for audiences?", a:"Offered personal, immersive experiences, with colour TV enhancing visual appeal."},
    {q:"Name three digital-era innovations that expanded advertising's reach.", a:"Any 3 of: websites, search engine marketing, social media advertising, mobile apps, programmatic advertising."},
    {q:"List four objectives of advertising covered this week.", a:"Any 4 of: promoting awareness, driving sales, building brand loyalty, educating consumers, creating emotional connections, influencing behaviour, differentiating from competitors."},
    {q:"What distinguishes advertising from public relations, per this week's material?", a:"Advertising is paid/commercial with identified sponsorship; PR is not."},
    {q:"Name two emerging technologies reshaping advertising today.", a:"Any 2 of: augmented reality, virtual reality, artificial intelligence."},
    {q:"What does advertising's evolution from ancient practices to digital campaigns reflect?", a:"Adapting to changes in consumer behaviour and technology."},
    {q:"What does this week's Call to Action ask students to do?", a:"Explore various advertisements around them (TV, online, print, outdoor) and analyse their messaging, imagery, and channels."},
    {q:"Name the two key references cited on the second page of this week's material.", a:"Shimp, T.A. (2020) Advertising, Promotion, and Other Aspects of IMC; Wells, Burnett, & Moriarty (2011) Advertising: Principles and Practice."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: critical analysis, media literacy, strategic thinking, communication skills, technological awareness, consumer insight."},
    {q:"Besides informing and persuading, name two other things advertising does per this week's material.", a:"Reminds; reinforces brand image; generates sales and revenue (any two)."}
      ]
    },
    {
      week: 2,
      topic: "History and Development of Advertising Practice in Nigeria",
      mcq: [
    {q:"How did pre-colonial Nigerian societies primarily advertise goods and services?", opts:["Through oral and communal communication","Through television commercials","Through printed newspapers only","Through digital platforms"], a:0},
    {q:"Who played key roles in disseminating information in pre-colonial Nigerian advertising?", opts:["Town criers, griots, and community elders","Television presenters","Newspaper editors","Billboard designers"], a:0},
    {q:"What conveyed persuasive messages in pre-colonial advertising, per this week's material?", opts:["Proverbs, metaphors, and traditional art forms","Digital banners","Radio jingles","Printed slogans"], a:0},
    {q:"What values were paramount in pre-colonial advertising practices?", opts:["Honesty, transparency, and cultural sensitivity","Speed and automation","Profit above all else","Anonymity"], a:0},
    {q:"What did European colonisation introduce to Nigerian advertising?", opts:["Western advertising techniques and ideologies","Only oral storytelling","A complete ban on advertising","Only community fairs"], a:0},
    {q:"What became primary tools for colonial advertising in Nigeria?", opts:["Newspapers, pamphlets, and billboards","Only radio broadcasts","Only television","Only social media"], a:0},
    {q:"What did colonial authorities organise to promote colonial products and ideologies?", opts:["Fairs and exhibitions","Only private meetings","Only court proceedings","Only religious ceremonies"], a:0},
    {q:"What effect did colonial advertising have on indigenous industries, per this week's material?", opts:["It marginalised indigenous industries and traditions, promoting European goods","It strengthened indigenous industries significantly","It had no effect on local trade","It eliminated the need for all advertising"], a:0},
    {q:"What emerged post-independence in Nigerian advertising, per this week's material?", opts:["Nigerian-owned businesses and advertising agencies, reflecting national pride","A complete return to pre-colonial methods only","A ban on all foreign advertising","Only state-controlled advertising"], a:0},
    {q:"What revolutionised advertising practices post-independence, per this week's material?", opts:["Television, radio, and digital media","Only print newspapers","Only billboards","Only oral tradition"], a:0},
    {q:"What do government regulations in Nigerian advertising aim to do?", opts:["Protect consumer interests, ensure fair competition, and promote ethical advertising","Eliminate all advertising entirely","Only benefit large corporations","Restrict advertising to government agencies only"], a:0},
    {q:"Which acts provide the legal framework for advertising standards and practices in Nigeria?", opts:["APCON, NBC, and CPC Acts","Only the Constitution","Only international trade law","Only state-level bylaws"], a:0},
    {q:"Which sectors have additional advertising rules, per this week's material?", opts:["Food and beverages, healthcare, and financial services","Only entertainment","Only education","Only transportation"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Cultural awareness","Historical understanding","Ethical reasoning","Software debugging"], a:3},
    {q:"Who wrote \"History of advertising in Nigeria: A chronicle of advertising practice from 1800 to 2018,\" a key reference this week?", opts:["Okoro, J.O.","Akinbode, M.A.","Adirika, E.O.","Nwosu, O.I."], a:0}
      ],
      fib: [
    {q:"In the pre-colonial era, indigenous Nigerian societies relied on oral and __________ communication for advertising.", a:"communal"},
    {q:"Town criers, griots, and community __________ played key roles in disseminating information.", a:"elders"},
    {q:"Language and symbolism such as proverbs, metaphors, and traditional art forms conveyed __________ messages.", a:"persuasive"},
    {q:"Ethics such as honesty, transparency, and cultural __________ were paramount in pre-colonial advertising.", a:"sensitivity"},
    {q:"European __________ introduced Western advertising techniques and ideologies.", a:"colonisation"},
    {q:"Newspapers, pamphlets, and __________ became primary tools for colonial advertising.", a:"billboards"},
    {q:"Colonial authorities organised fairs and __________ to promote colonial products.", a:"exhibitions"},
    {q:"Colonial advertising __________ indigenous industries and traditions, promoting European goods.", a:"marginalised"},
    {q:"Post-independence, Nigerian-owned businesses and advertising agencies emerged, reflecting national pride and __________.", a:"identity"},
    {q:"Television, radio, and digital media __________ advertising practices.", a:"revolutionised"},
    {q:"Regulations protect consumer interests, ensure fair competition, and promote __________ advertising.", a:"ethical"},
    {q:"__________, NBC, and CPC Acts provide the legal framework for advertising standards in Nigeria.", a:"APCON"},
    {q:"Additional rules govern advertising in food and beverages, __________, and financial services.", a:"healthcare"},
    {q:"One skill gained this week is __________ reasoning.", a:"ethical"},
    {q:"Okoro, J.O. (2018) wrote \"History of advertising in Nigeria: A chronicle of advertising practice from 1800 to __________.\"", a:"2018"}
      ],
      short: [
    {q:"How did pre-colonial Nigerian societies primarily advertise goods and services?", a:"Through oral and communal communication, including town criers, griots, and community elders."},
    {q:"What conveyed persuasive messages in pre-colonial advertising?", a:"Language and symbolism such as proverbs, metaphors, and traditional art forms."},
    {q:"What values were paramount in pre-colonial advertising practices?", a:"Honesty, transparency, and cultural sensitivity."},
    {q:"What did European colonisation introduce to Nigerian advertising, and what tools emerged?", a:"Western advertising techniques and ideologies; newspapers, pamphlets, and billboards became primary tools."},
    {q:"What effect did colonial advertising have on indigenous industries?", a:"It marginalised indigenous industries and traditions, promoting European goods and lifestyles."},
    {q:"What emerged in Nigerian advertising post-independence?", a:"Nigerian-owned businesses and advertising agencies, reflecting national pride and identity."},
    {q:"What revolutionised advertising practices post-independence?", a:"Television, radio, and digital media."},
    {q:"What do Nigerian government regulations in advertising aim to achieve?", a:"Protect consumer interests, ensure fair competition, and promote ethical advertising."},
    {q:"Which acts provide the legal framework for advertising standards in Nigeria?", a:"APCON, NBC, and CPC Acts."},
    {q:"Which sectors have additional advertising rules, per this week's material?", a:"Food and beverages, healthcare, and financial services."},
    {q:"What does this week's Call to Action ask students to do?", a:"Analyse contemporary advertisements, noting how they reflect or deviate from traditional, colonial, and post-independence practices."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: cultural awareness, historical understanding, critical thinking, media literacy, ethical reasoning, analytical skills."},
    {q:"What three questions does this week's Personal Reflection raise?", a:"Reflecting on a childhood advertisement; the impact of colonial advertising on cultural identity; and a culturally authentic advertisement that resonated."},
    {q:"Name two key references cited this week.", a:"Akinbode, M.A. (2017) Colonialism and Advertising in Nigeria; Okoro, J.O. (2018) History of Advertising in Nigeria."},
    {q:"How did pre-colonial Nigerian advertising involve collaboration?", a:"It was a collaborative effort involving producers, traders, and consumers for communal engagement."}
      ]
    },
    {
      week: 3,
      topic: "Principles and Tenets of Advertising",
      mcq: [
    {q:"What does advertising require, per this week's material?", opts:["Strategic thinking and creativity","Only a large budget","Only celebrity endorsements","Only legal compliance"], a:0},
    {q:"What does the AIDA model stand for?", opts:["Attention, Interest, Desire, Action","Awareness, Impact, Design, Analysis","Attraction, Information, Direction, Appeal","Audience, Idea, Distribution, Advertising"], a:0},
    {q:"What is the first step in the AIDA model?", opts:["Attention: capturing the audience's interest","Action: encouraging a purchase","Desire: creating a want","Interest: maintaining engagement"], a:0},
    {q:"How is \"Interest\" maintained in the AIDA model, per this week's material?", opts:["Through engaging and relevant content","Through repetition alone","Through discounts only","Through legal disclaimers"], a:0},
    {q:"What does the \"Desire\" stage of AIDA involve?", opts:["Creating a strong need or want for the product","Finalising the purchase","Capturing initial attention","Measuring ad performance"], a:0},
    {q:"What does the \"Action\" stage of AIDA encourage?", opts:["The audience to take the final step, such as purchasing","Only awareness of the brand","Only social media engagement","Only brand recall"], a:0},
    {q:"What is key to ensuring advertisements are seen by the target audience?", opts:["Visibility","Only low cost","Only humour","Only length"], a:0},
    {q:"What does \"Relevance\" in advertising refer to, per this week's material?", opts:["Tailoring the message to resonate with the audience","Using the cheapest media channel","Avoiding all target audience research","Only using text, no images"], a:0},
    {q:"What does \"Credibility\" ensure in advertising?", opts:["That the audience trusts the message and the brand","That the ad is the shortest possible","That the ad uses the most colours","That the ad avoids all data"], a:0},
    {q:"What does consistency in messaging strengthen, per this week's material?", opts:["Brand identity and recall","Only short-term sales","Only production costs","Only legal compliance"], a:0},
    {q:"What does a Call to Action (CTA) in advertising prompt?", opts:["Immediate audience response","Only long-term brand loyalty","Only legal review","Only internal company feedback"], a:0},
    {q:"Which brands are given as examples of successful advertising, per this week's material?", opts:["Apple and Coca-Cola","Only local Nigerian brands","Only tech startups","Only food brands"], a:0},
    {q:"What do digital platforms enhance, per this week's material?", opts:["Visibility and engagement through targeted ads","Only production costs","Only legal compliance","Only employee training"], a:0},
    {q:"What does social proof, like testimonials, boost in advertising?", opts:["Credibility and trust","Only entertainment value","Only production speed","Only cost efficiency"], a:0},
    {q:"What does measurement and analysis of ad performance inform, per this week's material?", opts:["Future strategies","Only legal disputes","Only employee salaries","Only office locations"], a:0}
      ],
      fib: [
    {q:"Advertising is a complex field requiring strategic thinking and __________.", a:"creativity"},
    {q:"The AIDA model stands for Attention, Interest, Desire, and __________.", a:"Action"},
    {q:"The first step in the AIDA model is __________: capturing the audience's interest.", a:"Attention"},
    {q:"The \"Desire\" stage of AIDA involves creating a strong need or __________ for the product.", a:"want"},
    {q:"The \"Action\" stage encourages the audience to take the final step, such as __________.", a:"purchasing"},
    {q:"__________ is key to ensuring advertisements are seen by the target audience.", a:"Visibility"},
    {q:"__________ is about tailoring the message to resonate with the audience.", a:"Relevance"},
    {q:"__________ ensures the audience trusts the message and the brand.", a:"Credibility"},
    {q:"__________ in messaging strengthens brand identity and recall.", a:"Consistency"},
    {q:"A Call to Action prompts __________ audience response.", a:"immediate"},
    {q:"Examples of successful ads include those by Apple and __________.", a:"Coca-Cola"},
    {q:"__________ platforms enhance visibility and engagement through targeted ads.", a:"Digital"},
    {q:"Social proof, like __________, boosts credibility and trust.", a:"testimonials"},
    {q:"Measurement and analysis of ad performance inform future __________.", a:"strategies"},
    {q:"This week's Call to Action invites students to create their own ad using the __________ model.", a:"AIDA"}
      ],
      short: [
    {q:"What are the four stages of the AIDA model, and why are they important in advertising?", a:"Attention, Interest, Desire, Action — they guide an audience from noticing an ad through to taking a purchasing action."},
    {q:"Explain the \"Attention\" and \"Interest\" stages of AIDA.", a:"Attention is capturing the audience's interest as the first step; Interest is maintaining that attention through engaging, relevant content."},
    {q:"Explain the \"Desire\" and \"Action\" stages of AIDA.", a:"Desire is creating a strong need or want for the product; Action is encouraging the audience to take the final step, such as purchasing."},
    {q:"How does visibility impact the effectiveness of an advertisement?", a:"Visibility is key to ensuring advertisements are seen by the target audience at all."},
    {q:"In what ways can an advertisement ensure its message is credible?", a:"By building trust through consistency, honesty, and social proof like testimonials."},
    {q:"Why is consistency important in advertising, and how can it be achieved?", a:"It strengthens brand identity and recall; achieved through consistent messaging across campaigns and platforms."},
    {q:"What does a Call to Action (CTA) do in an advertisement?", a:"Prompts an immediate audience response."},
    {q:"Name two brands given as examples of successful advertising this week.", a:"Apple and Coca-Cola."},
    {q:"How do digital platforms enhance advertising, per this week's material?", a:"They enhance visibility and engagement through targeted ads."},
    {q:"What role does social proof play in advertising?", a:"It boosts credibility and trust, for example through testimonials."},
    {q:"Why is measurement and analysis of ad performance important?", a:"It informs future advertising strategies."},
    {q:"What does this week's Call to Action offer as two project options?", a:"Create Your Own Ad using the AIDA model, OR conduct a Brand Trust Survey among peers."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: strategic thinking, creative development, audience analysis, brand positioning, performance measurement, effective communication."},
    {q:"What three questions does this week's Personal Reflection raise?", a:"A brand you trust and its advertising's role; whether you've acted on a CTA; and an ad you found irrelevant or unappealing."},
    {q:"Name two key references cited this week.", a:"Johnson, A.B., & Brown, C.D. (2019) The role of branding in advertising effectiveness; Jones, Smith, & Williams (2021) Strategies for effective brand positioning."}
      ]
    },
    {
      week: 4,
      topic: "Advertising in Marketing Mix",
      mcq: [
        {q:"What four components make up the marketing mix (4Ps)?", opts:["Product, Price, Place, Promotion","Product, Price, Process, Promotion","People, Price, Place, Promotion","Product, Profit, Place, Promotion"], a:0},
        {q:"Who originally developed the marketing mix concept?", opts:["E. Jerome McCarthy","Neil Borden","David Ogilvy","Philip Kotler"], a:1},
        {q:"Who popularised the 4Ps framework in the 1960s?", opts:["Gary Armstrong","E. Jerome McCarthy","Richard Lavidge","Neil Borden"], a:1},
        {q:"Which of the following best describes the Product component of the marketing mix?", opts:["Only distribution channels","Only tangible physical goods","Only pricing strategies","Tangible goods, intangible services, experiences, and ideas"], a:3},
        {q:"Which of the following is NOT listed as a factor influencing pricing decisions?", opts:["Costs","Perceived value","Competitor pricing","Employee training budgets"], a:3},
        {q:"The Place component of the marketing mix involves which of the following?", opts:["Product design and packaging only","Distribution channels, logistics, inventory management, and retailing","Personal selling and public relations","Advertising and sales promotions"], a:1},
        {q:"Which of these is included in the Promotion component of the marketing mix?", opts:["Inventory management","Public relations","Distribution logistics","Demand elasticity"], a:1},
        {q:"According to the summary, what is central to the Promotion component, shaping brand personality and driving sales?", opts:["Demand elasticity","Inventory management","Pricing strategy","Advertising"], a:3},
        {q:"Which promotion element provides direct, personalised interaction with potential customers?", opts:["Above the Line advertising","Personal selling","Public relations","Sales promotion"], a:1},
        {q:"What is the purpose of sales promotion activities, per the summary?", opts:["To manage distribution logistics","To manage company reputation","To incentivise purchases and spur short-term sales","To set product prices"], a:2},
        {q:"Public relations, as described in the summary, manages company reputation and image through which means?", opts:["Media relations and community engagement","Discount pricing and coupons","Personal selling visits","Inventory control systems"], a:0},
        {q:"Above the Line (ATL) advertising is best described as:", opts:["Direct one-on-one sales interactions","Inventory and logistics management","Targeted, personalised communication channels","Use of mass media to reach broad audiences"], a:3},
        {q:"Below the Line (BTL) advertising focuses on:", opts:["Distribution channel management","Long-term brand awareness only","Mass media campaigns for broad reach","Targeted, personalised communication channels"], a:3},
        {q:"Which type of advertising is described as building brand awareness?", opts:["BTL advertising","Personal selling","Sales promotion","ATL advertising"], a:3},
        {q:"Which type of advertising is described as driving immediate responses and deeper engagement?", opts:["Personal selling","Public relations","BTL advertising","ATL advertising"], a:2}
      ],
      fib: [
        {q:"The marketing mix is also known as the __________ framework.", a:"4Ps"},
        {q:"The marketing mix concept was developed by __________.", a:"Neil Borden"},
        {q:"The 4Ps framework was popularised by __________ in the 1960s.", a:"E. Jerome McCarthy"},
        {q:"The four components of the marketing mix are Product, Price, __________, and Promotion.", a:"Place"},
        {q:"Product includes tangible goods, intangible services, experiences, and __________.", a:"ideas"},
        {q:"Pricing decisions are influenced by costs, competitor pricing, perceived value, and __________.", a:"demand elasticity"},
        {q:"Place involves distribution channels, logistics, inventory management, and __________.", a:"retailing"},
        {q:"Promotion includes advertising, sales promotions, public relations, direct marketing, and __________.", a:"personal selling"},
        {q:"__________ is central to the Promotion component, shaping brand personality and driving sales.", a:"Advertising"},
        {q:"__________ provides direct, personalised interaction with potential customers.", a:"Personal selling"},
        {q:"Sales promotion activities incentivise purchases and spur __________ sales.", a:"short-term"},
        {q:"Public relations manage company reputation and image through media relations and __________ engagement.", a:"community"},
        {q:"__________ advertising uses mass media to reach broad audiences.", a:"Above the Line (ATL)"},
        {q:"__________ advertising focuses on targeted, personalised communication channels.", a:"Below the Line (BTL)"},
        {q:"ATL advertising builds brand awareness, while BTL advertising drives __________ responses and deeper engagement.", a:"immediate"}
      ],
      short: [
        {q:"What is the marketing mix, and what are its four components?", a:"The marketing mix is a core marketing strategy concept, also known as the 4Ps framework, made up of Product, Price, Place, and Promotion."},
        {q:"Who developed the marketing mix concept and who popularised it, and when?", a:"It was developed by Neil Borden and popularised by E. Jerome McCarthy in the 1960s."},
        {q:"What four types of offerings fall under the Product component?", a:"Tangible goods, intangible services, experiences, and ideas."},
        {q:"Name four factors that influence pricing decisions.", a:"Costs, competitor pricing, perceived value, and demand elasticity."},
        {q:"What activities fall under the Place component of the marketing mix?", a:"Distribution channels, logistics, inventory management, and retailing."},
        {q:"List the five elements included in Promotion.", a:"Advertising, sales promotions, public relations, direct marketing, and personal selling."},
        {q:"How does advertising relate to the Promotion component?", a:"Advertising is central to the Promotion component, shaping brand personality and driving sales."},
        {q:"In what ways does advertising interact with other elements of the marketing mix?", a:"Advertising interacts with product development, pricing, and distribution strategies."},
        {q:"What role does personal selling play in marketing?", a:"It provides direct, personalised interaction with potential customers."},
        {q:"What is the purpose of sales promotion activities?", a:"To incentivise purchases and spur short-term sales."},
        {q:"What does public relations aim to manage, and how?", a:"It manages company reputation and image through media relations and community engagement."},
        {q:"Define Above the Line (ATL) advertising.", a:"Advertising that uses mass media to reach broad audiences."},
        {q:"Define Below the Line (BTL) advertising.", a:"Advertising that focuses on targeted, personalised communication channels."},
        {q:"What is the key difference in impact between ATL and BTL advertising?", a:"ATL advertising builds brand awareness, while BTL advertising drives immediate responses and deeper engagement."},
        {q:"Name two skills or competencies students should acquire from studying this week's lesson.", a:"Any two of: Strategic thinking, Creative communication, Market analysis, Brand management, Customer engagement, Integrated marketing."}
      ]
    },
    {
      week: 5,
      topic: "Theories of Advertising",
      mcq: [
        {q:"According to the summary, what is advertising fundamentally about?", opts:["Managing distribution logistics","Setting legal regulations","Persuading consumers","Reducing production costs"], a:2},
        {q:"What do advertising theories provide, according to the summary?", opts:["Government tax regulations","Legal guidelines for advertisers","Frameworks for predicting consumer responses to advertising","Manufacturing cost estimates"], a:2},
        {q:"The Hierarchy of Effects Model outlines:", opts:["Stages of product manufacturing","Stages from awareness to purchase","Steps for setting advertising budgets","Legal stages of contract formation"], a:1},
        {q:"What does the Elaboration Likelihood Model (ELM) explain?", opts:["Stages of product distribution","Central and peripheral routes to persuasion","Stages of brand bankruptcy","Pricing elasticity of demand"], a:1},
        {q:"What does the AIDA Model focus on?", opts:["Awareness, Intent, Desire, Approval","Attention, Intent, Desire, Approval","Awareness, Interest, Decision, Action","Attention, Interest, Desire, Action"], a:3},
        {q:"Cognitive Dissonance Theory addresses:", opts:["The structure of distribution channels","The pricing of luxury goods","The need for internal consistency in consumer beliefs and actions","The stages of product development"], a:2},
        {q:"Social Learning Theory emphasises:", opts:["Observational learning and modeling in shaping consumer behaviour","Pricing elasticity","Inventory management techniques","Legal compliance in advertising"], a:0},
        {q:"What does the Reciprocity Principle leverage?", opts:["Fear of missing out on limited offers","The sense of obligation when consumers receive something of value","Conformity to popular opinion","Testimonials from celebrities"], a:1},
        {q:"The Scarcity Principle drives consumer urgency by:", opts:["Using celebrity endorsements","Encouraging social conformity","Offering free gifts","Highlighting limited availability"], a:3},
        {q:"Social Proof relies on which of the following to build credibility?", opts:["Credible expert sources only","Testimonials and endorsements","Limited-time discounts","Initial small commitments"], a:1},
        {q:"The Authority Principle influences consumer behaviour by:", opts:["Highlighting product scarcity","Encouraging reciprocal favours","Using credible sources","Leveraging popularity"], a:2},
        {q:"The Consistency Principle works by:", opts:["Highlighting limited availability","Appealing to relatability","Using testimonials from customers","Leveraging initial commitments to drive larger actions"], a:3},
        {q:"The Liking Principle enhances consumer receptivity through:", opts:["Relatability and positive emotions","Expert authority","Fear of scarcity","Social conformity"], a:0},
        {q:"The Consensus Principle encourages conformity by:", opts:["Citing credible authorities","Using scarcity tactics","Offering reciprocal gifts","Highlighting popularity and widespread adoption"], a:3},
        {q:"Who wrote \"Influence: The psychology of persuasion\" (1984), cited as a key reference for Week 5?", opts:["Albert Bandura","Leon Festinger","Robert B. Cialdini","Richard Petty"], a:2}
      ],
      fib: [
        {q:"Advertising is fundamentally about __________ consumers.", a:"persuading"},
        {q:"Advertising theories provide frameworks for __________ consumer responses to advertising.", a:"predicting"},
        {q:"The __________ Model outlines stages from awareness to purchase.", a:"Hierarchy of Effects"},
        {q:"The Elaboration Likelihood Model explains __________ and peripheral routes to persuasion.", a:"central"},
        {q:"The AIDA Model focuses on capturing attention, generating interest, stimulating desire, and prompting __________.", a:"action"},
        {q:"__________ Dissonance Theory addresses the need for internal consistency in consumer beliefs and actions.", a:"Cognitive"},
        {q:"__________ Learning Theory emphasises observational learning and modeling in shaping consumer behaviour.", a:"Social"},
        {q:"The __________ Principle leverages the sense of obligation when consumers receive something of value.", a:"Reciprocity"},
        {q:"The __________ Principle drives urgency by highlighting limited availability.", a:"Scarcity"},
        {q:"__________ relies on testimonials and endorsements to build credibility.", a:"Social Proof"},
        {q:"The __________ Principle uses credible sources to influence consumer behaviour.", a:"Authority"},
        {q:"The __________ Principle leverages initial commitments to drive larger actions.", a:"Consistency"},
        {q:"The __________ Principle enhances receptivity through relatability and positive emotions.", a:"Liking"},
        {q:"The __________ Principle encourages conformity by highlighting popularity and widespread adoption.", a:"Consensus"},
        {q:"Bandura's 1977 work introduced __________ Theory.", a:"Social Learning"}
      ],
      short: [
        {q:"Why is understanding consumer behaviour important to advertising?", a:"Advertising is about persuading consumers, and this involves understanding consumer behaviour so that responses to advertising can be predicted."},
        {q:"What role do advertising theories play in guiding resource allocation?", a:"They help distill meaningful insights from consumer data, which guides resource allocation."},
        {q:"Describe the stages outlined by the Hierarchy of Effects Model.", a:"It outlines stages from awareness to purchase."},
        {q:"Explain the central and peripheral routes to persuasion in the Elaboration Likelihood Model.", a:"The Elaboration Likelihood Model (ELM) explains that persuasion can occur through a central route or a peripheral route."},
        {q:"What are the four stages of the AIDA Model?", a:"Attention, Interest, Desire, and Action."},
        {q:"How does Cognitive Dissonance Theory relate to post-purchase consumer behaviour?", a:"It addresses the need for internal consistency in consumer beliefs and actions, which relates to resolving doubts after a purchase."},
        {q:"Explain Social Learning Theory and its relevance to advertising.", a:"Social Learning Theory emphasises observational learning and modeling in shaping consumer behaviour."},
        {q:"Describe how the Reciprocity Principle can be used in an advertising campaign.", a:"It leverages the sense of obligation consumers feel when they receive something of value."},
        {q:"How does the Scarcity Principle create urgency in consumers?", a:"By highlighting limited availability of a product or offer."},
        {q:"How does Social Proof build credibility for a brand?", a:"It relies on testimonials and endorsements to build credibility."},
        {q:"How does the Authority Principle influence consumer behaviour?", a:"It uses credible sources to influence consumer behaviour."},
        {q:"Explain how the Consistency Principle drives larger consumer commitments.", a:"It leverages initial, smaller commitments to drive larger actions later."},
        {q:"How does the Liking Principle affect consumer receptivity?", a:"It enhances receptivity through relatability and positive emotions."},
        {q:"How does the Consensus Principle encourage conformity among consumers?", a:"By highlighting popularity and widespread adoption of a product or behaviour."},
        {q:"Name two skills or competencies students should acquire from studying this week's lesson.", a:"Any two of: Critical Analysis, Media Literacy, Strategic Thinking, Communication Skills, Technological Awareness, Consumer Insight."}
      ]
    },
    {
      week: 6,
      topic: "Development of Advertising Agencies in Nigeria",
      mcq: [
        {q:"What societal transition set the stage for early advertising agencies in Nigeria?", opts:["The merger of regional broadcasting stations","The shift from a colonial to a federal government","The transition from an agrarian society to an urbanised and industrialised nation","The adoption of a new national currency"], a:2},
        {q:"What did urbanisation prompt Nigerian businesses to do?", opts:["Reduce advertising spend","Relocate factories to rural areas","Seek effective ways to reach growing urban populations","Focus solely on export markets"], a:2},
        {q:"Which cities are named as key commercial hubs that drove demand for advertising services?", opts:["Abuja, Kano, and Enugu","Kaduna, Sokoto, and Warri","Benin City, Jos, and Calabar","Lagos, Ibadan, and Port Harcourt"], a:3},
        {q:"How did industrialisation affect Nigeria's economy, according to the summary?", opts:["It diversified the economy, creating a need for advertising to market new products and services","It eliminated foreign investment","It reduced the need for advertising","It centralised all advertising in government hands"], a:0},
        {q:"What event in 1960 spurred industrial growth and boosted Nigeria's advertising sector?", opts:["The creation of Troyka Holdings","Nigeria's independence","The founding of Lintas","The opening of the Lagos port"], a:1},
        {q:"What did globalisation require of Nigerian advertising agencies, per the summary?", opts:["Sophisticated advertising strategies to navigate international markets and cross-cultural communication","Reduced creative investment","Simpler, local-only strategies","A ban on foreign advertising"], a:0},
        {q:"Which early agency is described as having played a pivotal role in shaping Nigeria's advertising landscape?", opts:["Troyka Holdings","STB McCann","Lintas","Promasidor"], a:2},
        {q:"Lintas is credited with setting high standards for:", opts:["Television broadcast licensing","Agricultural product pricing","Creativity and professionalism in consumer goods advertising","Government regulation of advertising"], a:2},
        {q:"Which agency is described as contributing significantly to Nigerian advertising through its global network and creative strategies?", opts:["STB McCann","Insight Communications","Rosabel Leo Burnett","TBWA\\Concept"], a:2},
        {q:"Who founded Insight Communications?", opts:["Steve Babaeko","Biodun Shobanjo","Kelechi Nwosu","Jimi Awosika"], a:3},
        {q:"Which company became a household name in Nigeria through its innovative advertising, according to the summary?", opts:["Rosabel Leo Burnett","Promasidor","Troyka Holdings","Lintas"], a:1},
        {q:"Who leads TBWA\\Concept, recognised for its creative excellence?", opts:["Jimi Awosika","Biodun Shobanjo","Steve Babaeko","Kelechi Nwosu"], a:3},
        {q:"Who leads Troyka Holdings, described as an influential conglomerate in advertising?", opts:["Kelechi Nwosu","Jimi Awosika","Steve Babaeko","Biodun Shobanjo"], a:3},
        {q:"Who founded STB McCann?", opts:["Jimi Awosika","Biodun Shobanjo","Kelechi Nwosu","Steve Babaeko"], a:3},
        {q:"What did advertising agencies help Nigerian businesses do as the country integrated into the global economy?", opts:["Reduce reliance on local commercial hubs","Avoid international trade","Navigate international markets and cross-cultural communication","Eliminate competition from foreign brands"], a:2}
      ],
      fib: [
        {q:"Nigeria's transition from an agrarian society to an __________ and industrialised nation set the stage for early advertising agencies.", a:"urbanised"},
        {q:"Urbanisation prompted businesses to seek effective ways to reach growing __________ populations.", a:"urban"},
        {q:"Lagos, Ibadan, and __________ became key commercial hubs, driving demand for advertising services.", a:"Port Harcourt"},
        {q:"__________ diversified Nigeria's economy, creating a need for advertising to market new products and services.", a:"Industrialisation"},
        {q:"Independence in __________ spurred industrial growth, further boosting the advertising sector.", a:"1960"},
        {q:"__________ integrated Nigeria into the global economy, requiring sophisticated advertising strategies.", a:"Globalisation"},
        {q:"Advertising agencies helped businesses navigate international markets and __________ communication.", a:"cross-cultural"},
        {q:"__________ played a pivotal role in shaping Nigeria's advertising landscape among early agencies.", a:"Lintas"},
        {q:"Lintas set high standards for creativity and professionalism in __________ advertising.", a:"consumer goods"},
        {q:"__________ contributed significantly to Nigerian advertising with its global network and creative strategies.", a:"Rosabel Leo Burnett"},
        {q:"Insight Communications was founded by __________.", a:"Jimi Awosika"},
        {q:"__________'s innovative advertising made it a household name in Nigeria.", a:"Promasidor"},
        {q:"TBWA\\Concept, under __________, gained recognition for its creative excellence.", a:"Kelechi Nwosu"},
        {q:"Troyka Holdings, led by __________, became an influential conglomerate in advertising.", a:"Biodun Shobanjo"},
        {q:"STB McCann, founded by __________, made a significant impact with strategic planning and creative execution.", a:"Steve Babaeko"}
      ],
      short: [
        {q:"How did Nigeria's transition from an agrarian to an urbanised and industrialised society set the stage for advertising agencies?", a:"This transition created the conditions, including growing urban populations and new commercial hubs, for early advertising agencies to emerge."},
        {q:"Why did urbanisation increase demand for advertising services?", a:"Urbanisation prompted businesses to seek effective ways to reach growing urban populations, increasing demand for advertising services."},
        {q:"Which Nigerian cities became key commercial hubs for advertising, and why?", a:"Lagos, Ibadan, and Port Harcourt, because they became key commercial hubs driving demand for advertising services."},
        {q:"How did industrialisation influence the advertising sector in Nigeria?", a:"Industrialisation diversified Nigeria's economy, creating a need for advertising to market new products and services."},
        {q:"How did Nigeria's independence in 1960 affect the advertising industry?", a:"Independence in 1960 spurred industrial growth, which further boosted the advertising sector."},
        {q:"How did globalisation shape the strategies used by Nigerian advertising agencies?", a:"Globalisation integrated Nigeria into the global economy, requiring more sophisticated advertising strategies and helping agencies navigate international markets and cross-cultural communication."},
        {q:"What role did Lintas play in Nigeria's advertising history?", a:"Lintas was an early agency that played a pivotal role in shaping Nigeria's advertising landscape, setting high standards for creativity and professionalism in consumer goods advertising."},
        {q:"Describe the contribution of Rosabel Leo Burnett to Nigerian advertising.", a:"Rosabel Leo Burnett contributed significantly to Nigerian advertising with its global network and creative strategies."},
        {q:"Who founded Insight Communications, and what is it known for?", a:"It was founded by Jimi Awosika and is known for impactful campaigns."},
        {q:"What made Promasidor notable in the context of Nigerian advertising?", a:"Promasidor's innovative advertising made it a household name in Nigeria."},
        {q:"What is TBWA\\Concept known for, and who leads it?", a:"It is known for creative excellence and is led by Kelechi Nwosu."},
        {q:"Describe Biodun Shobanjo's role at Troyka Holdings.", a:"Biodun Shobanjo leads Troyka Holdings, which became an influential conglomerate in advertising."},
        {q:"Who founded STB McCann, and what did the agency contribute?", a:"STB McCann was founded by Steve Babaeko, and it made a significant impact with strategic planning and creative execution."},
        {q:"Name two skills or competencies associated with this week's lesson.", a:"Any two of: Critical Analysis, Media Literacy, Strategic Thinking, Creative Communication, Technological Awareness, Consumer Insight."},
        {q:"What does the Week 6 call to action ask students to do?", a:"Identify and analyse three advertisements from different time periods in Nigeria, and consider how the strategies and messages have evolved."}
      ]
    }
  ]
},
{
  code: "MCM 105",
  title: "Introduction to Book Publishing",
  weeks: [
    {
      week: 1,
      topic: "Introduction to Publishing",
      mcq: [

    {q:"What is the key distinction between printing and publishing, per this week's material?", opts:["They are identical processes","Printing = producing physical copies; publishing = the entire process from manuscript to distribution","Printing only applies to digital books","Publishing refers only to marketing"], a:1},
    {q:"Which of these is NOT listed as part of the publishing process?", opts:["Seeking manuscripts","Editing","Designing","Manufacturing printing presses"], a:3},
    {q:"What common misconception does this week's material correct?", opts:["That publishing requires no editing","That publishing is the same as printing or writing","That publishing is always free for authors","That publishing only applies to fiction"], a:1},
    {q:"How is writing distinguished from publishing this week?", opts:["Writing is business-oriented; publishing is artistic","Writing is an artistic endeavour; publishing is business-oriented, involving editing and marketing","They are described as identical activities","Writing requires a contract; publishing does not"], a:1},
    {q:"What does a publishing contract typically establish, per this week's material?", opts:["Nothing legally binding","A contractual agreement between publisher and author","Only the author's royalty-free obligations","The publisher's ownership of unrelated future works"], a:1},
    {q:"How does self-publishing differ from traditional publishing, per this material?", opts:["It offers authors more control over the process","It eliminates the need for editing entirely","It is described as identical to traditional publishing","It cannot produce market-ready products"], a:0},
    {q:"Besides books, what other materials can publishing produce, per this week's summary?", opts:["Films and magazines","Only academic journals","Only newspapers","Nothing besides books"], a:0},
    {q:"Which of these is listed as a societal contribution of publishing?", opts:["Preserving culture and advancing knowledge","Reducing literacy rates","Eliminating the need for libraries","Restricting access to information"], a:0},
    {q:"Which \"mass communication feature\" is books said to fulfil, per this week's material?", opts:["Instant, real-time feedback","Mass dissemination","One-to-one private messaging","Exclusively oral transmission"], a:1},
    {q:"Why is persistence emphasized as part of the publishing process?", opts:["Because publishing can be lengthy, requiring persistence through queries and revisions","Because publishing is completed in a single step","Because publishers rarely reject manuscripts","Because writing and publishing happen simultaneously"], a:0},
    {q:"What does soliciting constructive feedback do, per this week's material?", opts:["Delays publication unnecessarily","Strengthens manuscripts and ensures clarity","Has no effect on manuscripts","Replaces the need for editing"], a:1},
    {q:"What are books said to be essential for, per this week's material?", opts:["Only entertainment","Literacy and national development","Only academic research","Only government archives"], a:1},
    {q:"What does this week's Call to Action recommend developing?", opts:["A marketing budget only","A personal writing and publishing plan","A list of competitor authors","A printing cost estimate"], a:1},
    {q:"Who wrote \"Introduction to book publishing: A practical guide,\" a key reference this week?", opts:["Nyeko, J.","Oso, L., & Biobaku, M.","Indeed (career site)","Findyourvoice.com"], a:1},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Publishing Knowledge","Feedback Handling","Self-Publishing Insight","Structural Welding"], a:3}
      ],
      fib: [

    {q:"Printing focuses on producing physical copies of text and images, while __________ covers the entire process from manuscript development to distribution.", a:"publishing"},
    {q:"Publishing involves seeking manuscripts, editing, __________, and managing distribution and sales.", a:"designing"},
    {q:"Writing is an artistic endeavour, whereas publishing is a __________-oriented process that involves editing and marketing.", a:"business"},
    {q:"Publishing transforms creative works into market-ready products and involves a __________ agreement with the author.", a:"contractual"},
    {q:"__________ with other writers provides insights into trends and reader interests.", a:"Connecting"},
    {q:"Self-publishing offers an alternative route for authors, providing more __________ over the publishing process.", a:"control"},
    {q:"Publishing involves producing and disseminating various materials, including books, films, and __________.", a:"magazines"},
    {q:"Publishing preserves __________, advances knowledge, and contributes to economic growth.", a:"culture"},
    {q:"Books are a mass communication medium, fulfilling features such as mass dissemination and delayed __________.", a:"feedback"},
    {q:"The publishing process can be lengthy, requiring __________ through queries and revisions.", a:"persistence"},
    {q:"Soliciting constructive __________ strengthens manuscripts and ensures clarity.", a:"feedback"},
    {q:"Books are essential for __________ and national development.", a:"literacy"},
    {q:"Publishing presents research and engages with society, promoting learning and cultural __________.", a:"preservation"},
    {q:"__________, L., & Biobaku, M. (2008) wrote \"Introduction to book publishing: A practical guide.\"", a:"Oso"},
    {q:"Consistency in writing improves material __________ and preparation for publication.", a:"accumulation"}
      ],
      short: [

    {q:"What's the key distinction between \"printing\" and \"publishing\"?", a:"Printing = producing physical copies; publishing = the entire process from manuscript development to distribution."},
    {q:"Name three activities involved in the publishing process.", a:"Any 3 of: seeking manuscripts, editing, designing, managing distribution/sales."},
    {q:"What's a common misconception about publishing that this week's material corrects?", a:"That publishing is the same as printing or writing."},
    {q:"How is writing described differently from publishing?", a:"Writing is artistic; publishing is business-oriented (editing and marketing)."},
    {q:"What does a publishing contract typically establish?", a:"A contractual agreement between publisher and author."},
    {q:"Name one way self-publishing differs from traditional publishing.", a:"It offers authors more control over the process."},
    {q:"What three types of material can publishing produce, besides books?", a:"Films and magazines."},
    {q:"Name two ways publishing contributes to society beyond entertainment.", a:"Preserves culture; advances knowledge/contributes to economic growth."},
    {q:"What is one \"mass communication feature\" that books fulfil?", a:"Mass dissemination (or delayed feedback)."},
    {q:"Why is persistence emphasized as part of the publishing process?", a:"Because publishing can be lengthy, requiring persistence through queries and revisions."},
    {q:"What does soliciting constructive feedback do for a manuscript, per this week's material?", a:"Strengthens manuscripts and ensures clarity."},
    {q:"What are books said to be essential for, according to this week's material?", a:"Literacy and national development."},
    {q:"What does this week's Call to Action recommend students develop?", a:"A personal writing and publishing plan, including goals for developing a manuscript and seeking feedback."},
    {q:"Name the two key references cited on the second page of this week's material.", a:"Oso, L. & Biobaku, M. (2008) Introduction to book publishing: A practical guide; Indeed (2023) Become a published writer: 5 steps and tips."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: publishing knowledge, writing routine, feedback handling, self-publishing insight, industry understanding, cultural impact awareness."}
      ]
    },
    {
      week: 2,
      topic: "Introduction to Book Publishing (History)",
      mcq: [
    {q:"What are the earliest known forms of book publishing, per this week's material?", opts:["Stone tablets in ancient Mesopotamia and Egypt, around 3500 BCE","Digital e-books","Printed newspapers","Handwritten scrolls in Rome"], a:0},
    {q:"Whose invention of the printing press in 1450 revolutionised the spread of information?", opts:["Johannes Gutenberg","Henry Townsend","Rev. Hope Waddell","Amos Tutuola"], a:0},
    {q:"What did the Industrial Revolution introduce to book publishing?", opts:["Mass production capabilities, making books more affordable and boosting literacy","A decline in book production","The end of printed books","Only digital formats"], a:0},
    {q:"Who is credited with starting early Nigerian publishing, setting up the first press in Calabar in 1846?", opts:["Rev. Hope Waddell","Henry Townsend","Amos Tutuola","Chinua Achebe"], a:0},
    {q:"Who published Nigeria's first newspaper, Iwe Irohin Fun Awon Ara Egba Ati Yoruba, in 1859?", opts:["Henry Townsend","Rev. Hope Waddell","Chinua Achebe","Amos Tutuola"], a:0},
    {q:"What caused a rise in local Nigerian publishers in the 1960s?", opts:["Laws requiring foreign companies to have Nigerian board members","A ban on foreign publishers","A decline in literacy","The invention of the printing press"], a:0},
    {q:"Which notable figures are named as shaping Nigeria's literary landscape through indigenous publishing?", opts:["Amos Tutuola and Chinua Achebe","Henry Townsend and Rev. Hope Waddell","Only foreign authors","Only journalists"], a:0},
    {q:"What does publishing encompass, beyond printing, per this week's material?", opts:["Writing, editing, and distribution","Only typesetting","Only binding","Only paper manufacturing"], a:0},
    {q:"What has technology done to traditional publishing, per this week's material?", opts:["Enhanced how books are published, distributed, and discovered, without rendering it obsolete","Made traditional publishing completely obsolete","Had no effect on publishing","Eliminated the need for editors"], a:0},
    {q:"What is described as the essence of publishing, per this week's material?", opts:["Creating, preparing, and distributing knowledge to ensure its accessibility and preservation","Only generating profit","Only producing physical copies","Only marketing books"], a:0},
    {q:"What three things does publishing contribute to, per this week's material?", opts:["Employment, knowledge preservation, and cultural promotion","Only tax revenue","Only paper production","Only international trade"], a:0},
    {q:"How is book publishing described as a mass communication medium?", opts:["Featuring mass dissemination, limited sensory channels, and delayed feedback","As a purely one-on-one communication form","As requiring no distribution","As an exclusively oral medium"], a:0},
    {q:"What does book publishing help preserve, per this week's material?", opts:["Cultural norms, traditions, and values through written materials","Only financial records","Only government policy","Only scientific data"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Project Management","Networking Skills","Marketing Strategies","Software Engineering"], a:3},
    {q:"Who wrote \"Introduction to book publishing: A practical guide,\" cited again this week?", opts:["Oso, L., & Baidaku, M.","Ogayi, M., & Igiri, T.","Dettori Publishing","Course Hero"], a:0}
      ],
      fib: [
    {q:"The history of book publishing begins with stone tablets in ancient Mesopotamia and Egypt around __________ BCE.", a:"3500"},
    {q:"Johannes Gutenberg's invention of the printing press in __________ revolutionised the spread of information.", a:"1450"},
    {q:"The __________ Revolution introduced mass production capabilities, making books more affordable.", a:"Industrial"},
    {q:"Rev. Hope __________ set up the first press in Calabar in 1846.", a:"Waddell"},
    {q:"Henry __________ published Nigeria's first newspaper in Abeokuta in 1859.", a:"Townsend"},
    {q:"The __________ saw a rise in local Nigerian publishers due to laws requiring Nigerian board members.", a:"1960s"},
    {q:"__________ Tutuola and Chinua Achebe were notable figures in Nigeria's indigenous publishing scene.", a:"Amos"},
    {q:"Publishing encompasses writing, editing, printing, and __________.", a:"distribution"},
    {q:"Technology has not rendered traditional publishing __________ but has enhanced it.", a:"obsolete"},
    {q:"The essence of publishing is creating, preparing, and distributing __________ to ensure accessibility and preservation.", a:"knowledge"},
    {q:"Publishing contributes to employment, knowledge preservation, and cultural __________.", a:"promotion"},
    {q:"Book publishing is a mass communication medium featuring mass dissemination and delayed __________.", a:"feedback"},
    {q:"Book publishing helps preserve cultural norms, traditions, and __________ through written materials.", a:"values"},
    {q:"One skill gained this week is __________ management.", a:"project"},
    {q:"Oso, L., & Baidaku, M. (2008) wrote \"Introduction to book publishing: A practical __________.\"", a:"guide"}
      ],
      short: [
    {q:"What were the earliest known forms of book publishing, and where did they originate?", a:"Stone tablets in ancient Mesopotamia and Egypt, around 3500 BCE."},
    {q:"How did Johannes Gutenberg's invention of the printing press revolutionise communication?", a:"It revolutionised the spread of information, comparable to the internet's impact today."},
    {q:"Who began early Nigerian publishing, and what did they establish?", a:"Rev. Hope Waddell, who set up the first press in Calabar in 1846."},
    {q:"Who published Nigeria's first newspaper, and when?", a:"Henry Townsend, in Abeokuta in 1859 (Iwe Irohin Fun Awon Ara Egba Ati Yoruba)."},
    {q:"What significant change occurred in Nigerian publishing in the 1960s?", a:"A rise in local Nigerian publishers, due to laws requiring foreign companies to have Nigerian board members."},
    {q:"Name two notable figures who shaped Nigeria's indigenous publishing landscape.", a:"Amos Tutuola and Chinua Achebe."},
    {q:"How does book publishing differ from printing, and why is this distinction important?", a:"Publishing encompasses writing, editing, printing, and distribution, while printing is just the technical part — understanding this clarifies the full scope of bringing a book to readers."},
    {q:"What has technology's effect on traditional publishing been, per this week's material?", a:"It has not rendered traditional publishing obsolete, but has enhanced how books are published, distributed, and discovered."},
    {q:"What is described as the essence of publishing?", a:"Creating, preparing, and distributing knowledge to ensure its accessibility and preservation."},
    {q:"What does publishing contribute to, beyond literature itself?", a:"Employment, knowledge preservation, cultural promotion, and societal engagement."},
    {q:"How is book publishing described as a mass communication medium?", a:"It features mass dissemination, limited sensory channels, and delayed feedback."},
    {q:"What does this week's Call to Action ask students to do?", a:"Explore a local publishing house or literary organisation, investigate its processes, and discuss technology's role in modern publishing."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: critical thinking, project management, networking skills, marketing strategies, cultural awareness, technological proficiency."},
    {q:"What three questions does this week's Personal Reflection raise?", a:"Whether you've considered publishing your own work; the role of books in preserving culture; and how technology has changed your reading habits."},
    {q:"Name two key references cited this week.", a:"Oso, L., & Baidaku, M. (2008) Introduction to book publishing: A practical guide; Ogayi, M., & Igiri, T. (2020) Onitsha market literature in language and literary development of Nigeria."}
      ]
    },
    {
      week: 3,
      topic: "Book Publishing as a Cultural Activity",
      mcq: [
    {q:"How are books described in relation to culture and heritage, per this week's material?", opts:["As time machines that capture the essence of different eras","As purely commercial products","As obsolete compared to digital media","As only entertainment"], a:0},
    {q:"What role do books play for future generations, per this week's material?", opts:["They archive history and spread information, ensuring understanding of past events","They have no lasting societal role","They only serve current readers","They replace oral tradition entirely"], a:0},
    {q:"What do books contribute to, regarding identity, per this week's material?", opts:["A broader understanding of personal and collective identities","Only individual entertainment","Only academic research","Only government record-keeping"], a:0},
    {q:"What do books reflect and influence, per this week's material?", opts:["Religious ideas, moral values, and language","Only fictional narratives","Only economic data","Only political structures"], a:0},
    {q:"What three qualities make books portable, focused, and long-lasting, per this week's material?", opts:["A rigorous publishing process ensuring authenticity and value","Random assembly with no editorial process","Only digital formatting","Only oral storytelling"], a:0},
    {q:"What made books part of mass communication, per this week's material?", opts:["The invention of the printing press","The invention of the internet","The invention of television","The invention of radio"], a:0},
    {q:"What do books foster, through communities like book clubs?", opts:["Connections between people over shared reading experiences","Isolation among readers","A decline in literacy","Competition between authors only"], a:0},
    {q:"What escape do books offer, per this week's material?", opts:["An escape from stress, transporting readers to different worlds","No meaningful escape","Only financial benefits","Only academic credit"], a:0},
    {q:"How does reading books contribute to personal growth, per this week's material?", opts:["By challenging thinking and inspiring self-improvement","By only providing entertainment","By replacing formal education entirely","By eliminating the need for critical thinking"], a:0},
    {q:"Who is named as a notable author whose works significantly impacted culture and society, per this week's material?", opts:["Chimamanda Ngozi Adichie","Amos Tutuola","Henry Townsend","Rev. Hope Waddell"], a:0},
    {q:"What do Adichie's works preserve, while addressing contemporary global issues?", opts:["Nigerian history and culture","Only fictional worlds","Only economic theory","Only scientific data"], a:0},
    {q:"What do Adichie's books emphasise, per this week's material?", opts:["The importance of self-identity and cultural assimilation","Only technological progress","Only political commentary","Only romantic themes"], a:0},
    {q:"Which Adichie novel is cited for contributing to understanding Nigerian history, per this week's material?", opts:["Half of a Yellow Sun","Things Fall Apart","The Joys of Motherhood","Efuru"], a:0},
    {q:"Which Adichie novel is cited for insight into Nigeria's cultural and societal dynamics?", opts:["Purple Hibiscus","Americanah","Half of a Yellow Sun","We Should All Be Feminists"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Cultural Understanding","Literary Analysis","Community Engagement","Financial Forecasting"], a:3}
      ],
      fib: [
    {q:"Books preserve culture and heritage, acting as __________ machines that capture the essence of different eras.", a:"time"},
    {q:"Books archive history and spread information, ensuring future generations understand past __________.", a:"events"},
    {q:"Books represent diverse experiences and stories, contributing to understanding of personal and __________ identities.", a:"collective"},
    {q:"Books reflect and influence culture, showcasing religious ideas, moral values, and __________.", a:"language"},
    {q:"Books became part of mass communication with the invention of the __________ press.", a:"printing"},
    {q:"Books foster communities, such as book __________, where people connect over shared reading.", a:"clubs"},
    {q:"Books offer an escape from stress, transporting readers to different __________.", a:"worlds"},
    {q:"Reading books contributes to personal growth by challenging thinking and inspiring __________.", a:"self-improvement"},
    {q:"__________ Ngozi Adichie is a notable author whose works have significantly impacted culture and society.", a:"Chimamanda"},
    {q:"Adichie's works preserve Nigerian history and culture while addressing contemporary __________ issues.", a:"global"},
    {q:"Adichie's books emphasise the importance of self-identity and cultural __________.", a:"assimilation"},
    {q:"\"Half of a Yellow Sun\" contributes to understanding Nigerian __________.", a:"history"},
    {q:"\"__________ Hibiscus\" provides insight into Nigeria's cultural and societal dynamics.", a:"Purple"},
    {q:"One skill gained this week is __________ awareness.", a:"historical"},
    {q:"Nyeko, J. (2009) wrote \"The ABC of Book __________: A training manual for NGOs in Africa.\"", a:"Publishing"}
      ],
      short: [
    {q:"How do books act as time machines that preserve and convey culture and history?", a:"They archive history and spread information, capturing the essence of different eras for future generations."},
    {q:"What role do books play in representing diverse experiences and societal beliefs?", a:"They represent diverse experiences and stories, contributing to a broader understanding of personal and collective identities, and reflect religious ideas, moral values, and language."},
    {q:"What three qualities does this week's material say make books effective cultural carriers?", a:"Books are portable, focused, and long-lasting, with a rigorous publishing process ensuring authenticity and value."},
    {q:"What made books part of mass communication, per this week's material?", a:"The invention of the printing press, which revolutionised information dissemination."},
    {q:"How do books foster community, per this week's material?", a:"Through book clubs, where people connect over shared reading experiences."},
    {q:"How does Chimamanda Ngozi Adichie's novel \"Half of a Yellow Sun\" contribute to understanding Nigerian history?", a:"It preserves Nigerian history and culture while addressing contemporary global issues."},
    {q:"In what ways does \"Purple Hibiscus\" provide insight into Nigeria's cultural and societal dynamics?", a:"It explores self-identity and cultural assimilation themes central to Nigerian society."},
    {q:"How does reading books contribute to personal growth?", a:"By challenging thinking and inspiring self-improvement."},
    {q:"What escape do books offer readers, per this week's material?", a:"An escape from stress, transporting readers to different worlds and sparking imagination."},
    {q:"What does this week's Call to Action ask students to do?", a:"Join a discussion on books' impact on cultural/historical narratives, and visit a library or bookshop to explore how books are organised and preserved."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: cultural understanding, historical awareness, literary analysis, critical thinking, personal reflection, community engagement."},
    {q:"What three questions does this week's Personal Reflection raise?", a:"How books helped you understand cultural heritage; a book club experience; and a time a book provided an escape from stress."},
    {q:"Name two key references cited this week.", a:"Nyeko, J. (2009) The ABC of Book Publishing; Pop, A.M. (2024) Introduction to mass communication: Books, background, characteristics, scope, and its types."},
    {q:"What do Adichie's novels educate readers about, per this week's material?", a:"Nigerian culture, history, and global cultural awareness."},
    {q:"What role do books play in representing personal and collective identity, per this week's material?", a:"They place stories within specific time frames, helping readers see how events are interconnected and contextualised."}
      ]
    },
    {
      week: 4,
      topic: "Book Publishing as a Business/Trade",
      mcq: [
        {q:"What does developing a business model in publishing require knowledge of, besides printing books?", opts:["Paper quality, printing speed, and binding type","Font selection, cover design, and page layout","Shipping logistics, warehousing, and inventory control","Audience needs, value creation, and revenue generation"], a:3},
        {q:"Which publisher business model targets loyal readers willing to pay for high-quality content through subscriptions or micropayments?", opts:["Publisher as Investor","Paid Content Publisher","Publisher as Retailer","Publisher as Data Broker"], a:1},
        {q:"The \"Publisher as Retailer\" model primarily involves what?", opts:["Offering IT consulting services to media companies","Selling directly to consumers with tailored content and exclusive offers","Licensing a brand for merchandise","Investing in emerging businesses"], a:1},
        {q:"Which model provides subscription packages with discounts and exclusive content to enhance reader engagement?", opts:["Ad Dependent Publisher","Publisher as Agency","Publisher as Club Membership","Publisher as Philanthropist"], a:2},
        {q:"The \"Publisher as Philanthropist\" model relies on what to support independent content?", opts:["Government subsidies","Bank loans","Stock market investment","Crowdfunding"], a:3},
        {q:"\"Publisher as Events Organiser\" generates income chiefly through what?", opts:["Brand licensing","Micropayments","Software solutions","Conferences and festivals"], a:3},
        {q:"Which model creates content for advertisers who lack in-house content teams?", opts:["Publisher as Brand Licenser","Publisher as Data Broker","Publisher as Agency","Publisher as Provider"], a:2},
        {q:"The \"Ad Dependent Publisher\" model creates relevant ads using what?", opts:["Subscription packages","Native advertising and branded content","Merchandise licensing","Crowdfunding campaigns"], a:1},
        {q:"\"Publisher as Provider\" generates revenue through what?", opts:["Software solutions, offering IT and consulting services to media companies","Investing in startups","Hosting branded events","Licensing its brand"], a:0},
        {q:"\"Publisher as Data Broker\" utilises audience data for what purpose?", opts:["Producing independent content","Enhancing advertising effectiveness with targeted marketing","Investing in emerging businesses","Expanding into merchandise"], a:1},
        {q:"\"Publisher as Brand Licenser\" expands into what by licensing its brand?", opts:["Crowdfunded books","Software products","Merchandise and experiences","Conference tickets"], a:2},
        {q:"\"Publisher as Investor\" gains returns through what?", opts:["Direct book sales only","Event ticket sales","Advertising deals and startup support","Print book royalties"], a:2},
        {q:"Which of these is listed in the summary as a source of publisher income?", opts:["Government grants","Tourism revenue","Film royalties","Licensing"], a:3},
        {q:"How do smaller publishers' annual earnings compare to major publishers, per the summary?", opts:["Smaller publishers earn between $500,000 and $5 million annually, while major publishers earn hundreds of millions","Both earn roughly the same amount","Smaller publishers earn more than major publishers","Earnings are unrelated to publisher size"], a:0},
        {q:"Which strategy is listed as a way publishers scale their business?", opts:["Focusing solely on physical bookstore sales","Expanding product offerings, adopting subscriptions, and leveraging partnerships and technology","Reducing the number of book titles published","Avoiding digital platforms entirely"], a:1}
      ],
      fib: [
        {q:"Business models in publishing require knowledge of audience needs, value creation, and __________.", a:"revenue generation"},
        {q:"The Paid Content Publisher model uses subscriptions or __________ to charge loyal readers.", a:"micropayments"},
        {q:"Publisher as __________ implies publishers sell directly to consumers, offering tailored content and exclusive offers.", a:"Retailer"},
        {q:"Publisher as Club Membership provides subscription packages with __________ and exclusive content.", a:"discounts"},
        {q:"Publisher as Philanthropist involves __________ for financial support to produce independent content.", a:"crowdfunding"},
        {q:"Publisher as Events Organiser hosts branded events and generates income through conferences and __________.", a:"festivals"},
        {q:"Publisher as Agency creates content for advertisers that lack __________ teams.", a:"in-house"},
        {q:"Ad Dependent Publisher partners with advertisers using native advertising and __________ content.", a:"branded"},
        {q:"Publisher as Provider offers IT and consulting services, generating revenue through __________ solutions.", a:"software"},
        {q:"Publisher as Data Broker utilises __________ data to enhance advertising effectiveness.", a:"audience"},
        {q:"Publisher as Brand Licenser licenses its brand for related products and services, expanding into merchandise and __________.", a:"experiences"},
        {q:"Publisher as Investor invests in emerging businesses, gaining returns through advertising deals and __________ support.", a:"startup"},
        {q:"Publishers generate income from direct sales, e-books, licensing, custom publishing, and __________.", a:"subscriptions"},
        {q:"Smaller publishers earn between $500,000 and __________ annually.", a:"$5 million"},
        {q:"One of the skills and competencies acquired in Week 4 is Contract __________.", a:"Negotiation"}
      ],
      short: [
        {q:"List three of the key questions publishers need to answer when setting up a business model.", a:"The needs publishers aim to satisfy, their target consumers, and considerations such as content uniqueness, payment methods, and production strategies (any three)."},
        {q:"Describe the Paid Content Publisher business model.", a:"It targets loyal readers who are willing to pay for high-quality content, typically through subscriptions or micropayments."},
        {q:"Explain how the Publisher as Retailer model differs from the Publisher as Club Membership model.", a:"Retailer sells directly to consumers with tailored content and exclusive offers, while Club Membership provides ongoing subscription packages with discounts and exclusive content to boost reader engagement."},
        {q:"What is the Publisher as Philanthropist model and what benefit does it provide?", a:"It involves crowdfunding for financial support, enabling publishers to produce independent content."},
        {q:"How does the Publisher as Events Organiser model generate income?", a:"By hosting branded events, such as conferences and festivals, that engage readers."},
        {q:"What is the Publisher as Agency model?", a:"Publishers create content for advertisers who lack in-house content teams, generating revenue through branded content."},
        {q:"How does the Ad Dependent Publisher model work?", a:"It partners with advertisers to create relevant ads, using native advertising and branded content."},
        {q:"What services does the Publisher as Provider model offer?", a:"IT and consulting services to other media companies, generating revenue through software solutions."},
        {q:"How does the Publisher as Data Broker model generate value?", a:"By utilising audience data to enhance advertising effectiveness and offer targeted marketing solutions."},
        {q:"Describe the Publisher as Brand Licenser model.", a:"Publishers license their brand for related products and services, expanding into merchandise and experiences."},
        {q:"How does the Publisher as Investor model generate returns?", a:"By investing in emerging businesses and gaining returns through advertising deals and startup support."},
        {q:"Name the main sources of publisher income listed in the Week 4 summary.", a:"Direct sales, e-books, licensing, custom publishing, and subscriptions."},
        {q:"Describe the range of profit margins among publishers, per the summary.", a:"Profit margins vary widely; major publishers can earn hundreds of millions, while smaller ones earn between $500,000 and $5 million annually."},
        {q:"What strategies help publishers scale their business, according to the summary?", a:"Expanding product offerings, adopting subscriptions, and leveraging partnerships and technology."},
        {q:"List the skills and competencies students should have acquired from the Week 4 lesson.", a:"Business Model Analysis, Revenue Stream Management, Contract Negotiation, Audience Understanding, Digital Strategy, and Profitability Assessment."}
      ]
    },
    {
      week: 5,
      topic: "The Environment of Book Publishing",
      mcq: [
        {q:"What has shifted the book publishing landscape toward online platforms and self-publishing?", opts:["A move away from physical bookstores","Stricter copyright laws","A decline in reader demand","An increase in printing costs"], a:0},
        {q:"Who do traditional publishers now compete with, giving readers a broader selection?", opts:["Government agencies","Film studios","Independent authors","Software companies"], a:2},
        {q:"Which themes are described as key in contemporary literature?", opts:["Diversity, representation, and inclusivity","Mystery, horror, and fantasy only","Historical fiction exclusively","Technical manuals"], a:0},
        {q:"What has changed reading habits, according to the Week 5 summary?", opts:["Digital platforms, with eBooks and audiobooks becoming popular","A decrease in literacy rates","The elimination of print books","The closure of all bookstores"], a:0},
        {q:"Which demographic groups are named as influencing reading tastes?", opts:["Generation X exclusively","The Silent Generation only","Baby Boomers only","Millennials, Gen Z, and Generation Alpha"], a:3},
        {q:"Which emerging technologies are mentioned as shaping the future of book publishing?", opts:["Cloud computing only","AI, blockchain, AR, and VR","Robotics only","3D printing only"], a:1},
        {q:"What must publishers conduct to understand reader preferences?", opts:["Printing trials","Stock audits","Tax assessments","Market research"], a:3},
        {q:"Collaborating with whom provides publishers valuable insights into new trends?", opts:["Government regulators","Competitors only","Authors and agents","Printers and distributors"], a:2},
        {q:"What do creative marketing campaigns help generate, according to the summary?", opts:["Buzz and increased book sales","Fewer print runs","Lower production costs","Shorter publishing timelines"], a:0},
        {q:"What has made self-publishing easier and more accessible?", opts:["Government funding","Technology","Traditional publishing houses","Physical bookstores"], a:1},
        {q:"What advantage do eBooks and online libraries offer, per the summary?", opts:["Higher prices than print books","Limited availability","Slower delivery than print","Instant access to books, often at a cheaper cost"], a:3},
        {q:"Despite the rise of digital formats, what is happening to print books according to the summary?", opts:["They are becoming treasured collectibles","They are no longer produced","They are mandatory in schools","They are being banned"], a:0},
        {q:"What do audiobooks offer readers, according to the summary?", opts:["Faster printing speeds","A new way to enjoy books through narration","Free unlimited book access","Better cover art"], a:1},
        {q:"Which type of strategies, including social media campaigns and virtual author events, are highlighted as important?", opts:["Door-to-door sales","Innovative marketing strategies","Radio jingles only","Traditional print-only advertising"], a:1},
        {q:"What can significantly impact book sales, per the Week 5 summary?", opts:["Weather conditions","Social media influencers","Currency exchange rates","Postal strikes"], a:1}
      ],
      fib: [
        {q:"Trends and __________ are crucial for success in the book publishing industry.", a:"demographics"},
        {q:"The book publishing landscape has shifted from physical bookstores to online platforms and __________.", a:"self-publishing"},
        {q:"__________, representation, and inclusivity are key themes in contemporary literature.", a:"Diversity"},
        {q:"Digital platforms have changed reading habits, with eBooks and __________ becoming popular.", a:"audiobooks"},
        {q:"Demographics like Millennials, Gen Z, and __________ influence reading tastes.", a:"Generation Alpha"},
        {q:"AI and other emerging technologies like blockchain, AR, and __________ are shaping the future of book publishing.", a:"VR"},
        {q:"Publishers must conduct __________ to understand reader preferences.", a:"market research"},
        {q:"Collaborating with authors and __________ provides valuable insights into new trends.", a:"agents"},
        {q:"__________ marketing campaigns help generate buzz and increase book sales.", a:"Creative"},
        {q:"Technology has made self-publishing easier and more __________.", a:"accessible"},
        {q:"eBooks and online libraries provide instant access to books and are often __________.", a:"cheaper"},
        {q:"Print books are becoming treasured __________ despite the rise of digital formats.", a:"collectibles"},
        {q:"Audiobooks offer a new way to enjoy books through __________.", a:"narration"},
        {q:"Social media __________ can significantly impact book sales.", a:"influencers"},
        {q:"One of the skills and competencies acquired in Week 5 is Trend __________.", a:"Analysis"}
      ],
      short: [
        {q:"How has the book publishing landscape shifted in recent years?", a:"It has shifted from physical bookstores toward online platforms and self-publishing, with traditional publishers now competing with independent authors who provide readers a broader selection."},
        {q:"Why are diversity, representation, and inclusivity important in contemporary literature, per the summary?", a:"Readers demand stories that reflect their experiences, which has led to success for inclusive books."},
        {q:"How have digital platforms changed reading habits?", a:"eBooks and audiobooks have become popular, giving readers new ways to access and consume content."},
        {q:"Which demographic groups influence current reading tastes, according to the summary?", a:"Millennials, Gen Z, and Generation Alpha."},
        {q:"Name the emerging technologies described as shaping the future of book publishing.", a:"AI, blockchain, AR, and VR."},
        {q:"Why is market research important for publishers, according to the summary?", a:"It helps publishers understand reader preferences and stay relevant in a dynamic market."},
        {q:"How does collaborating with authors and agents benefit publishers?", a:"It provides valuable insights into new trends."},
        {q:"What role do creative marketing campaigns play in publishing?", a:"They help generate buzz and increase book sales."},
        {q:"How has technology affected self-publishing?", a:"It has made self-publishing easier and more accessible."},
        {q:"What advantages do eBooks and online libraries offer readers?", a:"Instant access to books, often at a cheaper price than print."},
        {q:"What is happening to print books despite the rise of digital formats?", a:"They are becoming treasured collectibles."},
        {q:"What do audiobooks offer readers, according to the summary?", a:"A new way to enjoy books through narration."},
        {q:"How can social media influencers affect book publishing?", a:"They can significantly impact book sales."},
        {q:"What innovative marketing strategies are mentioned in the Week 5 summary?", a:"Social media campaigns and virtual author events."},
        {q:"List the skills and competencies students should have acquired from the Week 5 lesson.", a:"Trend Analysis, Market Research, Digital Adaptation, Strategic Collaboration, Innovative Marketing, and Technological Integration."}
      ]
    },
    {
      week: 6,
      topic: "Book Publishing as a Mass Communication Tool",
      mcq: [
        {q:"What does the \"scale\" of the book publishing industry refer to?", opts:["Only the number of publishing companies","The price of books","The number of literary awards given","Its size and reach, including millions of books published annually"], a:3},
        {q:"Approximately how many books are published each year in the UK alone?", opts:["15,000","1.6 million","1.5 million","150,000"], a:3},
        {q:"Approximately how many e-books were published globally in 2023?", opts:["Around 160,000","Around 1.6 million","Around 150,000","Around 16 million"], a:1},
        {q:"Which markets dominate the global book publishing industry, according to the summary?", opts:["Africa and South America","The US and Europe","Australia and Antarctica","Asia only"], a:1},
        {q:"What does the industry's infrastructure include, per the summary?", opts:["Only online stores","Printing facilities, distribution networks, and retail outlets","Music streaming services","Film studios"], a:1},
        {q:"Which formats does book publishing encompass, per the summary?", opts:["Only digital formats","Only audiobooks","Only print books","Print books, e-books, and audiobooks"], a:3},
        {q:"Which of the following is listed as a market segment in book publishing?", opts:["Educational publishing","Software development","Music licensing","Film distribution"], a:0},
        {q:"What role does technology play in modern publishing, according to the summary?", opts:["Technology plays no significant role","It only affects printing speed","It is limited to email marketing","Online sales platforms and self-publishing tools play a key role"], a:3},
        {q:"Which of these is an example of traditional marketing in book publishing?", opts:["Book signings and print ads","Bookstagram posts","BookTube videos","Google Ads"], a:0},
        {q:"Which tools are used in digital marketing for books, per the summary?", opts:["Social media, blogs, and book trailers","Print ads and billboards only","Door-to-door sales","Radio only"], a:0},
        {q:"What does media relations involve in book publishing?", opts:["Negotiating author contracts","Managing warehouse inventory","Pitching books to reviewers and bloggers for wider reach","Printing book covers"], a:2},
        {q:"What kind of influencers are mentioned as helping reach broader audiences?", opts:["Travel influencers","Fashion influencers","Fitness influencers","Bookstagrammers and BookTubers"], a:3},
        {q:"Which e-commerce platforms are named as essential for book sales?", opts:["Alibaba and Shopify","Walmart and Target","Amazon and Barnes & Noble","eBay and Etsy"], a:2},
        {q:"What does Goodreads facilitate, according to the summary?", opts:["Direct book printing","Warehouse logistics","Audiobook narration","Reader and author connections through reviews and discussions"], a:3},
        {q:"Which advertising tools are listed as targeting specific reader demographics?", opts:["TikTok Ads only","Print newspaper ads only","Google Ads, Facebook Ads, and Amazon Marketing Services","Billboard advertising only"], a:2}
      ],
      fib: [
        {q:"The book publishing industry is dynamic with a significant impact on culture, education, and __________.", a:"entertainment"},
        {q:"Approximately __________ books are published each year in the UK alone.", a:"150,000"},
        {q:"In 2023, around __________ e-Books were published globally.", a:"1.6 million"},
        {q:"The industry's infrastructure includes printing facilities, distribution networks, and __________.", a:"retail outlets"},
        {q:"Book publishing encompasses various formats: print books, e-books, and __________.", a:"audiobooks"},
        {q:"Different market segments include trade publishing, educational publishing, and __________ publishing.", a:"professional"},
        {q:"__________, such as online sales platforms and self-publishing tools, plays a key role in modern publishing.", a:"Technology"},
        {q:"Traditional marketing includes book signings, print ads, and physical __________ events.", a:"promotional"},
        {q:"Digital marketing uses social media, blogs, and __________ to promote books.", a:"book trailers"},
        {q:"Media relations involve pitching books to __________ and bloggers for wider reach.", a:"reviewers"},
        {q:"Influencer partnerships with Bookstagrammers and __________ help reach broader audiences.", a:"BookTubers"},
        {q:"__________ facilitates reader and author connections through reviews and discussions.", a:"Goodreads"},
        {q:"Advertising tools like Google Ads, Facebook Ads, and __________ target specific reader demographics.", a:"Amazon Marketing Services"},
        {q:"Book launch events, both physical and __________, engage fans and promote new releases.", a:"virtual"},
        {q:"One of the skills and competencies for Week 6 is Media __________.", a:"Relations"}
      ],
      short: [
        {q:"What does the \"scale\" of the book publishing industry refer to, and why is it important to understand?", a:"It refers to the size and reach of the industry, including the millions of books published annually; understanding it shows the industry's cultural and economic significance."},
        {q:"How many books are published each year in the UK, and how many e-books were published globally in 2023?", a:"Approximately 150,000 books are published annually in the UK, and around 1.6 million e-books were published globally in 2023."},
        {q:"What makes up the infrastructure of the book publishing industry, per the summary?", a:"Printing facilities, distribution networks, and retail outlets."},
        {q:"What formats and genres does book publishing cover, according to the summary?", a:"Formats include print books, e-books, and audiobooks; genres include fiction, non-fiction, academic, and children's books."},
        {q:"Name the different market segments in book publishing mentioned in the summary.", a:"Trade publishing, educational publishing, and professional publishing."},
        {q:"What traditional marketing strategies are used in book publishing?", a:"Book signings, print ads, and physical promotional events."},
        {q:"How have digital marketing tools transformed book promotion?", a:"They use social media, blogs, and book trailers, along with advertising tools like Google Ads, Facebook Ads, and Amazon Marketing Services, to reach and target readers."},
        {q:"What does media relations involve in book publishing?", a:"Pitching books to reviewers and bloggers to achieve wider reach."},
        {q:"How do book launch events support new releases?", a:"Both physical and virtual launch events engage fans and promote new releases."},
        {q:"How do influencer partnerships help publishers?", a:"Partnerships with Bookstagrammers and BookTubers help books reach broader audiences."},
        {q:"Which e-commerce platforms are essential for book sales, and what role does Goodreads play?", a:"Amazon and Barnes & Noble are essential e-commerce platforms; Goodreads facilitates reader and author connections through reviews and discussions."},
        {q:"What publishing services are mentioned as part of the industry?", a:"Editing, design, marketing, and distribution."},
        {q:"Which major markets dominate the global book publishing industry, according to the summary?", a:"The US and Europe, though local markets are also growing."},
        {q:"List the skills and competencies students should have acquired from the Week 6 lesson.", a:"Industry Analysis, Marketing Strategy, Media Relations, Digital Promotion, Event Planning, and Technological Adaptation."},
        {q:"What role does technology play in modern book publishing, according to the summary?", a:"Technology, such as online sales platforms and self-publishing tools, plays a key role in modern publishing."}
      ]
    }
  ]
},
{
  code: "CMS 101",
  title: "Introduction to Human Communication",
  weeks: [
    {
      week: 1,
      topic: "History and Functions of Communication in Human Society",
      mcq: [

    {q:"What Latin word does \"communication\" derive from, and what does it mean?", opts:["\"Communis,\" meaning silence","\"Communico,\" meaning to join, connect, participate, or share with all","\"Communitas,\" meaning distance","\"Communicare,\" meaning to isolate"], a:1},
    {q:"According to Poe (2011), how long was talking humanity's sole medium of communication?", opts:["About 10,000 years","About 50,000 years","Over 150,000 years","About 1,000 years"], a:2},
    {q:"What did Plato believe about the purpose of talking?", opts:["That people are meant to engage in monologue, not dialogue","That people are meant to engage in dialogue, not monologue","That talking is inferior to writing","That talking should be avoided in formal settings"], a:1},
    {q:"Which scholar defined communication as \"the transference and understanding of meaning\"?", opts:["Lewis (1987)","Robbins (1984)","Lustig and Koester (1996)","Plato"], a:1},
    {q:"What three types of needs does communication meet, per this week's material?", opts:["Physical, intellectual, and emotional","Financial, legal, and political","Technical, digital, and mechanical","Historical, artistic, and scientific"], a:0},
    {q:"Which of these is NOT listed as a function of communication this week?", opts:["Motivation","Information dissemination","Decision-making","Currency exchange"], a:3},
    {q:"What role do media organisations play, per this week's summary?", opts:["They have no defined societal role","They disseminate information and play a watchdog role","They only produce entertainment content","They replace advertising agencies entirely"], a:1},
    {q:"What role do advertising agencies play, per this week's material?", opts:["They regulate media organisations","They create and manage promotional content to build brand awareness and sales","They have no connection to communication functions","They exclusively handle legal disputes"], a:1},
    {q:"Besides speaking, which two communication modes are listed this week?", opts:["Body language and writing","Singing and drawing","Coding and translating","Broadcasting and printing"], a:0},
    {q:"Why is talking considered to have provided early humans an evolutionary advantage?", opts:["It had no real impact on survival","It led to better survival and reproductive success","It only mattered for social status, not survival","It replaced the need for physical cooperation"], a:1},
    {q:"How do Lustig and Koester (1996) define communication?", opts:["A one-way transmission of facts","A symbolic process creating shared meanings","A purely written form of exchange","An exclusively emotional exercise"], a:1},
    {q:"What does this week's Call to Action recommend practising to enhance communication skills?", opts:["Avoiding eye contact","Active listening, clear articulation, and empathetic responses","Speaking as quickly as possible","Only written communication"], a:1},
    {q:"Who wrote \"Organisational Communication\" (1987), a key reference this week?", opts:["Robbins","Lewis","Lustig","Poe"], a:1},
    {q:"What is the title of Marshal T. Poe's 2011 book cited this week?", opts:["The Media and Modernity","A History of Communications: Media and Society from the Evolution of Speech to the Internet","Mass Communication Theory","McQuail's Mass Communication Theory"], a:1},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Effective dialogue","Message clarity","Relationship building","Software debugging"], a:3}
      ],
      fib: [

    {q:"The word \"communication\" derives from the Latin \"__________,\" meaning to join, connect, participate, or share with all.", a:"communico"},
    {q:"According to Poe (2011), talking was humanity's first and sole medium of communication for over __________ years.", a:"150,000"},
    {q:"__________ believed that people are meant to engage in dialogue, not monologue.", a:"Plato"},
    {q:"Lewis (1987) defines communication as an exchange of messages resulting in __________ meaning.", a:"shared"},
    {q:"Robbins (1984) describes communication as the transference and __________ of meaning.", a:"understanding"},
    {q:"Effective communication benefits physical, intellectual, and __________ health.", a:"emotional"},
    {q:"Communication is vital for social needs such as pleasure, affection, and __________.", a:"relaxation"},
    {q:"__________ organisations disseminate information to the public, playing a watchdog role.", a:"Media"},
    {q:"Advertising agencies create and manage __________ content to enhance brand awareness and sales.", a:"promotional"},
    {q:"Communication serves functions such as motivation, information dissemination, decision-making, and __________.", a:"entertainment"},
    {q:"Lustig and Koester (1996) define communication as a __________ process creating shared meanings.", a:"symbolic"},
    {q:"This week's Call to Action encourages practising active listening, clear articulation, and __________ responses.", a:"empathetic"},
    {q:"Lewis (1987) wrote \"__________ Communication,\" a key reference this week.", a:"Organisational"},
    {q:"Marshal T. Poe's 2011 book is titled \"A History of __________: Media and Society from the Evolution of Speech to the Internet.\"", a:"Communications"},
    {q:"One skill gained this week is relationship __________.", a:"building"}
      ],
      short: [

    {q:"What Latin word does \"communication\" derive from, and what does it mean?", a:"\"Communico\" — to join, connect, participate, or share with all."},
    {q:"According to Poe (2011), how long was talking humanity's sole medium of communication?", a:"Over 150,000 years."},
    {q:"What did Plato believe about the purpose of talking?", a:"That people are meant to engage in dialogue, not monologue."},
    {q:"Give two of the three scholarly definitions of communication cited this week.", a:"Any 2 of: Lewis (exchange of messages resulting in shared meaning); Robbins (transference and understanding of meaning); Lustig & Koester (symbolic process creating shared meanings)."},
    {q:"What three types of human needs does communication meet, per this week's material?", a:"Physical, intellectual, and emotional health needs."},
    {q:"Name two functions communication serves in society.", a:"Any 2 of: motivation, information dissemination, decision-making, entertainment."},
    {q:"What role do media organisations play, as described this week?", a:"Disseminate information to the public, playing a watchdog role."},
    {q:"What role do advertising agencies play, per this week's material?", a:"Create and manage promotional content to build brand awareness/sales."},
    {q:"What communication modes are listed besides speaking?", a:"Body language and writing."},
    {q:"Why is talking considered to have provided an evolutionary advantage to early humans?", a:"It provided survival and reproductive advantages."},
    {q:"How do Lustig and Koester (1996) define communication?", a:"As a symbolic process creating shared meanings."},
    {q:"What does this week's Call to Action recommend practising to enhance communication skills?", a:"Active listening, clear articulation, and empathetic responses."},
    {q:"Name the key reference by Lewis cited this week, and its publication year.", a:"Organisational Communication, 1987."},
    {q:"What is the title of Marshal T. Poe's 2011 book cited this week?", a:"A History of Communications: Media and Society from the Evolution of Speech to the Internet."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: effective dialogue, active listening, message clarity, cultural awareness, relationship building, motivational communication."}
      ]
    },
    {
      week: 2,
      topic: "Elements of Human Communication",
      mcq: [
    {q:"What roles do individuals play in the communication process, per this week's material?", opts:["Both sources and receivers of messages, simultaneously","Only sources, never receivers","Only passive observers","Only receivers, never sources"], a:0},
    {q:"Which characteristics influence how people send and receive messages?", opts:["Race, sex, age, culture, values, and attitudes","Only height and weight","Only geographic location","Only occupation"], a:0},
    {q:"What is a message, per this week's material?", opts:["The verbal and non-verbal content one person wishes to convey to another","Only written text","Only spoken words","Only body language"], a:0},
    {q:"Can communication occur through unintentional messages, per this week's material?", opts:["Yes, despite challenges in proving intent","No, all communication must be intentional","Only in written form","Only between strangers"], a:0},
    {q:"What are channels, in the context of communication?", opts:["The means through which messages travel, like airwaves and cables","Only facial expressions","Only written documents","Only silence"], a:0},
    {q:"What is feedback, per this week's material?", opts:["The receiver's verbal and non-verbal response to the source's message","Only a written reply","Only a formal evaluation","Only a delayed response"], a:0},
    {q:"Can silence be a form of feedback, per this week's material?", opts:["Yes, even silence provides valuable information","No, silence is not feedback","Only in written communication","Only in formal settings"], a:0},
    {q:"What are codes, in the context of communication?", opts:["Systematic arrangements of symbols to create meanings","Only secret military signals","Only mathematical formulas","Only computer programming language"], a:0},
    {q:"What do verbal codes include, per this week's material?", opts:["Words and their grammatical arrangement","Only facial expressions","Only hand gestures","Only tone of voice"], a:0},
    {q:"What do non-verbal codes encompass, per this week's material?", opts:["Bodily movements, clothing, and sounds other than words","Only written text","Only spoken language","Only formal documents"], a:0},
    {q:"What is encoding, per this week's material?", opts:["Translating a thought into a code","Interpreting a received message","Ignoring a message","Repeating a message verbatim"], a:0},
    {q:"What is decoding, per this week's material?", opts:["Assigning meaning to a received code","Creating a new message","Sending a message","Translating a thought into a code"], a:1},
    {q:"What is noise, in the context of communication?", opts:["Any interference that reduces message clarity","Only loud background sounds","Only technical malfunctions","Only a lack of feedback"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Effective listening","Clear articulation","Non-verbal awareness","Financial budgeting"], a:3},
    {q:"Who wrote \"Human Communication: Fourth Edition,\" a key reference this week?", opts:["Judy C. Pearson, Paul Nelson, Scott Titsworth, & Lynn Harter","Radhika Kapur","Sholihatul Hamidah Daulay","Marshal T. Poe"], a:0}
      ],
      fib: [
    {q:"Individuals act as both sources and __________ of messages, engaging in continuous communication.", a:"receivers"},
    {q:"Characteristics such as race, sex, age, culture, values, and __________ influence how people send and receive messages.", a:"attitudes"},
    {q:"A message is the verbal and non-verbal __________ one person wishes to convey to another.", a:"content"},
    {q:"Communication can occur through both intentional and __________ messages.", a:"unintentional"},
    {q:"Channels are the means through which messages travel, including airwaves, sound waves, and __________ wires.", a:"copper"},
    {q:"Feedback is the receiver's verbal and non-verbal __________ to the source's message.", a:"response"},
    {q:"Even __________ or lack of response is a form of feedback.", a:"silence"},
    {q:"Communication uses __________, which are systematic arrangements of symbols to create meanings.", a:"codes"},
    {q:"Verbal codes include words and their grammatical __________.", a:"arrangement"},
    {q:"Non-verbal codes encompass bodily movements, clothing, and __________ other than words.", a:"sounds"},
    {q:"__________ is translating a thought into a code.", a:"Encoding"},
    {q:"__________ is assigning meaning to a received code.", a:"Decoding"},
    {q:"__________ is any interference in the communication process that reduces message clarity.", a:"Noise"},
    {q:"One skill gained this week is feedback __________.", a:"interpretation"},
    {q:"Judy C. Pearson, Paul Nelson, Scott Titsworth, & Lynn Harter wrote \"Human Communication: __________ Edition.\"", a:"Fourth"}
      ],
      short: [
    {q:"What roles do individuals play in the communication process, per this week's material?", a:"They act as both sources and receivers of messages, engaging in simultaneous and continuous communication."},
    {q:"How do individual characteristics influence the way messages are sent and received?", a:"Characteristics such as race, sex, age, culture, values, and attitudes shape how people send and receive messages."},
    {q:"What are the components of a message, in the context of human communication?", a:"Verbal and non-verbal content, including symbols, facial expressions, gestures, and tone of voice."},
    {q:"How does feedback contribute to the communication process, and what forms can it take?", a:"It indicates whether a message was received as intended; even silence or lack of response is a form of feedback."},
    {q:"What is the difference between encoding and decoding, and why are they important?", a:"Encoding is translating a thought into a code; decoding is assigning meaning to that code — both are crucial for sharing ideas and feelings."},
    {q:"What are channels, and give two examples.", a:"The means through which messages travel; examples include airwaves, sound waves, copper wires, glass fibres, and cables."},
    {q:"What is noise, in the context of communication, and name two types.", a:"Any interference that reduces message clarity; types include physical, mental, psychological, or semantic distractions."},
    {q:"What is the difference between verbal and non-verbal codes?", a:"Verbal codes include words and their grammatical arrangement; non-verbal codes encompass bodily movements, clothing, and sounds other than words."},
    {q:"What does this week's Call to Action ask students to commit to?", a:"Refining communication skills by actively listening, clearly articulating messages, and being mindful of non-verbal cues."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: effective listening, clear articulation, non-verbal awareness, feedback interpretation, cultural sensitivity, goal achievement."},
    {q:"What three questions does this week's Personal Reflection raise?", a:"How non-verbal codes impact message reception; an experience where feedback (or its absence) affected communication; and how individual differences influence communication."},
    {q:"Name this week's key reference on Human Communication.", a:"Judy C. Pearson, Paul Nelson, Scott Titsworth, & Lynn Harter, Human Communication: Fourth Edition (McGraw-Hill, 2003)."},
    {q:"How does effective communication help individuals, per this week's material?", a:"It allows individuals to understand each other's viewpoints and perspectives by considering all necessary factors."},
    {q:"Why is effective communication fundamental, per this week's material?", a:"It is fundamental for generating desired outcomes and achieving personal and professional goals."},
    {q:"What can communication with knowledgeable individuals help address, per this week's material?", a:"It can help address limitations and bring about improvements in various settings."}
      ]
    },
    {
      week: 3,
      topic: "Cultural Beliefs and Practices in Human Communication",
      mcq: [
    {q:"What role does culture play in communication, per this week's material?", opts:["It makes communication easier when understood","It has no effect on communication","It only matters in formal settings","It only affects written communication"], a:0},
    {q:"What aids interaction, per this week's material?", opts:["Understanding beliefs, dressing styles, and thought processes","Only speaking loudly","Only using formal language","Only avoiding eye contact"], a:0},
    {q:"What do societies have, influencing expected behaviour in relationships, per Knapp et al.?", opts:["Guidelines","No structure at all","Only legal contracts","Only religious doctrine"], a:0},
    {q:"What impacts relationship success or failure, per this week's material?", opts:["Cultural values, such as honesty","Only financial status","Only physical appearance","Only geographic proximity"], a:0},
    {q:"What often influences interpersonal relationships unknowingly, per this week's material?", opts:["Unspoken cultural assumptions","Only written agreements","Only formal education","Only income level"], a:0},
    {q:"What is communication influenced by, per this week's material?", opts:["Surrounding conditions and social background","Only personal preference","Only weather conditions","Only time of day"], a:0},
    {q:"What has technological evolution in communication altered, per this week's material?", opts:["Human interaction patterns","Only business operations","Only academic research","Only government policy"], a:0},
    {q:"What concerns have been raised about online connections, per this week's material?", opts:["The quality of deeper relationships","The cost of internet access only","The speed of data transfer only","The size of social networks only"], a:0},
    {q:"What does communication involve, per this week's material?", opts:["Sharing meaning through information exchange","Only one-way transmission","Only formal writing","Only silence"], a:0},
    {q:"Which historical advancements in communication are named this week?", opts:["Writing, printing, telegraph, telephone, radio, TV, and mobile phones","Only the internet","Only social media","Only smartphones"], a:0},
    {q:"What dominates 21st-century communication, per this week's material?", opts:["The internet and email","Only radio","Only print newspapers","Only face-to-face conversation"], a:0},
    {q:"Which communication technologies are listed this week?", opts:["Email, fax, telephony, television broadcasting, videoconferencing, and satellites","Only smoke signals","Only carrier pigeons","Only telegrams"], a:0},
    {q:"What does this week's Call to Action encourage regarding cross-cultural communication?", opts:["Understanding and respecting the cultural backgrounds of those you interact with","Avoiding interaction with different cultures","Only using one's native language","Ignoring cultural differences entirely"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Cultural awareness","Relationship building","Technological adaptability","Financial forecasting"], a:3},
    {q:"Who wrote \"Interpersonal Communication and Human Relationships: Seventh Edition,\" a key reference this week?", opts:["Mark L. Knapp, Anita L. Vangelisti, & John P. Caughlin","Dan Schiller","Radhika Kapur","Judy C. Pearson"], a:0}
      ],
      fib: [
    {q:"Culture plays a crucial role in communication by making it __________ when understood.", a:"easier"},
    {q:"Understanding beliefs, dressing styles, and __________ processes aids interaction.", a:"thought"},
    {q:"Societies have __________ influencing expected behaviour in relationships, per Knapp et al.", a:"guidelines"},
    {q:"Cultural values, such as __________, impact relationship success or failure.", a:"honesty"},
    {q:"Unspoken cultural __________ often influence interpersonal relationships unknowingly.", a:"assumptions"},
    {q:"Communication is influenced by surrounding conditions and social __________.", a:"background"},
    {q:"Technological evolution in communication has altered human interaction __________.", a:"patterns"},
    {q:"Online connections have raised concerns about the quality of __________ relationships.", a:"deeper"},
    {q:"Communication involves sharing __________ through information exchange.", a:"meaning"},
    {q:"Historical advancements in communication include the invention of writing, printing, telegraph, telephone, radio, TV, and __________ phones.", a:"mobile"},
    {q:"21st-century communication is heavily dominated by the internet and __________.", a:"email"},
    {q:"Communication technologies listed this week include email, fax, telephony, and __________.", a:"videoconferencing"},
    {q:"This week's Call to Action encourages engaging actively in __________-cultural communication.", a:"cross"},
    {q:"One skill gained this week is technological __________.", a:"adaptability"},
    {q:"Mark L. Knapp, Anita L. Vangelisti, & John P. __________ wrote \"Interpersonal Communication and Human Relationships.\"", a:"Caughlin"}
      ],
      short: [
    {q:"What role does culture play in communication, per this week's material?", a:"It plays a crucial role, making communication easier when understood."},
    {q:"What aids interaction, per this week's material?", a:"Understanding beliefs, dressing styles, and thought processes."},
    {q:"What do societies have that influences expected behaviour in relationships?", a:"Guidelines, as described by Knapp et al."},
    {q:"What impacts relationship success or failure, per this week's material?", a:"Cultural values, such as honesty."},
    {q:"What often influences interpersonal relationships unknowingly?", a:"Unspoken cultural assumptions."},
    {q:"What is communication influenced by, beyond the message itself?", a:"Surrounding conditions and social background."},
    {q:"What concerns have been raised regarding the impact of online connections on relationships?", a:"Concerns about the quality of deeper relationships."},
    {q:"In what ways have communication technologies evolved over the past few decades?", a:"They have drastically changed, now including email, fax, telephony, television broadcasting, videoconferencing, mobile phones, and more."},
    {q:"How do historical advancements in communication reflect societal changes?", a:"They trace a progression from writing and printing through to the telegraph, telephone, radio, TV, and now mobile phones and the internet."},
    {q:"What dominates 21st-century communication, per this week's material?", a:"The internet and email."},
    {q:"What does this week's Call to Action encourage students to do?", a:"Actively engage in cross-cultural communication by understanding and respecting others' cultural backgrounds, and using communication technologies responsibly."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: cultural awareness, communication technologies, relationship building, critical thinking, social interaction, technological adaptability."},
    {q:"What three questions does this week's Personal Reflection raise?", a:"How understanding another's culture positively impacted your interactions; a time cultural misunderstanding caused a breakdown; and a situation where an unspoken cultural assumption influenced communication."},
    {q:"Name this week's key reference on interpersonal communication and its authors.", a:"Interpersonal Communication and Human Relationships: Seventh Edition, by Mark L. Knapp, Anita L. Vangelisti, & John P. Caughlin (2014)."},
    {q:"What are some key aspects of culture that influence communication, per this week's material?", a:"Beliefs, dressing styles, thought processes, and cultural guidelines around relationships."}
      ]
    },
    {
      week: 4,
      topic: "The Development of Different Types of Communication",
      mcq: [
        {q:"Whose movable type printing press revolutionised mass production of print media in the 15th century?", opts:["Johannes Gutenberg","Marconi","Benedict Anderson","Friedrich Koenig"], a:0},
        {q:"Gutenberg's invention played a key role in which historical developments?", opts:["The European Renaissance and the Protestant Reformation","The invention of television","The rise of the internet","The invention of radio"], a:0},
        {q:"Who developed the steam-powered printing press in 1810?", opts:["Guglielmo Marconi","Johannes Gutenberg","Benedict Anderson","Friedrich Koenig"], a:3},
        {q:"By the 1930s, some steam-powered presses could produce how many pages per hour?", opts:["300,000","300","30,000","3,000"], a:3},
        {q:"The rise of daily newspapers in the 19th century mainly catered to:", opts:["Rural farming communities only","The urbanised American population","Radio listeners exclusively","Television audiences"], a:1},
        {q:"According to Benedict Anderson, newspapers fostered a sense of:", opts:["Global anonymity","National identity","Technological decline","Religious division"], a:1},
        {q:"Penny papers, which emerged in the 1830s, were known for providing:", opts:["Sensational news at low prices","Expensive subscription-only content","Only government announcements","Academic research papers"], a:0},
        {q:"Penny papers are considered forerunners to today's:", opts:["Radio dramas","Scholarly journals","Streaming platforms","Tabloids"], a:3},
        {q:"Which became the first major non-print mass medium in the early 20th century?", opts:["Social media","The internet","Radio","Television"], a:2},
        {q:"Radio allowed large audiences to:", opts:["Replace newspapers instantly","Listen to the same event simultaneously","Avoid advertising entirely","Read printed news only"], a:1},
        {q:"Radio provided advertisers with:", opts:["No commercial value","A platform limited to print ads","Only local reach","A valuable platform to reach a wide audience"], a:3},
        {q:"How did newspapers respond to the rise of radio and television?", opts:["They banned broadcast media","They had to adapt to the new media landscape","They merged completely with radio","They disappeared immediately"], a:1},
        {q:"Compared to broadcast media, print media offered:", opts:["No lasting record","Durability and flexibility","Only immediacy","Less portability"], a:1},
        {q:"Broadcast media, compared to print, mainly offered:", opts:["Lower production cost only","Permanent archiving","Immediacy","Durability"], a:2},
        {q:"What innovation in the late 1990s allowed viewers to pause and rewind live broadcasts?", opts:["Podcasting","Digital video recorders","The telegraph","The printing press"], a:1}
      ],
      fib: [
        {q:"Johannes Gutenberg's __________ type printing press revolutionised mass production of print media.", a:"movable"},
        {q:"Gutenberg's invention played a key role in the European __________ and the Protestant Reformation.", a:"Renaissance"},
        {q:"Friedrich Koenig's __________-powered printing press debuted in 1810.", a:"steam"},
        {q:"By the 1930s, some presses were producing __________ pages per hour.", a:"3,000"},
        {q:"The rise of daily newspapers in the 19th century catered to the __________ American population.", a:"urbanised"},
        {q:"__________ Anderson argued that newspapers fostered a sense of national identity.", a:"Benedict"},
        {q:"The 1830s saw the emergence of __________ papers, offering sensational news at low prices.", a:"penny"},
        {q:"Penny papers can be considered forerunners to today's __________.", a:"tabloids"},
        {q:"__________ became the first major non-print mass media in the early 20th century.", a:"Radio"},
        {q:"Radio allowed large audiences to listen to the same __________ simultaneously.", a:"event"},
        {q:"Radio provided a valuable platform for __________ to reach a wide audience.", a:"advertisers"},
        {q:"Newspapers had to __________ to the new media landscape created by radio and television.", a:"adapt"},
        {q:"Print media offered durability and __________, while broadcast media provided immediacy.", a:"flexibility"},
        {q:"The advent of __________ video recorders in the late 1990s allowed pausing and rewinding live broadcasts.", a:"digital"},
        {q:"Newspapers helped urban Americans navigate their rapidly __________ world.", a:"changing"}
      ],
      short: [
        {q:"What was the significance of Johannes Gutenberg's movable type printing press?", a:"It revolutionised the mass production of print media in the 15th century and played a key role in the European Renaissance and the Protestant Reformation."},
        {q:"How did Friedrich Koenig's invention advance on Gutenberg's printing press?", a:"Koenig's steam-powered printing press, introduced in 1810, further industrialised media production, dramatically increasing printing efficiency so that some presses produced 3,000 pages per hour by the 1930s."},
        {q:"Why did daily newspapers rise in popularity in the 19th century?", a:"They catered to the urbanised American population, helping them navigate their rapidly changing world."},
        {q:"What did Benedict Anderson argue about the role of newspapers?", a:"He argued that newspapers fostered a sense of national identity among readers."},
        {q:"How did penny papers differ from traditional newspapers in the 1830s?", a:"Penny papers provided sensational news at low prices, making them forerunners of today's tabloids, unlike the more formal traditional newspapers."},
        {q:"How did radio revolutionise mass communication in the early 20th century?", a:"Radio became the first major non-print mass medium, allowing large audiences to listen to the same event simultaneously and giving advertisers a valuable platform to reach wide audiences."},
        {q:"How did newspapers have to adapt once radio and television emerged?", a:"Newspapers had to adapt to the new media landscape created by radio and television, competing by leaning into the durability and flexibility that print offered compared to the immediacy of broadcast media."},
        {q:"Compare the strengths of print media and broadcast media.", a:"Print media offered durability and flexibility, meaning it could be kept and revisited, while broadcast media provided immediacy, delivering information to audiences in real time."},
        {q:"What impact did the digital video recorder have on broadcast media in the late 1990s?", a:"It allowed audiences to pause and rewind live broadcasts, giving viewers more control over how they consumed broadcast content."},
        {q:"Describe the overall historical trajectory of communication media covered this week.", a:"Communication media evolved from Gutenberg's printing press through industrialised print production, to newspapers, to radio as the first major broadcast medium, and eventually to digital recording technologies that changed how audiences consumed broadcasts."},
        {q:"Why is media literacy listed as a key skill from this week's lesson?", a:"Understanding how different media types developed and function helps individuals critically evaluate the information various media present."},
        {q:"What role did radio play for advertisers specifically?", a:"Radio provided a valuable platform for advertisers to reach a wide audience simultaneously, which was a new capability compared to print alone."},
        {q:"How might the evolution of communication media affect personal interactions, based on this week's reflection questions?", a:"Each medium shapes how people receive and share information, influencing personal interactions and perceptions of social or political issues over time."},
        {q:"Why is being a critical consumer of media emphasised in this week's call to action?", a:"Because media shapes public perception, influences elections, and affects accountability and transparency, so critical consumption helps individuals engage responsibly with media."},
        {q:"What distinguishes the penny press era from earlier print journalism?", a:"The penny press offered cheaper, more sensational news aimed at a broader audience, differing from earlier, more expensive and formal newspapers."}
      ]
    },
    {
      week: 5,
      topic: "Non-Verbal Communication Activity",
      mcq: [
        {q:"Non-verbal communication is described as crucial in:", opts:["Only written reports","Only formal contracts","Only statistical analysis","Storytelling"], a:3},
        {q:"Facial expressions are said to universally convey emotions such as:", opts:["Only happiness","Only sadness","Only confusion","Happiness, sadness, and anger"], a:3},
        {q:"Gestures are described as involving movements of:", opts:["Hands and arms to communicate messages","Only the feet","Only the eyes","Only the head"], a:0},
        {q:"Body language includes:", opts:["Posture and movements indicating various states","Only vocabulary choice","Only punctuation","Only written words"], a:0},
        {q:"Eye contact is said to convey:", opts:["Interest, attention, and involvement","Only confusion","Only hostility","Only boredom"], a:0},
        {q:"Touch is described as communicating:", opts:["Only distance","Only aggression","Affection, sympathy, and support","Only formality"], a:2},
        {q:"Proxemics refers to:", opts:["Physical space, indicating intimacy, aggression, or formality","Facial symmetry","Vocal tone only","Written grammar"], a:0},
        {q:"In Japan, which gesture is highlighted as showing respect with varying depth and duration?", opts:["Saluting","Waving","Handshaking","Bowing"], a:3},
        {q:"Italians are noted for using which non-verbal communication style?", opts:["Minimal facial expression","Avoidance of eye contact","Expressive hand gestures","Silence only"], a:2},
        {q:"In India, 'Namaste' involves:", opts:["Avoiding physical gestures entirely","Bowing deeply from the waist","Pressing palms together as a respectful greeting","Shaking hands firmly"], a:2},
        {q:"In the US, maintaining eye contact is said to signal:", opts:["Disrespect","Aggression only","Confidence and attentiveness","Indifference"], a:2},
        {q:"Non-verbal cues enhance storytelling by:", opts:["Eliminating the need for context","Confusing the audience intentionally","Replacing all spoken words","Conveying emotions and engaging the audience"], a:3},
        {q:"Which group activity is mentioned as helping practise non-verbal communication?", opts:["\"Silent Storytellers\"","\"Debate Club\"","\"Quiz Night\"","\"Spelling Bee\""], a:0},
        {q:"Matching gestures to meanings is said to improve:", opts:["Written grammar skills","Vocabulary memorisation","Understanding of non-verbal cues","Typing speed"], a:2},
        {q:"What mainly influences the specific methods used in non-verbal communication, according to this week's material?", opts:["Cultural norms","Font choice","Internet speed","Weather conditions"], a:0}
      ],
      fib: [
        {q:"Non-verbal communication is crucial in __________.", a:"storytelling"},
        {q:"Facial expressions universally convey emotions like happiness, sadness, and __________.", a:"anger"},
        {q:"__________ involve movements of hands and arms to communicate messages.", a:"Gestures"},
        {q:"Body language includes __________ and movements indicating various states.", a:"posture"},
        {q:"Eye contact conveys interest, attention, and __________.", a:"involvement"},
        {q:"__________ communicates affection, sympathy, and support.", a:"Touch"},
        {q:"__________, or physical space, indicates intimacy, aggression, or formality.", a:"Proxemics"},
        {q:"In Japan, __________ shows respect with varying depth and duration.", a:"bowing"},
        {q:"Italians use expressive hand __________ as part of their communication style.", a:"gestures"},
        {q:"In India, '__________' involves pressing palms together as a respectful greeting.", a:"Namaste"},
        {q:"In the US, maintaining eye contact signals __________ and attentiveness.", a:"confidence"},
        {q:"Non-verbal cues enhance storytelling by conveying __________ and engaging the audience.", a:"emotions"},
        {q:"Group activities like \"Silent __________\" help practise non-verbal communication.", a:"Storytellers"},
        {q:"Matching gestures to meanings improves understanding of __________ cues.", a:"non-verbal"},
        {q:"Cultural __________ influence non-verbal communication methods.", a:"norms"}
      ],
      short: [
        {q:"Why is non-verbal communication described as crucial in storytelling?", a:"Non-verbal cues such as facial expressions, gestures, and body language convey emotions and engage the audience, adding depth to the story being told."},
        {q:"Give examples of universal emotions conveyed through facial expressions.", a:"Facial expressions universally convey emotions such as happiness, sadness, and anger."},
        {q:"What is the difference between gestures and body language as discussed this week?", a:"Gestures involve specific movements of the hands and arms to communicate messages, while body language more broadly includes posture and movements that indicate various emotional or mental states."},
        {q:"What does eye contact typically convey in communication?", a:"Eye contact conveys interest, attention, and involvement in the interaction."},
        {q:"Explain the concept of proxemics and what it signals.", a:"Proxemics refers to the use of physical space in communication; the distance maintained between people can indicate intimacy, aggression, or formality."},
        {q:"How do cultural norms shape non-verbal communication, with examples from this week's material?", a:"Cultural norms shape specific non-verbal practices — for example, bowing shows respect in Japan, 'Namaste' is a respectful greeting in India, and Italians often use expressive hand gestures."},
        {q:"How does maintaining eye contact differ in meaning between cultures, based on the US example given?", a:"In the US, maintaining eye contact signals confidence and attentiveness, though this meaning can vary in other cultural contexts."},
        {q:"What was the purpose of the 'Silent Storytellers' group activity?", a:"It helped participants practise conveying and interpreting stories using only non-verbal communication, without spoken words."},
        {q:"Why is touch considered an important form of non-verbal communication?", a:"Touch communicates affection, sympathy, and support, conveying emotional connection without words."},
        {q:"How can understanding non-verbal cues improve storytelling ability?", a:"Understanding non-verbal cues allows a communicator to use facial expressions, gestures, and body language intentionally, making stories more emotionally engaging and easier to follow."},
        {q:"Why is matching gestures to meanings considered a valuable exercise?", a:"It helps learners improve their understanding and accurate interpretation of non-verbal cues in real communication settings."},
        {q:"What role does body language play beyond posture?", a:"Body language includes posture and other bodily movements that indicate a person's emotional or mental state during communication."},
        {q:"Why should communicators be mindful of cultural differences in non-verbal communication?", a:"Because gestures and non-verbal cues can carry different meanings across cultures, being mindful helps avoid misunderstanding and shows respect for cultural differences."},
        {q:"What is one way non-verbal communication enhances storytelling specifically?", a:"It engages the audience more fully by conveying emotion and nuance that words alone might not capture."},
        {q:"Summarise the main categories of non-verbal communication covered this week.", a:"The main categories are facial expressions, gestures, body language, eye contact, touch, and proxemics, all shaped by cultural norms."}
      ]
    },
    {
      week: 6,
      topic: "Verbal Communication Activity",
      mcq: [
        {q:"Presentation speeches are described as powerful tools for addressing:", opts:["Societal issues","Only personal hobbies","Only sports results","Only entertainment news"], a:0},
        {q:"Identifying societal concerns involves observing issues at which levels?", opts:["Only community level","Community, national, and global levels","Only national level","Only global level"], a:1},
        {q:"Effective research for a presentation should use:", opts:["Only personal opinions","Only outdated sources","No sources at all","Credible sources and real-life examples"], a:3},
        {q:"What should a presentation begin with to capture attention?", opts:["The conclusion","A hook","A list of references","A long disclaimer"], a:1},
        {q:"How should the main body of a presentation be organised?", opts:["Only with personal anecdotes","Without any supporting evidence","Logically, supporting points with evidence and examples","Randomly, without structure"], a:2},
        {q:"A strong conclusion should include:", opts:["A summary of main points and a strong call to action","An unrelated topic change","No summary at all","New information not mentioned before"], a:0},
        {q:"Why should new information be avoided in the conclusion?", opts:["To avoid a call to action","To confuse the audience","To maintain clarity","To make the speech longer"], a:2},
        {q:"What helps maintain audience interest during a speech?", opts:["Voice modulation and varying pace","Speaking in a monotone voice","Reading directly from notes only","Avoiding eye contact"], a:0},
        {q:"Using body language and eye contact helps a speaker appear:", opts:["Distracted","Unprepared","Disinterested","Confident and engaging"], a:3},
        {q:"Visual aids in a presentation should:", opts:["Contain as much text as possible","Enhance, not distract from, the presentation","Replace the speaker entirely","Be avoided at all costs"], a:1},
        {q:"What should a speaker do to prepare for a Q&A session?", opts:["Refuse to answer any questions","Avoid thinking about questions beforehand","Only prepare for easy questions","Anticipate potential questions and prepare answers in advance"], a:3},
        {q:"When responding to questions during Q&A, a speaker should:", opts:["Interrupt the questioner","Ignore difficult questions","Respond professionally, maintaining a respectful tone","Respond defensively"], a:2},
        {q:"If faced with a challenging question, a speaker should:", opts:["Stay calm and redirect to the main message","Change the topic entirely","Avoid answering at all","Panic and end the presentation"], a:0},
        {q:"What helps improve presentation skills over time, according to this week's material?", opts:["Practising regularly and staying informed about current events","Never researching current events","Memorising a script word-for-word only","Avoiding all practice"], a:0},
        {q:"What is the overall purpose of presentation speeches emphasised this week?", opts:["To avoid audience interaction","To engage and inspire audiences about societal issues","To fill allotted class time","To showcase visual aids only"], a:1}
      ],
      fib: [
        {q:"Presentation speeches are powerful tools for addressing __________ issues.", a:"societal"},
        {q:"Identifying societal concerns involves observing community, national, and __________ issues.", a:"global"},
        {q:"Effective research is crucial, using credible sources and __________ examples.", a:"real-life"},
        {q:"Start your presentation with a __________ to capture attention.", a:"hook"},
        {q:"Organise the main body logically, supporting points with evidence and __________.", a:"examples"},
        {q:"Conclude with a summary of main points and a strong call to __________.", a:"action"},
        {q:"Avoid introducing new information in the conclusion to maintain __________.", a:"clarity"},
        {q:"Voice __________ and varying pace help maintain audience interest.", a:"modulation"},
        {q:"Use body language and eye contact to appear __________ and engage the audience.", a:"confident"},
        {q:"Visual aids should enhance, not __________ from, the presentation.", a:"distract"},
        {q:"__________ potential questions and prepare answers in advance.", a:"Anticipate"},
        {q:"Respond to questions professionally, maintaining a respectful __________.", a:"tone"},
        {q:"Stay calm and __________ to your main message when faced with challenging questions.", a:"redirect"},
        {q:"Practise regularly and stay informed about current __________ to improve presentation skills.", a:"events"},
        {q:"Selecting a relevant and __________ topic is key for a compelling presentation.", a:"meaningful"}
      ],
      short: [
        {q:"Why are presentation speeches described as powerful tools for addressing societal issues?", a:"They allow a speaker to raise awareness, inform an audience, and inspire action on community, national, or global concerns."},
        {q:"How should a speaker go about identifying a societal concern to present on?", a:"By observing community, national, and global issues and selecting a topic that is both relevant to society and personally meaningful to the speaker."},
        {q:"What makes research effective when preparing a presentation?", a:"Using credible sources and real-life examples strengthens the presentation's credibility and relevance."},
        {q:"Describe the recommended structure of a presentation from opening to close.", a:"Start with a hook to capture attention, organise the main body logically with evidence and examples, and conclude with a summary of main points and a strong call to action."},
        {q:"Why should a speaker avoid introducing new information in the conclusion?", a:"Introducing new information at the end can confuse the audience and undermine the clarity of the overall message."},
        {q:"What techniques help a speaker maintain audience interest throughout a presentation?", a:"Voice modulation, varying pace, confident body language, and consistent eye contact all help keep the audience engaged."},
        {q:"What is the proper role of visual aids in a presentation?", a:"Visual aids should enhance the presentation and support the spoken content, not distract from or overwhelm it."},
        {q:"How should a speaker prepare for a question-and-answer session?", a:"By anticipating potential questions in advance and preparing thoughtful answers, so they are not caught off guard."},
        {q:"How should a speaker handle a challenging or difficult question during Q&A?", a:"They should stay calm, respond professionally and respectfully, and redirect the discussion back to their main message."},
        {q:"What ongoing practices help a speaker continue improving their presentation skills?", a:"Practising regularly and staying informed about current events helps speakers keep their skills sharp and their content relevant."},
        {q:"Why is selecting a relevant and meaningful topic described as key to a compelling presentation?", a:"A topic that matters both to society and to the speaker personally is more likely to resonate with and engage the audience."},
        {q:"What is the purpose of a 'hook' at the start of a presentation?", a:"A hook is used to immediately capture the audience's attention before the main content of the presentation begins."},
        {q:"How does organising the main body logically benefit a presentation?", a:"It helps the audience follow the argument clearly, as each point is supported by evidence and examples in a coherent sequence."},
        {q:"What is the function of a call to action at the end of a presentation?", a:"It encourages the audience to take a specific next step in response to the issue that was presented."},
        {q:"Summarise the key skills this week's lesson aims to build.", a:"The lesson builds public speaking, structuring presentations, audience engagement, handling Q&A sessions, research skills, and effective communication overall."}
      ]
    }
  ]
},
{
  code: "MCM 107",
  title: "Introduction to Photojournalism",
  weeks: [
    {
      week: 1,
      topic: "Introduction to Photojournalism",
      mcq: [

    {q:"How is photojournalism defined this week?", opts:["The art of telling stories through photographs","A purely technical camera-operating skill","Editing photographs for advertising purposes","Capturing images with no narrative intent"], a:0},
    {q:"Which three characteristics are named as essential to photojournalism?", opts:["Speed, cost, popularity","Relevance, objectivity, narrative","Color, composition, exposure","Bias, speed, drama"], a:1},
    {q:"What does \"objectivity\" mean in photojournalism, per this week's material?", opts:["Choosing only dramatic or shocking images","Capturing events without bias, presenting a clear window into the world","Editing images to fit a predetermined narrative","Avoiding all controversial subjects"], a:1},
    {q:"What does \"narrative\" mean in photojournalism, per this week's material?", opts:["Adding captions with opinions","Combining visual elements with context to tell a story","Using only black-and-white photography","Avoiding any accompanying text"], a:1},
    {q:"What does \"photojournalism makes the invisible visible\" refer to?", opts:["Using infrared cameras","Revealing realities or perspectives that might otherwise go unnoticed","Photographing only nighttime events","Editing out visible subjects"], a:1},
    {q:"Which of these is listed as a professional practice required for mastering photojournalism?", opts:["Avoiding ethical guidelines for faster results","Dedicated practice and ethical standards","Relying solely on inherited talent","Working exclusively in studio settings"], a:1},
    {q:"Why are ethical guidelines described as crucial in photojournalism?", opts:["They are legally optional but socially expected","To respect subjects and maintain integrity","They only apply to conflict photography","They are irrelevant to professional practice"], a:1},
    {q:"What can a single powerful photograph affect, per this week's material?", opts:["Only the photographer's personal reputation","Emotions and public understanding/perspective","Nothing beyond aesthetic appreciation","Only technical camera settings"], a:1},
    {q:"Besides news events, what kind of issues can photojournalism highlight?", opts:["Environmental issues and human costs of crises","Only celebrity culture","Only sports outcomes","Only fictional storytelling"], a:0},
    {q:"What tension does this week's personal reflection prompt raise?", opts:["Between technical skill and artistic style","Between the urgency of capturing a moment and ethical considerations","Between color and black-and-white photography","Between print and digital publishing formats"], a:1},
    {q:"What does photojournalism document for future generations, per this week's material?", opts:["Only celebrity events","History","Only sports scores","Only weather patterns"], a:1},
    {q:"What does this week's material say photojournalism provides into others' lives?", opts:["No real value","Insight and understanding","Only entertainment value","Legal documentation only"], a:1},
    {q:"What two activities does this week's Call to Action suggest?", opts:["Only a written essay","A photo analysis exercise and a photojournalist interview","Only a group debate","Only a quiz"], a:1},
    {q:"What is each photograph described as, in this week's personal reflection?", opts:["A distraction from real reporting","A gateway to broader understanding and empathy","A purely commercial product","An outdated form of storytelling"], a:1},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Visual storytelling","Narrative construction","Cultural sensitivity","Database administration"], a:3}
      ],
      fib: [

    {q:"Photojournalism is the art of telling stories through __________.", a:"photographs"},
    {q:"The three essential characteristics of photojournalism are relevance, objectivity, and __________.", a:"narrative"},
    {q:"__________ means capturing events without bias, presenting a clear window into the world.", a:"Objectivity"},
    {q:"Narrative involves combining visual elements with __________ to tell a story.", a:"context"},
    {q:"Photojournalism makes the __________ visible and the silent heard.", a:"invisible"},
    {q:"Professional practices in photojournalism include dedicated practice, __________ standards, and narrative skill.", a:"ethical"},
    {q:"Mastery in photojournalism comes from years of capturing moments and __________ the craft.", a:"refining"},
    {q:"Photojournalism can highlight environmental issues and the human __________ of crises.", a:"costs"},
    {q:"The power of a single __________ can be transformative.", a:"image"},
    {q:"Photojournalism affects __________ in ways words cannot.", a:"emotions"},
    {q:"Photojournalism documents __________ for future generations.", a:"history"},
    {q:"Photojournalism provides __________ and understanding into others' lives.", a:"insight"},
    {q:"This week's Call to Action includes a Photo Analysis Exercise and a Photojournalist __________.", a:"Interview"},
    {q:"Each photograph is described as a __________ to broader understanding and empathy.", a:"gateway"},
    {q:"Photojournalism broadens perspectives by showing struggles and __________ of others.", a:"triumphs"}
      ],
      short: [

    {q:"What is photojournalism defined as this week?", a:"The art of telling stories through photographs."},
    {q:"Name the three essential characteristics of photojournalism covered this week.", a:"Relevance, objectivity, and narrative."},
    {q:"Explain \"objectivity\" as it applies to photojournalism.", a:"Capturing events without bias, presenting a clear window into the world."},
    {q:"Explain \"narrative\" as it applies to photojournalism.", a:"Combining visual elements with context to tell a story."},
    {q:"What does \"photojournalism makes the invisible visible\" mean?", a:"It reveals realities or perspectives that might otherwise go unnoticed or unheard."},
    {q:"Name two professional practices required to master photojournalism.", a:"Any 2 of: dedicated practice, ethical standards, narrative skill."},
    {q:"Why are ethical guidelines described as crucial in this field?", a:"To respect subjects and maintain integrity."},
    {q:"What two things can a single powerful image affect?", a:"Emotions and public understanding/perspective."},
    {q:"What kind of issues can photojournalism highlight, besides news events?", a:"Environmental issues and the human costs of crises."},
    {q:"What tension does the personal reflection prompt raise about photojournalists' work?", a:"Balancing the urgency of capturing a moment against the ethical responsibility toward the subject."},
    {q:"What does photojournalism provide into others' lives, per this week's material?", a:"Insight and understanding."},
    {q:"What does photojournalism document for future generations?", a:"History."},
    {q:"Name the two activities suggested in this week's Call to Action.", a:"A Photo Analysis Exercise, and a Photojournalist Interview."},
    {q:"What is each photograph described as, in this week's personal reflection?", a:"A gateway to broader understanding and empathy."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: visual storytelling, ethical judgement, technical proficiency, critical analysis, narrative construction, cultural sensitivity."}
      ]
    },
    {
      week: 2,
      topic: "The Camera and Photography Basics",
      mcq: [
    {q:"What can photography do, per this week's material?", opts:["Transport, inspire, and tell stories","Only record evidence","Only produce art for sale","Only document weather"], a:0},
    {q:"What are the two main camera types, per this week's material?", opts:["Film and digital","Analog and mechanical","Compact and bridge","DSLR and mirrorless only"], a:0},
    {q:"What does the camera lens do, per this week's material?", opts:["Gathers and focusses light onto the image sensor","Stores captured images","Controls the battery","Displays the image after capture"], a:0},
    {q:"What does the shutter control, per this week's material?", opts:["Light entering the camera, affecting exposure and motion effects","The camera's battery life","The lens focal length","The memory card capacity"], a:0},
    {q:"What does aperture control, per this week's material?", opts:["Light entry and depth of field","Only the shutter speed","Only the ISO setting","Only the flash output"], a:0},
    {q:"What are viewfinders, and name the two types mentioned?", opts:["They show the scene to be captured; optical and electronic","They store images; SD and CF","They control exposure; manual and auto","They adjust focus; single and continuous"], a:0},
    {q:"What are compact cameras ideal for, per this week's material?", opts:["Beginners, with automatic settings and fixed lenses","Professional sports photography","Astrophotography only","Underwater filming only"], a:0},
    {q:"What distinguishes bridge cameras, per this week's material?", opts:["Manual controls with smaller sensors than DSLRs","No manual controls at all","Only automatic settings","Only waterproof casing"], a:0},
    {q:"What distinguishes mirrorless cameras, per this week's material?", opts:["Compact design with electronic viewfinders","Only optical viewfinders","Larger size than DSLRs","No viewfinder at all"], a:0},
    {q:"What are action cameras ideal for, per this week's material?", opts:["Rugged, waterproof use, capturing action","Studio portraits only","Low-light astrophotography only","Static landscape shots only"], a:0},
    {q:"What do 360 cameras capture, per this week's material?", opts:["Full 360-degree views for immersive images and videos","Only panoramic stills","Only underwater footage","Only macro close-ups"], a:0},
    {q:"What advantage do smartphone cameras offer for photojournalism, per this week's material?", opts:["Immediacy and accessibility","The highest possible image resolution always","Unlimited battery life","Professional-grade optical zoom only"], a:0},
    {q:"What does ethical storytelling in photography respect, per this week's material?", opts:["Subjects' dignity and story authenticity","Only the photographer's artistic vision","Only commercial interests","Only technical perfection"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Technical proficiency","Ethical storytelling","Cultural sensitivity","Financial accounting"], a:3},
    {q:"What question does this week's Personal Reflection raise about smartphone photography?", opts:["How to maintain photojournalism's ethical standards and narrative depth in an age of ubiquitous cameras","Whether smartphones should be banned from journalism","Why film cameras are superior","How to reduce camera costs"], a:0}
      ],
      fib: [
    {q:"Photography can transport, inspire, and tell __________.", a:"stories"},
    {q:"The two main camera types are film and __________.", a:"digital"},
    {q:"The __________ gathers and focusses light onto the image sensor.", a:"lens"},
    {q:"The __________ controls light entering the camera, affecting exposure and motion effects.", a:"shutter"},
    {q:"__________ controls light entry and depth of field.", a:"Aperture"},
    {q:"Viewfinders show the scene to be captured; types include optical and __________.", a:"electronic"},
    {q:"__________ cameras are ideal for beginners, with automatic settings and fixed lenses.", a:"Compact"},
    {q:"__________ cameras offer manual controls with smaller sensors than DSLRs.", a:"Bridge"},
    {q:"__________ cameras are compact with electronic viewfinders.", a:"Mirrorless"},
    {q:"__________ cameras are rugged, waterproof, and ideal for capturing action.", a:"Action"},
    {q:"360 cameras capture full __________-degree views for immersive images and videos.", a:"360"},
    {q:"Smartphone cameras offer __________ and accessibility for photojournalism.", a:"immediacy"},
    {q:"Ethical storytelling respects subjects' __________ and story authenticity.", a:"dignity"},
    {q:"__________ learning and portfolio building are crucial for growth in photojournalism.", a:"Continuous"},
    {q:"One skill gained this week is camera __________.", a:"operation"}
      ],
      short: [
    {q:"What can photography do, per this week's material?", a:"Transport, inspire, and tell stories."},
    {q:"What are the two main camera types, and how do they differ?", a:"Film and digital — film cameras use light-sensitive film, while digital cameras use electronic image sensors."},
    {q:"What do the lens, shutter, and aperture each control?", a:"The lens gathers and focusses light onto the sensor; the shutter controls light entering the camera (exposure/motion); the aperture controls light entry and depth of field."},
    {q:"Name three camera types mentioned this week, besides compact and bridge cameras.", a:"Any 3 of: mirrorless, action, 360, smartphone, DSLR cameras."},
    {q:"What are compact cameras and bridge cameras each suited for?", a:"Compact cameras suit beginners with automatic settings and fixed lenses; bridge cameras offer manual controls with smaller sensors than DSLRs."},
    {q:"What advantage do smartphone cameras offer for photojournalism?", a:"Immediacy and accessibility."},
    {q:"What does ethical storytelling in photography require, per this week's material?", a:"Respecting subjects' dignity and story authenticity."},
    {q:"How has the rise of smartphone photography influenced photojournalism, per this week's reflection?", a:"It has democratised photography, letting anyone capture and share moments, raising questions about the role of professional photojournalists."},
    {q:"What does this week's Call to Action's Time-lapse Project ask students to do?", a:"Create a time-lapse video of a changing scene and discuss how the technique can be used in photojournalism."},
    {q:"What does this week's Gear vs. Skill Debate ask students to consider?", a:"Whether expensive camera equipment makes a better photojournalist, weighing technical capability against storytelling ability."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: technical proficiency, ethical storytelling, visual composition, adaptability, cultural sensitivity, camera operation."},
    {q:"What question does this week's Personal Reflection raise?", a:"How to ensure photojournalism's ethical standards, objectivity, and narrative depth are maintained in an age of ubiquitous cameras."},
    {q:"Name two key references cited this week.", a:"Baetens, J., & Sánchez-Mesa, D. (2023) Photojournalism and Beyond; Galer, M. (2012) Digital Photography: Essential Skills."},
    {q:"What do image sensors and autofocus systems ensure, per this week's material?", a:"Clear, sharp images."},
    {q:"Where are captured images and videos stored, per this week's material?", a:"On memory cards, via memory card slots."}
      ]
    },
    {
      week: 3,
      topic: "Advanced Camera Techniques",
      mcq: [
    {q:"What is photojournalism about, per this week's material?", opts:["Freezing time and conveying emotions","Only technical precision","Only speed of publication","Only equipment cost"], a:0},
    {q:"What does low-light photography require adjusting?", opts:["ISO, aperture, and shutter speed","Only the lens type","Only the memory card","Only the camera strap"], a:0},
    {q:"What does a higher ISO setting do, per this week's material?", opts:["Increases light sensitivity but may introduce noise","Decreases light sensitivity entirely","Has no effect on image quality","Only affects colour saturation"], a:0},
    {q:"What trade-off comes with wider apertures, per this week's material?", opts:["They let in more light but reduce depth of field","They reduce light but increase depth of field","They have no effect on exposure","They only work in bright light"], a:0},
    {q:"What trade-off comes with slower shutter speeds, per this week's material?", opts:["They allow more light but may cause blur","They allow less light but prevent all blur","They have no effect on exposure","They only work with flash"], a:0},
    {q:"What helps avoid camera shake, per this week's material?", opts:["Tripods or image stabilisation","Higher ISO alone","A wider aperture alone","A faster shutter speed alone"], a:0},
    {q:"What challenges does harsh sunlight present, per this week's material?", opts:["Strong shadows and washed-out colours","No challenges at all","Only reduced battery life","Only lens fogging"], a:0},
    {q:"What do lens hoods help prevent, per this week's material?", opts:["Lens flare in bright conditions","Camera shake","Low battery drain","Memory card corruption"], a:0},
    {q:"What does the Sunny 16 rule help with, per this week's material?", opts:["Balancing exposure in bright light","Balancing exposure in low light only","Adjusting white balance indoors","Setting video frame rates"], a:0},
    {q:"What do rain or fog add to photos, per this week's material?", opts:["Drama","Only technical difficulty with no benefit","Nothing of value","Only risk to the photographer"], a:0},
    {q:"What is crucial for indoor photography, per this week's material?", opts:["White balance adjustment for accurate colours","Avoiding all artificial light","Using only natural light","Using only black-and-white mode"], a:0},
    {q:"What can soften harsh indoor lighting, per this week's material?", opts:["Bounce flash or diffusers","Higher shutter speed alone","A wider lens alone","A longer exposure alone"], a:0},
    {q:"What does colour temperature influence, per this week's material?", opts:["The mood and feel of images","Only the file size","Only the camera's battery life","Only the memory card speed"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Technical adaptability","Environmental awareness","Composition mastery","Financial auditing"], a:3},
    {q:"What question does this week's Personal Reflection raise about emerging photojournalists?", opts:["How they can continue to innovate and push the boundaries of visual storytelling","Whether photojournalism will disappear entirely","Why black-and-white photography is obsolete","How to reduce equipment costs"], a:0}
      ],
      fib: [
    {q:"Photojournalism captures raw, unfolding __________.", a:"moments"},
    {q:"Low-light photography requires adjusting ISO, aperture, and shutter __________.", a:"speed"},
    {q:"Higher ISO increases light sensitivity but may introduce __________.", a:"noise"},
    {q:"Wider apertures let in more light but reduce depth of __________.", a:"field"},
    {q:"Slower shutter speeds allow more light but may cause __________.", a:"blur"},
    {q:"__________ or image stabilisation help avoid camera shake.", a:"Tripods"},
    {q:"Harsh sunlight presents challenges like strong shadows and washed-out __________.", a:"colours"},
    {q:"Lens __________ help prevent lens flare in bright conditions.", a:"hoods"},
    {q:"The Sunny __________ rule helps balance exposure in bright light.", a:"16"},
    {q:"__________ balance adjustment is crucial for accurate colours indoors.", a:"White"},
    {q:"Bounce flash or __________ can soften harsh indoor lighting.", a:"diffusers"},
    {q:"__________ temperature influences the mood and feel of images.", a:"Colour"},
    {q:"Light modifiers help control the shape, direction, and __________ of light.", a:"quality"},
    {q:"Manual __________ may be necessary in challenging weather.", a:"focus"},
    {q:"One skill gained this week is __________ awareness (regarding conditions like lighting and weather).", a:"environmental"}
      ],
      short: [
    {q:"How does the emotional impact of an image change with different lighting conditions?", a:"Different lighting (low-light, harsh sunlight, indoor) changes mood, texture, contrast, and shadow, which affects how emotionally impactful an image feels."},
    {q:"What three camera settings must be adjusted for low-light photography?", a:"ISO, aperture, and shutter speed."},
    {q:"What trade-off comes with a higher ISO setting?", a:"It increases light sensitivity but may introduce noise."},
    {q:"What trade-offs come with wider apertures and slower shutter speeds?", a:"Wider apertures let in more light but reduce depth of field; slower shutter speeds allow more light but may cause blur."},
    {q:"What challenges does harsh sunlight present, and how can photographers manage them?", a:"Strong shadows and washed-out colours; managed using lens hoods and the Sunny 16 rule."},
    {q:"What is crucial for accurate colours in indoor photography?", a:"White balance adjustment."},
    {q:"How can harsh indoor lighting be softened, per this week's material?", a:"Using bounce flash or diffusers."},
    {q:"What does colour temperature influence in photography?", a:"The mood and feel of images."},
    {q:"What ethical considerations should photojournalists keep in mind when manipulating lighting?", a:"Ensuring the authenticity of the scene is preserved even while adjusting technical settings for impact."},
    {q:"What does this week's Low Light Mastery photo challenge ask students to do?", a:"Capture a series of photos in low-light conditions, experimenting with ISO, aperture, and shutter speed."},
    {q:"What does this week's Sunlight and Shadows assignment ask students to do?", a:"Take photographs in harsh midday sun using lens hoods, the Sunny 16 rule, and diffusers to manage light."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: technical adaptability, creative composition, ethical photography, environmental awareness, composition mastery, storytelling through visuals."},
    {q:"What question does this week's Personal Reflection raise about emerging photojournalists?", a:"How they can continue to innovate and push the boundaries of visual storytelling in an increasingly saturated media landscape."},
    {q:"Name this week's key references.", a:"Freeman, M. (2007) The Photographer's Eye; Peterson, B. (2016) Understanding Exposure, Fourth Edition."},
    {q:"What can protect gear and help photographers work in adverse weather, per this week's material?", a:"Protecting gear is crucial, and manual focus may be necessary in challenging weather conditions."}
      ]
    },
    {
      week: 4,
      topic: "Visual Storytelling",
      mcq: [
        {q:"Visual storytelling in photojournalism primarily involves:", opts:["Avoiding any editing of photos","Publishing photos without context","Writing long captions only","Using images to convey narratives"], a:3},
        {q:"The classic story arc used in visual storytelling comprises which three parts?", opts:["Beginning, middle, and end","Hook, body, hashtag","Introduction, climax, credits","Setup, twist, montage"], a:0},
        {q:"What does character development do in a photo story?", opts:["Shortens the narrative","Replaces the need for setting","Enhances story complexity","Removes emotional depth"], a:2},
        {q:"Setting, in a visual story, mainly provides:", opts:["The resolution","A caption","The lighting equipment list","Context and atmosphere"], a:3},
        {q:"What role does conflict play in a photo story?", opts:["It closes the story","It drives the story and heightens drama","It replaces composition","It is irrelevant to photojournalism"], a:1},
        {q:"Resolution in a photo story is important because it:", opts:["Removes the need for a beginning","Offers closure and imparts lessons","Is optional and rarely used","Introduces new conflict"], a:1},
        {q:"Which visual element is described as setting mood and evoking emotions?", opts:["Caption length","Colour","Camera brand","File size"], a:1},
        {q:"Lighting in photojournalism mainly shapes:", opts:["The story's publication date","Atmosphere and visual impact","The photographer's byline","The caption word count"], a:1},
        {q:"Composition refers to:", opts:["Arranging visual elements within a frame","The reporter's travel schedule","Audio recording levels","Editing software settings"], a:0},
        {q:"How does perspective function in a photo story?", opts:["It affects audience perception and connection","It determines the publication's logo","It only matters for black-and-white photos","It has no effect on viewers"], a:0},
        {q:"Why is topic selection described as crucial?", opts:["It replaces the need for editing","It is crucial for engaging photo stories","It only affects the photographer's pay","It is unrelated to audience interest"], a:1},
        {q:"What is the purpose of storyboarding in photo story creation?", opts:["It structures the photo story flow","It replaces the need for research","It deletes unwanted images","It is used only for video, never photos"], a:0},
        {q:"A wide shot in a photo story is mainly used to:", opts:["Highlight fine emotional details","Balance background and subject focus equally","Set scene context","Replace the need for a close-up"], a:2},
        {q:"What is the function of close-up shots?", opts:["They set broad scene context","They are used only for landscapes","They highlight details and emotions","They replace sequencing"], a:2},
        {q:"Which activity is described as boosting the visibility of a photo story?", opts:["Deleting storyboards","Avoiding all platforms","Removing captions","Social media utilisation"], a:3}
      ],
      fib: [
        {q:"Visual storytelling involves using __________ to convey narratives.", a:"images"},
        {q:"The story arc comprises beginning, __________, and end.", a:"middle"},
        {q:"__________ development enhances story complexity.", a:"Character"},
        {q:"Setting provides __________ and atmosphere.", a:"context"},
        {q:"__________ drives the story and heightens drama.", a:"Conflict"},
        {q:"Resolution offers closure and imparts __________.", a:"lessons"},
        {q:"__________ sets mood and evokes emotions.", a:"Colour"},
        {q:"Lighting shapes __________ and visual impact.", a:"atmosphere"},
        {q:"__________ arranges visual elements within a frame.", a:"Composition"},
        {q:"Perspective affects audience __________ and connection.", a:"perception"},
        {q:"__________ shots set scene context.", a:"Wide"},
        {q:"__________ shots balance background and subject focus.", a:"Medium"},
        {q:"Close-up shots highlight details and __________.", a:"emotions"},
        {q:"__________ involves selecting the finest images.", a:"Editing"},
        {q:"__________ arranges images for effective narration.", a:"Sequencing"}
      ],
      short: [
        {q:"Describe the three-part structure of a classic story arc in visual storytelling.", a:"The story arc comprises a beginning, a middle, and an end, giving a photo story a complete narrative shape."},
        {q:"Why does character development matter in a photo essay?", a:"It adds complexity and depth to the story, helping viewers connect with the individuals depicted."},
        {q:"What is the role of setting in visual storytelling?", a:"Setting provides context and atmosphere that frame the story for the viewer."},
        {q:"How does conflict function within a photo story?", a:"Conflict drives the story forward and heightens its dramatic tension."},
        {q:"What does resolution contribute to a photo story?", a:"It offers closure to the narrative and imparts a lesson or takeaway to the viewer."},
        {q:"Explain how colour and lighting work together in visual storytelling.", a:"Colour sets the mood and evokes emotion, while lighting shapes the atmosphere and overall visual impact of the image."},
        {q:"What is composition in the context of photojournalism, and why does it matter?", a:"Composition is the arrangement of visual elements within a frame; it guides the viewer's eye and strengthens the story's impact."},
        {q:"Why is topic selection described as crucial to engaging photo stories?", a:"A well-chosen topic ensures the story is relevant and compelling, which keeps the audience engaged."},
        {q:"What is the purpose of storyboarding before shooting a photo story?", a:"Storyboarding structures the flow of the photo story in advance, helping the photographer plan the narrative sequence."},
        {q:"Distinguish between wide shots, medium shots, and close-up shots.", a:"Wide shots set scene context, medium shots balance background with subject focus, and close-up shots highlight details and emotions."},
        {q:"What does editing involve in the visual storytelling process?", a:"Editing involves selecting the finest images from those captured to best tell the story."},
        {q:"Why is sequencing important after editing?", a:"Sequencing arranges the selected images in an order that supports effective narration."},
        {q:"How does narrative structure guide a photo story?", a:"It follows a logical story arc so that images build on one another coherently."},
        {q:"Why should a photojournalist balance different shot types in a single story?", a:"Balancing shot types maintains viewer engagement by varying scale and focus throughout the story."},
        {q:"What steps help a photo story perform well once published, according to the week's summary?", a:"Customising content for the platform, using social media, collaborating with others, and tracking performance all help extend a story's reach and effectiveness."}
      ]
    },
    {
      week: 5,
      topic: "Writing for Photojournalism",
      mcq: [
        {q:"In photojournalism, writing primarily serves to provide:", opts:["Only the photographer's name","Context, background, and interpretation","Background music suggestions","A replacement for all images"], a:1},
        {q:"Which three written elements complement visual tales in photojournalism?", opts:["Headlines, bylines, and footnotes","Hashtags, likes, and shares","Captions, stories, and narratives","Credits, dates, and file names"], a:2},
        {q:"A caption is best described as:", opts:["A copyright notice","A brief explanation accompanying a photograph","An audio transcript","A full-length feature article"], a:1},
        {q:"Captions typically provide context:", opts:["With heavy personal opinion","By replacing the photograph","Without interpretation","Only in a foreign language"], a:2},
        {q:"Which questions do effective captions typically answer?", opts:["None of these","Only When and Where","Only Who and What","Who, What, When, Where, and sometimes Why"], a:3},
        {q:"Stories, compared to captions, are described as:", opts:["Purely factual with no quotes","Shorter than captions","Irrelevant to photojournalism","Expanding on information with more detail and description"], a:3},
        {q:"Stories in photojournalism may include:", opts:["Only statistical tables","Quotes, anecdotes, or personal accounts","No reference to the subject","Only technical camera settings"], a:1},
        {q:"Unlike captions, stories typically answer:", opts:["The 'why' and 'how' questions","No questions at all","Only the 'where' question","Only the 'who' question"], a:0},
        {q:"A narrative in photojournalism arranges events:", opts:["Only in reverse chronological order","In a specific order","Randomly, with no order","Without reference to the photos"], a:1},
        {q:"What do narratives help create, according to the summary?", opts:["Flow and evoke emotions","A purely technical record","Confusion for the reader","A replacement for photographs"], a:0},
        {q:"Narratives explore themes, issues, or events:", opts:["Without connecting to photographs","Only superficially","In-depth","Only in bullet points"], a:2},
        {q:"In photojournalism writing, photographs are used as:", opts:["Visual evidence and emotional anchors","Replacements for all text","Background wallpaper only","Mere decoration with no purpose"], a:0},
        {q:"What is the first point of connection with the audience, according to this week's material?", opts:["The publication's logo","The photographer's biography","The printing press","Captions"], a:3},
        {q:"What does combining text with visuals achieve, per the summary?", opts:["It is unnecessary for most stories","It replaces the need for captions","It transforms understanding","It weakens emotional engagement"], a:2},
        {q:"The synergy between images and words is described as creating:", opts:["Silence","Confusion","Dialogue","Redundancy"], a:2}
      ],
      fib: [
        {q:"In photojournalism, writing provides context, background, and __________.", a:"interpretation"},
        {q:"Captions, stories, and __________ complement visual tales.", a:"narratives"},
        {q:"Captions are brief explanations accompanying __________.", a:"photographs"},
        {q:"Captions provide context without __________.", a:"interpretation"},
        {q:"Captions typically answer Who, What, When, Where, and sometimes __________.", a:"Why"},
        {q:"Stories expand on information presented in __________.", a:"captions"},
        {q:"Stories may include quotes, anecdotes, or personal __________.", a:"accounts"},
        {q:"Stories answer the 'why' and '__________' questions.", a:"how"},
        {q:"Narratives arrange events in a specific __________.", a:"order"},
        {q:"Narratives create flow and evoke __________.", a:"emotions"},
        {q:"Narratives use photographs as visual evidence and emotional __________.", a:"anchors"},
        {q:"__________ provide the initial connection with the audience.", a:"Captions"},
        {q:"Combining text with visuals __________ understanding.", a:"transforms"},
        {q:"Synergy between images and words creates __________.", a:"dialogue"},
        {q:"Photojournalists must convey underlying words with __________.", a:"integrity"}
      ],
      short: [
        {q:"What role does writing play in photojournalism?", a:"Writing provides context, background, and interpretation that complement the visual story told by the photographs."},
        {q:"Define a caption and explain what it typically answers.", a:"A caption is a brief explanation accompanying a photograph; it typically answers Who, What, When, Where, and sometimes Why, without offering interpretation."},
        {q:"How do stories differ from captions in photojournalism?", a:"Stories expand on the information in captions with more detail, description, quotes, or anecdotes, and they answer the 'why' and 'how' questions that captions leave out."},
        {q:"What is the function of a narrative in photojournalism writing?", a:"A narrative arranges events in a specific order to create flow, evoke emotion, and explore a theme or issue in depth."},
        {q:"How are photographs used within a written narrative?", a:"Photographs serve as visual evidence and emotional anchors that ground the narrative in reality."},
        {q:"Why is diversity in caption writing important?", a:"Different types of reporting call for different caption styles, so captions must be adapted to match the nature of the story being told."},
        {q:"Explain the synergy between images and words in photojournalism.", a:"Images and words work together, with captions making the first connection and narratives sustaining audience attention, creating a dialogue that transforms understanding."},
        {q:"What ethical responsibility do photojournalists have when writing about their images?", a:"They must convey the underlying story and words with integrity, ensuring accuracy and honesty in how the image is framed."},
        {q:"How does combining text with visuals affect audience engagement?", a:"It enhances emotional and intellectual engagement and helps capture and retain audience attention."},
        {q:"What kinds of material might a story include that a caption would not?", a:"A story may include quotes, anecdotes, or personal accounts that give more depth than a caption can provide."},
        {q:"Why are captions described as essential despite being brief?", a:"Captions provide the audience's initial point of connection to the image, quickly establishing the Who, What, When, and Where."},
        {q:"What is the bridging function of captions, stories, and narratives together?", a:"Together they bridge the gap between the viewer and the subject, giving the photograph meaning beyond what the image alone shows."},
        {q:"How does a narrative differ from a single caption in scope?", a:"A narrative explores themes, issues, or events in depth over an extended arrangement of events, while a caption is a brief, immediate explanation."},
        {q:"What is the risk if a photojournalist's writing is not handled with integrity?", a:"The written words could misrepresent the image's context, undermining the trust and accuracy that photojournalism depends on."},
        {q:"Why are captions, stories, and narratives together called essential tools of photojournalism?", a:"Because each plays a distinct role, together they give the audience the context, depth, and flow needed to fully understand and connect with a visual story."}
      ]
    },
    {
      week: 6,
      topic: "Portraiture and Interviews",
      mcq: [
        {q:"Portraiture in photojournalism is primarily described as capturing:", opts:["Equipment specifications","Group statistics only","An individual's personality, character, or life story","Only landscapes and buildings"], a:2},
        {q:"Which iconic photograph is cited as an example of powerful portraiture?", opts:["\"Earthrise\"","\"Migrant Mother\" by Dorothea Lange","\"Afghan Girl\" by an unnamed photographer","\"The Blue Marble\""], a:1},
        {q:"What does portraiture help viewers do, according to the summary?", opts:["Avoid emotional engagement","Connect with strangers' emotions and situations","Ignore the subject's context","Focus only on technical camera data"], a:1},
        {q:"Portraiture is described as humanising broad issues and fostering:", opts:["Competition","Empathy","Indifference","Confusion"], a:1},
        {q:"What can portraits create and preserve, per the material?", opts:["Printing schedules","Icons and collective memory","Advertising revenue","Only technical records"], a:1},
        {q:"Portraiture is said to amplify:", opts:["Marginalised voices","Only celebrity voices","Editorial deadlines","Advertiser messaging"], a:0},
        {q:"Which are listed as key technical aspects of portraiture?", opts:["Lighting, composition, and capturing the right moment","Only camera brand","Only printer resolution","Only file format"], a:0},
        {q:"Photo interviews combine:", opts:["Only written surveys","Only audio recordings","Visual and verbal narratives","Only statistical data"], a:2},
        {q:"Preparation for a photo interview involves:", opts:["Skipping research entirely","Only choosing camera settings","Research, setting objectives, and technical readiness","Avoiding all planning"], a:2},
        {q:"Why is building rapport described as crucial before a portrait session?", opts:["It is crucial for natural expressions","It only matters for group photos","It replaces the need for consent","It has no effect on the subject"], a:0},
        {q:"What type of questions elicit detailed personal stories during interviews?", opts:["Yes/no questions","Open-ended questions","Leading questions only","Rhetorical questions"], a:1},
        {q:"The post-interview process mainly involves:", opts:["Ignoring the interview content","Publishing without review","Deleting all images immediately","Selecting complementary photos and text"], a:3},
        {q:"Which is described as essential in portraiture and photo interviews?", opts:["Informed consent","Hiding the subject's identity","Using only staged images","Avoiding any permissions"], a:0},
        {q:"What must photojournalists maintain in representing subjects through portraiture?", opts:["Exaggeration","Secrecy","Indifference","Truthfulness"], a:3},
        {q:"What is described as the overall goal of portraiture in photojournalism?", opts:["Minimising subject involvement","Fostering connection between subject and audience","Avoiding emotional content","Maximising advertising clicks"], a:1}
      ],
      fib: [
        {q:"Portraiture captures individuals' personality, character, or __________.", a:"life story"},
        {q:"\"__________ Mother\" by Dorothea Lange exemplifies powerful portraiture.", a:"Migrant"},
        {q:"Portraiture connects viewers with strangers' __________ and situations.", a:"emotions"},
        {q:"Portraiture humanises broad issues and fosters __________.", a:"empathy"},
        {q:"Portraits create icons and preserve collective __________.", a:"memory"},
        {q:"Portraiture amplifies __________ voices.", a:"marginalised"},
        {q:"Key technical aspects of portraiture include lighting, composition, and capturing the right __________.", a:"moment"},
        {q:"Photo interviews combine visual and __________ narratives.", a:"verbal"},
        {q:"Preparation for a photo interview involves research, setting objectives, and technical __________.", a:"readiness"},
        {q:"Building __________ is crucial for natural expressions.", a:"rapport"},
        {q:"__________ questions elicit detailed personal stories.", a:"Open-ended"},
        {q:"The post-interview process involves selecting complementary photos and __________.", a:"text"},
        {q:"__________ consent is essential in portraiture and photo interviews.", a:"Informed"},
        {q:"Respect for __________ is crucial in portrait photography.", a:"dignity"},
        {q:"__________ in representation is paramount.", a:"Truthfulness"}
      ],
      short: [
        {q:"What does portraiture capture in photojournalism?", a:"Portraiture captures an individual's personality, character, or life story through a single image or short series."},
        {q:"Explain why \"Migrant Mother\" by Dorothea Lange is cited as an example of powerful portraiture.", a:"It exemplifies how a single portrait can connect viewers with a stranger's emotions and situation, humanising a broader social issue."},
        {q:"How does portraiture humanise broad issues?", a:"By focusing on an individual's face and story, portraiture fosters empathy and helps viewers connect emotionally with issues that might otherwise feel abstract."},
        {q:"What preparation is needed before conducting a photo interview?", a:"Preparation involves research, setting clear objectives, and ensuring technical readiness with equipment."},
        {q:"Why is building rapport with a subject important in portraiture?", a:"Rapport helps the subject feel comfortable, which is crucial for capturing natural expressions rather than posed or stiff ones."},
        {q:"What kind of questions should be used during a photo interview, and why?", a:"Open-ended questions should be used because they elicit detailed personal stories rather than short, closed answers."},
        {q:"Describe the post-interview process in photo interviews.", a:"It involves selecting the photographs and text that complement each other best to present a coherent combined visual and verbal narrative."},
        {q:"What ethical considerations are fundamental to portraiture and photo interviews?", a:"Informed consent, respect for the subject's dignity, and truthfulness in representation are all fundamental ethical considerations."},
        {q:"Why is informed consent essential in portrait photography?", a:"It ensures the subject has agreed to be photographed and understands how their image and story will be used, protecting their dignity and autonomy."},
        {q:"What is meant by 'truthfulness in representation' in portraiture?", a:"It means representing the subject accurately and honestly, without distorting their character or story for dramatic effect."},
        {q:"What is the overall goal of portraiture according to this week's summary?", a:"The goal is to foster a connection between the subject and the audience, going beyond capturing faces to amplify the essence of humanity."},
        {q:"How do photojournalistic elements like context and background function in a portrait?", a:"They situate the subject within their environment or story, adding depth and meaning beyond the face alone."},
        {q:"What should photojournalists look for during a portrait or interview session to capture authentic moments?", a:"They should look for natural moments that capture the subject's personality and the essence of their story."},
        {q:"How can portraiture nurture a more empathetic worldview?", a:"By repeatedly presenting individual human stories with dignity and truth, portraiture encourages viewers to see shared humanity across different situations."},
        {q:"What tension must photojournalists balance when creating portraits, according to the week's reflection?", a:"They must balance their own artistic vision with their ethical obligations to the subject being photographed."}
      ]
    }
  ]
},
{
  code: "GST 121",
  title: "Use of Library, Skills and ICT",
  weeks: [
    {
      week: 1,
      topic: "Definition, History and Relevance of Libraries to Education",
      mcq: [

    {q:"Which three historical eras of library development are covered this week?", opts:["Ancient, medieval, modern","Classical, industrial, digital","Prehistoric, colonial, contemporary","Early, middle, late"], a:0},
    {q:"What materials did ancient Sumerian libraries rely on?", opts:["Papyrus scrolls","Clay tablets and cuneiform writing","Parchment and paper","Printed books"], a:1},
    {q:"What material did Egyptians transition to, and in what context?", opts:["Paper, in the Islamic world","Papyrus, developed in palace libraries","Parchment, in monasteries","Printed pages, in the modern era"], a:1},
    {q:"Which two religions influenced library development in the medieval era?", opts:["Buddhism and Hinduism","Christianity and Islam","Judaism and Christianity","Islam and Buddhism"], a:1},
    {q:"What innovation defined the modern era of libraries, per this week's material?", opts:["The internet","The invention of printing and wider access to paper","Digital cataloguing systems","The telegraph"], a:1},
    {q:"Which of these is NOT listed among the skills/competencies gained this week?", opts:["Information literacy","Research skills","Technological literacy","Financial accounting"], a:3},
    {q:"What role did monasteries play in the medieval era, per this week's summary?", opts:["They had no connection to libraries","They preserved and disseminated knowledge, using parchments","They banned the use of written materials","They focused solely on oral tradition"], a:1},
    {q:"Why are libraries described as still relevant in \"today's digital age\"?", opts:["They have remained completely unchanged since ancient times","They have continuously evolved and adapted to changing technologies","They are now obsolete compared to the internet","They only serve historical/archival purposes"], a:1},
    {q:"What does this week's case study aim to explore?", opts:["The decline of libraries in modern society","The continued relevance of libraries to education across historical periods","The cost of building new libraries","The role of libraries in national sports development"], a:1},
    {q:"Per the personal reflection prompt, how have libraries \"evolved with different writing surfaces\"?", opts:["They have stayed with cuneiform tablets exclusively","They progressed from clay tablets to papyrus, parchment, and paper, adapting across eras","They eliminated all physical materials in favour of digital-only content","They reverted to oral tradition in the modern era"], a:1},
    {q:"What are libraries described as, per the case study's introduction?", opts:["Optional community spaces","Fundamental institutions in preserving and disseminating knowledge","Purely commercial ventures","Obsolete institutions"], a:1},
    {q:"What approach does this week's case study use to explore libraries and education?", opts:["A purely fictional narrative","A comparative approach analysing primary sources, scholarly literature, and historical records","A single-interview method only","No formal method described"], a:1},
    {q:"Which of these is NOT among the skills/competencies listed this week?", opts:["Information literacy","Organisation skills","Lifelong learning","Structural engineering"], a:3},
    {q:"Who is the author of \"Role of libraries in education,\" this week's key reference?", opts:["Darmingliana, H.","Todd, J.","Poe, M.T.","McQuail, D."], a:0},
    {q:"What does the case study examine regarding library materials, per its methods section?", opts:["Only the cost of materials","Types of educational materials, their accessibility, and impact on literacy/knowledge dissemination","Only digital materials","Only materials from one country"], a:1}
      ],
      fib: [

    {q:"Libraries have a rich history spanning the ancient, __________, and modern periods.", a:"medieval"},
    {q:"Ancient libraries relied on clay tablets and __________ writing.", a:"cuneiform"},
    {q:"The Egyptians used papyrus and later transitioned to parchments in the __________ Library.", a:"Pergamum"},
    {q:"The medieval era saw the influence of Christianity and __________, with monasteries and mosques preserving knowledge.", a:"Islam"},
    {q:"The modern era witnessed the invention of __________ and paper, leading to widespread availability of books.", a:"printing"},
    {q:"Libraries have continuously evolved and adapted to changing __________, remaining valuable educational resources.", a:"technologies"},
    {q:"Skills gained this week include information literacy, research skills, and __________ thinking.", a:"critical"},
    {q:"The case study this week examines the relevance of libraries to __________ across historical eras.", a:"education"},
    {q:"__________ used parchments to preserve and disseminate knowledge in the medieval era.", a:"Monks (or monasteries)"},
    {q:"Reflecting on the invention of paper and printing shows how it revolutionised access to __________ and education.", a:"knowledge"},
    {q:"Libraries have been fundamental institutions in preserving and __________ knowledge.", a:"disseminating"},
    {q:"This week's case study employs a __________ approach, analysing primary sources and historical records.", a:"comparative"},
    {q:"Among the skills gained this week are organisation skills and __________ skills.", a:"reading"},
    {q:"__________, H. (2019) is the author of \"Role of libraries in education,\" this week's key reference.", a:"Darmingliana"},
    {q:"Libraries continue to be valuable sources of information and __________ resources in today's digital age.", a:"educational"}
      ],
      short: [

    {q:"Name the three historical eras of library development covered this week.", a:"Ancient, medieval, modern."},
    {q:"What materials did ancient Sumerian libraries rely on?", a:"Clay tablets and cuneiform writing."},
    {q:"What material did Egyptians transition to, and where?", a:"Papyrus, developed in palace libraries."},
    {q:"Which two religions influenced library development in the medieval era, and how?", a:"Christianity and Islam — monasteries used parchments; the Islamic world introduced paper."},
    {q:"What innovation defined the modern era of libraries?", a:"The invention of printing (and wider access to paper)."},
    {q:"Name three skills/competencies this week's lesson says you should have gained.", a:"Any 3 of: information literacy, research skills, reading skills, critical thinking, collaboration, technological literacy."},
    {q:"What role did monasteries play in the medieval era, per this week's summary?", a:"Preserved and disseminated knowledge."},
    {q:"Why are libraries described as still relevant in today's digital age?", a:"They continue adapting to changing technologies, remaining valuable information/educational resources."},
    {q:"What does the case study this week aim to explore?", a:"The continued relevance of libraries to education across historical periods."},
    {q:"Per your personal reflection prompt, how have libraries \"evolved with different writing surfaces\"?", a:"From clay tablets to papyrus, parchment, and paper, libraries adapted their materials and format across eras while remaining central to education."},
    {q:"What are libraries described as, per the case study's introduction?", a:"Fundamental institutions in preserving and disseminating knowledge, supporting educational endeavours, and fostering intellectual growth."},
    {q:"What approach does this week's case study use to explore libraries and education?", a:"A comparative approach, analysing primary sources, scholarly literature, and historical records."},
    {q:"Name four of the ten skills/competencies listed this week.", a:"Any 4 of: information literacy, research skills, reading skills, critical thinking, collaboration, technological literacy, organisation skills, communication skills, creativity and innovation, lifelong learning."},
    {q:"Who is the author of this week's key reference on the role of libraries in education?", a:"Darmingliana, H. (2019)."},
    {q:"What three things does the case study examine regarding library materials, per its methods section?", a:"Types of educational materials housed in libraries, their accessibility to different segments of society, and the impact on literacy/knowledge dissemination/intellectual development."}
      ]
    },
    {
      week: 2,
      topic: "Types of Libraries",
      mcq: [
    {q:"What types of libraries are covered this week?", opts:["School, academic, special, public, and national libraries","Only public libraries","Only digital libraries","Only university libraries"], a:0},
    {q:"What does a school library serve as, per this week's material?", opts:["A resource hub for students, teachers, and parents","Only a storage space for old books","Only a staff lounge","Only an exam hall"], a:0},
    {q:"What does a school library promote, per this week's material?", opts:["Literacy, information retrieval skills, and a love for reading","Only silence and discipline","Only sports activities","Only technology repair"], a:0},
    {q:"What do academic and special libraries cater to, per this week's material?", opts:["The specific needs of educational institutions and specialised fields","Only recreational reading","Only children's books","Only fiction collections"], a:0},
    {q:"What do academic and special libraries support, per this week's material?", opts:["Research and access to scholarly resources","Only entertainment","Only administrative paperwork","Only sports records"], a:0},
    {q:"What do public libraries serve, per this week's material?", opts:["The community, promoting literacy and lifelong learning","Only academic researchers","Only government officials","Only private corporations"], a:0},
    {q:"What do national libraries preserve, per this week's material?", opts:["Cultural heritage, collecting and archiving national publications","Only foreign literature","Only digital files","Only legal contracts"], a:0},
    {q:"What was the focus of this week's lesson, per the summary?", opts:["The school library, as a resource hub for literacy and reading","Only national libraries","Only special libraries","Only digital archives"], a:0},
    {q:"What is the title of this week's case study?", opts:["The Impact of a School Library on Student Learning","The History of National Libraries","Digital Libraries in the 21st Century","Academic Research Methods"], a:0},
    {q:"What was the objective of this week's case study?", opts:["To examine the impact of a newly established school library on student learning outcomes","To compare library budgets across countries","To digitise all library records","To close underperforming libraries"], a:0},
    {q:"What did the case study's pre-library assessment gauge?", opts:["Students' reading abilities, information retrieval skills, and interest in books","Only students' attendance records","Only teachers' qualifications","Only the school's budget"], a:0},
    {q:"What improvements did students show after the school invested in a library and librarian, per the case study?", opts:["Improved reading proficiency, research skills, and academic performance","No measurable change","A decline in test scores","Reduced attendance"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Information literacy","Organisation skills","Creativity and innovation","Financial auditing"], a:3},
    {q:"What role do libraries play in education, per this week's personal reflection?", opts:["Providing access to information, fostering literacy and critical thinking, and supporting lifelong learning","Only storing unused materials","Only serving as a quiet study space","Only hosting events"], a:0},
    {q:"Who wrote \"Library and information science text for Africa,\" a key reference this week?", opts:["Aina, L.O.","Okhakhu, D.O.","Darmingliana, H.","Baskar, A."], a:0}
      ],
      fib: [
    {q:"Types of libraries include school, academic, special, public, and __________ libraries.", a:"national"},
    {q:"School libraries are attached to educational institutions and provide resources for students, teachers, and __________.", a:"parents"},
    {q:"Academic and special libraries cater to specific fields or institutions, supporting __________ and access to scholarly resources.", a:"research"},
    {q:"Public libraries serve the community, promoting literacy, lifelong learning, and access to __________ for all.", a:"information"},
    {q:"National libraries preserve cultural heritage and serve as repositories of national __________.", a:"knowledge"},
    {q:"This week's case study title is \"The Impact of a School Library on Student __________.\"", a:"Learning"},
    {q:"The case study's objective was to examine the impact of a newly established school library on student learning __________.", a:"outcomes"},
    {q:"The school in the case study conducted a pre-library __________ to gauge students' reading abilities.", a:"assessment"},
    {q:"After the library was established, students showed improved reading proficiency and __________ skills.", a:"research"},
    {q:"The school invested in a diverse library collection and appointed a __________.", a:"librarian"},
    {q:"One skill gained this week is __________ and innovation.", a:"creativity"},
    {q:"Libraries play a vital role in education by fostering literacy and critical __________ skills.", a:"thinking"},
    {q:"Aina, L.O. (2004) wrote \"Library and information science text for __________.\"", a:"Africa"},
    {q:"Okhakhu, D.O. (2019) wrote \"Use of library resources and information __________ skills text.\"", a:"literacy"},
    {q:"This week's Questions to ponder ask how school library resources can contribute to your __________.", a:"learning"}
      ],
      short: [
    {q:"Name the five types of libraries covered this week.", a:"School, academic, special, public, and national libraries."},
    {q:"What does a school library serve as, and what does it promote?", a:"A resource hub for students, teachers, and parents, promoting literacy, information retrieval skills, and a love for reading."},
    {q:"What do academic and special libraries cater to and support?", a:"The specific needs of educational institutions and specialised fields, supporting research and access to scholarly resources."},
    {q:"What do public libraries and national libraries serve, respectively?", a:"Public libraries serve the community, promoting literacy and lifelong learning; national libraries preserve cultural heritage and archive national publications."},
    {q:"What is the title and objective of this week's case study?", a:"\"The Impact of a School Library on Student Learning\" — to examine the impact of a newly established school library on student learning outcomes and academic development."},
    {q:"What did the case study's pre-library assessment measure?", a:"Students' reading abilities, information retrieval skills, and overall interest in books."},
    {q:"What improvements did students show after the school library was established?", a:"Improved reading proficiency, research skills, enhanced academic performance, and a love for reading."},
    {q:"Think of the different types of resources in a school library — name three and how they contribute to learning.", a:"Any 3 resource types (books, reference materials, digital resources, etc.) that support information retrieval, research, and reading skills."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: information literacy, research skills, reading skills, critical thinking, collaboration, technological literacy, organisation skills, creativity and innovation, lifelong learning."},
    {q:"What role do libraries play in education, per this week's Personal Reflection?", a:"Providing access to information resources, fostering literacy and critical thinking skills, promoting collaboration and creativity, and supporting lifelong learning."},
    {q:"Name this week's two key references.", a:"Aina, L.O. (2004) Library and information science text for Africa; Okhakhu, D.O. (2019) Use of library resources and information literacy skills text."},
    {q:"Explain why it is essential for a school library to have resources in different formats.", a:"Different formats serve different learning needs and research purposes, ensuring broader accessibility and richer information retrieval."},
    {q:"Imagine conducting a research project — how could a school library help find relevant information?", a:"Through its range of information resources, librarian guidance, and research/information retrieval skill-building."},
    {q:"What organisations/institutions were featured in this week's case study?", a:"ABC International School, which established a new school library."},
    {q:"Why did ABC International School decide to invest in a library, per the case study?", a:"To enhance student learning and foster a love for reading, supporting their broader educational goals."}
      ]
    },
    {
      week: 3,
      topic: "Library Information Resources",
      mcq: [
    {q:"What are textbooks described as, per this week's material?", opts:["Essential educational resources used by teachers and students","Outdated materials rarely used today","Only reference material for teachers","Only used in primary schools"], a:0},
    {q:"What do textbooks provide, per this week's material?", opts:["Guidance, examples, and reference materials","Only entertainment","Only historical data","Only test answers"], a:0},
    {q:"What are serials, and what do they do?", opts:["Magazines and newspapers, which keep us informed about current events","Only academic journals, used for citations","Only reference books, for quick facts","Only government reports"], a:0},
    {q:"What do reference sources like encyclopaedias and dictionaries offer?", opts:["Quick and reliable information retrieval","Only entertainment value","Only historical fiction","Only unverified information"], a:0},
    {q:"What do audio-visual resources, including CDs and videos, provide?", opts:["Dynamic and engaging learning experiences","Only background noise","Only storage challenges","Only outdated content"], a:0},
    {q:"What do electronic information resources include, per this week's material?", opts:["E-books and online databases","Only printed books","Only VHS tapes","Only physical maps"], a:0},
    {q:"What do electronic information resources offer, per this week's material?", opts:["Convenient access to a vast wealth of knowledge","Only limited access to a few books","Only access during library hours","Only access for staff"], a:0},
    {q:"What is the title of this week's case study?", opts:["Research Project at Miva Open University","The History of E-books","Library Funding Models","Digital Literacy for Beginners"], a:0},
    {q:"Who is the subject of this week's case study, and what is their research topic?", opts:["Alex, an undergraduate student, researching mindfulness meditation and stress reduction","A librarian researching cataloguing systems","A professor researching funding models","A journalist researching press freedom"], a:0},
    {q:"What resources did Alex use for his research project, per the case study?", opts:["Library resources including librarian assistance, reference sources, audio-visual materials, and electronic resources","Only social media posts","Only personal interviews","Only newspaper clippings"], a:0},
    {q:"What did Alex's research project demonstrate, per the case study?", opts:["His research skills and academic accomplishments","A failure to find relevant sources","A decline in library usage","A lack of research skills"], a:0},
    {q:"Which of these is NOT listed among this week's skills/competencies?", opts:["Resource management","Self-directed learning","Ethical use of information","Financial forecasting"], a:3},
    {q:"What role do libraries play, per this week's personal reflection?", opts:["Providing access to diverse information resources, fostering learning and research","Only serving as a quiet space","Only storing outdated materials","Only hosting events"], a:0},
    {q:"Who wrote \"E-resources and its uses in library,\" a key reference this week?", opts:["Baskar, A.","Aina, L.O.","Okhakhu, D.O.","Darmingliana, H."], a:0},
    {q:"What publication is \"What is a public library and their characteristics, type and functions\" attributed to this week?", opts:["Library Academy (2020)","Journal of Critical Reviews","Course Hero","Journal of Advances and Scholarly Researchers"], a:0}
      ],
      fib: [
    {q:"Textbooks are essential educational resources used by teachers and __________.", a:"students"},
    {q:"Serials, such as magazines and newspapers, keep us informed about current events and __________.", a:"developments"},
    {q:"Reference sources, like encyclopaedias and dictionaries, offer quick and reliable information __________.", a:"retrieval"},
    {q:"Audio-visual resources, including CDs and videos, provide dynamic and __________ learning experiences.", a:"engaging"},
    {q:"Electronic information resources, such as e-books and online __________, offer convenient access to knowledge.", a:"databases"},
    {q:"This week's case study title is \"Research Project at __________ Open University.\"", a:"Miva"},
    {q:"The case study follows Alex, an __________ student researching mindfulness meditation and stress reduction.", a:"undergraduate"},
    {q:"Alex leveraged Miva Open University's library resources, including __________ assistance, for his research.", a:"librarian"},
    {q:"Alex conducted a comprehensive literature __________ and consulted psychology reference sources.", a:"review"},
    {q:"Alex's research project contributes to __________, demonstrating his research skills.", a:"psychology"},
    {q:"One skill gained this week is __________ use of information.", a:"ethical"},
    {q:"Libraries play a crucial role in providing access to diverse information resources, fostering learning and __________.", a:"research"},
    {q:"Baskar, A. (2017) wrote \"__________ and its uses in library,\" a key reference this week.", a:"E-resources"},
    {q:"Library Academy (2020) published \"What is a public library and their characteristics, type and __________.\"", a:"functions"},
    {q:"This week's Questions to ponder ask how electronic databases, e-books, and e-journals will enhance your __________ process.", a:"research"}
      ],
      short: [
    {q:"What are the five types of library information resources covered this week?", a:"Textbooks, serials, reference sources, audio-visual resources, and electronic information resources."},
    {q:"What are textbooks, and what do they provide?", a:"Essential educational resources for teachers and students, providing guidance, examples, and reference materials."},
    {q:"What are serials, and what do they do?", a:"Magazines and newspapers, which keep readers informed about current events and developments."},
    {q:"What do reference sources and audio-visual resources each offer?", a:"Reference sources (encyclopaedias, dictionaries) offer quick, reliable information retrieval; audio-visual resources (CDs, videos) provide dynamic, engaging learning experiences."},
    {q:"What do electronic information resources include, and what do they offer?", a:"E-books and online databases, offering convenient access to a vast wealth of knowledge."},
    {q:"What is the title and objective of this week's case study?", a:"\"Research Project at Miva Open University\" — to examine the impact of mindfulness meditation techniques on reducing stress levels."},
    {q:"Who is the subject of this week's case study, and what field is their research in?", a:"Alex, an undergraduate student at Miva Open University, researching in the field of psychology."},
    {q:"What library resources did Alex use for his research project?", a:"Librarian assistance, a comprehensive literature review, psychology reference sources, audio-visual materials, and electronic information resources."},
    {q:"Can you provide examples of reference sources and how they support research?", a:"Encyclopaedias and dictionaries, which offer quick and reliable background information to support research and learning."},
    {q:"Explain the significance of audio-visual resources in libraries.", a:"They enhance the learning experience by providing dynamic and engaging ways to absorb information, beyond text alone."},
    {q:"Name three skills/competencies gained this week.", a:"Any 3 of: information literacy, research skills, critical thinking, technological literacy, communication skills, resource management, self-directed learning, collaboration, adaptability, ethical use of information."},
    {q:"What role do libraries play, per this week's Personal Reflection?", a:"Providing access to diverse information resources, fostering learning and research, and supporting educational and personal development."},
    {q:"Name this week's two key references.", a:"Baskar, A. (2017) E-resources and its uses in library; Library Academy (2020) What is a public library and their characteristics, type and functions."},
    {q:"Think of a research project you might work on — how would electronic databases, e-books, and e-journals enhance it?", a:"They provide quick, wide-ranging access to current and historical scholarship, supporting thorough and efficient research."},
    {q:"What did Alex's research project demonstrate, per the case study?", a:"His research skills and academic accomplishments, contributing to the field of psychology."}
      ]
    },
    {
      week: 4,
      topic: "Reference Service",
      mcq: [
        {q:"The library reference service is best described as acting like a:", opts:["Photocopy counter only","Knowledgeable guide that helps users find information","Book-binding workshop","Security checkpoint"], a:1},
        {q:"The reference service aims to strike a balance between providing assistance and:", opts:["Replacing the catalogue","Charging users for help","Empowering users to find information independently","Restricting access to resources"], a:2},
        {q:"How many philosophical schools of thought on reference services were covered this week?", opts:["Five","Three","Two","Four"], a:1},
        {q:"Which of these is one of the three schools of thought on reference service?", opts:["Digital Service School","Closed Access School","Maximum Service School","Self-Service School"], a:2},
        {q:"Which of these is also one of the three schools of thought?", opts:["Central School","Rapid School","Optimal School","Middling School"], a:3},
        {q:"The third school of thought alongside Maximum and Middling is the:", opts:["Open School","Minimum Service School","Premium School","Zero Service School"], a:1},
        {q:"Who plays the key role in delivering reference services?", opts:["The security officer","The IT technician only","The cataloguer only","The reference librarian"], a:3},
        {q:"Which qualities should a reference librarian possess?", opts:["Strictness and secrecy","Indifference to users","Speed typing only","Approachability, resourcefulness, and good communication skills"], a:3},
        {q:"Which is an objective of the reference service?", opts:["Closing the library early","Answering user questions","Discouraging library use","Selling books to users"], a:1},
        {q:"The objectives of reference service also include providing:", opts:["Entertainment only","Guidance and facilitating access to information resources","Building maintenance","Cataloguing exams"], a:1},
        {q:"The objectives of reference service emphasise promoting:", opts:["Collaboration","Competition between users","Fines","Silence only"], a:0},
        {q:"Reference service can be offered through which channels?", opts:["Only a reference desk","Only email","Reference desks, telephone, email, or chat services","Only in-person queues"], a:2},
        {q:"In the XYZ Library case study, which method was used to evaluate existing reference services?", opts:["Closing the library","Surveys, feedback collection, and statistical analysis","Guesswork only","Removing all staff"], a:1},
        {q:"In the case study, what was used to enhance reference librarians' expertise?", opts:["Reduced opening hours","Specialised training programs","Removing the reference desk","Fewer resources"], a:1},
        {q:"In the case study, reference services were expanded to include:", opts:["Only walk-in help","Email, telephone, and online chat support","Only printed notices","Only the reference desk"], a:1}
      ],
      fib: [
        {q:"The reference service acts as a knowledgeable __________ for library users.", a:"guide"},
        {q:"There are __________ philosophical schools of thought regarding reference services.", a:"three"},
        {q:"The first school of thought is the __________ Service School.", a:"Maximum"},
        {q:"The second school of thought is the __________ Service School.", a:"Minimum"},
        {q:"The third school of thought is the __________ School.", a:"Middling"},
        {q:"A reference __________ plays a key role in delivering reference services.", a:"librarian"},
        {q:"A reference librarian should be approachable, resourceful, and have good __________ skills.", a:"communication"},
        {q:"One objective of the reference service is answering user __________.", a:"questions"},
        {q:"Reference service also provides guidance and facilitates access to information __________.", a:"resources"},
        {q:"Reference service can be offered through dedicated reference desks, telephone, email, or __________ services.", a:"chat"},
        {q:"The reference service balances assistance with empowering users to find information __________.", a:"independently"},
        {q:"The case study library is called __________ Library.", a:"XYZ"},
        {q:"The case study used surveys, feedback collection, and statistical __________ to find strengths and weaknesses.", a:"analysis"},
        {q:"Specialised __________ programs enhanced the expertise of reference librarians.", a:"training"},
        {q:"Reference service is vital in supporting learning, research, and knowledge __________.", a:"sharing"}
      ],
      short: [
        {q:"What is the reference service in a library?", a:"It is a crucial service that assists users in their quest for information, with the librarian acting as a knowledgeable guide."},
        {q:"Name the three philosophical schools of thought on reference service.", a:"The Maximum Service School, the Minimum Service School, and the Middling School."},
        {q:"What balance does the reference service try to strike?", a:"It balances providing assistance to users with empowering them to find information independently."},
        {q:"What is the role of a reference librarian?", a:"The reference librarian plays the key role in delivering reference services by helping users find and access information."},
        {q:"List qualities a reference librarian should have.", a:"Approachability, resourcefulness, and good communication skills."},
        {q:"State the objectives of the reference service.", a:"To answer user questions, provide guidance, facilitate access to information resources, and promote collaboration."},
        {q:"Through which channels can reference service be delivered?", a:"Through dedicated reference desks, telephone, email, or chat services."},
        {q:"Why are alternative channels like email and chat useful beyond the reference desk?", a:"They give users diverse avenues of support, making help accessible without having to visit the desk in person."},
        {q:"How did XYZ Library assess its existing reference services in the case study?", a:"It used surveys, feedback collection, and statistical analysis to uncover strengths and weaknesses."},
        {q:"How did XYZ Library improve its librarians' abilities?", a:"It introduced specialised training programs to enhance their expertise in information retrieval and user assistance."},
        {q:"How did XYZ Library expand its reference services?", a:"It added email, telephone, and online chat support alongside the traditional service."},
        {q:"Why is the reference service important to learning and research?", a:"It supports learning, research, and knowledge sharing by helping users locate the information they need."},
        {q:"Give examples of questions you might take to a reference librarian.", a:"Questions about finding a specific resource, locating information on a topic, or how to use library tools to research an assignment."},
        {q:"What skills does this week's lesson say you acquire?", a:"Information retrieval, communication, critical thinking, problem-solving, technological proficiency, customer service, empathy and interpersonal skills, collaboration, self-directed learning, and research skills."},
        {q:"Summarise this week's key message on reference service.", a:"Reference service is essential for assisting library users, and librarians serve as knowledgeable guides who help while encouraging independent information seeking."}
      ]
    },
    {
      week: 5,
      topic: "Organisation of Library Information Resources",
      mcq: [
        {q:"A library catalogue is best described as:", opts:["A list of library staff","A record of fines","A schedule of events","A guide or index to the holdings of a library"], a:3},
        {q:"What does the catalogue provide about resources?", opts:["Bibliographical information","Only their colours","Only their prices","Only their weights"], a:0},
        {q:"The catalogue helps users to:", opts:["Replace librarians","Locate items within the library","Avoid using the library","Pay fees"], a:1},
        {q:"Using the catalogue helps develop which skills?", opts:["Driving skills","Information retrieval skills","Cooking skills","Painting skills"], a:1},
        {q:"The catalogue helps users make informed decisions on:", opts:["Which fines to pay","Which resources to consult","Which staff to hire","Which building to enter"], a:1},
        {q:"Efficient retrieval of resources is facilitated through:", opts:["Call numbers","Postcodes","Telephone numbers","Staff ID numbers"], a:0},
        {q:"How does the catalogue help other libraries?", opts:["It plays a role in resource selection to expand collections","It sets their fees","It lists their staff","It forces them to close"], a:0},
        {q:"Which is a form of library cataloguing?", opts:["Financial cataloguing","Descriptive cataloguing","Digital shelving","Decorative cataloguing"], a:1},
        {q:"Which is another form of library cataloguing?", opts:["Weight cataloguing","Colour cataloguing","Price cataloguing","Subject cataloguing"], a:3},
        {q:"Which third element contributes to effective resource organisation alongside descriptive and subject cataloguing?", opts:["Lending fines","Binding","Classification","Advertising"], a:2},
        {q:"Which details are examples of bibliographical information?", opts:["Title, author, and publication details","Librarian's address","Shelf paint colour","Opening hours"], a:0},
        {q:"In the XYZ University Library case study, the previous system lacked:", opts:["Any books","A building","User-friendly features and comprehensive resource information","Any users"], a:2},
        {q:"The case study began its improvement with:", opts:["Closing the library","A needs assessment gathering user feedback","Selling books","Removing the catalogue"], a:1},
        {q:"Which activities ensured a seamless transition to the new system?", opts:["Removing all books","Reducing hours","Ignoring users","Data migration and staff training"], a:3},
        {q:"User education programmes in the case study aimed to:", opts:["Close the catalogue","Discourage library use","Familiarise users with the upgraded system","Raise fines"], a:2}
      ],
      fib: [
        {q:"A library catalogue is a guide or __________ to the holdings of a library.", a:"index"},
        {q:"The catalogue provides __________ information about resources.", a:"bibliographical"},
        {q:"The catalogue helps users locate items within the __________.", a:"library"},
        {q:"Efficient resource retrieval is facilitated through call __________.", a:"numbers"},
        {q:"The catalogue develops your information __________ skills.", a:"retrieval"},
        {q:"The catalogue plays a role in resource __________ for other libraries.", a:"selection"},
        {q:"__________ cataloguing is one form of library cataloguing that describes the item.", a:"Descriptive"},
        {q:"__________ cataloguing is a form of cataloguing based on what an item is about.", a:"Subject"},
        {q:"__________ is the third form of cataloguing alongside descriptive and subject cataloguing.", a:"Classification"},
        {q:"Title, author, and publication details are examples of __________ information.", a:"bibliographical"},
        {q:"The case study was about __________ University Library.", a:"XYZ"},
        {q:"The case study began with a needs __________ that gathered user feedback.", a:"assessment"},
        {q:"Data __________ and staff training ensured a seamless transition.", a:"migration"},
        {q:"User __________ programmes familiarised users with the upgraded system.", a:"education"},
        {q:"The catalogue enables __________ decision-making about which resources to consult.", a:"informed"}
      ],
      short: [
        {q:"What is a library catalogue?", a:"It is a guide or index to the holdings of a library, providing information about available resources and their locations."},
        {q:"Why is bibliographical information important in a catalogue?", a:"Details such as title, author, and publication information help users identify resources and decide which ones to consult."},
        {q:"How do call numbers help users?", a:"Call numbers facilitate efficient retrieval by directing users to the exact location of a resource within the library."},
        {q:"How does the catalogue help develop users' skills?", a:"It develops information retrieval skills by teaching users to search for and locate resources efficiently."},
        {q:"How does the catalogue help other libraries?", a:"It plays a crucial role in resource selection for other libraries, helping them expand and enhance their collections."},
        {q:"Name the three forms of library cataloguing.", a:"Descriptive cataloguing, subject cataloguing, and classification."},
        {q:"Why is a consistent, standardised system for organising resources important?", a:"It makes resources easier to find, describe, and retrieve in a predictable way across the library."},
        {q:"Describe how a catalogue could make finding a book easier.", a:"By searching the catalogue for the title, author, or subject, a user obtains the call number and location instead of searching shelves blindly."},
        {q:"What problem did XYZ University Library face in the case study?", a:"Its existing catalogue system lacked user-friendly features and comprehensive information about available resources."},
        {q:"What steps did the library take to upgrade its catalogue?", a:"A needs assessment gathered user feedback, a modern user-friendly system was implemented, data migration and staff training ensured smooth transition, and user education familiarised users."},
        {q:"What outcomes did the upgrade aim to improve?", a:"The user experience, resource retrieval, and staff productivity."},
        {q:"How does the catalogue support informed decision-making?", a:"By offering bibliographical details, it lets users judge which resources are relevant before consulting them."},
        {q:"List skills gained from this week's lesson.", a:"Using a library catalogue effectively, navigating and searching for resources, interpreting bibliographical information, information literacy, critical thinking, problem-solving, and research skills."},
        {q:"Why was staff training included in the case study?", a:"To ensure staff could use the new system effectively, enabling a seamless transition."},
        {q:"Summarise the importance of the library catalogue.", a:"It is a vital tool for accessing and locating resources, improving research skills, facilitating retrieval, and enabling informed decisions."}
      ]
    },
    {
      week: 6,
      topic: "Ethical Issues in Information Use",
      mcq: [
        {q:"Ethics is about:", opts:["Avoiding all rules","Maximising profit","Following only personal convenience","Behaving responsibly and adhering to standards of what is right, just, and fair"], a:3},
        {q:"Which of these is one of the three prominent ethical issues in information use?", opts:["Paraphrasing","Indexing","Plagiarism","Proofreading"], a:2},
        {q:"Which is another of the three ethical issues covered?", opts:["Shelf reading","Book binding","Copyright infringement","Library cataloguing"], a:2},
        {q:"The third ethical issue covered is:", opts:["Peer review","Open access","Ethical shelving","Unethical referencing"], a:3},
        {q:"Plagiarism is the act of:", opts:["Writing original work","Asking permission to quote","Using someone else's work without proper acknowledgement","Citing sources correctly"], a:2},
        {q:"Plagiarism is described as a kind of:", opts:["Accounting error","Intellectual crime","Printing fault","Cataloguing method"], a:1},
        {q:"Copyright infringement involves:", opts:["Writing a bibliography","Borrowing library books","Unauthorised reproduction, distribution, or display of intellectual property","Citing sources properly"], a:2},
        {q:"Copyright infringement carries:", opts:["Legal consequences","Only praise","No consequences","Library discounts"], a:0},
        {q:"To avoid copyright infringement, one should:", opts:["Copy freely","Remove the author's name","Cite properly and seek permission","Alter publication dates"], a:2},
        {q:"Which is an example of unethical referencing?", opts:["Citing accurately","Providing a complete reference list","Not providing a reference list","Using correct dates"], a:2},
        {q:"Which is another unethical referencing practice?", opts:["Providing page numbers","Citing real publications","Verifying every source","Using fictitious details"], a:3},
        {q:"Which is also unethical referencing?", opts:["Listing all sources","Using accurate dates","Checking details","Altering publication dates"], a:3},
        {q:"In the case study, how was Alex's unethical behaviour identified?", opts:["A reference desk","A library catalogue","Plagiarism detection software","A student survey"], a:2},
        {q:"What followed detection in the case study?", opts:["Rewards","Disciplinary consequences","A promotion","Nothing"], a:1},
        {q:"What is emphasised as important in academic work?", opts:["Avoiding references","Upholding integrity and fairness","Speed over accuracy","Copying widely"], a:1}
      ],
      fib: [
        {q:"Ethics is about behaving __________ and adhering to standards of what is right, just, and fair.", a:"responsibly"},
        {q:"Three ethical issues in information use are plagiarism, copyright infringement, and unethical __________.", a:"referencing"},
        {q:"__________ is using someone else's work without proper acknowledgement.", a:"Plagiarism"},
        {q:"Plagiarism is considered an intellectual __________.", a:"crime"},
        {q:"Copyright infringement is the __________ reproduction, distribution, or display of intellectual property.", a:"unauthorised"},
        {q:"Copyright infringement carries __________ consequences.", a:"legal"},
        {q:"Properly citing and seeking __________ is essential to avoid copyright infringement.", a:"permission"},
        {q:"Not providing a reference __________ is an unethical referencing practice.", a:"list"},
        {q:"Using __________ details in references is unethical.", a:"fictitious"},
        {q:"Copying others' __________ is an unethical referencing practice.", a:"references"},
        {q:"Altering publication __________ is unethical referencing.", a:"dates"},
        {q:"In the case study, the student's name was __________.", a:"Alex"},
        {q:"__________ detection software identified the unethical behaviour in the case study.", a:"Plagiarism"},
        {q:"The case study emphasises upholding __________ in academic work.", a:"integrity"},
        {q:"Respecting intellectual __________ means giving proper credit to others' work.", a:"property"}
      ],
      short: [
        {q:"What is meant by ethics in information use?", a:"Ethics is behaving responsibly and following standards of what is right, just, and fair when using information."},
        {q:"Name the three ethical issues covered this week.", a:"Plagiarism, copyright infringement, and unethical referencing."},
        {q:"Define plagiarism.", a:"Plagiarism is using someone else's work without proper acknowledgement, which is considered an intellectual crime."},
        {q:"What is copyright infringement?", a:"The unauthorised reproduction, distribution, or display of intellectual property, which carries legal consequences."},
        {q:"How can copyright infringement be avoided?", a:"By properly citing sources and seeking permission before using someone else's intellectual property."},
        {q:"List unethical referencing practices.", a:"Not providing a reference list, providing an incomplete list, using fictitious details, copying others' references, and altering publication dates."},
        {q:"Why is it important to respect others' intellectual property?", a:"It upholds integrity and fairness, gives creators proper credit, and avoids legal and academic penalties."},
        {q:"What happened to Alex in the case study and why?", a:"Alex engaged in plagiarism and improper referencing, which plagiarism detection software identified, leading to disciplinary consequences."},
        {q:"What strategies can help you avoid plagiarism?", a:"Acknowledging all sources, citing properly, managing time to avoid shortcuts, and using plagiarism detection tools to check your work."},
        {q:"Why is accurate and complete referencing an ethical responsibility?", a:"It gives credit to original authors and lets readers verify sources, so the work remains honest and trustworthy."},
        {q:"What are the consequences of unethical information use?", a:"Disciplinary action in academic settings, legal consequences for copyright infringement, and damage to one's integrity."},
        {q:"Why is plagiarism treated so seriously in academic scholarship?", a:"Because it violates integrity and fairness by presenting others' work as one's own."},
        {q:"List skills acquired from this week's lesson.", a:"Understanding ethical principles, critical thinking, ethical decision-making, research skills, proper citation, awareness of academic integrity, time management, digital literacy and plagiarism detection, and personal ethical responsibility."},
        {q:"What is the purpose of the case study this week?", a:"To analyse the consequences of unethical information use and raise awareness of the importance of integrity in academic work."},
        {q:"Summarise this week's personal reflection message.", a:"Ethical information use is crucial: avoid plagiarism, copyright infringement, and unethical referencing, respect intellectual property, cite sources properly, and uphold integrity and fairness."}
      ]
    }
  ]
},
];

/* ---------------- STATE ---------------- */
/* ================= GAME / PROGRESS LAYER (saved per-device via localStorage) ================= */
const STORAGE_KEY = "mcm_quiz_progress_v1";
const NOTE_DISMISS_KEY = "mcm_quiz_device_note_dismissed_v1";
const XP_PER_MCQ_CORRECT = 10;
const XP_PER_FIB_CORRECT = 15;
const XP_PER_SHORT_DONE = 5;
const XP_STREAK_BONUS_PER_LEVEL = 2; // per correct-in-a-row beyond the first, within one sitting
const REVIEW_DUE_DAYS = 3;

function todayStr() {
  return new Date().toISOString().slice(0, 10);
}
function daysBetween(a, b) {
  const d1 = new Date(a + "T00:00:00");
  const d2 = new Date(b + "T00:00:00");
  return Math.round((d2 - d1) / 86400000);
}

function loadProgress() {
  try {
    const raw = localStorage.getItem(STORAGE_KEY);
    if (!raw) throw new Error("none");
    const parsed = JSON.parse(raw);
    if (!parsed.courses) parsed.courses = {};
    if (typeof parsed.totalXP !== "number") parsed.totalXP = 0;
    if (typeof parsed.dayStreak !== "number") parsed.dayStreak = 0;
    if (typeof parsed.bestSittingStreak !== "number") parsed.bestSittingStreak = 0;
    return parsed;
  } catch (e) {
    return { totalXP: 0, dayStreak: 0, lastPlayedDate: null, bestSittingStreak: 0, courses: {} };
  }
}
function saveProgress(p) {
  try { localStorage.setItem(STORAGE_KEY, JSON.stringify(p)); } catch (e) { /* storage unavailable, ignore */ }
}

let PROGRESS = loadProgress();

function bumpDailyStreak() {
  const today = todayStr();
  if (PROGRESS.lastPlayedDate === today) return; // already counted today
  if (PROGRESS.lastPlayedDate) {
    const gap = daysBetween(PROGRESS.lastPlayedDate, today);
    PROGRESS.dayStreak = (gap === 1) ? PROGRESS.dayStreak + 1 : 1;
  } else {
    PROGRESS.dayStreak = 1;
  }
  PROGRESS.lastPlayedDate = today;
}

function ensureProgressPath(c, w) {
  if (!PROGRESS.courses[c]) PROGRESS.courses[c] = { weeks: {} };
  if (!PROGRESS.courses[c].weeks[w]) PROGRESS.courses[c].weeks[w] = { stages: {} };
  return PROGRESS.courses[c].weeks[w];
}

function recordStageCompletion(c, w, stageKey, result) {
  bumpDailyStreak();
  const weekProg = ensureProgressPath(c, w);
  const prevStage = weekProg.stages[stageKey] || { attempts: 0, bestScored: 0, bestTotal: 0 };
  const attempts = prevStage.attempts + 1;
  const today = todayStr();

  let xpEarned = 0;
  let sittingStreak = 0;
  let maxSittingStreak = 0;

  if (stageKey === "mcq" || stageKey === "fib") {
    const perCorrectXP = stageKey === "mcq" ? XP_PER_MCQ_CORRECT : XP_PER_FIB_CORRECT;
    result.correctFlags.forEach(flag => {
      if (flag) {
        sittingStreak++;
        maxSittingStreak = Math.max(maxSittingStreak, sittingStreak);
        xpEarned += perCorrectXP + (sittingStreak > 1 ? XP_STREAK_BONUS_PER_LEVEL * (sittingStreak - 1) : 0);
      } else {
        sittingStreak = 0;
      }
    });
    const bestScored = Math.max(prevStage.bestScored || 0, result.scored);
    weekProg.stages[stageKey] = {
      attempts, bestScored, bestTotal: result.total,
      lastScored: result.scored, lastTotal: result.total, lastAttemptDate: today
    };
  } else {
    xpEarned = XP_PER_SHORT_DONE * result.count;
    weekProg.stages[stageKey] = { attempts, lastAttemptDate: today, completed: true };
  }

  PROGRESS.totalXP += xpEarned;
  if (maxSittingStreak > PROGRESS.bestSittingStreak) PROGRESS.bestSittingStreak = maxSittingStreak;

  saveProgress(PROGRESS);
  return { xpEarned, maxSittingStreak };
}

function weekMasteryBadge(c, w) {
  const weekProg = PROGRESS.courses[c] && PROGRESS.courses[c].weeks[w];
  if (!weekProg) return null;
  const mcq = weekProg.stages.mcq;
  const fib = weekProg.stages.fib;
  if (!mcq && !fib) return null;
  const scored = (mcq ? mcq.bestScored : 0) + (fib ? fib.bestScored : 0);
  const total = (mcq ? mcq.bestTotal : 0) + (fib ? fib.bestTotal : 0);
  if (total === 0) return null;
  if (scored === total) return { icon: "🥇", label: "Gold" };
  if (scored >= total * 0.7) return { icon: "🥈", label: "Silver" };
  if (scored >= total * 0.5) return { icon: "🥉", label: "Bronze" };
  return null;
}

function weekReviewDue(c, w) {
  const weekProg = PROGRESS.courses[c] && PROGRESS.courses[c].weeks[w];
  if (!weekProg) return false;
  const dates = Object.values(weekProg.stages).map(s => s.lastAttemptDate).filter(Boolean);
  if (dates.length === 0) return false;
  const mostRecent = dates.sort().slice(-1)[0];
  return daysBetween(mostRecent, todayStr()) >= REVIEW_DUE_DAYS;
}

const STAGES = [
  { key: "mcq",   label: "Multiple Choice" },
  { key: "fib",   label: "Fill in the Blank" },
  { key: "short", label: "Short Answer" }
];
let view = "home";        // "home" | "weeks" | "quiz"
let currentCourse = 0;
let currentWeek = 0;      // index into course.weeks (0-5)
let stageIndex = 0;       // 0=mcq, 1=fib, 2=short
let phase = "test";       // "test" | "results"
let answers = {};
let selectedIdx = [];
let stageResults = {};    // stageResults[c][w][stageKey] = {scored,total} or true
let courseStageDone = {}; // courseStageDone[c][w][stageKey] = true/false
let lastGameResult = null; // {xpEarned, maxSittingStreak} from the most recent submitStage()

const QUESTIONS_PER_SITTING = 5;
const STAGES_PER_WEEK = 3;
const TOTAL_STAGES_PER_COURSE = STAGES_PER_WEEK * 6; // 6 weeks

function pickRandomIndices(poolSize, n) {
  const all = Array.from({ length: poolSize }, (_, i) => i);
  for (let i = all.length - 1; i > 0; i--) {
    const j = Math.floor(Math.random() * (i + 1));
    [all[i], all[j]] = [all[j], all[i]];
  }
  return all.slice(0, Math.min(n, poolSize));
}

function norm(s) {
  return (s || "").toLowerCase().trim().replace(/[^a-z0-9 ;]/g, "").replace(/\s+/g, " ");
}
function fibMatches(userVal, correctVal) {
  const u = norm(userVal);
  if (!u) return false;
  const parts = correctVal.split(";").map(p => norm(p)).filter(Boolean);
  if (parts.length > 1) {
    return parts.every(p => u.includes(p)) || parts.some(p => u === p);
  }
  const c = norm(correctVal);
  return u === c || u.includes(c) || c.includes(u);
}

function ensureDoneMap(c, w) {
  if (!courseStageDone[c]) courseStageDone[c] = {};
  if (!courseStageDone[c][w]) courseStageDone[c][w] = {};
  return courseStageDone[c][w];
}
function ensureResultsMap(c, w) {
  if (!stageResults[c]) stageResults[c] = {};
  if (!stageResults[c][w]) stageResults[c][w] = {};
  return stageResults[c][w];
}

function weekProgressLabel(c, w) {
  const done = (courseStageDone[c] && courseStageDone[c][w]) || {};
  const n = STAGES.filter(s => done[s.key]).length;
  if (n === 0) return null;
  if (n === STAGES_PER_WEEK) return "Completed";
  return `${n}/${STAGES_PER_WEEK} stages done`;
}
function courseProgressLabel(c) {
  const weeks = (courseStageDone[c]) || {};
  let n = 0;
  Object.keys(weeks).forEach(w => {
    n += STAGES.filter(s => weeks[w][s.key]).length;
  });
  if (n === 0) return null;
  if (n === TOTAL_STAGES_PER_COURSE) return "Completed";
  return `${n}/${TOTAL_STAGES_PER_COURSE} stages done`;
}

function render() {
  const el = document.getElementById("app");
  if (view === "home") el.innerHTML = renderHome();
  else if (view === "weeks") el.innerHTML = renderWeeks();
  else if (phase === "test") el.innerHTML = renderStageTest();
  else el.innerHTML = renderStageResults();
  attachHandlers();
}

function renderHome() {
  const rows = courses.map((c, i) => {
    const label = courseProgressLabel(i);
    return `
    <button class="course-row" data-course="${i}">
      <div class="course-code">${c.code}</div>
      <div class="course-meta">
        <div class="course-title">${c.title}</div>
        <div class="course-topic">6 weeks available</div>
      </div>
      ${label ? `<div class="course-progress">${label}</div>` : ''}
      <div class="course-arrow">→</div>
    </button>
  `;
  }).join("");
  const noteDismissed = (() => { try { return localStorage.getItem(NOTE_DISMISS_KEY) === "1"; } catch (e) { return false; } })();

  return `
    <div class="masthead">
      <div class="kicker">Course Self-Test</div>
      <h1>Course Self-Test</h1>
      <p>Mass Communication &amp; Media Studies — 100 Level, First Semester. Pick a course to begin.</p>
    </div>
    <div class="hud">
      <div class="hud-pill gold">🔥 <span class="n">${PROGRESS.dayStreak}</span> day streak</div>
      <div class="hud-pill">⭐ <span class="n">${PROGRESS.totalXP}</span> XP</div>
    </div>
    ${noteDismissed ? "" : `
    <div class="device-note" id="deviceNote">
      Your progress (streaks, XP, badges) is saved only on this device and browser — it won't appear if you switch phones or computers.
      <button id="dismissNoteBtn">Got it</button>
    </div>`}
    <div class="course-list">${rows}</div>
  `;
}

function renderWeeks() {
  const c = courses[currentCourse];
  const rows = c.weeks.map((w, i) => {
    const label = weekProgressLabel(currentCourse, i);
    const badge = weekMasteryBadge(currentCourse, i);
    const reviewDue = weekReviewDue(currentCourse, i);
    return `
    <button class="week-row" data-week="${i}">
      <div class="week-label">${badge ? `<span class="badge-icon" title="${badge.label}">${badge.icon}</span>` : ''}Week ${w.week}</div>
      <div class="week-topic">${w.topic}</div>
      ${reviewDue ? `<div class="review-due">Review due</div>` : ''}
      ${label ? `<div class="course-progress">${label}</div>` : ''}
      <div class="week-arrow">→</div>
    </button>
  `;
  }).join("");
  return `
    <button class="back-link" id="backHomeBtn">← All courses</button>
    <div class="masthead">
      <div class="kicker">${c.code}</div>
      <h1>${c.title}</h1>
      <p>Choose a week to test yourself on.</p>
    </div>
    <div class="course-list">${rows}</div>
  `;
}

function stageTrackHtml() {
  return `
    <div class="stage-track">
      ${STAGES.map((s, i) => {
        const cls = i === stageIndex ? "active" : (i < stageIndex ? "done" : "");
        const dotContent = i < stageIndex ? "✓" : (i + 1);
        return `
          <div class="stage-step ${cls}">
            <div class="dot">${dotContent}</div>
            <span>${s.label}</span>
          </div>
          ${i < STAGES.length - 1 ? '<div class="stage-line"></div>' : ''}
        `;
      }).join("")}
    </div>
  `;
}

function renderStageTest() {
  const c = courses[currentCourse];
  const w = c.weeks[currentWeek];
  const stage = STAGES[stageIndex].key;
  const items = w[stage];
  const shown = selectedIdx.map(poolIdx => ({ poolIdx, item: items[poolIdx] }));

  let qHtml = "";
  if (stage === "mcq") {
    qHtml = shown.map(({ poolIdx, item }, i) => {
      const key = `${poolIdx}`;
      const opts = item.opts.map((opt, oi) => {
        const checked = answers[key] === oi ? "selected" : "";
        return `
          <label class="opt ${checked}">
            <input type="radio" name="q${key}" value="${oi}" ${answers[key] === oi ? "checked" : ""} data-key="${key}">
            <span>${opt}</span>
          </label>`;
      }).join("");
      return `
        <div class="q-block">
          <div class="q-text"><span class="q-num">${i + 1}.</span>${item.q}</div>
          ${opts}
        </div>`;
    }).join("");
  } else if (stage === "fib") {
    qHtml = shown.map(({ poolIdx, item }, i) => {
      const key = `${poolIdx}`;
      const val = answers[key] || "";
      return `
        <div class="q-block">
          <div class="q-text"><span class="q-num">${i + 1}.</span>${item.q}</div>
          <input type="text" class="fib-input" data-key="${key}" value="${val.replace(/"/g,'&quot;')}" placeholder="Type your answer">
        </div>`;
    }).join("");
  } else {
    qHtml = shown.map(({ poolIdx, item }, i) => {
      const key = `${poolIdx}`;
      const val = answers[key] || "";
      return `
        <div class="q-block">
          <div class="q-text"><span class="q-num">${i + 1}.</span>${item.q}</div>
          <textarea class="short-input" data-key="${key}" placeholder="Answer from memory...">${val}</textarea>
        </div>`;
    }).join("");
  }

  const note = stage === "fib"
    ? '<div class="section-note">One word/phrase per blank. Close matches are accepted.</div>'
    : stage === "short"
    ? '<div class="section-note">These aren\'t auto-graded — you\'ll compare your answer to a suggested answer after submitting.</div>'
    : "";

  return `
    <button class="back-link" id="backWeeksBtn">← ${c.code} weeks</button>
    <div class="masthead">
      <div class="kicker">${c.code} — Week ${w.week}</div>
      <h1>${c.title}</h1>
      <p>${w.topic}</p>
    </div>
    ${stageTrackHtml()}
    <div class="section-header"><h2>${STAGES[stageIndex].label}</h2><span class="count">${QUESTIONS_PER_SITTING} questions (random from a larger pool)</span></div>
    ${note}
    ${qHtml}
    <div class="submit-bar">
      <button class="btn" id="submitBtn">${stage === "short" ? "Submit & Review" : "Submit & See Score"}</button>
    </div>
  `;
}

function renderStageResults() {
  const c = courses[currentCourse];
  const w = c.weeks[currentWeek];
  const stage = STAGES[stageIndex].key;
  const items = w[stage];
  const shown = selectedIdx.map(poolIdx => ({ poolIdx, item: items[poolIdx] }));
  const isLast = stageIndex === STAGES.length - 1;
  const r = stageResults[currentCourse] && stageResults[currentCourse][currentWeek] && stageResults[currentCourse][currentWeek][stage];

  let scoreCardHtml = "";
  let reviewHtml = "";

  if (stage === "mcq" || stage === "fib") {
    const pct = Math.round((r.scored / r.total) * 100);
    scoreCardHtml = `
      <div class="score-card">
        <div class="big">${r.scored}/${r.total}</div>
        <div class="label">${STAGES[stageIndex].label} score (${pct}%)</div>
      </div>`;
    reviewHtml = shown.map(({ poolIdx, item }, i) => {
      const key = `${poolIdx}`;
      if (stage === "mcq") {
        const userIdx = answers[key];
        const isCorrect = userIdx === item.a;
        const userText = userIdx === undefined ? '<span class="unanswered">No answer given</span>' : item.opts[userIdx];
        return `
          <div class="review-block ${isCorrect ? 'correct' : 'incorrect'}">
            <div class="review-q">${i + 1}. ${item.q}</div>
            <div class="review-row"><span class="tag ${isCorrect ? '' : 'your-ans wrong'}">Your answer</span><span class="${isCorrect ? '' : 'your-ans wrong'}">${userText}</span></div>
            ${!isCorrect ? `<div class="review-row"><span class="tag correct-ans">Correct answer</span><span class="correct-ans">${item.opts[item.a]}</span></div>` : ''}
          </div>`;
      } else {
        const userVal = answers[key] || "";
        const isCorrect = fibMatches(userVal, item.a);
        const userText = userVal.trim() ? userVal : '<span class="unanswered">No answer given</span>';
        return `
          <div class="review-block ${isCorrect ? 'correct' : 'incorrect'}">
            <div class="review-q">${i + 1}. ${item.q}</div>
            <div class="review-row"><span class="tag ${isCorrect ? '' : 'your-ans wrong'}">Your answer</span><span class="${isCorrect ? '' : 'your-ans wrong'}">${userText}</span></div>
            ${!isCorrect ? `<div class="review-row"><span class="tag correct-ans">Correct answer</span><span class="correct-ans">${item.a.replace(';', ' / ')}</span></div>` : ''}
          </div>`;
      }
    }).join("");
  } else {
    scoreCardHtml = `
      <div class="score-card">
        <div class="big">Done</div>
        <div class="label">Short Answer — self-review</div>
        <div class="sub">Compare your own wording to the suggested answer below. No auto-score for this section.</div>
      </div>`;
    reviewHtml = shown.map(({ poolIdx, item }, i) => {
      const key = `${poolIdx}`;
      const userVal = answers[key] || "";
      const userText = userVal.trim() ? userVal : '<span class="unanswered">No answer given</span>';
      return `
        <div class="review-block">
          <div class="review-q">${i + 1}. ${item.q}</div>
          <div class="review-row"><span class="tag">Your answer</span><span>${userText}</span></div>
          <div class="suggested-box"><span class="tag">Suggested answer</span>${item.a}</div>
        </div>`;
    }).join("");
  }

  const nextLabel = !isLast ? `Continue to ${STAGES[stageIndex + 1].label} →` : `Finish Week ${w.week}`;

  const gr = lastGameResult || { xpEarned: 0, maxSittingStreak: 0 };
  const streakBannerHtml = gr.maxSittingStreak >= 3
    ? `<div class="streak-banner">🔥 ${gr.maxSittingStreak}-in-a-row streak this round! Bonus XP applied.</div>`
    : "";
  const xpSummaryHtml = (stage === "mcq" || stage === "fib")
    ? `<div class="xp-summary">
        <div><div class="stat-num">+${gr.xpEarned}</div><div class="stat-label">XP earned</div></div>
        <div><div class="stat-num">${PROGRESS.totalXP}</div><div class="stat-label">Total XP</div></div>
        <div><div class="stat-num">🔥 ${PROGRESS.dayStreak}</div><div class="stat-label">Day streak</div></div>
      </div>`
    : "";
  const badgeNow = weekMasteryBadge(currentCourse, currentWeek);
  const badgeEncourage = badgeNow && badgeNow.label === "Gold"
    ? "You've hit full marks on this week's best attempts!"
    : "Keep retrying to push for a higher badge.";
  const badgeToastHtml = (stage === "mcq" || stage === "fib") && badgeNow
    ? `<div class="new-badge-toast">${badgeNow.icon} Current mastery for Week ${w.week}: ${badgeNow.label} — ${badgeEncourage}</div>`
    : "";

  return `
    <button class="back-link" id="backWeeksBtn">← ${c.code} weeks</button>
    <div class="masthead">
      <div class="kicker">${c.code} — Week ${w.week} Results</div>
      <h1>${c.title}</h1>
    </div>
    ${stageTrackHtml()}
    ${streakBannerHtml}
    ${scoreCardHtml}
    ${xpSummaryHtml}
    ${badgeToastHtml}
    <div class="section-header"><h2>${STAGES[stageIndex].label} — Review</h2></div>
    ${reviewHtml}
    <div class="results-actions">
      <button class="btn secondary" id="retryBtn">Try Again</button>
      <button class="btn" id="nextBtn">${nextLabel}</button>
    </div>
  `;
}

function goHome() {
  view = "home";
  render();
  window.scrollTo(0, 0);
}

function goWeeks(courseIdx) {
  currentCourse = courseIdx;
  view = "weeks";
  render();
  window.scrollTo(0, 0);
}

function startStage(weekIdx, idx) {
  currentWeek = weekIdx;
  stageIndex = idx;
  phase = "test";
  answers = {};
  view = "quiz";
  const pool = courses[currentCourse].weeks[weekIdx][STAGES[idx].key];
  selectedIdx = pickRandomIndices(pool.length, QUESTIONS_PER_SITTING);
  render();
  window.scrollTo(0, 0);
}

function submitStage() {
  const c = courses[currentCourse];
  const w = c.weeks[currentWeek];
  const stage = STAGES[stageIndex].key;
  const items = w[stage];

  const resultsMap = ensureResultsMap(currentCourse, currentWeek);
  const doneMap = ensureDoneMap(currentCourse, currentWeek);

  let gameResult;
  if (stage === "mcq") {
    let scored = 0;
    const correctFlags = selectedIdx.map(poolIdx => {
      const ok = answers[`${poolIdx}`] === items[poolIdx].a;
      if (ok) scored++;
      return ok;
    });
    resultsMap.mcq = { scored, total: selectedIdx.length };
    gameResult = recordStageCompletion(currentCourse, currentWeek, "mcq", { correctFlags, scored, total: selectedIdx.length });
  } else if (stage === "fib") {
    let scored = 0;
    const correctFlags = selectedIdx.map(poolIdx => {
      const ok = fibMatches(answers[`${poolIdx}`] || "", items[poolIdx].a);
      if (ok) scored++;
      return ok;
    });
    resultsMap.fib = { scored, total: selectedIdx.length };
    gameResult = recordStageCompletion(currentCourse, currentWeek, "fib", { correctFlags, scored, total: selectedIdx.length });
  } else {
    resultsMap.short = true;
    gameResult = recordStageCompletion(currentCourse, currentWeek, "short", { count: selectedIdx.length });
  }
  doneMap[stage] = true;
  lastGameResult = gameResult;

  phase = "results";
  render();
  window.scrollTo(0, 0);
}

function attachHandlers() {
  if (view === "home") {
    document.querySelectorAll("[data-course]").forEach(btn => {
      btn.addEventListener("click", () => {
        goWeeks(parseInt(btn.getAttribute("data-course"), 10));
      });
    });
    const dismissBtn = document.getElementById("dismissNoteBtn");
    if (dismissBtn) {
      dismissBtn.addEventListener("click", () => {
        try { localStorage.setItem(NOTE_DISMISS_KEY, "1"); } catch (e) {}
        render();
      });
    }
    return;
  }

  if (view === "weeks") {
    document.getElementById("backHomeBtn").addEventListener("click", goHome);
    document.querySelectorAll("[data-week]").forEach(btn => {
      btn.addEventListener("click", () => {
        startStage(parseInt(btn.getAttribute("data-week"), 10), 0);
      });
    });
    return;
  }

  // view === "quiz"
  document.getElementById("backWeeksBtn").addEventListener("click", () => goWeeks(currentCourse));

  if (phase === "test") {
    document.querySelectorAll('input[type=radio]').forEach(r => {
      r.addEventListener("change", (e) => {
        answers[e.target.getAttribute("data-key")] = parseInt(e.target.value, 10);
        render();
      });
    });
    document.querySelectorAll('.fib-input').forEach(inp => {
      inp.addEventListener("input", (e) => {
        answers[e.target.getAttribute("data-key")] = e.target.value;
      });
    });
    document.querySelectorAll('.short-input').forEach(inp => {
      inp.addEventListener("input", (e) => {
        answers[e.target.getAttribute("data-key")] = e.target.value;
      });
    });
    document.getElementById("submitBtn").addEventListener("click", submitStage);
  } else {
    document.getElementById("retryBtn").addEventListener("click", () => {
      startStage(currentWeek, stageIndex);
    });
    document.getElementById("nextBtn").addEventListener("click", () => {
      if (stageIndex < STAGES.length - 1) {
        startStage(currentWeek, stageIndex + 1);
      } else {
        goWeeks(currentCourse);
      }
    });
  }
}

try {
  render();
} catch (e) {
  document.getElementById("app").innerHTML =
    '<div style="padding:24px;font-family:sans-serif;color:#9B3B32;">' +
    '<h2 style="margin-top:0;">Something went wrong loading the quiz</h2>' +
    '<p>Please try reopening this file in a full browser app (Safari or Chrome), not a quick preview.</p>' +
    '<p style="font-size:12px;color:#666;">' + (e && e.message ? e.message : e) + '</p>' +
    '</div>';
}

</script>
</body>
</html>
