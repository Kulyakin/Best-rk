<template >
    <header class="header" ref="headRef">
        <input class="input" placeholder="Поиск по всем категориям"/>
        <div class="btn-block">
            <button class="btn">
                <img class="btn-svg" src="../assets/IconMenu.svg" alt="">
                <span>Подборки</span>
            </button>
            <button class="btn-all">
                <img class="btn-svg" src="../assets/IconAll.svg" alt="">
                <span>Все категории</span>
            </button>
        </div>
    </header>
</template>
<script>
export default {
     methods: {
      vueOnScroll() {
        var prev = window.pageYOffset;
        const refs = this.$refs.headRef; // assign the reference in variable
        window.addEventListener("scroll", () => {
          var curr = window.pageYOffset;
          if (prev > curr) {
            refs.classList.add("scrolled");
            refs.classList.remove("scrollDown");
          } else {
            refs.classList.add("scrollDown");
            refs.classList.remove("scrolled");
          }
          if (curr === 0) {
            refs.classList.remove("scrollDown");
            refs.classList.remove("scrolled");
          }
            prev = curr;
        });
      },
    },
    mounted() {
      // run the function when the component's mount
      this.vueOnScroll();
    }
}
</script>
<style scoped>
    .header {
        width: 414px;
        height: 127px;
        background-color: #EDEDED;
    }

    .scrolled {
        position: sticky;
        top: 0px;
        z-index: 3;
        animation: 0.3s show ease-in-out;
    }

    .scrollDown {
        position: sticky;
        top: -127px;
        z-index: 3;
        animation: 0.3s hide ease-in-out;

    }

    @keyframes show {
    from {
        top: -127px;
    }
    to {
        top: 0px;
    
        }
    }

    @keyframes hide {
    from {
        top: 0px;
    }
    to {
        top: -127px;
    
        }
    }

    .input {
        width: 365px;
        height: 50px;
        border-radius: 56px;
        font-size: 18px;
        background-color: #D9D9D9;
        box-shadow: inset 0px 4px 4px rgba(0, 0, 0, 0.25);
        margin: 15px 25px 8px 25px;
        padding-left: 25px;
        outline: none;
        border: none;
        box-sizing: border-box;
    }

    .btn-block {
        display: flex;
    }
    .btn {
        width: 160px;
        height: 45px;
        margin-left: 25px;
        padding-left: 6px;
        outline: none;
        border: none;
        background-color: #D9D9D9;
        color: white;
        font-size: 16px;
        box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
        border-radius: 46px;
        display: flex;
        cursor: pointer;
        align-items: center;
        transition: all 0.1s ease-in-out;
    }
    .btn-all {
        width: 174px;
        height: 45px;
        margin-left: 31px;
        padding-left: 6px;
        outline: none;
        border: none;
        background-color: #fff;
        color: #D9D9D9;
        font-size: 16px;
        box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
        border-radius: 46px;
        display: flex;
        align-items: center;
        cursor: pointer;
        transition: all 0.1s ease-in-out;

    }

.btn-svg {
    margin-left: 8px;
    margin-right: 14px;
}

.btn:hover {
    opacity: 0.7;
}

.btn-all:hover {
    opacity: 0.7;
}
.btn:active {
    transform: translateY(2px);
    background-color: rgba(75, 75, 75, 0.25);

}
.btn-all:active {
    transform: translateY(2px);
    background-color: rgba(75, 75, 75, 0.25);


}


</style>