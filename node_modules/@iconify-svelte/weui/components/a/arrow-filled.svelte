<script>
import Icon from '@iconify/css-svelte';
import '../../css/t/twku4hbjt.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":12,"height":24};
const content = `<path class="twku4hbjt"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:arrow-filled" {...props}></Icon>
