<template>
    <nav class="navbar fixed-top navbar-expand-xl navbar-dark">
        <a class="navbar-brand custom-font" href="#">The Nerd Cave</a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarSupportedContent" aria-controls="navbarSupportedContent" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon"></span>
        </button>

        <div class="collapse navbar-collapse" id="navbarSupportedContent">
            <ul class="navbar-nav mr-auto">
                <li class="nav-item active">
                    <a class="nav-link" href="#">Home</a>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Events</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                    Games
                    </a>
                    <div class="dropdown-menu dropdown-dark" aria-labelledby="navbarDropdown">
                        <a class="dropdown-item" href="#">Dice</a>
                        <a class="dropdown-item" href="#">Board games</a>
                        <a class="dropdown-item" href="#">Yu-Gi-Oh!</a>
                        <a class="dropdown-item" href="#">Magic the Gathering</a>
                        <a class="dropdown-item" href="#">Pokemon</a>
                    </div>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                    Graphic Novels
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                        <a class="dropdown-item" href="#">DC</a>
                        <a class="dropdown-item" href="#">Marvel</a>
                        <a class="dropdown-item" href="#">Manga</a>
                    </div>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                    Merchandise
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                        <a class="dropdown-item" href="#">Toys</a>
                    </div>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
                    Accesories
                    </a>
                    <div class="dropdown-menu" aria-labelledby="navbarDropdown">
                        <a class="dropdown-item" href="#">Games workshop</a>
                        <a class="dropdown-item" href="#">TCG Accessories</a>
                    </div>
                </li>
                <li class="nav-item">
                    <a class="nav-link" href="#">Contact Us</a>
                </li>   
            </ul>
            <form class="form-inline my-2 my-lg-0">
                <div class="input-group mb-3">
                    <input type="text" class="form-control" placeholder="Search" aria-label="Search" aria-describedby="Search Products">
                    <div class="input-group-append">
                        <button class="btn btn-icon-primary" type="button" id="button-addon2"><MenuIcon/></button>
                    </div>
                </div>
            </form>
        </div>
    </nav>
</template>

<script>
import MenuIcon from 'vue-material-design-icons/Magnify.vue'
export default {
    components: {
        MenuIcon
    }
}
</script>