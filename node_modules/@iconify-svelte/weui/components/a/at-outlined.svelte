<script>
import Icon from '@iconify/css-svelte';
import '../../css/j/j355qtbmd.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="j355qtbmd"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:at-outlined" {...props}></Icon>
