<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="육산갈비 가맹점 모집 - 30년 양념내공의 대형 평수 갈비 전문 브랜드">
    <title>육산갈비 가맹점 모집</title>
    <style>
        /* Reset & Base */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Noto Sans KR', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            color: #333;
            line-height: 1.6;
            overflow-x: hidden;
        }

        /* Color Variables */
        :root {
            --primary-navy: #001D3D;
            --primary-brown: #634632;
            --accent-orange: #F77F00;
            --light-gray: #F8F5F2;
            --text-dark: #2C2C2C;
        }

        /* Header with Enhanced Transition */
        header {
            position: fixed;
            top: 0;
            left: 0;
            right: 0;
            background: rgba(255, 255, 255, 0.95);
            backdrop-filter: blur(10px);
            box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
            z-index: 1000;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            transform: translateY(0);
        }

        header.scrolled {
            padding: 5px 0;
            box-shadow: 0 4px 20px rgba(0, 0, 0, 0.15);
        }

        header.hide {
            transform: translateY(-100%);
        }

        .header-container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px 40px;
            display: flex;
            justify-content: space-between;
            align-items: center;
            transition: padding 0.3s ease;
        }

        .logo {
            font-size: 28px;
            font-weight: 700;
            color: var(--primary-navy);
            text-decoration: none;
            position: relative;
            transition: all 0.3s ease;
        }

        .logo::after {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 0;
            width: 0;
            height: 3px;
            background: var(--accent-orange);
            transition: width 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .logo:hover::after {
            width: 100%;
        }

        .logo:hover {
            transform: scale(1.05);
        }

        nav ul {
            display: flex;
            list-style: none;
            gap: 40px;
        }

        nav a {
            text-decoration: none;
            color: var(--text-dark);
            font-weight: 500;
            position: relative;
            font-size: 15px;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        nav a::before {
            content: '';
            position: absolute;
            bottom: -5px;
            left: 50%;
            transform: translateX(-50%) scaleX(0);
            width: 100%;
            height: 2px;
            background: var(--accent-orange);
            transition: transform 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }

        nav a:hover {
            color: var(--accent-orange);
            transform: translateY(-2px);
        }

        nav a:hover::before {
            transform: translateX(-50%) scaleX(1);
        }

        nav a.active {
            color: var(--accent-orange);
        }

        /* Hero Section with Enhanced Animation */
        .hero {
            height: 100vh;
            background: linear-gradient(135deg, var(--primary-navy) 0%, var(--primary-brown) 100%);
            display: flex;
            align-items: center;
            justify-content: center;
            text-align: center;
            color: white;
            position: relative;
            overflow: hidden;
        }

        .hero::before {
            content: '';
            position: absolute;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(247, 127, 0, 0.15) 0%, transparent 70%);
            animation: rotate 20s linear infinite;
        }

        @keyframes rotate {
            from { transform: rotate(0deg); }
            to { transform: rotate(360deg); }
        }

        /* Floating Animation */
        @keyframes float {
            0%, 100% { transform: translateY(0px); }
            50% { transform: translateY(-20px); }
        }

        .hero-content {
            position: relative;
            z-index: 1;
            max-width: 900px;
            padding: 0 20px;
            animation: fadeInUp 1s ease-out;
        }

        @keyframes fadeInUp {
            from {
                opacity: 0;
                transform: translateY(30px);
            }
            to {
                opacity: 1;
                transform: translateY(0);
            }
        }

        .hero h1 {
            font-size: 60px;
            font-weight: 800;
            margin-bottom: 20px;
            line-height: 1.2;
            text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
            animation: fadeInUp 1s ease-out 0.2s both;
        }

        .hero-subtitle {
            font-size: 24px;
            margin-bottom: 30px;
            opacity: 0.95;
            animation: fadeInUp 1s ease-out 0.4s both;
        }

        .hero-desc {
            font-size: 18px;
            margin-bottom: 50px;
            opacity: 0.9;
            line-height: 1.8;
            animation: fadeInUp 1s ease-out 0.6s both;
        }

        .cta-button {
            display: inline-block;
            padding: 18px 50px;
            background: var(--accent-orange);
            color: white;
            text-decoration: none;
            border-radius: 50px;
            font-weight: 700;
            font-size: 18px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            box-shadow: 0 4px 15px rgba(247, 127, 0, 0.4);
            position: relative;
            overflow: hidden;
            animation: fadeInUp 1s ease-out 0.8s both, pulse 2s ease-in-out 2s infinite;
        }

        @keyframes pulse {
            0%, 100% { transform: scale(1); }
            50% { transform: scale(1.05); }
        }

        .cta-button::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(255, 255, 255, 0.2);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            transition: width 0.6s ease, height 0.6s ease;
        }

        .cta-button:hover::before {
            width: 300px;
            height: 300px;
        }

        .cta-button:hover {
            transform: translateY(-5px) scale(1.05);
            box-shadow: 0 8px 30px rgba(247, 127, 0, 0.6);
        }

        .cta-button:active {
            transform: translateY(-2px) scale(1.02);
        }

        /* Section Common Styles */
        section {
            padding: 100px 40px;
            position: relative;
        }

        .section-title {
            text-align: center;
            font-size: 42px;
            font-weight: 700;
            color: var(--primary-navy);
            margin-bottom: 20px;
            position: relative;
            display: inline-block;
            left: 50%;
            transform: translateX(-50%);
        }

        .section-title::after {
            content: '';
            position: absolute;
            bottom: -10px;
            left: 50%;
            transform: translateX(-50%);
            width: 60px;
            height: 4px;
            background: var(--accent-orange);
            border-radius: 2px;
        }

        .section-subtitle {
            text-align: center;
            font-size: 18px;
            color: #666;
            margin-bottom: 60px;
            max-width: 700px;
            margin-left: auto;
            margin-right: auto;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
        }

        /* Story Section with Enhanced Cards */
        #story {
            background: var(--light-gray);
        }

        .story-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 40px;
            margin-top: 60px;
        }

        .story-card {
            background: white;
            padding: 40px;
            border-radius: 15px;
            box-shadow: 0 5px 20px rgba(0, 0, 0, 0.08);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .story-card::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 4px;
            background: linear-gradient(90deg, var(--accent-orange), var(--primary-brown));
            transform: scaleX(0);
            transform-origin: left;
            transition: transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .story-card:hover::before {
            transform: scaleX(1);
        }

        .story-card:hover {
            transform: translateY(-15px) scale(1.02);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
        }

        .story-card h3 {
            font-size: 24px;
            color: var(--primary-navy);
            margin-bottom: 20px;
            font-weight: 700;
            transition: color 0.3s ease;
        }

        .story-card:hover h3 {
            color: var(--accent-orange);
        }

        .story-card p {
            color: #555;
            line-height: 1.8;
            transition: color 0.3s ease;
        }

        .story-card:hover p {
            color: var(--text-dark);
        }

        /* Strengths Section */
        #strengths {
            background: white;
        }

        .strengths-list {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
            gap: 30px;
            margin-top: 60px;
        }

        .strength-item {
            background: linear-gradient(135deg, var(--primary-navy) 0%, var(--primary-brown) 100%);
            padding: 40px 30px;
            border-radius: 15px;
            color: white;
            text-align: center;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
            cursor: pointer;
        }

        .strength-item::before {
            content: '';
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 5px;
            background: var(--accent-orange);
        }

        .strength-item::after {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(255, 255, 255, 0.1);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            transition: width 0.6s ease, height 0.6s ease;
        }

        .strength-item:hover::after {
            width: 500px;
            height: 500px;
        }

        .strength-item:hover {
            transform: scale(1.08) rotate(1deg);
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.3);
        }

        .strength-number {
            font-size: 48px;
            font-weight: 800;
            color: var(--accent-orange);
            margin-bottom: 15px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .strength-item:hover .strength-number {
            transform: scale(1.2) rotate(5deg);
        }

        .strength-item h3 {
            font-size: 20px;
            margin-bottom: 15px;
            font-weight: 700;
            position: relative;
            z-index: 1;
        }

        .strength-item p {
            font-size: 15px;
            line-height: 1.6;
            opacity: 0.9;
            position: relative;
            z-index: 1;
        }

        /* Menu Section */
        #menu {
            background: var(--light-gray);
        }

        .menu-text {
            text-align: center;
            font-size: 18px;
            color: #555;
            line-height: 2;
            max-width: 800px;
            margin: 0 auto;
        }

        .menu-highlight {
            background: white;
            padding: 60px 40px;
            border-radius: 20px;
            margin-top: 50px;
            box-shadow: 0 5px 25px rgba(0, 0, 0, 0.08);
            transition: all 0.4s ease;
        }

        .menu-highlight:hover {
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.12);
            transform: translateY(-5px);
        }

        .menu-items {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 40px;
        }

        .menu-item {
            text-align: center;
            padding: 30px;
            background: var(--light-gray);
            border-radius: 15px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            cursor: pointer;
            position: relative;
            overflow: hidden;
        }

        .menu-item::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: var(--primary-navy);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            transition: width 0.6s ease, height 0.6s ease;
        }

        .menu-item:hover::before {
            width: 500px;
            height: 500px;
        }

        .menu-item:hover {
            transform: translateY(-10px) scale(1.05);
        }

        .menu-item h4 {
            font-size: 20px;
            margin-bottom: 10px;
            color: var(--primary-navy);
            position: relative;
            z-index: 1;
            transition: color 0.3s ease;
        }

        .menu-item p {
            position: relative;
            z-index: 1;
            transition: color 0.3s ease;
        }

        .menu-item:hover h4,
        .menu-item:hover p {
            color: white;
        }

        /* Points Section */
        #points {
            background: white;
        }

        .points-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(350px, 1fr));
            gap: 40px;
            margin-top: 60px;
        }

        .point-card {
            background: var(--light-gray);
            padding: 40px;
            border-radius: 15px;
            border-left: 5px solid var(--accent-orange);
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
        }

        .point-card::after {
            content: '';
            position: absolute;
            left: 0;
            top: 0;
            width: 5px;
            height: 0;
            background: var(--primary-navy);
            transition: height 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .point-card:hover::after {
            height: 100%;
        }

        .point-card:hover {
            box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
            transform: translateX(15px);
            background: white;
        }

        .point-label {
            display: inline-block;
            background: var(--accent-orange);
            color: white;
            padding: 5px 15px;
            border-radius: 20px;
            font-size: 14px;
            font-weight: 700;
            margin-bottom: 15px;
            transition: all 0.3s ease;
        }

        .point-card:hover .point-label {
            transform: scale(1.1);
            box-shadow: 0 5px 15px rgba(247, 127, 0, 0.4);
        }

        .point-card h3 {
            font-size: 22px;
            color: var(--primary-navy);
            margin-bottom: 20px;
            font-weight: 700;
        }

        .point-card ul {
            list-style: none;
            padding-left: 0;
        }

        .point-card li {
            padding: 8px 0;
            padding-left: 25px;
            position: relative;
            color: #555;
            line-height: 1.6;
            transition: all 0.3s ease;
        }

        .point-card li::before {
            content: '✓';
            position: absolute;
            left: 0;
            color: var(--accent-orange);
            font-weight: 700;
            transition: all 0.3s ease;
        }

        .point-card:hover li {
            padding-left: 30px;
        }

        .point-card:hover li::before {
            transform: scale(1.3);
        }

        /* Guide Section */
        #guide {
            background: var(--light-gray);
        }

        .guide-content {
            background: white;
            padding: 60px;
            border-radius: 20px;
            box-shadow: 0 5px 25px rgba(0, 0, 0, 0.08);
            transition: all 0.4s ease;
        }

        .guide-content:hover {
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.12);
        }

        .guide-info {
            font-size: 18px;
            line-height: 2;
            color: #555;
            margin-bottom: 40px;
        }

        .guide-box {
            background: var(--primary-navy);
            color: white;
            padding: 40px;
            border-radius: 15px;
            margin-top: 30px;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .guide-box:hover {
            transform: scale(1.02);
            box-shadow: 0 10px 30px rgba(0, 29, 61, 0.3);
        }

        .guide-box h3 {
            font-size: 24px;
            margin-bottom: 20px;
            color: var(--accent-orange);
        }

        .guide-box p {
            font-size: 16px;
            line-height: 1.8;
        }

        /* Contact Section */
        #contact {
            background: linear-gradient(135deg, var(--primary-navy) 0%, var(--primary-brown) 100%);
            color: white;
            position: relative;
            overflow: hidden;
        }

        #contact::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(247, 127, 0, 0.1) 0%, transparent 70%);
            animation: rotate 30s linear infinite;
        }

        #contact .section-title,
        #contact .section-subtitle {
            color: white;
            position: relative;
            z-index: 1;
        }

        .contact-form {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            padding: 50px;
            border-radius: 20px;
            box-shadow: 0 10px 40px rgba(0, 0, 0, 0.3);
            position: relative;
            z-index: 1;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .contact-form:hover {
            box-shadow: 0 15px 60px rgba(0, 0, 0, 0.4);
            transform: translateY(-5px);
        }

        .form-group {
            margin-bottom: 25px;
        }

        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: var(--primary-navy);
            font-weight: 600;
            font-size: 15px;
            transition: all 0.3s ease;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 15px;
            border: 2px solid #e0e0e0;
            border-radius: 10px;
            font-size: 15px;
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
            font-family: inherit;
        }

        .form-group input:focus,
        .form-group textarea:focus {
            outline: none;
            border-color: var(--accent-orange);
            box-shadow: 0 0 0 4px rgba(247, 127, 0, 0.1);
            transform: translateY(-2px);
        }

        .form-group input:focus + label,
        .form-group textarea:focus + label {
            color: var(--accent-orange);
        }

        .form-group textarea {
            resize: vertical;
            min-height: 120px;
        }

        .submit-button {
            width: 100%;
            padding: 18px;
            background: var(--accent-orange);
            color: white;
            border: none;
            border-radius: 50px;
            font-size: 18px;
            font-weight: 700;
            cursor: pointer;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            position: relative;
            overflow: hidden;
        }

        .submit-button::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 0;
            height: 0;
            background: rgba(255, 255, 255, 0.3);
            border-radius: 50%;
            transform: translate(-50%, -50%);
            transition: width 0.6s ease, height 0.6s ease;
        }

        .submit-button:hover::before {
            width: 500px;
            height: 500px;
        }

        .submit-button:hover {
            background: #e67300;
            transform: translateY(-3px);
            box-shadow: 0 8px 25px rgba(247, 127, 0, 0.5);
        }

        .submit-button:active {
            transform: translateY(0);
        }

        /* Floating Phone Button */
        .floating-phone {
            position: fixed;
            bottom: 30px;
            right: 30px;
            background: var(--accent-orange);
            color: white;
            padding: 20px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: 700;
            font-size: 18px;
            box-shadow: 0 5px 25px rgba(247, 127, 0, 0.5);
            z-index: 999;
            transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
            display: flex;
            align-items: center;
            gap: 10px;
            animation: float 3s ease-in-out infinite;
        }

        .floating-phone::before {
            content: '';
            position: absolute;
            top: 50%;
            left: 50%;
            width: 100%;
            height: 100%;
            background: var(--accent-orange);
            border-radius: 50px;
            transform: translate(-50%, -50%) scale(1);
            opacity: 0;
            animation: pulse-ring 2s cubic-bezier(0.4, 0, 0.2, 1) infinite;
        }

        @keyframes pulse-ring {
            0% {
                transform: translate(-50%, -50%) scale(1);
                opacity: 0.5;
            }
            100% {
                transform: translate(-50%, -50%) scale(1.3);
                opacity: 0;
            }
        }

        .floating-phone:hover {
            transform: translateY(-8px) scale(1.05);
            box-shadow: 0 10px 40px rgba(247, 127, 0, 0.7);
        }

        .phone-icon {
            font-size: 24px;
            animation: ring 2s ease-in-out infinite;
        }

        @keyframes ring {
            0%, 100% { transform: rotate(0deg); }
            10%, 30% { transform: rotate(-10deg); }
            20% { transform: rotate(10deg); }
        }

        /* Footer */
        footer {
            background: var(--primary-navy);
            color: white;
            padding: 40px;
            text-align: center;
        }

        footer p {
            margin: 5px 0;
            opacity: 0.8;
        }

        /* Responsive */
        @media (max-width: 768px) {
            .header-container {
                padding: 15px 20px;
            }

            nav ul {
                display: none;
            }

            .hero h1 {
                font-size: 36px;
            }

            .hero-subtitle {
                font-size: 18px;
            }

            .section-title {
                font-size: 32px;
            }

            section {
                padding: 60px 20px;
            }

            .story-grid,
            .strengths-list,
            .points-grid,
            .menu-items {
                grid-template-columns: 1fr;
            }

            .contact-form {
                padding: 30px 20px;
            }

            .floating-phone {
                bottom: 20px;
                right: 20px;
                padding: 15px 20px;
                font-size: 16px;
            }

            .guide-content {
                padding: 30px 20px;
            }
        }

        /* Scroll Animation */
        .fade-in {
            opacity: 0;
            transform: translateY(30px);
            transition: opacity 0.6s cubic-bezier(0.4, 0, 0.2, 1), transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .fade-in.visible {
            opacity: 1;
            transform: translateY(0);
        }

        .fade-in-left {
            opacity: 0;
            transform: translateX(-50px);
            transition: opacity 0.6s cubic-bezier(0.4, 0, 0.2, 1), transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .fade-in-left.visible {
            opacity: 1;
            transform: translateX(0);
        }

        .fade-in-right {
            opacity: 0;
            transform: translateX(50px);
            transition: opacity 0.6s cubic-bezier(0.4, 0, 0.2, 1), transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .fade-in-right.visible {
            opacity: 1;
            transform: translateX(0);
        }

        .scale-in {
            opacity: 0;
            transform: scale(0.8);
            transition: opacity 0.6s cubic-bezier(0.4, 0, 0.2, 1), transform 0.6s cubic-bezier(0.4, 0, 0.2, 1);
        }

        .scale-in.visible {
            opacity: 1;
            transform: scale(1);
        }

        /* Loading Animation */
        @keyframes shimmer {
            0% {
                background-position: -1000px 0;
            }
            100% {
                background-position: 1000px 0;
            }
        }

        /* Parallax Effect */
        .parallax {
            transform: translateY(0);
            transition: transform 0.5s cubic-bezier(0.4, 0, 0.2, 1);
        }
    </style>
</head>
<body>
    <!-- Header -->
    <header id="header">
        <div class="header-container">
            <a href="#" class="logo">육산</a>
            <nav>
                <ul>
                    <li><a href="#story" class="nav-link">육산 스토리</a></li>
                    <li><a href="#menu" class="nav-link">육산 메뉴</a></li>
                    <li><a href="#points" class="nav-link">창업포인트</a></li>
                    <li><a href="#guide" class="nav-link">창업안내</a></li>
                    <li><a href="#contact" class="nav-link">가맹문의</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <!-- Hero Section -->
    <section class="hero">
        <div class="hero-content">
            <h1>산(山)처럼 우직한<br>고기(肉) 철학 육산</h1>
            <p class="hero-subtitle">30년 양념내공으로 완성한 대형 평수 갈비 전문 브랜드</p>
            <p class="hero-desc">유행을 따르지 않고, 결과로 증명해왔습니다.<br>무한리필은 흉내낼 수 없는 30년 내공의 깊은 맛</p>
            <a href="#contact" class="cta-button">가맹 문의하기</a>
        </div>
    </section>

    <!-- Story Section -->
    <section id="story">
        <div class="container">
            <h2 class="section-title">육산 스토리 & 브랜드 경쟁력</h2>
            <p class="section-subtitle">흔한 생고기 운영이 아닌, 30년 노하우로 완성된 독보적 양념육 시스템</p>
            
            <div class="story-grid fade-in">
                <div class="story-card">
                    <h3>🏔️ 산처럼 우직한 철학</h3>
                    <p>육산갈비는 유행을 타지 않는 진짜 양념갈비로 30년간 묵묵히 그 자리를 지켜왔습니다. 빠른 트렌드보다 변하지 않는 본질에 집중합니다.</p>
                </div>
                <div class="story-card">
                    <h3>🔥 30년 양념 내공</h3>
                    <p>무한리필로는 절대 따라올 수 없는 깊은 맛의 비밀. 3대째 이어온 양념 레시피로 가족외식과 회식을 동시에 만족시킵니다.</p>
                </div>
                <div class="story-card">
                    <h3>💪 검증된 시스템</h3>
                    <p>8년간 월매출 2~3억, 200평 매장까지 운영 가능한 검증된 동선, 주방, 운영시스템. 입지보다 중요한 것은 시스템입니다.</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Strengths Section -->
    <section id="strengths">
        <div class="container">
            <h2 class="section-title">육산만의 핵심 강점</h2>
            <p class="section-subtitle">맛과 시스템으로 증명하는 흔들림 없는 수익력</p>
            
            <div class="strengths-list fade-in">
                <div class="strength-item">
                    <div class="strength-number">01</div>
                    <h3>8년 연속 월 2~3억 매출</h3>
                    <p>세종시 220평 매장, 40개 테이블의 효율을 극대화한 운영 노하우. 8년간 쌓아온 데이터로 검증된 안정적인 가족 외식형 비즈니스</p>
                </div>
                <div class="strength-item">
                    <div class="strength-number">02</div>
                    <h3>빈틈 없는 메뉴 라인업</h3>
                    <p>저녁: 고퀄리티 양념육과 자가제면 수제 냉면<br>점심: 소불고기 전골, 궁중소갈비찜<br>하루 종일 손님이 끊이지 않는 강력한 메뉴 구성</p>
                </div>
                <div class="strength-item">
                    <div class="strength-number">03</div>
                    <h3>실속 중심 입지 전략</h3>
                    <p>비싼 메인 상권 대신 맛으로 고객을 끌어들이는 '목적지형 맛집' 전략. 50평 이상 대형 평수 최적화로 고수익 실현</p>
                </div>
            </div>
        </div>
    </section>

    <!-- Menu Section -->
    <section id="menu">
        <div class="container">
            <h2 class="section-title">육산의 메뉴</h2>
            <p class="section-subtitle">품격 있는 양념육부터 궁중 소갈비찜까지, 점심과 저녁을 모두 잡는 맛</p>
            
            <div class="menu-highlight fade-in scale-in">
                <h3 style="text-align: center; color: var(--primary-navy); font-size: 28px; margin-bottom: 30px;">풀타임 매출 구조</h3>
                <p class="menu-text">
                    <strong>낮에는</strong> 갈비찜으로 식사 수요를<br>
                    <strong>저녁엔</strong> 양념갈비로 회식 수요를<br>
                    빈틈없는 메뉴로 실현하는 <span style="color: var(--accent-orange); font-weight: 700;">풀타임 매출 구조</span>
                </p>
                
                <div class="menu-items">
                    <div class="menu-item">
                        <h4>양념 갈비</h4>
                        <p>30년 비법 양념</p>
                    </div>
                    <div class="menu-item">
                        <h4>궁중 소갈비찜</h4>
                        <p>점심 특선 메뉴</p>
                    </div>
                    <div class="menu-item">
                        <h4>소불고기 전골</h4>
                        <p>객단가 업</p>
                    </div>
                    <div class="menu-item">
                        <h4>자가제면 냉면</h4>
                        <p>수제 냉면</p>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- Points Section -->
    <section id="points">
        <div class="container">
            <h2 class="section-title">창업 포인트</h2>
            <p class="section-subtitle">육산갈비가 제시하는 성공적인 창업의 핵심 요소</p>
            
            <div class="points-grid fade-in">
                <div class="point-card fade-in-left">
                    <span class="point-label">POINT 1</span>
                    <h3>8년 연속 월 2~3억 매출, 대형 매장이 증명한 흔들림 없는 수익력</h3>
                    <ul>
                        <li>세종시 220평 매장, 40개 테이블의 효율을 극대화한 운영 노하우</li>
                        <li>8년간 쌓아온 데이터로 검증된 안정적인 가족 외식형 비즈니스</li>
                        <li>유행에 민감한 아이템이 아닌, 지역 1등 맛집으로 자리 잡는 생존력</li>
                    </ul>
                </div>
                
                <div class="point-card fade-in">
                    <span class="point-label">POINT 2</span>
                    <h3>빈틈 없는 메뉴 라인업, 품격 있는 양념육부터 궁중 소갈비찜까지</h3>
                    <ul>
                        <li>저녁: 무한리필은 따라올 수 없는 고퀄리티 양념육과 자가제면 수제 냉면</li>
                        <li>점심: 소불고기 전골, 궁중소갈비찜 등 객단가와 만족도를 모두 높인 특선메뉴</li>
                        <li>상권에 구애받지 않고 하루 종일 손님이 끊이지 않는 강력한 메뉴 구성</li>
                    </ul>
                </div>
                
                <div class="point-card fade-in-right">
                    <span class="point-label">POINT 3</span>
                    <h3>실속 중심의 입지 전략: 임대료 부담은 낮추고 수익은 높이는 대형 가든 모델</h3>
                    <ul>
                        <li>비싼 메인 상권 대신, 맛으로 고객을 끌어들이는 '목적지형 맛집' 전략</li>
                        <li>50평 이상 대형 평수에 최적화된 동선과 가족 단위 단체 손님 수용 시스템</li>
                        <li>절감된 임대료를 원재료와 서비스에 투자하여 선순환 구조의 고수익 실현</li>
                    </ul>
                </div>
            </div>
        </div>
    </section>

    <!-- Guide Section -->
    <section id="guide">
        <div class="container">
            <h2 class="section-title">창업 안내</h2>
            <p class="section-subtitle">육산갈비와 함께하는 성공 창업 프로세스</p>
            
            <div class="guide-content fade-in">
                <div class="guide-info">
                    육산갈비는 <strong style="color: var(--accent-orange);">50평 이상 대형 평수</strong>에 최적화된 시스템을 제공합니다.<br>
                    맛과 시스템으로 증명된 <strong style="color: var(--primary-navy);">목적지형 맛집</strong> 모델로,<br>
                    비싼 핵심 상권이 아니어도 안정적인 수익을 실현할 수 있습니다.
                </div>
                
                <div class="guide-box">
                    <h3>⭐ 육산갈비 창업 특징</h3>
                    <p>
                        • 검증된 8년 운영 데이터 제공<br>
                        • 30년 전통 양념 레시피 전수<br>
                        • 대형 매장 운영 노하우 공유<br>
                        • 점심·저녁 풀타임 매출 구조<br>
                        • 가족 외식 + 회식 집객 시스템<br>
                        • 지속적인 운영 지원 및 컨설팅
                    </p>
                </div>
                
                <div class="guide-box" style="background: var(--primary-brown); margin-top: 20px;">
                    <h3>📞 창업 상담 문의</h3>
                    <p>
                        자세한 창업 정보와 상담은 아래 문의 폼을 통해<br>
                        신청하시거나 전화로 직접 문의해주시기 바랍니다.<br><br>
                        <strong style="font-size: 24px; color: var(--accent-orange);">010-6601-2927</strong>
                    </p>
                </div>
            </div>
        </div>
    </section>

    <!-- Contact Section -->
    <section id="contact">
        <div class="container">
            <h2 class="section-title">가맹 문의</h2>
            <p class="section-subtitle">육산갈비와 함께 성공 창업을 시작하세요</p>
            
            <form class="contact-form fade-in scale-in" onsubmit="return handleSubmit(event)">
                <div class="form-group">
                    <label for="name">이름 *</label>
                    <input type="text" id="name" name="name" required placeholder="이름을 입력해주세요">
                </div>
                
                <div class="form-group">
                    <label for="phone">연락처 *</label>
                    <input type="tel" id="phone" name="phone" required placeholder="010-0000-0000">
                </div>
                
                <div class="form-group">
                    <label for="email">이메일 *</label>
                    <input type="email" id="email" name="email" required placeholder="example@email.com">
                </div>
                
                <div class="form-group">
                    <label for="message">문의내용</label>
                    <textarea id="message" name="message" placeholder="문의하실 내용을 자유롭게 작성해주세요"></textarea>
                </div>
                
                <button type="submit" class="submit-button">문의하기</button>
            </form>
        </div>
    </section>

    <!-- Footer -->
    <footer>
        <p><strong>육산갈비</strong></p>
        <p>대표번호: 010-6601-2927 | 이메일: ys-food@naver.com</p>
        <p>© 2024 Yuksan Galbi. All Rights Reserved.</p>
    </footer>

    <!-- Floating Phone Button -->
    <a href="tel:010-6601-2927" class="floating-phone">
        <span class="phone-icon">📞</span>
        <span>010-6601-2927</span>
    </a>

    <script>
        // ========================================
        // Smooth Scrolling
        // ========================================
        document.querySelectorAll('a[href^="#"]').forEach(anchor => {
            anchor.addEventListener('click', function (e) {
                e.preventDefault();
                const target = document.querySelector(this.getAttribute('href'));
                if (target) {
                    target.scrollIntoView({
                        behavior: 'smooth',
                        block: 'start'
                    });
                }
            });
        });

        // ========================================
        // Scroll Animation with Intersection Observer
        // ========================================
        const observerOptions = {
            threshold: 0.1,
            rootMargin: '0px 0px -50px 0px'
        };

        const observer = new IntersectionObserver((entries) => {
            entries.forEach(entry => {
                if (entry.isIntersecting) {
                    entry.target.classList.add('visible');
                }
            });
        }, observerOptions);

        // Observe all animated elements
        document.querySelectorAll('.fade-in, .fade-in-left, .fade-in-right, .scale-in').forEach(el => {
            observer.observe(el);
        });

        // ========================================
        // Header Scroll Effects
        // ========================================
        let lastScroll = 0;
        const header = document.getElementById('header');
        
        window.addEventListener('scroll', () => {
            const currentScroll = window.pageYOffset;
            
            // Add scrolled class for styling
            if (currentScroll > 100) {
                header.classList.add('scrolled');
            } else {
                header.classList.remove('scrolled');
            }
            
            // Hide header on scroll down, show on scroll up
            if (currentScroll > lastScroll && currentScroll > 500) {
                header.classList.add('hide');
            } else {
                header.classList.remove('hide');
            }
            
            lastScroll = currentScroll;
        });

        // ========================================
        // Active Navigation Link
        // ========================================
        const sections = document.querySelectorAll('section[id]');
        const navLinks = document.querySelectorAll('.nav-link');

        window.addEventListener('scroll', () => {
            let current = '';
            
            sections.forEach(section => {
                const sectionTop = section.offsetTop;
                const sectionHeight = section.clientHeight;
                if (pageYOffset >= (sectionTop - 200)) {
                    current = section.getAttribute('id');
                }
            });

            navLinks.forEach(link => {
                link.classList.remove('active');
                if (link.getAttribute('href') === `#${current}`) {
                    link.classList.add('active');
                }
            });
        });

        // ========================================
        // Parallax Effect
        // ========================================
        window.addEventListener('scroll', () => {
            const scrolled = window.pageYOffset;
            const parallaxElements = document.querySelectorAll('.parallax');
            
            parallaxElements.forEach(el => {
                const speed = el.dataset.speed || 0.5;
                el.style.transform = `translateY(${scrolled * speed}px)`;
            });
        });

        // ========================================
        // Form Submit Handler
        // ========================================
        function handleSubmit(event) {
            event.preventDefault();
            
            const formData = {
                name: document.getElementById('name').value,
                phone: document.getElementById('phone').value,
                email: document.getElementById('email').value,
                message: document.getElementById('message').value
            };
            
            // Add submit animation
            const submitBtn = event.target.querySelector('.submit-button');
            submitBtn.style.transform = 'scale(0.95)';
            submitBtn.textContent = '전송 중...';
            
            // Simulate form submission
            setTimeout(() => {
                submitBtn.style.transform = 'scale(1)';
                submitBtn.textContent = '전송 완료!';
                submitBtn.style.background = '#28a745';
                
                setTimeout(() => {
                    alert('문의가 접수되었습니다. 빠른 시일 내에 연락드리겠습니다.');
                    event.target.reset();
                    submitBtn.textContent = '문의하기';
                    submitBtn.style.background = '';
                }, 1000);
            }, 1500);
            
            return false;
        }

        // ========================================
        // Card Tilt Effect (3D)
        // ========================================
        document.querySelectorAll('.story-card, .strength-item, .point-card').forEach(card => {
            card.addEventListener('mousemove', (e) => {
                const rect = card.getBoundingClientRect();
                const x = e.clientX - rect.left;
                const y = e.clientY - rect.top;
                
                const centerX = rect.width / 2;
                const centerY = rect.height / 2;
                
                const rotateX = (y - centerY) / 10;
                const rotateY = (centerX - x) / 10;
                
                card.style.transform = `perspective(1000px) rotateX(${rotateX}deg) rotateY(${rotateY}deg) scale(1.05)`;
            });
            
            card.addEventListener('mouseleave', () => {
                card.style.transform = '';
            });
        });

        // ========================================
        // Cursor Trail Effect
        // ========================================
        const coords = { x: 0, y: 0 };
        const circles = document.querySelectorAll('.cta-button, .submit-button');

        circles.forEach(function(circle) {
            circle.x = 0;
            circle.y = 0;
        });

        window.addEventListener('mousemove', function(e) {
            coords.x = e.clientX;
            coords.y = e.clientY;
        });

        // ========================================
        // Loading Animation Complete
        // ========================================
        window.addEventListener('load', () => {
            document.body.style.opacity = '0';
            setTimeout(() => {
                document.body.style.transition = 'opacity 0.5s ease';
                document.body.style.opacity = '1';
            }, 100);
        });

        // ========================================
        // Prevent Right Click (Optional)
        // ========================================
        // document.addEventListener('contextmenu', e => e.preventDefault());

        // ========================================
        // Performance: Debounce Scroll
        // ========================================
        function debounce(func, wait = 10, immediate = true) {
            let timeout;
            return function() {
                const context = this, args = arguments;
                const later = function() {
                    timeout = null;
                    if (!immediate) func.apply(context, args);
                };
                const callNow = immediate && !timeout;
                clearTimeout(timeout);
                timeout = setTimeout(later, wait);
                if (callNow) func.apply(context, args);
            };
        }

        // ========================================
        // Easter Egg: Konami Code
        // ========================================
        let konamiCode = [];
        const konamiPattern = ['ArrowUp', 'ArrowUp', 'ArrowDown', 'ArrowDown', 'ArrowLeft', 'ArrowRight', 'ArrowLeft', 'ArrowRight', 'b', 'a'];
        
        window.addEventListener('keydown', (e) => {
            konamiCode.push(e.key);
            konamiCode.splice(-konamiPattern.length - 1, konamiCode.length - konamiPattern.length);
            
            if (konamiCode.join('').includes(konamiPattern.join(''))) {
                document.body.style.animation = 'rainbow 3s linear infinite';
            }
        });

        // ========================================
        // Console Easter Egg
        // ========================================
        console.log('%c육산갈비 가맹점 모집', 'font-size: 24px; font-weight: bold; color: #F77F00;');
        console.log('%c🏔️ 30년 양념내공의 대형 평수 갈비 전문 브랜드', 'font-size: 14px; color: #001D3D;');
        console.log('%c문의: 010-6601-2927', 'font-size: 12px; color: #634632;');
    </script>
</body>
</html>
