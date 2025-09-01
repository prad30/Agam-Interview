<script>
    import Logo from "/Logo.png";
    let activebutton="Dashboard"

    let sideList = [
        {
            id: 1,
            name: "Dashboard",
            path: "/",
        },
        {
            id: 2,
            name: "Products",
            path: "/products",
            sublinks: ["Sneakers", "JAcket", "T-shirt", "Bag"],
        },
        {
            id: 1,
            name: "Transaction(44)",
            path: "/",
        },
        {
            id: 1,
            name: "Customers",
            path: "/",
        },
        {
            id: 1,
            name: "Sales Report",
            path: "/",
        },
    ];
</script>

<aside
    class="w-70 h-screen fixed bg-[#1A1A1B] border-2-r py-8 px-4 flex flex-col gap-5"
>
    <div class="flex justify-between items-center">
        <img src={Logo} alt="Site Logo" class="w-30 h-[31px]" />
        <div class=" w-[21px] h-[18px] bg-white rounded-full"></div>
    </div>
    <div
        class="w-[247px] h-[56px] rounded-md p-2 flex gap-2 border border-[#737373]"
    >
        <div class="w-10 h-10 rounded-full bg-white"></div>
        <div>
            <p class="font-regular text-sm text-[#D1D1D1]">Company</p>
            <div class="font-bold text-[#F6F6F6]">Kanky Store</div>
        </div>
    </div>
    <div class=" flex flex-col gap-[10px]">
        <div class="text-[#737373] font-regular text-sm">GENERAL</div>
        {#each sideList as list}
            <button class="flex gap-2 mb-4 p-2 rounded-md items-center {activebutton === list.name ? 'bg-[#D9EDFF]' : ''}" on:click={() => activebutton = list.name}>
                <div class="w-5 h-5 bg-white rounded-full "></div>
                <div class="text-[#B0B0B0] text-sm {activebutton === list.name ? 'text-black' : ''}">{list.name}</div>
            </button>
        {/each}
    </div>
</aside>
