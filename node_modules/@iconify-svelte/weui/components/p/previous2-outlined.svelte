<script>
import Icon from '@iconify/css-svelte';
import '../../css/a/ahd-08pqr.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ahd-08pqr"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:previous2-outlined" {...props}></Icon>
