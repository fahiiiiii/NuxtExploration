<template>
    <div>
        <NuxtLink to="/">Home</NuxtLink>
        <NuxtLink to="/about">About</NuxtLink>
        <NuxtLink to="/portfolio">Portfolio</NuxtLink>
        <!-- <NuxtLink to="/product">Product</NuxtLink> -->
        <slot />
    </div>
</template>

<script>
    export default {
        
    }
</script>

<style lang="scss" scoped>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

html, body {
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
    background: #F4F6F8;
}

div {
    font-family: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif;
    background: #F4F6F8;
    min-height: 100vh;
    width: 100%;
    margin: 0;
    padding: 0;
    position: relative;
    
    // Clean professional navbar
    &::before {
        content: '';
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        width: 100%;
        height: 70px;
        background: #ffffff;
        border-bottom: 1px solid rgba(44, 62, 80, 0.1);
        z-index: 1000;
        box-shadow: 0 2px 10px rgba(44, 62, 80, 0.08);
    }
    
    padding-top: 70px;
}

// Navigation container - spread across navbar
a {
    position: fixed;
    top: 20px;
    padding: 12px 28px;
    background: transparent;
    border: 1px solid transparent;
    border-radius: 8px;
    color: #2C3E50;
    text-decoration: none;
    font-weight: 600;
    font-size: 15px;
    transition: all 0.2s ease;
    z-index: 1001;
    
    // Spread navigation items across the navbar width
    &:nth-child(1) { 
        left: 8%; 
    }
    &:nth-child(2) { 
        left: 50%; 
        transform: translateX(-50%);
    }
    &:nth-child(3) { 
        right: 8%; 
    }
    
    &:hover {
        background: rgba(52, 152, 219, 0.1);
        color: #1D6FA5;
        border-color: rgba(52, 152, 219, 0.2);
    }
    
    // Professional active state
    &.router-link-active,
    &.router-link-exact-active {
        background: #3498DB;
        color: #ffffff;
        border-color: #3498DB;
        box-shadow: 0 2px 8px rgba(52, 152, 219, 0.3);
    }
}

// Clean content area
div > :last-child {
    width: calc(100% - 80px);
    max-width: 1200px;
    margin: 40px auto;
    padding: 50px 40px;
    background: #ffffff;
    border-radius: 12px;
    box-shadow: 0 4px 20px rgba(44, 62, 80, 0.08);
    color: #2C3E50;
    line-height: 1.7;
    border: 1px solid rgba(44, 62, 80, 0.05);
}

// Professional responsive design
@media (max-width: 1024px) {
    a {
        &:nth-child(1) { left: 5%; }
        &:nth-child(3) { right: 5%; }
    }
    
    div > :last-child {
        width: calc(100% - 60px);
        margin: 30px auto;
        padding: 40px 30px;
    }
}

@media (max-width: 768px) {
    a {
        padding: 10px 24px;
        font-size: 14px;
        
        &:nth-child(1) { left: 3%; }
        &:nth-child(3) { right: 3%; }
    }
    
    div > :last-child {
        width: calc(100% - 40px);
        margin: 25px auto;
        padding: 35px 25px;
        border-radius: 10px;
    }
}

@media (max-width: 600px) {
    div::before {
        height: 120px;
    }
    
    div {
        padding-top: 120px;
    }
    
    a {
        left: 50% !important;
        right: auto !important;
        transform: translateX(-50%);
        width: 100px;
        text-align: center;
        padding: 10px 20px;
        font-size: 13px;
        
        &:nth-child(1) { top: 15px; }
        &:nth-child(2) { top: 50px; }
        &:nth-child(3) { top: 85px; }
    }
    
    div > :last-child {
        width: calc(100% - 20px);
        margin: 20px auto;
        padding: 25px 20px;
        border-radius: 8px;
    }
}

// Global styling
:global(html) {
    margin: 0 !important;
    padding: 0 !important;
    background: #F4F6F8;
}

:global(body) {
    margin: 0 !important;
    padding: 0 !important;
    background: #F4F6F8;
    width: 100%;
    min-height: 100vh;
    color: #2C3E50;
}

// Professional focus states for accessibility
a:focus {
    outline: 2px solid #3498DB;
    outline-offset: 2px;
}

// Typography styling
div > :last-child {
    h1, h2, h3, h4, h5, h6 {
        color: #2C3E50;
        margin-bottom: 16px;
        font-weight: 700;
    }
    
    p {
        margin-bottom: 16px;
        color: #2C3E50;
        font-weight: 400;
    }
}
</style>