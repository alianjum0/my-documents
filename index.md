---
layout: home
title: Document Hub
---

# My Documents

Welcome to my personal document repository. This site organizes notes, plans, and information across various categories.

## Browse by Category

<div class="category-section">
    <div class="category-card">
        <h3>📆 Daily Planning</h3>
        <p>Day-to-day schedules, tasks, and planning notes to keep track of activities and goals.</p>
        <a href="./daily_planning/" class="category-link">View Daily Plans →</a>
    </div>
    
    <div class="category-card">
        <h3>🔍 Research</h3>
        <p>Notes, findings, and summaries from various research topics and interests.</p>
        <a href="./research/" class="category-link">Browse Research →</a>
    </div>
    
    <div class="category-card">
        <h3>🛒 Shopping</h3>
        <p>Shopping lists, product research, and purchase planning information.</p>
        <a href="./shopping/" class="category-link">See Shopping Lists →</a>
    </div>
    
    <div class="category-card">
        <h3>✈️ Trips</h3>
        <p>Travel plans, itineraries, packing lists, and trip reports from various destinations.</p>
        <a href="./trips/" class="category-link">Explore Trips →</a>
    </div>
</div>

## About This Site

This is a personal collection of markdown documents, organized by category. The site is built with Jekyll using the Minima theme and hosted on GitHub Pages.

<style>
.category-section {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
    margin: 30px 0;
}
.category-card {
    border: 1px solid #e8e8e8;
    border-radius: 5px;
    padding: 15px;
    background-color: #f9f9f9;
    transition: all 0.3s ease;
}
.category-card:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
}
.category-link {
    display: inline-block;
    margin-top: 10px;
    font-weight: bold;
    text-decoration: none;
}
</style> 