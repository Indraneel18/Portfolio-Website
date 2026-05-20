<script>
import Icon from '@iconify/css-svelte';
import '../../css/d/dsqayxb2l.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="dsqayxb2l"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:mobile-contacts-filled" {...props}></Icon>
