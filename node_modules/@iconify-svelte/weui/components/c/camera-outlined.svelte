<script>
import Icon from '@iconify/css-svelte';
import '../../css/m/m9h46gbul.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="m9h46gbul"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:camera-outlined" {...props}></Icon>
