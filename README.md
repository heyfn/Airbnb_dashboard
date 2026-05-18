# Airbnb_dashboard

Airbnb Analytics: Listings, Ratings & Reviews Dashboard
A multi-page interactive Power BI report designed to explore Airbnb listing data across cities — covering host behaviour, pricing, room types, guest ratings, and review patterns.

The Airbnb Analytics Dashboard is a structured, three-page Power BI report built to surface actionable insights from Airbnb listing and review data. It enables analysts, property managers, and platform strategists to understand how listings are distributed across cities, how guests rate their stays across multiple dimensions, and how review activity trends over time. The dashboard is designed to support decisions around host quality assessment, market competitiveness, and guest experience benchmarking.

Tech Stack
The dashboard was built using the following tools and technologies:
📊 Power BI Desktop — Main data visualisation platform for report design and publishing.
📂 Power Query — Data transformation and cleaning layer used to reshape the Listings and Reviews tables.
🧠 DAX (Data Analysis Expressions) — Used extensively for calculated measures including cumulative rankings, percentage splits, conditional host segmentation, and dynamic review frequency distributions.
📐 Data Modelling — Relationships established between Listings and Reviews tables using listing_id as the key, with supporting DateTable templates for time intelligence.
📁 File Format — .pbit (Power BI Template) for portability and reuse across datasets.

Data Source
The dashboard is built on two core tables:
Listings — Contains property-level details for each Airbnb listing, including:
Host attributes: host_id, host_since, host_response_time, host_acceptance_rate, host_is_superhost, host_identity_verified, host_has_profile_pic
Location: city, district, neighbourhood, latitude, longitude
Property details: property_type, room_type, accommodates, bedrooms, amenities, price, minimum_nights, maximum_nights, instant_bookable
Review scores: review_scores_rating, review_scores_accuracy, review_scores_cleanliness, review_scores_checkin, review_scores_communication, review_scores_location, review_scores_value
Reviews — Contains guest review records linked to listings, including listing_id, review_id, date, reviewer_id, and derived fields for frequency analysis and monthly aggregation.

Features & Highlights
Business Problem
Airbnb hosts, property managers, and market analysts often struggle to make sense of large volumes of listing and review data scattered across cities. Key questions such as: Which cities have the most listings and how are they distributed by room type? How do ratings vary across cleanliness, location, and value dimensions? Are superhosts genuinely better rated? How frequently do reviewers return, and how has review activity changed over time? — are difficult to answer at a glance without a structured visual tool.
Goal of the Dashboard
To deliver an interactive, multi-page analytical report that enables users to:

Benchmark listings and hosts across cities and room types.
Evaluate guest satisfaction across six distinct rating dimensions.
Understand review volume trends and reviewer loyalty patterns over time.

Walkthrough of Key Pages & Visuals
Page 1 — Overview
Provides a high-level summary of the listings landscape.
KPI Cards (Top Row): Five card visuals surface headline metrics — Total Listings, Total Hosts, Average Price, Superhost Listings, and Avg Rating — giving an instant snapshot of the market.
Line Chart — Cumulative Listings by City: Shows the cumulative distribution of listings ranked by city, highlighting how listing volume is concentrated in a handful of dominant markets (Pareto-style view).
Room Type Breakdown: Four dedicated measures (Entire Place, Private Room, Hotel Room, Shared Room) feed summary visuals that show the split in accommodation type across the dataset.
Host Trust Segmentation: A 2×2 matrix of measures (Verified_Profile, Verified_NoProfile, NotVerified_Profile, NotVerified_NoProfile) surfaces the relationship between identity verification and profile picture presence, useful for trust and quality analysis.
Page 2 — Ratings
Drills into how guests score their stays across six review dimensions.
Combo Chart — Avg Rating by City: A line and stacked column combo chart overlays average overall rating against the volume of listings per city, making it easy to spot whether highly-rated cities are also the most listed.
Bar Chart — Ratings Comparison: Ranks cities or property types by one of the six review score dimensions (accuracy, cleanliness, check-in, communication, location, value).
Column Chart: Provides a granular breakdown of score distributions across the dataset.
Pivot Table: A detailed matrix showing all six review score dimensions (Accuracy, Cleanliness, Check-in, Communication, Location, Value) side by side — useful for spotting which dimension consistently underperforms.
Page 3 — Reviews
Focuses on review activity, reviewer behaviour, and temporal trends.
KPI Cards: Four cards display Total Reviews, Total Reviewers, unique Reviewer count (distinct), and a derived activity metric.
Column Chart — Reviews by Month: Shows the distribution of review activity across calendar months, revealing seasonal booking and travel patterns.
Combo Chart — Review Frequency Distribution with Cumulative %: Overlays review frequency (how many times a reviewer has reviewed) with a cumulative percentage line, illustrating reviewer loyalty and the proportion of one-time versus repeat reviewers.
Ribbon Chart — Reviews by City Over Time: Tracks how review volumes shift between cities over time, with ribbon width and colour indicating relative share — useful for spotting emerging or declining markets.
% of Monthly Reviews: A DAX measure normalises review counts by city selection, enabling fair cross-city comparisons regardless of total listing volume.
Business Impact & Insights
Host Quality Assessment: The trust segmentation and superhost measures help platform teams or property managers identify gaps between verified identity and actual listing quality.
Pricing Strategy: Average price cards combined with city-level listing counts enable hosts to benchmark their pricing against the local market.
Guest Experience Improvement: The six-dimension ratings breakdown pinpoints where hosts consistently fall short — whether in cleanliness, communication, or perceived value — enabling targeted improvements.
Market Trend Analysis: The ribbon and monthly review charts help analysts track which cities are gaining traction and which are stagnating, supporting investment and partnership decisions.
Reviewer Loyalty Modelling: The cumulative review frequency chart reveals the concentration of reviews among a small pool of active reviewers — critical insight for trust and authenticity strategies.

<img width="569" height="429" alt="image" src="https://github.com/user-attachments/assets/8adec17e-f045-43a6-bdad-407c23364f9d" />
