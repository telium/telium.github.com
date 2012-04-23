---
layout: post
title: "that one pixel gif"
description: ""
category: 
tags: []
---
{% include JB/setup %}

A green pixel. That's all.

    import io::writer_util;
    
    #[doc = "target of the code is to write a pixel image"]
    fn main() {
    	let w = io::file_writer("green_pixel.gif", [io::create]);
    
    	let wtr = result::get(w);
    
    	wtr.write([0x47_u8, 0x49_u8, 0x46_u8, 0x38_u8, 0x39_u8, 0x61_u8, 0x01_u8, 0x00_u8, 0x01_u8, 0x00_u8, 0x80_u8, 0xff_u8, 0x00_u8, 0x00_u8, 0xff_u8, 0x00_u8, 0x00_u8, 0x00_u8, 0x00_u8, 0x2c_u8, 0x00_u8, 0x00_u8, 0x00_u8, 0x00_u8, 0x01_u8, 0x00_u8, 0x01_u8, 0x00_u8, 0x00_u8, 0x02_u8, 0x02_u8, 0x44_u8, 0x01_u8, 0x00_u8, 0x3b_u8, 0x00_u8]);
    
    	wtr.flush();
    }


