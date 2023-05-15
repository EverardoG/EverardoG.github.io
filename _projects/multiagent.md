---
title: 'Leader-Follower Swarms'
subtitle: 'Structural Credit Assignment for Leader Agents'
date: 2020-11-10 00:00:00
description:
featured_image: '/images/landing_page/landing_leader_follower.png'
---

<img src="/images/landing_page/landing_leader_follower.png" alt="drawing" width="800"/>

<p style="text-align: left;"> On the left is a leader agent capapble of sensing other swarm members, and points of interest the swarm must visit. On the right is a follower agent only capable of sensing and responding to other swarm members by repulsing away from nearby members and moving towards far away members. Leader agents learn how to guide follower agents to visit various points of interest. </p>

### Overview 

**Timeline:** Ongoing research project started in Summer 2022 at Oregon State University

**Collaborators:** Andrew Festa, Nathan Hewitt, w. Advisor Kagan Tumer

This research explores how to modify difference rewards from reward shaping in order to work for a multiagent learning approach to swarm shepherding. The swarm is split into leaders and followers, pictured above, where each leader is an independent learning agent and each follower uses a simple pre-programmed following behavior to respond to nearby neighbors. The idea is to shape leaders' rewards such that the leaders can learn how to intelligently split the swarm across multiple points of interest without any central coordination.

I first explored this idea in depth with Andrew and Nathan in a 9-week final project for our multiagent systems course in Winter 2023. The [write-up](https://everardog.github.io/files/leader_follower_project.pdf) goes into detail as to how the method works and what preliminary results show. 

I am currently working on a paper independently for [MRS 2023](https://sites.bu.edu/mrs2023/) that further investigates this concept. I gave a [live interview](https://open.spotify.com/episode/2VWn9AGBBKOcNHGutHgcQZ?si=73eadafd697c4725) with a radio station explaining how my reward shaping method works to the public. My [qualifying exam documnet](https://everardog.github.io/files/quals.pdf) goes into detail as to where this research fits into the existing literature, related research directions, and some of the broader societal impacts of this work.
