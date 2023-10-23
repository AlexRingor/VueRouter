you can replace the vue-router active class in the router function 

const router = createRouter({
    history: createWebHistory(),
    routes,
    linkActiveClass: 'active-link'
})
