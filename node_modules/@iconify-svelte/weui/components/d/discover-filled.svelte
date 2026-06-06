<script>
import Icon from '@iconify/css-svelte';
import '../../css/n/n2y87ub0v.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="n2y87ub0v"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:discover-filled" {...props}></Icon>
