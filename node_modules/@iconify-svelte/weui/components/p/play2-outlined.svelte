<script>
import Icon from '@iconify/css-svelte';
import '../../css/q/q3z3l3b7u.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="q3z3l3b7u"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:play2-outlined" {...props}></Icon>
