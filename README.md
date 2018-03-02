# random-stuff

## Amiga Power Chips

Machine|Motherboard|CPU|ISA
-|-|-|-
AmigaONE X5000 | Cyrus | *e5500-core** | Power v2.06**
AmigaONE X1000 | Nemo | PA6T-1682M | Power v2.04

*no specific part listed  
**incomplete support, AltiVec is missing for example

### More Links
* [AmigaONE X5000 page](http://www.a-eon.com/index.php?page=x5000) at AEON site - mostly store links ATM
* [AmigaONE X1000 page](http://www.a-eon.com/index.php?page=x1000) at AEON site
* [Nemo page](http://www.a-eon.com/?page=nemo) at AEON site
* [AmigaONE X5000 ArsTechnica review](https://arstechnica.com/gadgets/2017/05/the-a-eon-amiga-x5000-reviewed-the-beloved-amiga-meets-2017/)
* [amigaworld.net forum posts on X3500 model](http://amigaworld.net/modules/newbb/viewtopic.php?topic_id=39529&forum=33)

## Power Architecture SIMD

The newer vector instructions are called *Vector-Scalar Extension* (VSX); but the older instructions are have different names: IBM calls them *Vector Media Extensions* (VMX); Freescale, *AltiVec*; and Apple, *Velocity Engine*. The AES instructions don't have a fancy name as far as I can tell.

The Power ISA document for version 2.07B barely even mentions VMX, and version 3.0B never mentions VMX at all. So my impression here is that VSX is a superset of the VMX/AltiVec/Velocity-Engine specification. Otherwise, how could you never mention it in the version 3.0B spec?

A table for Vector support [in IBM's compiler documentation](https://www.ibm.com/support/knowledgecenter/SSGH2K_13.1.0/com.ibm.xlc131.aix.doc/compiler_ref/opt_arch.html):

<table><thead>
	<tr><th>Architecture</th><th>Graphics support</th><th>Square root support</th><th>64-bit support</th><th>Vector processing support</th><th>Large page support</th></tr>
	</thead><tbody>
	<tr><td>pwr4</td><td>yes</td><td>yes</td><td>yes</td><td>no</td><td>yes</td></tr>
	<tr><td>pwr5</td><td>yes</td><td>yes</td><td>yes</td><td>no</td><td>yes</td></tr>
	<tr><td>pwr5x</td><td>yes</td><td>yes</td><td>yes</td><td>no</td><td>yes</td></tr>
	<tr><td>ppc</td><td>yes</td><td>yes</td><td>yes</td><td>no</td><td>yes</td></tr>
	<tr><td>ppc64</td><td>yes</td><td>yes</td><td>yes</td><td>no</td><td>yes</td></tr>
	<tr><td>ppc64gr</td><td>yes</td><td>yes</td><td>yes</td><td>no</td><td>yes</td></tr>
	<tr><td>ppc64grsq</td><td>yes</td><td>yes</td><td>yes</td><td>no</td><td>yes</td></tr>
	<tr><td>ppc64v</td><td>yes</td><td>yes</td><td>yes</td><td>VMX</td><td>yes</td></tr>
	<tr><td>ppc970</td><td>yes</td><td>yes</td><td>yes</td><td>VMX</td><td>yes</td></tr>
	<tr><td>pwr6</td><td>yes</td><td>yes</td><td>yes</td><td>VMX</td><td>yes</td></tr>
	<tr><td>pwr6e</td><td>yes</td><td>yes</td><td>yes</td><td>VMX</td><td>yes</td></tr>
	<tr><td>pwr7</td><td>yes</td><td>yes</td><td>yes</td><td>VMX, VSX</td><td>yes</td></tr>
	<tr><td>pwr8</td><td>yes</td><td>yes</td><td>yes</td><td>VMX, VSX</td><td>yes</td></tr>
</tbody></table>

Also, a paper on Power SIMD [at ResearchGate](https://www.researchgate.net/publication/299472451_Workload_acceleration_with_the_IBM_POWER_vector-scalar_architecture) I am currently reading.
