<script>
    import { prevent_default } from "svelte/internal";
    import Section from "../components/Section.svelte";
    import {
        Button,
        Container,
        Row,
        Col,
        Image,
        Card,
        CardTitle,
        CardSubtitle,
        CardBody,
        CardHeader,
        CardText,
        AccordionItem,
        AccordionHeader,
        Accordion,
        ListGroup,
        ListGroupItem,
        Badge,
        Form,
        FormGroup,
        FormText,
        FormCheck,
        Icon,
        Label,
        Input,
        InputGroup,
        InputGroupText,
        Tooltip,
        Modal,
        ModalHeader,
        ModalBody,
        ModalFooter,
        Offcanvas,
        OffcanvasHeader,
        OffcanvasBody,
        Dropdown,
        DropdownToggle,
        DropdownMenu,
        DropdownItem,
        ButtonDropdown,
        TabContent,
        TabPane,
    } from "sveltestrap";
    let isOpen = false;
    let isModalOpen = false;
    let isDrawerOpen = false;
</script>

<Section id="intro">
    <Container lg>
        <Row class="justify-content-center align-items-md-center">
            <Col md="5" class="text-center text-md-start">
                <div class="display-2">Black-belt</div>
                <div class="display-5 text-muted">You Coding Skills</div>
                <p class="lead my-4 text-muted">
                    Lorem, ipsum dolor sit amet consectetur adipisicing elit.
                </p>
                <Button
                    on:click={() => (isDrawerOpen = true)}
                    size="lg"
                    color="secondary">Buy Now</Button
                >
            </Col>
            <Col md="5" class="text-center d-none d-md-block">
                <Image
                    fluid
                    src="./assets/ebook-cover.png"
                    alt="ebook cover"
                    id="book"
                />
                <Tooltip target="book" placement="bottom"
                    >The best coding book</Tooltip
                >
            </Col>
        </Row>
    </Container>
</Section>
<section id="pricing" class="bg-light mt-5">
    <Container lg class="text-center">
        <h1>Pricing plans</h1>
        <p class="lead text-muted">Choose your plan</p>
        <Row class="align-items-center justify-content-center g-0">
            <Col xs="8" lg="4" xl="3" class="my-5">
                <Card class="border-0 p-2">
                    <!-- <CardHeader> -->
                    <CardTitle>Starter Edition</CardTitle>
                    <!-- </CardHeader> -->
                    <CardBody class="py-4 lead">
                        <CardSubtitle>Basic plans</CardSubtitle>
                        <CardText class="fw-bold text-primary display-5"
                            >$12.5</CardText
                        >
                        <CardText class="text-muted"
                            >Lorem ipsum dolor sit amet, consectetur adipisicing
                            elit. Libero neque laboriosam eveniet voluptates in
                            a eum nostrum qui id deleniti.</CardText
                        >
                        <Button
                            on:click={() => (isDrawerOpen = true)}
                            color="primary"
                            size="lg"
                            outline>Purchase</Button
                        >
                    </CardBody>
                </Card>
            </Col>
            <Col xs="8" lg="4" class="my-5">
                <Card class="border-2 border-primary">
                    <!-- <CardHeader> -->
                    <CardHeader>Most Popular</CardHeader>
                    <CardTitle>Starter Edition</CardTitle>
                    <!-- </CardHeader> -->
                    <CardBody class="py-4 lead">
                        <CardSubtitle>Basic plans</CardSubtitle>
                        <CardText class="fw-bold text-primary display-5"
                            >$12.5</CardText
                        >
                        <CardText class="text-muted"
                            >Lorem ipsum dolor sit amet, consectetur adipisicing
                            elit. Libero neque laboriosam eveniet voluptates in
                            a eum nostrum qui id deleniti.</CardText
                        >
                        <Button href="#" color="primary" size="lg" outline
                            >Purchase</Button
                        >
                    </CardBody>
                </Card>
            </Col>
            <Col xs="8" lg="4" xl="3" class="my-5">
                <Card class="border-0 p-2">
                    <!-- <CardHeader> -->
                    <CardTitle>Starter Edition</CardTitle>
                    <!-- </CardHeader> -->
                    <CardBody class="py-4 lead">
                        <CardSubtitle>Basic plans</CardSubtitle>
                        <CardText class="fw-bold text-primary display-5"
                            >$12.5</CardText
                        >
                        <CardText class="text-muted"
                            >Lorem ipsum dolor sit amet, consectetur adipisicing
                            elit. Libero neque laboriosam eveniet voluptates in
                            a eum nostrum qui id deleniti.</CardText
                        >
                        <Button href="#" color="primary" size="lg" outline
                            >Purchase</Button
                        >
                    </CardBody>
                </Card>
            </Col>
        </Row>
    </Container>
