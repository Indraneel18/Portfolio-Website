<script>
import Icon from '@iconify/css-svelte';
import '../../css/s/sdqoy3z0g.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="sdqoy3z0g"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:at-filled" {...props}></Icon>
