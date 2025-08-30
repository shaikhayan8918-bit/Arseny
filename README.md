# Arseny
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>VRSEN AI Agents-as-a-Service</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
    <style>
        /* CSS Reset & Normalization */
        :root {
            --bg-color: #0a0a1a;
            --text-color: #e0e0e0;
            --primary-color: #00aaff;
            --primary-hover: #0088cc;
            --secondary-color: #1a1a3a;
            --border-color: #2a2a4a;
            --headline-font: 'Inter', sans-serif;
            --body-font: 'Inter', sans-serif;
        }

        *, *::before, *::after {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
        }

        html, body {
            overflow-x: hidden;
            scroll-behavior: smooth;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-color);
            font-family: var(--body-font);
            line-height: 1.7;
            -webkit-font-smoothing: antialiased;
        }

        /* General Styles */
        .container {
            width: 100%;
            max-width: 800px;
            margin: 0 auto;
            padding: 0 20px;
        }

        section {
            padding: 80px 0;
            border-bottom: 1px solid var(--border-color);
        }

        h1, h2, h3 {
            font-family: var(--headline-font);
            font-weight: 700;
            line-height: 1.2;
            color: #ffffff;
            text-align: center;
        }

        h1 {
            font-size: 2.8rem;
            margin-bottom: 1rem;
        }
        
        .preheader {
            text-align: center;
            font-size: 0.9rem;
            font-weight: 600;
            color: var(--primary-color);
            text-transform: uppercase;
            letter-spacing: 1.5px;
            margin-bottom: 1rem;
        }

        .subheader {
            font-size: 1.2rem;
            max-width: 650px;
            margin: 0 auto 2rem auto;
            color: #b0b0c0;
            text-align: center;
        }
        
        .fascination-headline {
            font-size: 2.2rem;
            font-weight: 700;
            margin-bottom: 3rem;
            color: #ffffff;
            text-align: center;
        }
        
        p {
            font-size: 1.1rem;
            margin-bottom: 1.5rem;
            max-width: 650px;
            margin-left: auto;
            margin-right: auto;
        }

        b, strong {
            font-weight: 600;
            color: #ffffff;
        }
        
        .cta-button {
            display: inline-block;
            background: linear-gradient(90deg, var(--primary-color) 0%, #00c2ff 100%);
            color: #000;
            font-size: 1.1rem;
            font-weight: 700;
            text-decoration: none;
            padding: 18px 36px;
            border-radius: 8px;
            text-align: center;
            transition: transform 0.2s ease, box-shadow 0.2s ease;
            box-shadow: 0 4px 15px rgba(0, 170, 255, 0.3);
        }

        .cta-button:hover {
            transform: translateY(-3px);
            box-shadow: 0 6px 20px rgba(0, 170, 255, 0.4);
        }

        .center-content {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        /* Hero Section */
        .hero {
            padding-top: 100px;
            padding-bottom: 100px;
            background: radial-gradient(circle at 50% 0%, rgba(0, 170, 255, 0.1), transparent 40%);
        }

        .vsl-container {
            width: 100%;
            max-width: 600px;
            margin: 2rem auto 2.5rem auto;
            aspect-ratio: 16 / 9;
            background-image: url('https://placehold.co/600x338/0a0a1a/e0e0e0?text=See+How+It+Works');
            background-size: cover;
            background-position: center;
            border-radius: 12px;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            position: relative;
            box-shadow: 0 10px 30px rgba(0,0,0,0.5);
            border: 1px solid var(--border-color);
        }
        
        .vsl-container::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            right: 0;
            bottom: 0;
            background: rgba(0,0,0,0.3);
            border-radius: 12px;
        }

        .play-button {
            width: 80px;
            height: 80px;
            background-color: rgba(255, 255, 255, 0.9);
            border-radius: 50%;
            display: flex;
            justify-content: center;
            align-items: center;
            z-index: 1;
            transition: transform 0.2s ease;
        }
        
        .vsl-container:hover .play-button {
            transform: scale(1.1);
        }

        .play-button svg {
            width: 40px;
            height: 40px;
            fill: #000;
            margin-left: 5px;
        }

        /* Content Sections */
        .outcome-bullets ul {
            list-style: none;
            max-width: 650px;
            margin: 0 auto;
        }
        
        .outcome-bullets li {
            font-size: 1.1rem;
            padding: 20px;
            margin-bottom: 1rem;
            background-color: var(--secondary-color);
            border-left: 4px solid var(--primary-color);
            border-radius: 0 8px 8px 0;
        }
        
        /* FAQ Section */
        .faq-item {
            background-color: var(--secondary-color);
            border-radius: 8px;
            padding: 25px;
            margin-bottom: 1rem;
            border: 1px solid var(--border-color);
        }
        
        .faq-item h3 {
            font-size: 1.2rem;
            text-align: left;
            margin-bottom: 0.5rem;
        }
        
        .faq-item p {
            margin-bottom: 0;
            text-align: left;
            color: #b0b0c0;
        }

        /* Responsive Design */
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            .fascination-headline {
                font-size: 1.8rem;
            }
            p {
                font-size: 1rem;
            }
            section {
                padding: 60px 0;
            }
            .hero {
                padding-top: 80px;
                padding-bottom: 80px;
            }
        }
    </style>
