<!DOCTYPE html>
<html>
<head>
    <title>Kyle J Shanks - Jr Front-End Developer</title>
    <link href='https://fonts.googleapis.com/css?family=Open+Sans:300,400,600' rel='stylesheet' type='text/css'>
    <link href='https://fonts.googleapis.com/css?family=Raleway:100' rel='stylesheet' type='text/css'>
    <link href='https://fonts.googleapis.com/css?family=Montserrat' rel='stylesheet' type='text/css'>
    <style>
        /* MIXINS */
        /*Dummy Variable*/
        $x = false;
        /* The top, left, right, and bottom are optional */
        @mixin setup($display, $position, $margin, $top: null, $right: null, $bottom: null, $left: null) {
            display: $display;
            position: $position;
            margin: $margin;
            top: $top;
            right: $right;
            bottom: $bottom;
            left: $left;
        }
        
        @mixin font($font-family, $font-size, $letter-spacing, $font-weight, $line-height: 1) {
            font-family: $font-family;
            font-size: $font-size;
            letter-spacing: $letter-spacing;
            font-weight: $font-weight;
            line-height: $line-height;
        }
        
        /* GENERAL FONTS AND CLASSES AND SETUP STUFF */
        * {
            box-sizing: border-box;
            transition: 0.35s ease;
        }
        
        .rela-block {
            @include setup(block, relative, auto);
        }
        
        .rela-inline {
            @include setup(inline-block, relative, auto);
        }
        
        .floated {
            @include setup(inline-block, relative, $x);
            float: left;
        }
        
        .abs-center {
            @include setup($x, absolute, $x, 50%, $x, $x, 50%);
            transform: translate(-50%, -50%);
            text-align: center;
            width: 88%;
        }
        
        /* --- COLORS --- */
        
        /* --- PAGE STYLINGS --- */
        body {
            @include font('Open Sans', 18px, 0px, 400, 28px);
            background: url('http://kingofwallpapers.com/leaves/leaves-016.jpg') right no-repeat;
            background-size: cover;
        }
        
        body:before {
            content: "";
            @include setup($x, fixed, 0, 0, 0, 0, 0);
            background-color: rgba(255, 255, 255, 0.92);
        }
        
        .caps {
            text-transform: uppercase;
        }
        
        .justified {
            text-align: justify;
        }
        
        p.light {
            color: #777;
        }
        
        h2 {
            @include font('Open Sans', 30px, 5px, 600, 40px);
            color: black;
        }
        
        h3 {
            @include font('Open Sans', 21px, 1px, 600, 28px);
            color: black;
        }
        
        /* ... (rest of the CSS) ... */
    </style>
</head>
<body>
    <div class="rela-block page">
        <div class="rela-block top-bar">
            <div class="caps name"><div class="abs-center">Kyle J Shanks</div></div>
        </div>
        <div class="side-bar">
            <!-- ... (rest of the HTML content) ... -->
        </div>
        <div class="rela-block content-container">
            <!-- ... (rest of the HTML content) ... -->
        </div>
    </div>
</body>
</html>
