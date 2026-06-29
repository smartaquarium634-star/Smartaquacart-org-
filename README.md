<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>SMART AQUA CART | Premium Quality Live Fishes & Accessories</title>
    <meta name="description" content="Premium Quality Live Fishes & Aquarium Accessories in Karad, Maharashtra.">
    
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;600;700&family=Poppins:wght@300;400;500;600&display=swap" rel="stylesheet">
    
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">

    <style>
        /* --- CSS VARIABLES & THEME --- */
        :root {
            --pine-green: #01796F;
            --pine-green-dark: #015c54;
            --soft-lavender: #E6E6FA;
            --linen-white: #FAF9F6;
            --text-dark: #1A1A1A;
            --text-light: #666666;
            --glass-bg: rgba(250, 249, 246, 0.85);
            --glass-border: rgba(255, 255, 255, 0.4);
            --shadow: 0 8px 32px rgba(0, 0, 0, 0.1);
            --radius: 16px;
            --transition: all 0.3s cubic-bezier(0.25, 0.8, 0.25, 1);
        }

        [data-theme="dark"] {
            --pine-green: #029a8e;
            --pine-green-dark: #01796F;
            --soft-lavender: #2a2a35;
            --linen-white: #121212;
            --text-dark: #FAF9F6;
            --text-light: #aaaaaa;
            --glass-bg: rgba(18, 18, 18, 0.85);
            --glass-border: rgba(255, 255, 255, 0.1);
            --shadow: 0 8px 32px rgba(0, 0, 0, 0.5);
        }

        /* --- RESET & TYPOGRAPHY --- */
        * { margin: 0; padding: 0; box-sizing: border-box; }
        html { scroll-behavior: smooth; font-size: 16px; }
        body {
            font-family: 'Poppins', sans-serif;
            background-color: var(--linen-white);
            color: var(--text-dark);
            overflow-x: hidden;
            transition: background-color 0.3s, color 0.3s;
        }
        h1, h2, h3, h4, .brand-font { font-family: 'Playfair Display', serif; }
        a { text-decoration: none; color: inherit; }
        button { cursor: pointer; border: none; outline: none; font-family: inherit; }
        ul { list-style: none; }
        img { max-width: 100%; height: auto; display: block; }

        /* --- UTILITIES --- */
        .container { max-width: 1200px; margin: 0 auto; padding: 0 20px; }
        .glass { background: var(--glass-bg); backdrop-filter: blur(12px); -webkit-backdrop-filter: blur(12px); border: 1px solid var(--glass-border); }
        .btn { padding: 12px 24px; border-radius: 30px; font-weight: 500; transition: var(--transition); display: inline-flex; align-items: center; gap: 8px; justify-content: center; }
        .btn-primary { background: var(--pine-green); color: white; }
        .btn-primary:hover { background: var(--pine-green-dark); transform: translateY(-2px); box-shadow: 0 4px 15px rgba(1, 121, 111, 0.3); }
        .btn-outline { background: transparent; border: 2px solid var(--pine-green); color: var(--pine-green); }
        .btn-outline:hover { background: var(--pine-green); color: white; transform: translateY(-2px); }
        .section-title { text-align: center; margin-bottom: 40px; font-size: 2.5rem; color: var(--pine-green); }

        /* --- LOADER --- */
        #loader { position: fixed; top: 0; left: 0; width: 100%; height: 100%; background: var(--linen-white); z-index: 9999; display: flex; justify-content: center; align-items: center; flex-direction: column; transition: opacity 0.5s; }
        .spinner { width: 50px; height: 50px; border: 5px solid var(--soft-lavender); border-top-color: var(--pine-green); border-radius: 50%; animation: spin 1s linear infinite; }
        @keyframes spin { 100% { transform: rotate(360deg); } }

        /* --- HEADER --- */
        header { position: sticky; top: 0; z-index: 1000; padding: 15px 0; transition: var(--transition); }
        .header-inner { display: flex; justify-content: space-between; align-items: center; padding: 10px 20px; border-radius: 20px; }
        .logo-container { display: flex; align-items: center; gap: 10px; }
        .logo-icon { font-size: 1.8rem; color: var(--pine-green); }
        .shop-name { font-size: 1.5rem; font-weight: 700; line-height: 1.2; }
        .shop-tagline { font-size: 0.7rem; color: var(--text-light); font-family: 'Poppins', sans-serif; display: block; }
        
        .nav-menu { display: flex; gap: 20px; align-items: center; }
        .nav-links { display: flex; gap: 20px; font-weight: 500; }
        .nav-links a:hover { color: var(--pine-green); }
        .header-actions { display: flex; gap: 15px; align-items: center; font-size: 1.2rem; }
        .icon-btn { background: transparent; color: var(--text-dark); position: relative; transition: var(--transition); }
        .icon-btn:hover { color: var(--pine-green); transform: scale(1.1); }
        .badge { position: absolute; top: -8px; right: -8px; background: #e74c3c; color: white; font-size: 0.7rem; width: 18px; height: 18px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-weight: bold; }
        .mobile-menu-btn { display: none; }

        /* --- HERO SECTION --- */
        .hero { position: relative; min-height: 80vh; display: flex; align-items: center; overflow: hidden; background: linear-gradient(135deg, var(--soft-lavender) 0%, var(--linen-white) 100%); }
        .hero-content { position: relative; z-index: 2; max-width: 600px; padding: 20px; }
        .hero h1 { font-size: 4rem; margin-bottom: 20px; color: var(--pine-green); line-height: 1.1; }
        .hero p { font-size: 1.2rem; margin-bottom: 30px; color: var(--text-light); }
        .hero-btns { display: flex; gap: 15px; }
        
        /* Bubble Animation */
        .bubbles { position: absolute; top: 0; left: 0; width: 100%; height: 100%; z-index: 1; pointer-events: none; }
        .bubble { position: absolute; background: rgba(1, 121, 111, 0.1); border-radius: 50%; bottom: -50px; animation: floatUp linear infinite; }
        @keyframes floatUp {
            0% { transform: translateY(0) scale(1); opacity: 0; }
            50% { opacity: 1; }
            100% { transform: translateY(-100vh) scale(1.5); opacity: 0; }
        }

        /* --- FILTERS & SEARCH --- */
        .controls-section { padding: 40px 0 20px; }
        .controls-inner { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 20px; padding: 20px; border-radius: var(--radius); }
        .search-box { position: relative; flex: 1; min-width: 250px; }
        .search-box input { width: 100%; padding: 12px 20px 12px 40px; border-radius: 30px; border: 1px solid var(--glass-border); background: var(--linen-white); color: var(--text-dark); font-family: inherit; }
        .search-box i { position: absolute; left: 15px; top: 50%; transform: translateY(-50%); color: var(--text-light); }
        .filter-group { display: flex; gap: 15px; flex-wrap: wrap; }
        select { padding: 12px 20px; border-radius: 30px; border: 1px solid var(--glass-border); background: var(--linen-white); color: var(--text-dark); font-family: inherit; outline: none; cursor: pointer; }

        /* --- PRODUCT GRID --- */
        .products-section { padding: 40px 0; }
        .product-grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(250px, 1fr)); gap: 30px; }
        .product-card { background: var(--glass-bg); border-radius: var(--radius); padding: 15px; transition: var(--transition); position: relative; border: 1px solid var(--glass-border); box-shadow: var(--shadow); display: flex; flex-direction: column; }
        .product-card:hover { transform: translateY(-10px); box-shadow: 0 15px 40px rgba(0,0,0,0.15); }
        .product-img-wrap { position: relative; border-radius: 12px; overflow: hidden; height: 250px; margin-bottom: 15px; background: #fff; display: flex; align-items: center; justify-content: center;}
        .product-img-wrap img { width: 100%; height: 100%; object-fit: contain; transition: transform 0.5s ease; }
        .product-card:hover .product-img-wrap img { transform: scale(1.1); }
        
        .product-badges { position: absolute; top: 10px; left: 10px; display: flex; flex-direction: column; gap: 5px; z-index: 2; }
        .prod-badge { padding: 4px 8px; border-radius: 4px; font-size: 0.7rem; font-weight: 600; color: white; }
        .badge-sale { background: #e74c3c; }
        .badge-new { background: var(--pine-green); }
        
        .card-actions-overlay { position: absolute; top: 10px; right: 10px; display: flex; flex-direction: Smartaquacart-org-
