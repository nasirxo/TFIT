## TFIT

TSALLIS DISTRIBUTION EQUATION CURVE FITTER.

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install tfit. or with github

```bash
pip install ptfit
```
 ```bash
 git clone https://github.com/nasirxo/TFIT.git
 cd TFIT
 chmod +x tfit
 ./tfit
 ```
 
 
## Usage

```python
usage: tfit [-h] [-m M_VALUE [M_VALUE ...]] [-n N_VALUE] [-n0 N0_VALUE] [-b B_VALUE] [-q Q_VALUE] [-t T_VALUE]
            [-nbounds N_BOUNDS [N_BOUNDS ...]] [-n0bounds N0_BOUNDS [N0_BOUNDS ...]] [-bbounds B_BOUNDS [B_BOUNDS ...]]
            [-qbounds Q_BOUNDS [Q_BOUNDS ...]] [-tbounds T_BOUNDS [T_BOUNDS ...]] [-show SHOW_PLOT] [-save SAVE_PATH]
            [-saveformat SAVE_FORMAT] [-pstyle PLOT_STYLE] [-fsize FONT_SIZE] [-lfsize LEGEND_FONT_SIZE] [-grid PLOT_GRID]
            [-use_eq USE_EQ] [-tune TUNE_VALUES] [-markers MARKER_SHAPES [MARKER_SHAPES ...]] [-markersize MARKER_SIZE]
            [-linesize LINE_SIZE] [-fitlinesize FIT_LINE_SIZE] [-output OUTPUT_RESULTS] [-co CONSTANTS_OUTPUT]
            [-lco LATEX_CONSTANTS_OUTPUT] [-xlabel X_LABEL] [-ylabel Y_LABEL] [-rlabel R_LABEL] [-title MAIN_TITLE]
            [-stitle SIMPLE_TITLE] [-ltitle LOG_TITLE] [-plot MAKE_PLOT] [-fit MAKE_FIT] [-maxfev MAX_FEV] [-scale LPLOT_SCALE]
            [-logplot LOG_PLOT] [-simpleplot SIMPLE_PLOT] [-ratioplot RATIO_PLOT] [-ratiorange RATIO_RANGE [RATIO_RANGE ...]]
            [-figsize FIGURE_SIZE [FIGURE_SIZE ...]] [-plotall MAKE_PLOT_ALL] [-fitall MAKE_FIT_ALL]
            [-extrapolate EXTRAPOLATE [EXTRAPOLATE ...]] [-errorbar ERROR_BAR] [-derrorbar DATA_ERROR_BAR]
            [-merrorbar MODEL_ERROR_BAR] [-dline DATA_LINE] [-mline MODEL_LINE] [-cdist CONTINUOUS_DISTRIBUTION]
            [-tunedata TUNE_DATA] [-editmode EDIT_MODE] [-csvlegend CSV_LEGEND]
            [-yscalefactor SET_YSCALE_FACTOR [SET_YSCALE_FACTOR ...]] [-legendnames SET_LEGEND_NAMES [SET_LEGEND_NAMES ...]]
            [--particles] [--particles_masses]
            file [file ...]

positional arguments:
  file                  path to input file Accepts : rivet .dat and hepdata csv files

options:
  -h, --help            show this help message and exit
  -m M_VALUE [M_VALUE ...], --m_value M_VALUE [M_VALUE ...]
                        m is the initial value of the particle mass in GeV, which is used to calculate the transverse mass
                        variable. In this case, it is set to the mass of the pion (0.14 GeV) also support multiple mass input for
                        multiple fit
  -n N_VALUE, --n_value N_VALUE
                        n value default 3.5
  -n0 N0_VALUE, --n0_value N0_VALUE
                        Normalization Factor (2*pi*N)
  -b B_VALUE, --b_value B_VALUE
                        Beta Value (the boost velocity Bt) default 0.2
  -q Q_VALUE, --q_value Q_VALUE
                        q is the initial value of the q parameter, which is a dimensionless constant that characterizes the shape
                        of the transverse momentum distribution. It is typically chosen to be between 1 and 2.
  -t T_VALUE, --t_value T_VALUE
                        t is the initial value of the pt0 parameter, which is a characteristic transverse momentum scale. It
                        represents the transverse momentum at which the exponential cut-off occurs in the Tsallis distribution
  -nbounds N_BOUNDS [N_BOUNDS ...], --n_bounds N_BOUNDS [N_BOUNDS ...]
                        n value bounds default 0-20
  -n0bounds N0_BOUNDS [N0_BOUNDS ...], --n0_bounds N0_BOUNDS [N0_BOUNDS ...]
                        N0 value bounds default -inf to +inf
  -bbounds B_BOUNDS [B_BOUNDS ...], --b_bounds B_BOUNDS [B_BOUNDS ...]
                        Beta value bounds default 0 to 1
  -qbounds Q_BOUNDS [Q_BOUNDS ...], --q_bounds Q_BOUNDS [Q_BOUNDS ...]
                        q value bounds default 1 to 2
  -tbounds T_BOUNDS [T_BOUNDS ...], --t_bounds T_BOUNDS [T_BOUNDS ...]
                        t value bounds default 0 to 1
  -show SHOW_PLOT, --show_plot SHOW_PLOT
                        To Show Plot or Not ? 1 or 0
  -save SAVE_PATH, --save_path SAVE_PATH
                        Path to save Plot default current dir
  -saveformat SAVE_FORMAT, --save_format SAVE_FORMAT
                        Plot output file format supports png jpeg pdf ps eps svg tif pgf default png
  -pstyle PLOT_STYLE, --plot_style PLOT_STYLE
                        Plot Styles Supported : PYTHON, ALICE ,ATLAS, CMS, LHCb1, LHCb2 default CMS
  -fsize FONT_SIZE, --font_size FONT_SIZE
                        Plot Font Size default 18
  -lfsize LEGEND_FONT_SIZE, --legend_font_size LEGEND_FONT_SIZE
                        Plot Legend Font Size default 13
  -grid PLOT_GRID, --plot_grid PLOT_GRID
                        To Show Grids on Plot ? 1 or 0
  -use_eq USE_EQ, --use_eq USE_EQ
                        Use Equation Type 0) without pt 1) with pt 2) beta Term included 3) Beta and n term includedn
  -tune TUNE_VALUES, --tune_values TUNE_VALUES
                        To Tune Values Interactively
  -markers MARKER_SHAPES [MARKER_SHAPES ...], --marker_shapes MARKER_SHAPES [MARKER_SHAPES ...]
                        Plot Marker Shapes : -, --, -., :, ., ,, o, v, ^, <, >, 1, 2, 3, 4, s, p, *, h, H, +, x, D, d, |, _
  -markersize MARKER_SIZE, --marker_size MARKER_SIZE
                        To set size of marker on plot
  -linesize LINE_SIZE, --line_size LINE_SIZE
                        To set size of line on plot
  -fitlinesize FIT_LINE_SIZE, --fit_line_size FIT_LINE_SIZE
                        To set size of fit line on plot
  -output OUTPUT_RESULTS, --output_results OUTPUT_RESULTS
                        Output Results to files json/csv
  -co CONSTANTS_OUTPUT, --constants_output CONSTANTS_OUTPUT
                        Output Results with constants only or not ? 1 or 0
  -lco LATEX_CONSTANTS_OUTPUT, --latex_constants_output LATEX_CONSTANTS_OUTPUT
                        Output Results with constants in latex or not ? 1 or 0
  -xlabel X_LABEL, --x_label X_LABEL
                        Plot X axis Label
  -ylabel Y_LABEL, --y_label Y_LABEL
                        Plot Y axis Label
  -rlabel R_LABEL, --r_label R_LABEL
                        Plot Ratio Y axis Label
  -title MAIN_TITLE, --main_title MAIN_TITLE
                        To set a main title for all plots
  -stitle SIMPLE_TITLE, --simple_title SIMPLE_TITLE
                        Simple Plot Title
  -ltitle LOG_TITLE, --log_title LOG_TITLE
                        Log Plot Title
  -plot MAKE_PLOT, --make_plot MAKE_PLOT
                        Only Plot Data By Specifying Histogram No
  -fit MAKE_FIT, --make_fit MAKE_FIT
                        Only Fit Data By Specifying Histogram No
  -maxfev MAX_FEV, --max_fev MAX_FEV
                        Max no of iteration to solve the curve fit
  -scale LPLOT_SCALE, --lplot_scale LPLOT_SCALE
                        Plot Y axis scale default log can use linear, symlog, logit
  -logplot LOG_PLOT, --log_plot LOG_PLOT
                        To Use Log Plot or not ? 1 or 0
  -simpleplot SIMPLE_PLOT, --simple_plot SIMPLE_PLOT
                        To Use Simple Plot or not ? 1 or 0
  -ratioplot RATIO_PLOT, --ratio_plot RATIO_PLOT
                        To Use Ratio Plot or not ? 1 or 0
  -ratiorange RATIO_RANGE [RATIO_RANGE ...], --ratio_range RATIO_RANGE [RATIO_RANGE ...]
                        Ratio Plot Y axis range
  -figsize FIGURE_SIZE [FIGURE_SIZE ...], --figure_size FIGURE_SIZE [FIGURE_SIZE ...]
                        Figure Size x y by default its 12x6
  -plotall MAKE_PLOT_ALL, --make_plot_all MAKE_PLOT_ALL
                        Plot All Histogram in Dat file
  -fitall MAKE_FIT_ALL, --make_fit_all MAKE_FIT_ALL
                        Fit All Histogram in Dat file
  -extrapolate EXTRAPOLATE [EXTRAPOLATE ...], --extrapolate EXTRAPOLATE [EXTRAPOLATE ...]
                        To extrapolate the fit function over x values
  -errorbar ERROR_BAR, --error_bar ERROR_BAR
                        To show errorbar or not ? 1 or 0
  -derrorbar DATA_ERROR_BAR, --data_error_bar DATA_ERROR_BAR
                        To show errorbar on data or not ? 1 or 0
  -merrorbar MODEL_ERROR_BAR, --model_error_bar MODEL_ERROR_BAR
                        To show errorbar on model or not ? 1 or 0
  -dline DATA_LINE, --data_line DATA_LINE
                        To show Line on Data instead of Marker ? 1 or 0
  -mline MODEL_LINE, --model_line MODEL_LINE
                        To show Line on Model Data ? 1 or 0
  -cdist CONTINUOUS_DISTRIBUTION, --continuous_distribution CONTINUOUS_DISTRIBUTION
                        To test all continuous distribution on Data and print results
  -tunedata TUNE_DATA, --tune_data TUNE_DATA
                        To Analyze Csv as tune data or not ? 1 or 0
  -editmode EDIT_MODE, --edit_mode EDIT_MODE
                        To edit the generated plots graphically or not ? 1 or 0
  -csvlegend CSV_LEGEND, --csv_legend CSV_LEGEND
                        To show legend names from csv files
  -yscalefactor SET_YSCALE_FACTOR [SET_YSCALE_FACTOR ...], --set_yscale_factor SET_YSCALE_FACTOR [SET_YSCALE_FACTOR ...]
                        To Set a scale factor to y axis
  -legendnames SET_LEGEND_NAMES [SET_LEGEND_NAMES ...], --set_legend_names SET_LEGEND_NAMES [SET_LEGEND_NAMES ...]
                        To Set Names for each Legend / Latex Supported
  --particles           List of particles: $e^-$, $e^+$, $\mu^-$, $\mu^+$, $\tau^-$, $\tau^+$, $\nu_e$, $\bar{\nu}_e$, $\nu_{\mu}$,
                        $\bar{\nu}_{\mu}$, $\nu_{\tau}$, $\bar{\nu}_{\tau}$, $u$, $\bar{u}$, $d$, $\bar{d}$, $c$, $\bar{c}$, $s$,
                        $\bar{s}$, $t$, $\bar{t}$, $b$, $\bar{b}$, $\gamma$, $g$, $W^{\pm}$, $Z^0$, $H^0$, $\pi^{\pm}$, $K^{\pm}$,
                        $p$, $\bar{p}$, $n$, $\bar{n}$, $\Lambda$, $\Xi^{\pm}$, $\Sigma^{\pm}$, $\Delta^{\pm}$, $\Omega^-$
  --particles_masses    Electron (e-) : 0.5109989461 MeV, Positron (e+) : 0.5109989461 MeV, Muon (μ-) : 105.6583745 MeV, Anti-muon
                        (μ+) : 105.6583745 MeV, Tau (τ-) : 1776.86 MeV, Anti-tau (τ+) : 1776.86 MeV, Electron neutrino (νe) :
                        0.000000320 MeV, Anti-electron neutrino (𝜈̅e) : 0.000000320 MeV, Muon neutrino (νμ) : 0.000000320 MeV,
                        Anti-muon neutrino (𝜈̅μ) : 0.000000320 MeV, Tau neutrino (𝜈τ) : 15.5 MeV, Anti-tau neutrino (𝜈̅τ) : 15.5
                        MeV, Up quark (u) : 2.2 MeV, Anti-up quark (𝑢̅) : 2.2 MeV, Down quark (d) : 4.7 MeV, Anti-down quark (𝑑̅) :
                        4.7 MeV, Charm quark (c) : 1270 MeV, Anti-charm quark (𝑐̅) : 1270 MeV, Strange quark (s) : 96 MeV, Anti-
                        strange quark (𝑠̅) : 96 MeV, Top quark (t) : 172900 MeV, Anti-top quark (𝑡̅) : 172900 MeV, Bottom quark (b)
                        : 4180 MeV, Anti-bottom quark (𝑏̅) : 4180 MeV, Photon (γ) : 0 MeV, Gluon (g) : 0 MeV, W boson (W±) : 80387
                        MeV, Z boson (Z0) : 91187.6 MeV, Higgs boson (H0) : 125100 MeV, Pion (π±) : 139.57039 MeV, Kaon (K±) :
                        493.677 MeV, Proton (p) : 938.272081 MeV, Anti-proton (𝑝̅) : 938.272081 MeV, Neutron (n) : 939.565413 MeV,
                        Anti-neutron (𝑛̅) : 939.565413 MeV, Lambda baryon (Λ) : 1115.683 MeV, Xi baryon (Ξ±) : 1314.9 MeV, Sigma
                        baryon (Σ±) : 1189.4 MeV, Delta baryon (Δ±) : 1232 MeV, Omega baryon (Ω-) : 1672.45 MeV

```

## Command Line Interface
```
/* TYPE FOLLOWING IN LINUX or MAC TERMINAL */
$ tfit
```

## Contact
```
Github : https://github.com/nasirxo
Facebook : https://fb.com/nasir.xo
```

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

Please make sure to update tests as appropriate.

## License
[MIT](https://choosealicense.com/licenses/mit/)

