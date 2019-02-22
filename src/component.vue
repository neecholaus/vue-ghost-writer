<template>
	<span :class="classes">
		{{ prefix }}
		<span :class="phraseClasses">{{ phrase }}</span>
		{{ suffix }}
	</span>
</template>

<script>
    export default {
        data: function() {
            return {
				phrase: ''
            }
        },
		props: {
			prefix: {
				type: String,
				required: false,
				default: ''
			},
			suffix: {
				type: String,
				required: false,
				default: ''
			},
			classes: {
				type: String,
				required: false,
				default: ''
			},
			phraseClasses: {
				type: String,
				required: false,
				default: ''
			},
			phrases: {
				type: Array,
				required: true
			}
		},
        mounted: function() {
			let [index,next] = [0,0];
			let currPhrase = this.phrases[index].split('');

			setInterval(() => {
				if(currPhrase.length) this.phrase += currPhrase.splice(0,1);
				else next++;

				// milliseconds / 50 which passes each step
				if(next >= 40) {
					next = 0;
					this.phrase = '';
					index++;
					if(index >= this.phrases.length) index = 0;
					currPhrase = this.phrases[index].split('');
				}
			}, 50);
        },
		methods: {}
    }
</script>
