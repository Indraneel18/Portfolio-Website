<script>
import Icon from '@iconify/css-svelte';
import '../../css/s/s-6o88bxm.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="s-6o88bxm"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:me-outlined" {...props}></Icon>
