<script>
import Icon from '@iconify/css-svelte';
import '../../css/e/ewz4qxb1q.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ewz4qxb1q"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:comment-outlined" {...props}></Icon>
