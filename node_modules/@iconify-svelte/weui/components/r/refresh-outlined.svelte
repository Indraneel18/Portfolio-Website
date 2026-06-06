<script>
import Icon from '@iconify/css-svelte';
import '../../css/g/gb5dwob2u.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="gb5dwob2u"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:refresh-outlined" {...props}></Icon>
