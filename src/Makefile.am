moggiedir=$(pkglibdir)
moggie_SCRIPTS = moggie.exe
EXTRA_DIST = $(moggie_sources) $(moggie_sources_in)
CLEANFILES = moggie.exe

moggie_sources_in = AssemblyInfo.cs.in
moggie_generated_sources = $(moggie_sources_in:.in=)
moggie_sources = main.cs

moggie_build_sources = $(addprefix $(srcdir)/, $(moggie_sources))
moggie_build_sources += $(moggie_generated_sources)

moggie.exe: $(moggie_build_sources) $(resources)
	$(MCS) -out:$@ $< 