</head>
<body>

    <!-- HERO SECTION -->
    <header class="hero">
        <div class="container center-content">
            <p class="preheader">FOR MARKETING AGENCIES & DATA TEAMS DROWNING IN MANUAL WORK</p>
            <h1>Get Client-Ready BigQuery Reports & Ad Previews in Minutes… Not Days.</h1>
            <p class="subheader">And do it with custom AI agents, without writing another complex query or manually taking another screenshot.</p>
            
            <div class="vsl-container" aria-label="Watch video demonstration">
                <div class="play-button">
                    <svg viewBox="0 0 24 24"><path d="M8 5v14l11-7z"></path></svg>
                </div>
            </div>
            
            <a href="#offer" class="cta-button">Book My Automation Strategy Call</a>
        </div>
    </header>

    <!-- PROBLEM IDENTIFICATION -->
    <section id="problem">
        <div class="container">
            <h2 class="fascination-headline">That Sinking Feeling When You Realize It’s 4 PM and the Report Is Still Running…</h2>
            <p>You know the feeling.</p>
            <p>The little wheel is spinning on the BigQuery tab. Your client is expecting insights for their end-of-week meeting, and you’re stuck here, waiting.</p>
            <p>When it finally finishes, the real "fun" begins.</p>
            <p>Manually exporting data. Fiddling with chart settings. Tediously creating dozens of "tare sheets"—taking screenshot after screenshot to show clients how their ads will look on major websites.</p>
            <p>It’s mundane. It’s soul-crushing. And it’s a colossal waste of your team's talent.</p>
            <p>You’ve tried hiring more junior analysts. You’ve tried buying more expensive BI tools. But they don't fix the core problem: <b>the bottleneck is still manual human effort.</b></p>
            <p>And the cost of doing nothing? It’s not just wasted hours. It’s delayed campaigns. It’s clients questioning your efficiency. It’s the constant, nagging fear that one tiny human error in a query could send an entire strategy off course.</p>
        </div>
    </section>

    <!-- ORIGIN STORY -->
    <section id="story">
        <div class="container">
            <h2 class="fascination-headline">We Built This After a $50,000 Campaign Nearly Derailed Over a Single Typo.</h2>
            <p>Years ago, our team was on the verge of landing a career-defining client. The final pitch was in two days. All we needed was one critical report from BigQuery and a deck of ad placement previews.</p>
            <p>Simple, right?</p>
            <p>Our best data analyst was swamped. He pulled an all-nighter running queries. Our design intern spent an entire day manually placing ad mockups onto screenshots.</p>
            <p>At the eleventh hour, we found it. A tiny typo in a SQL query. The entire dataset was skewed. The insights were wrong. <i>Panic.</i></p>
            <p>We fixed it, we landed the client, but the near-miss haunted us. We were a team of strategists, yet we were operating like a 1990s data entry firm.</p>
            <p>That’s when it hit us. We didn't need another dashboard or a faster computer. We needed a better employee… a digital one.</p>
            <p>One that could understand our plain-English requests, run the query perfectly every time, visualize the data, and generate the previews… all in the time it takes to make a coffee. So we built our first AI agent using a framework we called Agency Swarm.</p>
        </div>
    </section>

    <!-- SOLUTION REVELATION -->
    <section id="solution">
        <div class="container">
            <h2 class="fascination-headline">What If You Could ‘Hire’ a Team of AI Agents That Never Sleep, Make Zero Errors, and Cost Less Than a Team Lunch?</h2>
            <p>This isn't just one tool. It’s an orchestrated team of specialist AI agents, working together inside our Agency Swarm framework.</p>
            <p>You get two key agents to start:</p>
            <p><b>1. The BigQuery Insight Agent:</b> Your 24/7 data analyst. Simply tell it what you need in plain English. It dives into BigQuery, pulls the right data, analyzes it, visualizes it with tools like ArcGIS, and delivers a finished report. Customers have cut query and reporting time by over 80%.</p>
            <p><b>2. The Tare Sheet Agent:</b> Your tireless creative assistant. Give it a list of high-profile websites and your ad creative. Using OpenCV and GPT-4O, it generates hundreds of pixel-perfect visual previews in seconds… for just <b>three to five cents per sheet.</b></p>
            <p>The results aren't just faster work. It’s a fundamental shift in how your agency operates.</p>
            
            <div class="outcome-bullets">
                <ul>
                    <li><b>Custom AI Agent Roles…</b> so you can finally delegate the mind-numbing data pulls and get back to actual strategy, making you the most valuable person in the room.</li>
                    <li><b>Direct BigQuery & OpenCV Integration…</b> which means no more exporting CSVs or messy manual checks, giving you unshakeable confidence in your numbers.</li>
                    <li><b>Automated Tare Sheet Generation…</b> letting you send clients hundreds of ad previews in minutes, not weeks, positioning your agency as impossibly fast and efficient.</li>
                </ul>
            </div>
        </div>
    </section>

    <!-- PRODUCT INTRODUCTION -->
    <section id="product">
        <div class="container">
            <h2 class="fascination-headline">This Isn’t Another Dashboard. It's Your New Automation Department.</h2>
            <p>We’re now offering this as <b>VRSEN Agents-as-a-Service.</b></p>
            <p>Forget the old way of doing things. No more hiring expensive engineers to build fragile scripts. No more paying for seats on another complex software platform your team will never fully use.</p>
            <p>This is a direct, automated pipeline from your raw data to client-ready insights and creative previews.</p>
            <p>We do the setup. We configure the agents to your exact needs. You simply give them their assignments.</p>
            <p>It's the efficiency of a dedicated automation team, without the overhead.</p>
        </div>
    </section>

    <!-- OFFER STRUCTURE -->
    <section id="offer" class="center-content">
        <div class="container">
            <h2 class="fascination-headline">Stop Trading Your Team's Hours for Dollars. Start Scaling With Intelligence.</h2>
            <p>Because this is a tailored service, not a one-size-fits-all piece of software, we need to talk.</p>
            <p>The next step is to book a free, no-obligation Automation Strategy Call. On this call, we will map out your current data and creative workflows and identify the single biggest bottleneck that's costing you time and money.</p>
            <p>Then, we'll show you exactly how a custom-configured AI agent could solve it.</p>
            <p><b>Our promise for the call:</b> If you don't leave the session with a clear plan that you believe can save your team at least 10 hours a week, you can walk away with the plan for free. No hard feelings, no pressure.</p>
            <p>Our consultants' calendars are open for these calls for the next 7 days. Once these slots are taken, we will be closing access to focus on our new clients. This is your window.</p>
            <br>
            <a href="https://calendly.com/" class="cta-button" target="_blank" rel="noopener noreferrer">Book My Free Automation Strategy Call</a>
        </div>
    </section>

    <!-- FAQ SECTION -->
    <section id="faq">
        <div class="container">
            <h2 class="fascination-headline">Your Questions, Answered.</h2>
            <div class="faq-list">
                <div class="faq-item">
                    <h3>This sounds expensive. What’s the catch?</h3>
                    <p>It's significantly less than hiring a full-time junior data analyst and it delivers 100x the output. We build a package based on your exact needs on our call, so you only pay for the automation you use. No bloat, no shelf-ware.</p>
                </div>
                <div class="faq-item">
                    <h3>How can I trust an AI with my critical client data?</h3>
                    <p>Think of it less like a creative chatbot and more like a hyper-advanced calculator. Our agents use validation and error-correction loops to follow precise instructions with checks and balances. It's often more accurate than a tired human at 5 PM on a Friday.</p>
                </div>
                <div class="faq-item">
                    <h3>I'm not a Python developer. Is this too technical for my team?</h3>
                    <p>Not at all. That's the point of our "Agents-as-a-Service" model. We handle all the technical setup and configuration. You and your team interact with the agents using simple, plain-English commands. If you can write an email, you can use this.</p>
                </div>
                <div class="faq-item">
                    <h3>How long will this take to get up and running?</h3>
                    <p>This isn't a 6-month enterprise integration project. We can have your first core agents—like the BigQuery report-puller or the Tare Sheet generator—operational and saving you time within days of our initial strategy call.</p>
                </div>
            </div>
            <div class="center-content" style="margin-top: 4rem;">
                <h3>Ready to Replace Repetitive Work With Automated Results?</h3>
                <br>
                <a href="https://calendly.com/" class="cta-button" target="_blank" rel="noopener noreferrer">Book My Call & Get My Automation Plan</a>
            </div>
        </div>
    </section>

</body>
</html>
