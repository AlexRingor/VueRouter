you can replace the vue-router active class in the router function 

const router = createRouter({
    history: createWebHistory(),
    routes,
    linkActiveClass: 'active-link'
})



Routes
Adding a notFound page in the route has a caveat, if the non existent page matches the existing route destination i.e destination/:id/:slug but in reality there is no content for that specific id and slug, it will show the page even without any content.
You have to setup a ROUTE GUARD to fix this.
https://router.vuejs.org/guide/advanced/navigation-guards.html