</section>
<section id="topics">
    <Container md class="text-center">
        <h2>Inside the book...</h2>
        <p class="lead text-muted">
            A quick glance at the topic you will learn
        </p>
        <Row class="my-5 g-5 justify-content-around align-items-center">
            <Col xs="6" lg="4">
                <Image fluid src="./assets/kindle.png" alt="kindle" />
            </Col>
            <Col xl="6">
                <Accordion id="chapters" active>
                    <AccordionItem header="UMA Maths" active>
                        <h2>UMA Maths</h2>
                        <p class="text-muted">
                            Lorem ipsum dolor sit amet consectetur, adipisicing
                            elit. Consequatur quis eaque voluptatem id, quidem
                            necessitatibus optio sapiente libero voluptas culpa!
                        </p>
                    </AccordionItem>
                    <AccordionItem header="UMA Maths">
                        <h2>UMA Abacus</h2>
                        <p class="text-muted">
                            Lorem ipsum dolor sit amet consectetur, adipisicing
                            elit. Consequatur quis eaque voluptatem id, quidem
                            necessitatibus optio sapiente libero voluptas culpa!
                        </p>
                    </AccordionItem>
                    <AccordionItem header="WHy UMA Maths">
                        <h2>Why UMA Maths</h2>

                        <p class="text-muted">
                            Lorem ipsum, dolor sit amet consectetur adipisicing
                            elit. Blanditiis explicabo maiores eos incidunt
                            impedit, est illum. Sapiente vitae minus odio? Lorem
                            ipsum dolor sit amet consectetur, adipisicing elit.
                            Consequatur quis eaque voluptatem id, quidem
                            necessitatibus optio sapiente libero voluptas culpa!
                        </p>
                    </AccordionItem>
                </Accordion>
            </Col>
        </Row>
    </Container>
</section>
<section class="bg-light" id="reviews">
    <Container lg class="text-center">
        <h3 class="text-secondary text-center">
            <Icon name="stars" class="text-altdark" /> Book Reviews
        </h3>
        <p class="lead text-muted">What our students said about our book.</p>
        <Row class="justify-content-center">
            <Col lg="8">
                <ListGroup>
                    <ListGroupItem class="py-3 text-start">
                        <div class="mb-2">
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                        </div>
                        <h5 class="text-secondary mb-1">
                            A must buy for every spiring web developer
                        </h5>
                        <p class="text-muted mb-1">
                            Lorem ipsum dolor sit amet consectetur adipisicing
                            elit. Odit voluptas praesentium odio vitae nulla a
                            ratione. Animi eveniet tenetur quae!
                        </p>
                        <small>Review by Mario</small>
                    </ListGroupItem>
                    <ListGroupItem class="py-3 text-start">
                        <div class="mb-2">
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                        </div>
                        <h5 class="text-secondary mb-1">
                            A must buy for every spiring web developer
                        </h5>
                        <p class="text-muted mb-1">
                            Lorem ipsum dolor sit amet consectetur adipisicing
                            elit. Odit voluptas praesentium odio vitae nulla a
                            ratione. Animi eveniet tenetur quae!
                        </p>
                        <small>Review by Mario</small>
                    </ListGroupItem>
                    <ListGroupItem class="py-3 text-start">
                        <div class="mb-2">
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                        </div>
                        <h5 class="text-secondary mb-1">
                            A must buy for every spiring web developer
                        </h5>
                        <p class="text-muted mb-1">
                            Lorem ipsum dolor sit amet consectetur adipisicing
                            elit. Odit voluptas praesentium odio vitae nulla a
                            ratione. Animi eveniet tenetur quae!
                        </p>
                        <small>Review by Mario</small>
                    </ListGroupItem>
                    <ListGroupItem class="py-3 text-start">
                        <h5 class="text-secondary mb-1">
                            A must buy for every spiring web developer
                        </h5>
                        <p class="text-muted mb-1">
                            Lorem ipsum dolor sit amet consectetur adipisicing
                            elit. Odit voluptas praesentium odio vitae nulla a
                            ratione. Animi eveniet tenetur quae!
                        </p>
                        <small>Review by Mario</small>
                    </ListGroupItem>
                    <ListGroupItem class="py-3 text-start">
                        <div class="mb-2">
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                        </div>
                        <h5 class="text-secondary mb-1">
                            A must buy for every spiring web developer
                        </h5>
                        <p class="text-muted mb-1">
                            Lorem ipsum dolor sit amet consectetur adipisicing
                            elit. Odit voluptas praesentium odio vitae nulla a
                            ratione. Animi eveniet tenetur quae!
                        </p>
                        <small>Review by Mario</small>
                    </ListGroupItem>
                    <ListGroupItem class="py-3 text-start">
                        <div class="mb-2">
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                        </div>
                        <h5 class="text-secondary mb-1">
                            A must buy for every spiring web developer
                        </h5>
                        <p class="text-muted mb-1">
                            Lorem ipsum dolor sit amet consectetur adipisicing
                            elit. Odit voluptas praesentium odio vitae nulla a
                            ratione. Animi eveniet tenetur quae!
                        </p>
                        <small>Review by Mario</small>
                    </ListGroupItem>
                    <ListGroupItem class="py-3 text-start">
                        <div class="mb-2">
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                        </div>
                        <h5 class="text-secondary mb-1">
                            A must buy for every spiring web developer
                        </h5>
                        <p class="text-muted mb-1">
                            Lorem ipsum dolor sit amet consectetur adipisicing
                            elit. Odit voluptas praesentium odio vitae nulla a
                            ratione. Animi eveniet tenetur quae!
                        </p>
                        <small>Review by Mario</small>
                    </ListGroupItem>
                    <ListGroupItem class="py-3 text-start">
                        <div class="mb-2">
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                        </div>
                        <h5 class="text-secondary mb-1">
                            A must buy for every spiring web developer
                        </h5>
                        <p class="text-muted mb-1">
                            Lorem ipsum dolor sit amet consectetur adipisicing
                            elit. Odit voluptas praesentium odio vitae nulla a
                            ratione. Animi eveniet tenetur quae!
                        </p>
                        <small>Review by Mario</small>
                    </ListGroupItem>
                    <ListGroupItem class="py-3 text-start">
                        <div class="mb-2 text-danger">
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                            <Icon name="star-fill" />
                        </div>
                        <h5 class="text-secondary mb-1">
                            A must buy for every spiring web developer
                        </h5>
                        <p class="text-muted mb-1">
                            Lorem ipsum dolor sit amet consectetur adipisicing
                            elit. Odit voluptas praesentium odio vitae nulla a
                            ratione. Animi eveniet tenetur quae!
                        </p>
                        <small>Review by Mario</small>
                    </ListGroupItem>
                </ListGroup>
            </Col>
        </Row>
    </Container>
