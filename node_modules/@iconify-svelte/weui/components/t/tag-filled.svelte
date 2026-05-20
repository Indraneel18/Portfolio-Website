<script>
import Icon from '@iconify/css-svelte';
import '../../css/s/ss3bv0b2f.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="ss3bv0b2f"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:tag-filled" {...props}></Icon>
