---
layout: post
title:  "External Featured Image"
author: sal
categories: [ Jekyll, tutorial, web development ]
image: "https://media.istockphoto.com/id/1076840920/vector/music-background.jpg?s=612x612&w=0&k=20&c=bMG2SEUYaurIHAjtRbw7bmjLsXyT7iJUvAM5HjL3G3I="
---

<!DOCTYPE html>
<html>
<head>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-EVSTQN3/azprG1Anm3QDgpJLIm9Nao0Yz1ztcQTwFspd3yD65VohhpuuCOmLASjC">
    <style>
        body {
            animation: colorTransition 10s infinite;
            background-color: #87cefa;
        }
@keyframes colorTransition {
            0% { background-color: #87cefa; }
            10% { background-color: #87cefa; }
            20% { background-color: #a4d3ff; }
            30% { background-color: #c1e8ff; }
            40% { background-color: #def3ff; }
            50% { background-color: #ebf9ff; }
            60% { background-color: #f8fdff; }
            70% { background-color: #ebf9ff; }
            80% { background-color: #def3ff; }
            90% { background-color: #c1e8ff; }
            100% { background-color: #a4d3ff; }
        }
.cloud-container {
            position: relative;
        }
.cloud {
            position: absolute;
            width: 200px;
            height: 100px;
            background-color: #fff;
            border-radius: 100px;
            box-shadow: 0px 0px 20px #888888;
            animation: cloudAnimation 10s linear infinite;
            z-index: -1; /* Set a lower z-index to keep the clouds in the background */
        }
.cloud::after,
        .cloud::before {
            content: "";
            position: absolute;
            background-color: #fff;
        }
.cloud::after {
            width: 80px;
            height: 80px;
            border-radius: 50%;
            top: -30px;
            left: 50px;
        }
.cloud::before {
            width: 120px;
            height: 120px;
            border-radius: 50%;
            top: -50px;
            right: 50px;
        }
@keyframes cloudAnimation {
            0% {
                transform: translateX(-200px);
            }
            50% {
                transform: translateX(calc(100% + 200px));
            }
            100% {
                transform: translateX(-200px);
            }
        }
.cloud:nth-child(2) {
            top: 150px;
            left: 200px;
            animation-duration: 15s;
            animation-direction: reverse;
        }
.cloud:nth-child(3) {
            top: 300px;
            left: 500px;
            animation-duration: 12s;
            animation-direction: reverse;
        }
.cloud:nth-child(4) {
            top: 450px;
            left: 800px;
            animation-duration: 10s;
            animation-direction: normal;
        }
.cloud:nth-child(5) {
            top: 600px;
            left: 200px;
            animation-duration: 14s;
            animation-direction: reverse;
        }
.cloud:nth-child(6) {
            top: 750px;
            left: 500px;
            animation-duration: 11s;
            animation-direction: normal;
        }
.title {
            text-align: center;
            font-size: 48px;
        }
.letter {
            display: inline-block;
            animation: bounce 1s infinite alternate, color-change 2s infinite;
        }
@keyframes bounce {
            0% {
                transform: translateY(0);
            }

            100% {
                transform: translateY(-10px);
            }
        }
@keyframes color-change {
            0% {
                color: red;
            }

            25% {
                color: blue;
            }

            50% {
                color: green;
            }

            75% {
                color: orange;
            }

            100% {
                color: purple;
            }
        }
</style>
</head>
<body>

