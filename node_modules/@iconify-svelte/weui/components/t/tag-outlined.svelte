<script>
import Icon from '@iconify/css-svelte';
import '../../css/l/lv9mq4pxm.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="lv9mq4pxm"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:tag-outlined" {...props}></Icon>
