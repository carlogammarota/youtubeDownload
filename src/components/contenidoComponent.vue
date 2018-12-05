<template>

	<div class="content-class">
		<section>
		<v-container grid-list-md text-xs-center>

			</br>
			 <b-field position="is-centered"size="is-medium">
	            <b-input placeholder="https://www.youtube.com/watch?v=o-kdLek1rW4" expanded type="url" icon="download">
	            </b-input>
	            <p class="control">
	                <button class="button is-info">Agree</button>
	            </p>
	        </b-field>




	        <div class="block">
	            <b-radio v-model="radio"
	                native-value="mp3">
	                .mp3
	            </b-radio>
	            <b-radio v-model="radio"
	                native-value="mp4">
	                .mp4
	            </b-radio>
	            <b-radio v-model="radio"
	                native-value="flv">
	                .flv
	            </b-radio>
	            <b-radio v-model="radio"
	                native-value="flac"
	                disabled>
	                .flac
	            </b-radio>
	        </div>
	        <p class="content">
	            <b>Format:</b>
	            {{ radio }}
	        </p>

	        <b-message type="is-danger" has-icon>
	            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce id fermentum quam. Proin sagittis, nibh id hendrerit imperdiet, elit sapien laoreet elit
	        </b-message>

	        <b-message type="is-success" has-icon>
	            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce id fermentum quam. Proin sagittis, nibh id hendrerit imperdiet, elit sapien laoreet elit
	        </b-message>

	        <b-message type="is-info" has-icon>
	            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Fusce id fermentum quam. Proin sagittis, nibh id hendrerit imperdiet, elit sapien laoreet elit
	        </b-message>

	        <b-message type="is-warning" has-icon>
	            Lorem ipsum dolor sit amet, consectetur warning elit. Fusce id fermentum quam. Proin sagittis, nibh id hendrerit imperdiet, elit sapien laoreet elit
	        </b-message>
	    	</br>
	    	
		</v-container>
	</section>
	</div>
</template>
<script>

	
	 export default {
	 	components:{

	 	},
        data() {
            return {
                radio: ''
            }
        }
    }
	
</script>
<style>
	.content-class{
		    background-color: #ecef35;
    	min-height: 300px;
	}
	.b-field{
		height: 50px !important;
	}
</style>