<script>
import Icon from '@iconify/css-svelte';
import '../../css/x/xachhj26g.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="xachhj26g"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:discover-outlined" {...props}></Icon>
