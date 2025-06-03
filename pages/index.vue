<template>
    <footer class="foot">
        <div class="footCont">
            <div class="brandCont">
                <a href="https://cesida.org/"><img src="/assets/img/CESIDA_Actual.png" alt=""></a>
            </div>
            <div class="designers"> Los Diseñadores:
                <ul class="designList">
                    <li><a href="https://www.linkedin.com/in/hugo-manzano-lara/">Hugo Manzano</a></li>
                    <li><a href="https://www.linkedin.com/in/alejandra-veloso-fern%C3%A1ndez/">Alejandra Veloso</a></li>
                    <li><a href="https://www.linkedin.com/in/anad%C3%ADazsantos/">Ana Díaz</a></li>
                </ul>
            </div>
        </div>
    </footer>


</template>


<style>
.foot {
    display: flex;
    background-color: #181818;
    width: 100vw;
    height: 6rem;
    justify-content: center;
    align-items: center;


}

.footCont {
    width: 80%;
    display: flex;
    justify-content: space-between;
    padding: 2rem;
    align-items: center;
}

.brandCont {
    height: 2rem;
    align-items: center;

}

.brandCont img {
    height: 100%;

}

.designers {
    display: flex;
    flex-direction: column;
    color: white;
    align-items: center;
}

.designList {
    display: flex;
    flex-direction: row;
    gap: 1rem;
    list-style-type: none;
    color: white;
}

.designList a {
    font-variant: normal;
    text-decoration: none;
    color: white;
}

.designList a:hover {
    
    color: gray;
}
</style>