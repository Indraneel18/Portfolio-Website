<script>
import Icon from '@iconify/css-svelte';
import '../../css/h/hov8pmbzf.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<path class="hov8pmbzf"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:note-outlined" {...props}></Icon>
