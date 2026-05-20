<script>
import Icon from '@iconify/css-svelte';
import '../../css/q/qfk6fpb2q.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="qfk6fpb2q"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:group-detail-filled" {...props}></Icon>
