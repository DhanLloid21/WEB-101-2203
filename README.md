<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Profile Resume</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background: #f4f4f4;
        text-align: center;
        margin: 0;
        padding: 0;
    }
    h1 {
        background: #333;
        color: #fff;
        padding: 15px;
        margin: 0;
    }
    .nav {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        background: #eee;
        padding: 10px;
    }
    .profile-link {
        background: #ddd;
        margin: 5px;
        padding: 10px 15px;
        border-radius: 8px;
        cursor: pointer;
        transition: background 0.3s;
    }
    .profile-link:hover {
        background: #bbb;
    }
    .active {
        background: #007bff;
        color: white;
    }
    #profileDisplay {
        margin: 20px auto;
        background: white;
        max-width: 600px;
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    #profileDisplay img {
        width: 150px;
        height: 150px;
        border-radius: 50%;
        object-fit: cover;
        margin-bottom: 10px;
        border: 3px solid #007bff;
    }
</style>
</head>
<body>

<h1>📸 Profile Resume</h1>

<div class="nav">
    <div class="profile-link" onclick="showProfile('allen', this)">Allen</div>
    <div class="profile-link" onclick="showProfile('russell', this)">Russell</div>
    <div class="profile-link" onclick="showProfile('jhonrey', this)">Jhon Rey</div>
    <div class="profile-link" onclick="showProfile('robert', this)">Robert</div>
    <div class="profile-link" onclick="showProfile('dhan', this)">Dhan</div>
</div>

<div id="profileDisplay">
    <p>Click a name above to view their profile.</p>
</div>

<script>
const profiles = {
    allen: {
        name: "ALLEN MIGUE",
        bio: "SHY TYPE",
        address: "B-10 ROAD 2 DON JULIO GREGORIO ST. BAGBAG QC",
        phone: "09557489507",
        email: "JOHNALLENMIGUE@GMAIL.COM",
        work: "STUDIO PHOTOGRAPHER",
        hobby: "BASKETBALL, WATCHING, READING, GAMES",
        age: "19",
        sex: "MALE",
        civil: "SINGLE",
        height: "5'4",
        weight: "45KG",
        quote: "LIFE IS SHORT SO ALWAYS BE HAPPY.",
        image: "https://via.placeholder.com/150/007bff/ffffff?text=Allen"
    },
    russell: { 
        name:"RUSSELL LAMSON", 
        bio:"COMING SOON", 
        address:"B9 L6 PH3 ELYSIAN HOMES PHASE 3 BAHAY PARE, MEYCAUAYAN, BULACAN", 
        phone:"09939219637", 
        email:"RUSSELLAMSON9@GMAIL.COM", 
        work:"LALAMOVE RIDER", 
        hobby:"RIDING MOTORCYCLE", 
        age:"19", 
        sex:"MALE", 
        civil:"SINGLE", 
        height:"5'7", 
        weight:"60KG", 
        quote:"KUNG KAYA NILA, PAGAWA MO SAKANILA!",
        image: "https://via.placeholder.com/150/ff7f50/ffffff?text=Russell"
    },
    jhonrey: { 
        name:"JHON REY BERNALES", 
        bio:"SLEEPYY", 
        address:"BLK 2 LOT 13 GARDEN VIEW HEIGHTS BALUYOT PARK BRGY. SAUYO QUEZON CITY", 
        phone:"09917410416", 
        email:"JHONREYBERNALES14@GMAIL.COM", 
        work:"NONE", 
        hobby:"BASKETBALL, WATCHING ANIME, GAMES", 
        age:"19", 
        sex:"MALE", 
        civil:"SINGLE", 
        height:"5'7", 
        weight:"48KG", 
        quote:"YOUR LIFE DOES NOT GET BETTER BY CHANCE, IT GETS BETTER BY CHANGE.",
        image: "https://via.placeholder.com/150/ffa500/ffffff?text=Jhon+Rey"
    },
    robert: { 
        name:"ROBERT CARIÑO", 
        bio:"COMING SOON", 
        address:"BLK 2 148 LOWER JASMIN ST.PAYATAS A QUEZON CITY", 
        phone:"09917409653", 
        email:"robertcarino58@gmail.com", 
        work:"STUDIO PHOTOGRAPHER", 
        hobby:"ONLINE GAMES AND MOVIE", 
        age:"20", 
        sex:"MALE ", 
        civil:"SINGLE", 
        height:"5'7", 
        weight:"50KG", 
        quote:"LIFE IS VERY SHORT,BE HAPPY ALWAYS",
        image: "https://via.placeholder.com/150/28a745/ffffff?text=Robert"
    },
    dhan: { 
        name:"DHAN TAGASLING", 
        bio:"BBS BERNALES ", 
        address:"102 IDANG STREET BRGY SANTA MONICA NOVALICHES QUEZON CITY ", 
        phone:"09816709811 ", 
        email:"TAGASLING.DHANLLOID.BOLIMA@GMAIL.COM ", 
        work:"STUDIO PHOTOGRAPHER ", 
        hobby:"PLAYING MOBILE GAMES,MATULOG", 
        age:"19", 
        sex:"MALE", 
        civil:"SINGLE", 
        height:"5'4", 
        weight:"48KG", 
        quote:"HINDE MAHALAGA ANG MAGWAGI ANG MAHALAGA IKAW AY NAKIBAHAGI",
        image: "https://via.placeholder.com/150/6f42c1/ffffff?text=Dhan"
    }
};

