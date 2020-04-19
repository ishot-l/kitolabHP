<i18n>
{
    "ja": {
        "h1": "複雑な関係性を科学する",
        "h2": "複雑系価値創造ネットワーク研究室"
    },
    "en": {
        "h1": "複雑な関係性を科学する",
        "h2": "Complex Value Creation Network Laboratory"
    }
}
</i18n>
<template>
    <div class="background">
        <div class="text">
            <h1 class="mb-3 px-5">{{ $t('h1') }}</h1>
            <h2 class="px-3">{{ $t('h2') }}</h2>
        </div>
        <div id="particles">
        </div>
    </div>
</template>
<script>
export default {
    mounted() {
        particlesJS('particles', {
            "particles": {
                "number": {
                "value": 100,
                "density": {
                    "enable": true,
                    "value_area": 800
                }
                },
                "color": {
                "value": "#ffffff"
                },
                "shape": {
                "type": "circle",
                "stroke": {
                    "width": 0,
                    "color": "#000000"
                },
                "polygon": {
                    "nb_sides": 5
                },
                "image": {
                    "src": "img/github.svg",
                    "width": 100,
                    "height": 100
                }
                },
                "opacity": {
                "value": 0.32034597365154366,
                "random": true,
                "anim": {
                    "enable": false,
                    "speed": 1,
                    "opacity_min": 0.1,
                    "sync": false
                }
                },
                "size": {
                "value": 12,
                "random": true,
                "anim": {
                    "enable": false,
                    "speed": 40,
                    "size_min": 0.1,
                    "sync": false
                }
                },
                "line_linked": {
                "enable": true,
                "distance": 128.13838946061745,
                "color": "#ffffff",
                "opacity": 0.40043246706442953,
                "width": 2
                },
                "move": {
                "enable": true,
                "speed": 1,
                "direction": "none",
                "random": false,
                "straight": false,
                "out_mode": "out",
                "bounce": false,
                "attract": {
                    "enable": false,
                    "rotateX": 600,
                    "rotateY": 1200
                }
                }
            },
            "interactivity": {
                "detect_on": "canvas",
                "events": {
                "onhover": {
                    "enable": false,
                    "mode": "repulse"
                },
                "onclick": {
                    "enable": false,
                    "mode": "push"
                },
                "resize": true
                },
                "modes": {
                "grab": {
                    "distance": 400,
                    "line_linked": {
                    "opacity": 1
                    }
                },
                "bubble": {
                    "distance": 400,
                    "size": 40,
                    "duration": 2,
                    "opacity": 8,
                    "speed": 3
                },
                "repulse": {
                    "distance": 200,
                    "duration": 0.4
                },
                "push": {
                    "particles_nb": 4
                },
                "remove": {
                    "particles_nb": 2
                }
                }
            },
            "retina_detect": true
            });
    }
}
</script>
<style scoped>
.background {
    position: relative;
}

.text {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 360px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    color: #fff;
    text-align: center;
}

#particles {
    width: 100%;
    height: 360px;
    background: rgb(2,0,36);
    background: linear-gradient(351deg, rgba(2,0,36,0.6) 0%, rgba(14,14,121,0.6) 28%, rgba(0,212,255,0.6) 100%);
    box-shadow: inset 0 0 2px 2px #fff;
}
</style>