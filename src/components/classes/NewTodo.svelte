<script context="module" lang="ts">
	export interface Todo {
		title:string, 
		description: string, 
		priority: string,
		dueDate: string, 
		checked: boolean,
		id: string,
	}

	import { idGenerator } from '../utils';
	
	export class NewTodo implements Todo {
		constructor(public title:string, 
					public description: string = '', 
					public priority: string = 'low',
					public dueDate: string = new Date().toJSON(),
					public checked: boolean = false,
					public id: string = idGenerator(),
					){
		}
	}

</script>
