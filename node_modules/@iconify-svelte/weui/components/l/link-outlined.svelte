<script>
import Icon from '@iconify/css-svelte';
import '../../css/o/oow0oqbqv.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="oow0oqbqv"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:link-outlined" {...props}></Icon>
