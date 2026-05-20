<script>
import Icon from '@iconify/css-svelte';
import '../../css/z/z1nd-duxb.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":12,"height":24};
const content = `<path class="z1nd-duxb"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:back-outlined" {...props}></Icon>
