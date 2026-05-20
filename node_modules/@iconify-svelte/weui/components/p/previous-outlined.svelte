<script>
import Icon from '@iconify/css-svelte';
import '../../css/k/kg6arbbbf.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="kg6arbbbf"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:previous-outlined" {...props}></Icon>
