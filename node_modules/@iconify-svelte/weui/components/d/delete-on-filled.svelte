<script>
import Icon from '@iconify/css-svelte';
import '../../css/s/smvzpprvs.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="smvzpprvs"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:delete-on-filled" {...props}></Icon>