function showProfile(person, element) {
    const p = profiles[person];
    
    document.querySelectorAll(".profile-link").forEach(link => {
        link.classList.remove("active");
    });
    element.classList.add("active");

    document.getElementById("profileDisplay").innerHTML = `
        <img src="${p.image}" alt="${p.name}">
        <h2>${p.name}</h2>
        <p><strong>BIO:</strong> ${p.bio}</p>
        <p><strong>ADDRESS:</strong> ${p.address}</p>
        <p><strong>PHONE:</strong> ${p.phone}</p>
        <p><strong>EMAIL:</strong> ${p.email}</p>
        <p><strong>WORK:</strong> ${p.work}</p>
        <p><strong>HOBBY:</strong> ${p.hobby}</p>

        <br><h3>PERSONAL DETAILS</h3>
        <p><strong>AGE:</strong> ${p.age}</p>
        <p><strong>SEX:</strong> ${p.sex}</p>
        <p><strong>CIVIL STATUS:</strong> ${p.civil}</p>
        <p><strong>HEIGHT:</strong> ${p.height}</p>
        <p><strong>WEIGHT:</strong> ${p.weight}</p>

        <br><p><strong>QUOTE:</strong> ${p.quote}</p>
    `;
}
</script>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Profile Resume</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background: #f4f4f4;
        text-align: center;
        margin: 0;
        padding: 0;
    }
    h1 {
        background: #333;
        color: #fff;
        padding: 15px;
        margin: 0;
    }
    .nav {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        background: #eee;
        padding: 10px;
    }
    .profile-link {
        background: #ddd;
        margin: 5px;
        padding: 10px 15px;
        border-radius: 8px;
        cursor: pointer;
        transition: background 0.3s;
    }
    .profile-link:hover {
        background: #bbb;
    }
    .active {
        background: #007bff;
        color: white;
    }
    #profileDisplay {
        margin: 20px auto;
        background: white;
        max-width: 600px;
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    #profileDisplay img {
        width: 150px;
        height: 150px;
        border-radius: 50%;
        object-fit: cover;
        margin-bottom: 10px;
        border: 3px solid #007bff;
    }
</style>
</head>
<body>

<h1>📸 Profile Resume</h1>

<div class="nav">
    <div class="profile-link" onclick="showProfile('allen', this)">Allen</div>
    <div class="profile-link" onclick="showProfile('russell', this)">Russell</div>
    <div class="profile-link" onclick="showProfile('jhonrey', this)">Jhon Rey</div>
    <div class="profile-link" onclick="showProfile('robert', this)">Robert</div>
    <div class="profile-link" onclick="showProfile('dhan', this)">Dhan</div>
