<script>
import Icon from '@iconify/css-svelte';
import '../../css/y/yz96fzzhj.css';
import '../../css/d/d2kvgvbvc.css';

/** @type {{width?: string; height?: string;}} */
let {width, height, ...props} = $props();

const viewBox = {"width":24,"height":24};
const content = `<defs><path id="SVG0kegTdID" class="yz96fzzhj"/></defs><use href="#SVG0kegTdID" transform="translate(4 4)" class="d2kvgvbvc"/>`;
</script>
<Icon width={width} height={height} viewBox={viewBox} content={content} fallback="weui:close-outlined" {...props}></Icon>
