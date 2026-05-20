<script>
import Icon from '@iconify/css-svelte';
import '../../css/t/to0cm_bxr.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="to0cm_bxr"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:close2-filled" {...props}></Icon>