</div>

<div id="profileDisplay">
    <p>Click a name above to view their profile.</p>
</div>

<script>
const profiles = {
    allen: {
        name: "ALLEN MIGUE",
        bio: "SHY TYPE",
        address: "B-10 ROAD 2 DON JULIO GREGORIO ST. BAGBAG QC",
        phone: "09557489507",
        email: "JOHNALLENMIGUE@GMAIL.COM",
        work: "STUDIO PHOTOGRAPHER",
        hobby: "BASKETBALL, WATCHING, READING, GAMES",
        age: "19",
        sex: "MALE",
        civil: "SINGLE",
        height: "5'4",
        weight: "45KG",
        quote: "LIFE IS SHORT SO ALWAYS BE HAPPY.",
        image: "https://via.placeholder.com/150/007bff/ffffff?text=Allen"
    },
    russell: { 
        name:"RUSSELL LAMSON", 
        bio:"COMING SOON", 
        address:"B9 L6 PH3 ELYSIAN HOMES PHASE 3 BAHAY PARE, MEYCAUAYAN, BULACAN", 
        phone:"09939219637", 
        email:"RUSSELLAMSON9@GMAIL.COM", 
        work:"LALAMOVE RIDER", 
        hobby:"RIDING MOTORCYCLE", 
        age:"19", 
        sex:"MALE", 
        civil:"SINGLE", 
        height:"5'7", 
        weight:"60KG", 
        quote:"KUNG KAYA NILA, PAGAWA MO SAKANILA!",
        image: "https://via.placeholder.com/150/ff7f50/ffffff?text=Russell"
    },
    jhonrey: { 
        name:"JHON REY BERNALES", 
        bio:"SLEEPYY", 
        address:"BLK 2 LOT 13 GARDEN VIEW HEIGHTS BALUYOT PARK BRGY. SAUYO QUEZON CITY", 
        phone:"09917410416", 
        email:"JHONREYBERNALES14@GMAIL.COM", 
        work:"NONE", 
        hobby:"BASKETBALL, WATCHING ANIME, GAMES", 
        age:"19", 
        sex:"MALE", 
        civil:"SINGLE", 
        height:"5'7", 
        weight:"48KG", 
        quote:"YOUR LIFE DOES NOT GET BETTER BY CHANCE, IT GETS BETTER BY CHANGE.",
        image: "https://via.placeholder.com/150/ffa500/ffffff?text=Jhon+Rey"
    },
    robert: { 
        name:"ROBERT CARIÑO", 
        bio:"COMING SOON", 
        address:"BLK 2 148 LOWER JASMIN ST.PAYATAS A QUEZON CITY", 
        phone:"09917409653", 
        email:"robertcarino58@gmail.com", 
        work:"STUDIO PHOTOGRAPHER", 
        hobby:"ONLINE GAMES AND MOVIE", 
        age:"20", 
        sex:"MALE ", 
        civil:"SINGLE", 
        height:"5'7", 
        weight:"50KG", 
        quote:"LIFE IS VERY SHORT,BE HAPPY ALWAYS",
        image: "https://via.placeholder.com/150/28a745/ffffff?text=Robert"
    },
    dhan: { 
        name:"DHAN TAGASLING", 
        bio:"BBS BERNALES ", 
        address:"102 IDANG STREET BRGY SANTA MONICA NOVALICHES QUEZON CITY ", 
        phone:"09816709811 ", 
        email:"TAGASLING.DHANLLOID.BOLIMA@GMAIL.COM ", 
        work:"STUDIO PHOTOGRAPHER ", 
        hobby:"PLAYING MOBILE GAMES,MATULOG", 
        age:"19", 
        sex:"MALE", 
        civil:"SINGLE", 
        height:"5'4", 
        weight:"48KG", 
        quote:"HINDE MAHALAGA ANG MAGWAGI ANG MAHALAGA IKAW AY NAKIBAHAGI",
        image: "https://via.placeholder.com/150/6f42c1/ffffff?text=Dhan"
    }
};

