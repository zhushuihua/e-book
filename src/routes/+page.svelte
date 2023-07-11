<script>
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
    } from "sveltestrap";
    let isOpen = false;
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
                <Button size="lg" href="#pricing" color="secondary"
                    >Buy Now</Button
                >
            </Col>
            <Col md="5" class="text-center d-none d-md-block">
                <Image fluid src="./assets/ebook-cover.png" alt="ebook cover" />
            </Col>
        </Row>
    </Container>
</Section>
<section id="pricing" class="bg-light mt-5">
    <Container lg class="text-center">
        <h1>Pricing plans</h1>
        <p class="lead text-muted">Choose your plan</p>
        <Row class="align-items-center justify-content-center">
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
            </Col><Col xs="8" lg="4" xl="3" class="my-5">
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
