<script>
    import Button from "./Button.svelte";
</script>
<main>
    <div class="presentation">
        <ul style="list-style: none;">
            <div class="science_img"/>
            <div class="science_block">
                <li>
                    Computer Science student
                </li>
            </div>
            <div class="programmer_block">
                <li>
                    Programmer
                </li>
            </div>
            <div class="music_block">
                <li>
                    Musician
                </li>
            </div>
        </ul>
        <Button/>
    </div>
</main>
<style>
    @import url('https://fonts.cdnfonts.com/css/mad-hacker');
    @import url('https://fonts.cdnfonts.com/css/go-soul');
    .presentation{
        text-align: center;
        justify-content: center;
        position: fixed;
        background-color: red;
    }
    .music_block{
        background-image: url('../../assets/Piano.svg');
        background-color: white;
    }
    .music_block li{
        font-family: 'GoSoul', sans-serif; 
        font-size:50px;
        left:45%;
        top:70%;
        position:fixed;
    }
    .programmer_block{
        background-image: url('../../assets/Object.svg');
    }
    .programmer_block li{
        font-family: 'MAD hacker', sans-serif;
        font-size:50px;
        left:40%;
        top:50%;
        position:fixed;
    }
    .science_img{
        background-image: url('../../assets/Terminal.svg');
        height: 5%;
        background-image: c;
        width: 2.5%;
        position: fixed;
        top:30%;
        left:30%;
        transform: scale(3);
        filter: invert(31%) sepia(68%) saturate(2557%) hue-rotate(103deg) brightness(100%) contrast(102%);
    }
    .science_block{
        background-color: white;
    }
    .science_block li{
        font-family:'Times New Roman', serif;
        font-size:50px;
        left:35%;
        top:30%;
        position:fixed;
    }
</style>