function showProfile(person, element) {
    const p = profiles[person];
    
    document.querySelectorAll(".profile-link").forEach(link => {
        link.classList.remove("active");
    });
    element.classList.add("active");

    document.getElementById("profileDisplay").innerHTML = `
        <img src="${p.image}" alt="${p.name}">
        <h2>${p.name}</h2>
        <p><strong>BIO:</strong> ${p.bio}</p>
        <p><strong>ADDRESS:</strong> ${p.address}</p>
        <p><strong>PHONE:</strong> ${p.phone}</p>
        <p><strong>EMAIL:</strong> ${p.email}</p>
        <p><strong>WORK:</strong> ${p.work}</p>
        <p><strong>HOBBY:</strong> ${p.hobby}</p>

        <br><h3>PERSONAL DETAILS</h3>
        <p><strong>AGE:</strong> ${p.age}</p>
        <p><strong>SEX:</strong> ${p.sex}</p>
        <p><strong>CIVIL STATUS:</strong> ${p.civil}</p>
        <p><strong>HEIGHT:</strong> ${p.height}</p>
        <p><strong>WEIGHT:</strong> ${p.weight}</p>

        <br><p><strong>QUOTE:</strong> ${p.quote}</p>
    `;
}
</script>

</body>
</html><!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Profile Resume</title>
<style>
    body {
        font-family: Arial, sans-serif;
        background: #f4f4f4;
        text-align: center;
        margin: 0;
        padding: 0;
    }
    h1 {
        background: #333;
        color: #fff;
        padding: 15px;
        margin: 0;
    }
    .nav {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
        background: #eee;
        padding: 10px;
    }
    .profile-link {
        background: #ddd;
        margin: 5px;
        padding: 10px 15px;
        border-radius: 8px;
        cursor: pointer;
        transition: background 0.3s;
    }
    .profile-link:hover {
        background: #bbb;
    }
    .active {
        background: #007bff;
        color: white;
    }
    #profileDisplay {
        margin: 20px auto;
        background: white;
        max-width: 600px;
        padding: 20px;
        border-radius: 12px;
        box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    #profileDisplay img {
        width: 150px;
        height: 150px;
        border-radius: 50%;
        object-fit: cover;
        margin-bottom: 10px;
        border: 3px solid #007bff;
    }
</style>
</head>
<body>

<h1>📸 Profile Resume</h1>

<div class="nav">
    <div class="profile-link" onclick="showProfile('allen', this)">Allen</div>
    <div class="profile-link" onclick="showProfile('russell', this)">Russell</div>
    <div class="profile-link" onclick="showProfile('jhonrey', this)">Jhon Rey</div>
    <div class="profile-link" onclick="showProfile('robert', this)">Robert</div>
    <div class="profile-link" onclick="showProfile('dhan', this)">Dhan</div>
</div>

<div id="profileDisplay">
    <p>Click a name above to view their profile.</p>
</div>