</section>
<section id="contact">
    <Container lg>
        <div class="text-center">
            <h2>Get in touch</h2>
            <p class="lead">
                Questions to ask, fill out the form to contact me directly...
            </p>
            <Row class="justify-content-center my-5">
                <Col lg="6">
                    <Form
                        class="text-start"
                        on:submit={(e) => {
                            e.preventDefault();
                            alert("abc");
                        }}
                    >
                        <FormGroup id="fxx">
                            <Label for="email">Email Address:</Label>
                            <InputGroup
                                ><InputGroupText>
                                    <Icon name="envelope" /></InputGroupText
                                >
                                <Input
                                    placeholder="Welcome to UMA"
                                    type="email"
                                    id="email"
                                />
                                <InputGroupText>
                                    <Icon
                                        name="question-circle"
                                        id="email_question"
                                    />
                                </InputGroupText>
                            </InputGroup>
                            <Tooltip
                                target="email_question"
                                placement="bottom"
                                class="mt-1">Enter your email</Tooltip
                            >
                        </FormGroup>

                        <FormGroup>
                            <Label for="name">Name:</Label>
                            <InputGroup>
                                <InputGroupText>
                                    <Icon name="person-fill" />
                                </InputGroupText>
                                <Input
                                    placeholder="e.g. James"
                                    type="text"
                                    id="name"
                                />
                                <InputGroupText>
                                    <Icon name="question-circle" id="name_id" />
                                </InputGroupText>
                            </InputGroup>
                            <Tooltip
                                target="name_id"
                                placement={"right"}
                                class="ms-1">Enter your name</Tooltip
                            >
                        </FormGroup>
                        <FormGroup>
                            <Label for="select"
                                >What is your question about?</Label
                            >
                            <InputGroup>
                                <InputGroupText>
                                    <Icon name="diagram-3" />
                                </InputGroupText>
                                <Input
                                    type="select"
                                    id="select"
                                    value="pricing"
                                >
                                    <option value="pricing"
                                        >Pricing query</option
                                    >
                                    <option value="content"
                                        >Content query</option
                                    >
                                    <option value="other">Other query</option>
                                </Input>
                            </InputGroup>
                        </FormGroup>
                        <FormGroup floating label="Your query...">
                            <Input type="textarea" style="height:10em" />
                        </FormGroup>
                        <div class="mt-4 mb-5 text-center">
                            <Button id="bbtn">Submit</Button>
                            <Tooltip target="bbtn" placement={"right"}
                                >Click to submit</Tooltip
                            >
                        </div>
                    </Form></Col
                >
            </Row>
        </div>
    </Container>
