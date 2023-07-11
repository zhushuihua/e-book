<script>
    import {
        Collapse,
        Nav,
        NavItem,
        NavLink,
        Navbar,
        NavbarBrand,
        NavbarToggler,
        Icon,
        ButtonDropdown,
        Dropdown,
        DropdownToggle,
        DropdownMenu,
        DropdownItem,
        Button,
    } from "sveltestrap/src";
    let isOpen = false;
</script>

<!-- fixed-top fixed-bottom (class) -->
<Navbar expand="md">
    <NavbarBrand href="#intro" class="fw-bold text-secondary"
        >Net Ninjia Pro</NavbarBrand
    >
    <NavbarToggler on:click={() => (isOpen = !isOpen)} />
    <Collapse {isOpen} navbar expand="md">
        <Nav class="ms-auto" navbar>
            <NavItem><NavLink href="#pricing">Pricing</NavLink></NavItem>
            <NavItem
                ><NavLink href="https://uma.sg/abacus">UMA Abacus</NavLink
                ></NavItem
            >
            <Dropdown inNavbar nav>
                <DropdownToggle nav caret>Apps</DropdownToggle>
                <DropdownMenu end>
                    <DropdownItem href="https://store.apple.com">
                        iOS
                    </DropdownItem>
                    <DropdownItem href="https://store.apple.com">
                        Android
                    </DropdownItem>
                    <DropdownItem divider />
                    <DropdownItem>Download (Android)</DropdownItem>
                </DropdownMenu>
            </Dropdown>
            <NavItem>
                <Button color="secondary" outline>Register</Button>
            </NavItem>
        </Nav>
    </Collapse>
</Navbar>
