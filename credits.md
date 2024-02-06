---
layout: page
title: Credits
citations:
    - name: An arithmetic count of osculating lines
      url: https://arxiv.org/pdf/2312.12129
      authors: Giosuè Muratore
    - name: Computations of Gromov-Witten invariants of toric varieties
      url: https://arxiv.org/abs/2309.03741
      authors: Giosuè Muratore
    - name: Exact semidefinite programming bounds for packing problems
      url: https://arxiv.org/abs/2001.00256
      authors: Maria Dostert, David de Laat, Philippe Moustrou
    - name: "Brill-Noether-general limit root bundles: Absence of vector-like exotics in F-theory Standard Models"
      url: https://doi.org/10.1007/JHEP11(2022)004
      authors: Martin Bies, Mirjam Cvetič, Ron Donagi, Marielle Ong
    - name: Introduction to Toric Geometry
      url: https://arxiv.org/abs/2203.01690
      authors: Simon Telen
    - name: Toric Geometry in OSCAR
      url: https://arxiv.org/abs/2303.08110
      authors: Martin Bies, Lars Kastner
    - name: Algebraic and geometric computations in OSCAR
      url: https://sinews.siam.org/Details-Page/algebraic-and-geometric-computations-in-oscar
      authors: Mara Belotti, Michael Joswig, Chiara Meroni, Victoria Schleis, Johannes Schmitt
    - name: Computing Galois Groups of Ehrhart Polynomials in OSCAR
      url: https://www.emis.de/journals/SLC/wpapers/FPSAC2022/87.html
      authors: Claus Fieker, Tommy Hofmann, Michael Joswig
    - name: Some thoughts and experiments on Bergman's compact amalgamation problem
      url: https://arxiv.org/abs/2304.08365
      authors: Michael Joswig, Mario Kummer, Andreas Thom, Claudia He Yun
    - name: On $\mathbb{Q}$-factorial terminalizations of symplectic linear quotient singularities
      url: https://doi.org/10.26204/KLUEDO/7351
      authors: Johannes Schmitt
    - name: Invariant Grassmannians and a K3 surface with an action of order 192*2
      url: https://arxiv.org/abs/2210.14585
      authors: Stevell Muller
    - name: Classification of Symplectic Birational Involutions of Manifolds of OG10 type
      url: https://arxiv.org/abs/2206.13814
      authors: Lisa Marquand, Stevell Muller
    - name: Finite groups of symplectic birational transformations of IHS manifolds of OG10 type
      url: https://arxiv.org/abs/2310.06580
      authors: Lisa Marquand, Stevell Muller

used_software:
    - name: GAP
      website: https://www.gap-system.org

    - name: Nemo
      website: https://github.com/Nemocas/Nemo.jl/

    - name: Hecke
      website: https://github.com/thofma/Hecke.jl/

    - name: Polymake
      website: https://www.polymake.org/

    - name: Singular
      website: https://www.singular.uni-kl.de/

    - name: GMP
      website: https://gmplib.org/

    - name: MPIR
      website: http://mpir.org/

    - name: MPFR
      website: https://www.mpfr.org/

    - name: Arb
      website: http://arblib.org/

    - name: NTL
      website: https://www.shoup.net/ntl

    - name: Flint
      website: http://www.flintlib.org

    - name: Antic
      website: https://github.com/wbhart/antic

    - name: gfanlib
      website: http://home.imf.au.dk/jensen/software/gfan/gfan.html

    - name: Factory
      website: https://www.mathematik.uni-kl.de/ftp/pub/Math/Singular/Factory

    - name: cdd
      website: http://www-oldurls.inf.ethz.ch/personal/fukudak/cdd_home/

    - name: AbstractAlgebra
      website: https://github.com/Nemocas/AbstractAlgebra.jl
      
    - name: msolve
      website: https://msolve.lip6.fr/

used_software_technical:
    - name: CxxWrap.jl
      website: https://github.com/JuliaInterop/CxxWrap.jl

    - name: Julia
      website: https://www.julialang.org
---

## Software used in the OSCAR project

### Mathematical software

The OSCAR project is based on the following mathematical software:

{% assign entries = page.used_software | sort_natural:"name" %}
<ul class="software_credits_list">
{% for p in entries %}
  <li>
    <a href="{{ p.website }}">
    <strong>{{ p.name }}</strong>
    </a>
  </li>
{% endfor %}
</ul>

### Technical software

The following software is used as technical components in the OSCAR project:

{% assign entries = page.used_software_technical | sort_natural:"name" %}
<ul>
{% for p in entries %}
  <li>
    <a href="{{ p.website }}">
    <strong>{{ p.name }}</strong>
    </a>
  </li>
{% endfor %}
</ul>

## Citations of Oscar and its components

### Papers

<ul>
  {% for p in page.citations %}
  <li>
      {% if p.url != null %}
          <a href="{{ p.url }}">
          {% assign link_open = true %}
      {% endif %}
      <strong>{{ p.name }}</strong>{% if link_open %}</a>{% assign link_open = false %}{% endif %}
      {% if p.authors != null %} ({{p.authors }}){% endif %}
  </li>
  {% endfor %}
</ul>