</section>
<section>
    <Container lg class="text-center bg-light p-3">
        <h2>Stay in the loop</h2>
        <p class="lead">Get the latest update as they happen...</p>
        <Row class="justify-content-center">
            <Col md="8">
                <p class="text-muted">
                    Lorem ipsum dolor sit amet, consectetur adipisicing elit.
                    Delectus, ab nemo ipsam quos nostrum, nihil illo tempore
                    incidunt repellat quisquam ad molestias, maiores culpa
                    corrupti. Odio quisquam quas iusto earum.
                </p>
                <Button
                    color="primary"
                    class="text-altlight"
                    on:click={() => (isModalOpen = true)}
                    >Register For update</Button
                >
                <Modal
                    fade={true}
                    isOpen={isModalOpen}
                    centered={true}
                    toggle={() => (isModalOpen = false)}
                >
                    <ModalHeader
                        toggle={() => {
                            isModalOpen = false;
                        }}
                        >UMA Maths
                    </ModalHeader>
                    <ModalBody
                        >Lorem ipsum dolor sit amet consectetur adipisicing
                        elit. Adipisci blanditiis commodi, tempora, itaque
                        distinctio quidem iste maxime consectetur modi voluptas
                        distinctio quas ullam excepturi fuga laborum?
                        <!-- <Form> -->
                        <FormGroup label="Your Email:" floating class="mt-2">
                            <Input placeholder="email" />
                        </FormGroup>
                        <FormGroup floating label="Floating Label">
                            <Input placeholder="Enter a value" />
                        </FormGroup>
                        <!-- </Form> -->
                    </ModalBody>

                    <ModalFooter>
                        <Button
                            outline
                            color="primary"
                            on:click={() => (isModalOpen = false)}
                            >Register</Button
                        >
                        <Button
                            outline
                            color="secondary"
                            on:click={() => (isModalOpen = false)}
                            >Cancel</Button
                        >
                    </ModalFooter>
                </Modal>
            </Col>
        </Row>
    </Container>
</section>
<Offcanvas
    isOpen={isDrawerOpen}
    toggle={() => (isDrawerOpen = false)}
    placement="start"
>
    <OffcanvasHeader>My Other books</OffcanvasHeader>
    <OffcanvasBody>
        Lorem ipsum dolor sit, amet consectetur adipisicing elit. Hic
        praesentium aliquam debitis ratione, earum qui aliquid! Eum distinctio
        dolore porro quis maiores maxime ea, fugiat vero esse reiciendis, non
        ullam amet fuga possimus saepe earum error, sapiente quisquam
        blanditiis! Vero, quo esse asperiores voluptatem similique modi
        exercitationem fugiat illo blanditiis? //Dropdown and ButtonDropdown
        <div />
        <Dropdown direction="up" class="m-4">
            <DropdownToggle outline caret>Dropdown</DropdownToggle>
            <DropdownMenu direction="down" end>
                <DropdownItem href="https://uma.sg">Header</DropdownItem>
                <DropdownItem>Some Action</DropdownItem>
                <DropdownItem disabled>Action (disabled)</DropdownItem>
                <DropdownItem divider />
                <DropdownItem>Foo Action</DropdownItem>
                <DropdownItem>Bar Action</DropdownItem>
                <DropdownItem>Quo Action</DropdownItem>
            </DropdownMenu>
        </Dropdown>
        Tabs
        <TabContent>
            <TabPane tabId="abc">
                <span slot="tab">UMA <Icon name="gear" /></span>
                abc Lorem ipsum dolor sit, amet consectetur adipisicing elit. Amet
                laudantium mollitia commodi libero itaque assumenda illo nulla quibusdam
                fugit, velit et facilis non accusantium obcaecati, ea quae, aperiam
                neque vel.
            </TabPane>
            <TabPane tabId="xyz">
                <span slot="tab">Apple <Icon name="apple" /></span>
                xyz Lorem ipsum dolor sit, amet consectetur adipisicing elit. Amet
                laudantium mollitia commodi libero itaque assumenda illo nulla quibusdam
                fugit, velit et facilis non accusantium obcaecati, ea quae, aperiam
                neque vel.
            </TabPane>
            <TabPane tabId="123" active>
                <span slot="tab">Android <Icon name="android2" /></span>
                123 Lorem ipsum dolor sit, amet consectetur adipisicing elit. Amet
                laudantium mollitia commodi libero itaque assumenda illo nulla quibusdam
                fugit, velit et facilis non accusantium obcaecati, ea quae, aperiam
                neque vel.
            </TabPane>
        </TabContent>
    </OffcanvasBody>
</Offcanvas>
