<script>
import Icon from '@iconify/css-svelte';
import '../../css/k/k1vrrv3og.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="k1vrrv3og"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:mike2-filled" {...props}></Icon>
