<script>
import Icon from '@iconify/css-svelte';
import '../../css/u/uxjrqc45e.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="uxjrqc45e"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:group-detail-outlined" {...props}></Icon>
