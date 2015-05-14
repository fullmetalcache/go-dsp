# GO-DSP

go-dsp is a digital signal processing package for the [Go programming language](http://golang.org).

This was orginally written by mjibson. This version removes multi-threading from the FFT for cases where the actual calls to the FFT function are multithreaded (e.g., 8 threads that are all calling the FFT function).

## Packages

* **[dsputils](http://godoc.org/github.com/fullmetalcache/go-dsp/dsputils)** - utilities and data structures for DSP
* **[fft](http://godoc.org/github.com/fullmetalcache/go-dsp/fft)** - fast Fourier transform
* **[spectral](http://godoc.org/github.com/fullmetalcache/go-dsp/spectral)** - power spectral density functions (e.g., Pwelch)
* **[wav](http://godoc.org/github.com/fullmetalcache/go-dsp/wav)** - wav file reader functions
* **[window](http://godoc.org/github.com/fullmetalcache/go-dsp/window)** - window functions (e.g., Hamming, Hann, Bartlett)

## Installation and Usage

```$ go get github.com/fullmetalcache/go-dsp/fft```

```
package main

import (
        "fmt"
        
        "github.com/fullmetalcache/go-dsp/fft"
)

func main() {
        fmt.Println(fft.FFTReal([]float64 {1, 2, 3}))
}
```
