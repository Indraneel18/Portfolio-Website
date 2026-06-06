<script>
import Icon from '@iconify/css-svelte';
import '../../css/k/k0thszh3s.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="k0thszh3s"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:volume-off-filled" {...props}></Icon>
