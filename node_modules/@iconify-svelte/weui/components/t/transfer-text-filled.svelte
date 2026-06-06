<script>
import Icon from '@iconify/css-svelte';
import '../../css/c/cq_-9tbrt.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="cq_-9tbrt"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:transfer-text-filled" {...props}></Icon>