<script>
const profiles = {
    allen: {
        name: "ALLEN MIGUE",
        bio: "SHY TYPE",
        address: "B-10 ROAD 2 DON JULIO GREGORIO ST. BAGBAG QC",
        phone: "09557489507",
        email: "JOHNALLENMIGUE@GMAIL.COM",
        work: "STUDIO PHOTOGRAPHER",
        hobby: "BASKETBALL, WATCHING, READING, GAMES",
        age: "19",
        sex: "MALE",
        civil: "SINGLE",
        height: "5'4",
        weight: "45KG",
        quote: "LIFE IS SHORT SO ALWAYS BE HAPPY.",
        image: "https://via.placeholder.com/150/007bff/ffffff?text=Allen"
    },
    russell: { 
        name:"RUSSELL LAMSON", 
        bio:"COMING SOON", 
        address:"B9 L6 PH3 ELYSIAN HOMES PHASE 3 BAHAY PARE, MEYCAUAYAN, BULACAN", 
        phone:"09939219637", 
        email:"RUSSELLAMSON9@GMAIL.COM", 
        work:"LALAMOVE RIDER", 
        hobby:"RIDING MOTORCYCLE", 
        age:"19", 
        sex:"MALE", 
        civil:"SINGLE", 
        height:"5'7", 
        weight:"60KG", 
        quote:"KUNG KAYA NILA, PAGAWA MO SAKANILA!",
        image: "https://via.placeholder.com/150/ff7f50/ffffff?text=Russell"
    },
    jhonrey: { 
        name:"JHON REY BERNALES", 
        bio:"SLEEPYY", 
        address:"BLK 2 LOT 13 GARDEN VIEW HEIGHTS BALUYOT PARK BRGY. SAUYO QUEZON CITY", 
        phone:"09917410416", 
        email:"JHONREYBERNALES14@GMAIL.COM", 
        work:"NONE", 
        hobby:"BASKETBALL, WATCHING ANIME, GAMES", 
        age:"19", 
        sex:"MALE", 
        civil:"SINGLE", 
        height:"5'7", 
        weight:"48KG", 
        quote:"YOUR LIFE DOES NOT GET BETTER BY CHANCE, IT GETS BETTER BY CHANGE.",
        image: "https://via.placeholder.com/150/ffa500/ffffff?text=Jhon+Rey"
    },
    robert: { 
        name:"ROBERT CARIÑO", 
        bio:"COMING SOON", 
        address:"BLK 2 148 LOWER JASMIN ST.PAYATAS A QUEZON CITY", 
        phone:"09917409653", 
        email:"robertcarino58@gmail.com", 
        work:"STUDIO PHOTOGRAPHER", 
        hobby:"ONLINE GAMES AND MOVIE", 
        age:"20", 
        sex:"MALE ", 
        civil:"SINGLE", 
        height:"5'7", 
        weight:"50KG", 
        quote:"LIFE IS VERY SHORT,BE HAPPY ALWAYS",
        image: "https://via.placeholder.com/150/28a745/ffffff?text=Robert"
    },
    dhan: { 
        name:"DHAN TAGASLING", 
        bio:"BBS BERNALES ", 
        address:"102 IDANG STREET BRGY SANTA MONICA NOVALICHES QUEZON CITY ", 
        phone:"09816709811 ", 
        email:"TAGASLING.DHANLLOID.BOLIMA@GMAIL.COM ", 
        work:"STUDIO PHOTOGRAPHER ", 
        hobby:"PLAYING MOBILE GAMES,MATULOG", 
        age:"19", 
        sex:"MALE", 
        civil:"SINGLE", 
        height:"5'4", 
        weight:"48KG", 
        quote:"HINDE MAHALAGA ANG MAGWAGI ANG MAHALAGA IKAW AY NAKIBAHAGI",
        image: "https://via.placeholder.com/150/6f42c1/ffffff?text=Dhan"
    }
};

function showProfile(person, element) {
    const p = profiles[person];
    
    document.querySelectorAll(".profile-link").forEach(link => {
        link.classList.remove("active");
    });
    element.classList.add("active");

    document.getElementById("profileDisplay").innerHTML = `
        <img src="${p.image}" alt="${p.name}">
        <h2>${p.name}</h2>
        <p><strong>BIO:</strong> ${p.bio}</p>
        <p><strong>ADDRESS:</strong> ${p.address}</p>
        <p><strong>PHONE:</strong> ${p.phone}</p>
        <p><strong>EMAIL:</strong> ${p.email}</p>
        <p><strong>WORK:</strong> ${p.work}</p>
        <p><strong>HOBBY:</strong> ${p.hobby}</p>

        <br><h3>PERSONAL DETAILS</h3>
        <p><strong>AGE:</strong> ${p.age}</p>
        <p><strong>SEX:</strong> ${p.sex}</p>
        <p><strong>CIVIL STATUS:</strong> ${p.civil}</p>
        <p><strong>HEIGHT:</strong> ${p.height}</p>
        <p><strong>WEIGHT:</strong> ${p.weight}</p>

        <br><p><strong>QUOTE:</strong> ${p.quote}</p>
    `;
}
</script>

</body>
</html>
