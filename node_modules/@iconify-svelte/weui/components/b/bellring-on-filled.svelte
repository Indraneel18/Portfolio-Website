<script>
import Icon from '@iconify/css-svelte';
import '../../css/e/e0fkkpbji.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="e0fkkpbji"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:bellring-on-filled" {...props}></Icon>
