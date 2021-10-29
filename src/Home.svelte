<script>
    import Film from './components/Film.svelte';
	import Welcome from './components/Welcome.svelte';
	import Campus from './components/Campus.svelte';
	import Online from './components/Online.svelte';
	import Second_Life from './components/Second_Life.svelte';
    
</script>


<div class="twelve wide column"style = "border:1px solid black">
    <div class="row" style = "border:1px solid black" > <Film/> </div>
    &nbsp;
    <div class= 'row'>
    <div class="ui two column grid">
        <div class="column" style = "border:1px solid black" > <Welcome/></div>
        <div class="column" style = "border:1px solid black"> 
            <div class="row" style = "border:1px solid black"> <Campus/> </div>
            &nbsp;
            <div class="row" style = "border:1px solid black"> <Online/> </div>
            &nbsp;
            <div class="row" style = "border:1px solid black"> <Second_Life/> </div>

        </div>
    </div>
    </div>

</div>