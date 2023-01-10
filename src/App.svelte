<script>
    import { createEventDispatcher } from "svelte";
    import Button from "./lib/Button.svelte";
    import Card from "./lib/Card.svelte";
    import Dropdown from "./lib/Dropdown.svelte";
    import Image from "./lib/Image.svelte";
    import Input from "./lib/Input.svelte";
    import List from "./lib/List.svelte";
    import Pagination from "./lib/Pagination.svelte";
    import Table from "./lib/Table.svelte";
    import Textarea from "./lib/Textarea.svelte";

    let listData = [
        'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis, illum.',
        'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis, illum.',
        'Lorem ipsum dolor sit amet consectetur adipisicing elit. Omnis, illum.'
    ]
    
    let headers_menu = ['no', 'nama', 'semester', 'nilai']
    let mahasiswa = [
        ['ach zaki', '5', '90'],
        ['ach ainul', '5', '30'],
        ['ach rohim', '3', '70'],
    ]
</script>

<main class="container">
  <div class="row">
    <!-- button -->
      <h1 class="text-center">Button</h1>
      <div class="d-flex">
          <Button text="primary" className="btn-primary mb-5"/>
          <Button text="secondary" className="btn-secondary" />
      </div>
    <!-- end button -->

    <!-- images -->
      <h1 class="my-15 text-center">Images and Cards</h1>
      <div class="d-flex">
        <div class="col">
          <Card>
            <Image
              src="https://images.unsplash.com/photo-1661956600684-97d3a4320e45?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
              width="full"
              slot="image"
              alt="img"
            />
            <h3 slot="title">Title</h3>
            <p slot="desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa dolor nobis id repudiandae. Magni accusamus quisquam at consequatur ea ad!</p>
          </Card>
        </div>
        <div class="col">
          <Card>
            <Image
              src="https://images.unsplash.com/photo-1661956600684-97d3a4320e45?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
              width="full"
              slot="image"
              alt="img"
            />
            <h3 slot="title">Title</h3>
            <p slot="desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa dolor nobis id repudiandae. Magni accusamus quisquam at consequatur ea ad!</p>
          </Card>
        </div>
        <div class="col">
          <Card>
            <Image
              src="https://images.unsplash.com/photo-1661956600684-97d3a4320e45?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1470&q=80"
              width="full"
              slot="image"
              alt="img"
            />
            <h3 slot="title">Title</h3>
            <p slot="desc">Lorem ipsum dolor sit amet consectetur adipisicing elit. Ipsa dolor nobis id repudiandae. Magni accusamus quisquam at consequatur ea ad!</p>
          </Card>
        </div>
      </div>
    <!-- end images -->

    <!-- list -->
      <h1 class="my-15 text-center">List</h1>
      <div class="d-flex">
        <List type='bullet' data={listData}/>
      </div>
    <!-- end list -->
    
    <!-- table -->
      <h1 class="my-15 text-center">Table</h1>
      <div class="d-flex">
        <Table headers={headers_menu} data={mahasiswa}/>
      </div>
    <!-- end table -->
  </div>
</main>