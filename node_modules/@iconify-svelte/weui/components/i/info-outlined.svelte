<script>
import Icon from '@iconify/css-svelte';
import '../../css/f/fwfpq_bia.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="fwfpq_bia"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:info-outlined" {...props}></Icon>
