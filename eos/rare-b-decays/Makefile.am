CLEANFILES = *~
MAINTAINERCLEANFILES = Makefile.in

AM_CXXFLAGS = @AM_CXXFLAGS@

lib_LTLIBRARIES = libeosrarebdecays.la
libeosrarebdecays_la_SOURCES = \
	b-to-k-charmonium.cc b-to-k-charmonium.hh \
	b-to-kstar-charmonium.cc b-to-kstar-charmonium.hh \
	bremsstrahlung.cc bremsstrahlung.hh \
	charm-loops.cc charm-loops.hh \
	em-contributions.hh em-contributions.cc \
	exclusive-b-to-dilepton.cc exclusive-b-to-dilepton.hh \
	exclusive-b-to-s-dilepton.hh \
	exclusive-b-to-s-dilepton-low-recoil.cc exclusive-b-to-s-dilepton-large-recoil.cc \
	exclusive-b-to-s-dilepton-low-recoil.hh exclusive-b-to-s-dilepton-large-recoil.hh \
	exclusive-b-to-s-gamma.cc exclusive-b-to-s-gamma.hh \
	inclusive-b-to-s-dilepton.cc inclusive-b-to-s-dilepton.hh \
	inclusive-b-to-s-gamma.cc inclusive-b-to-s-gamma.hh \
	hard-scattering.cc hard-scattering.hh \
	long-distance.cc long-distance.hh \
	lambda-b-to-lambda-dilepton.cc lambda-b-to-lambda-dilepton.hh \
	nonlocal-formfactors.hh nonlocal-formfactors.cc nonlocal-formfactors-fwd.hh\
	nonlocal-formfactors-p-to-p.cc \
	nonlocal-formfactors-p-to-v.cc \
	observables.cc observables.hh \
	qcdf_integrals.cc qcdf_integrals.hh
libeosrarebdecays_la_CXXFLAGS = $(AM_CXXFLAGS) $(GSL_CXXFLAGS)
libeosrarebdecays_la_LDFLAGS = $(GSL_LDFLAGS)
libeosrarebdecays_la_LIBADD = \
	$(top_builddir)/eos/utils/libeosutils.la \
	$(top_builddir)/eos/form-factors/libeosformfactors.la \
	-lboost_filesystem -lboost_system \
	-lgsl -lgslcblas -lm

include_eos_rarebdecaysdir = $(includedir)/eos/rare-b-decays
include_eos_rarebdecays_HEADERS = \
	bremsstrahlung.hh \
	charm-loops.hh \
	em-contributions.hh \
	exclusive-b-to-dilepton.hh \
	exclusive-b-to-s-dilepton.hh \
	exclusive-b-to-s-dilepton-large-recoil.hh \
	exclusive-b-to-s-dilepton-low-recoil.hh \
	exclusive-b-to-s-gamma.hh \
	inclusive-b-to-s-dilepton.hh \
	inclusive-b-to-s-gamma.hh \
	hard-scattering.hh \
	lambda-b-to-lambda-dilepton.hh \
	long-distance.hh \
	qcdf_integrals.hh

EXTRA_DIST = \
	exclusive-b-to-s-dilepton-low-recoil_TEST-btokll.data \
	exclusive-b-to-s-dilepton-low-recoil_TEST-btokstarll.data \
	exclusive-b-to-s-gamma_TEST-btokstargamma.data

AM_TESTS_ENVIRONMENT = \
	export EOS_TESTS_PARAMETERS="$(top_srcdir)/eos/parameters";

TESTS = \
	bremsstrahlung_TEST \
	charm-loops_TEST \
	em-contributions_TEST \
	exclusive-b-to-dilepton_TEST \
	exclusive-b-to-s-dilepton-low-recoil_TEST \
	exclusive-b-to-s-dilepton-large-recoil_TEST \
	exclusive-b-to-s-gamma_TEST \
	inclusive-b-to-s-dilepton_TEST \
	inclusive-b-to-s-gamma_TEST \
	hard-scattering_TEST \
	lambda-b-to-lambda-dilepton_TEST \
	long-distance_TEST \
	qcdf_integrals_TEST \
	nonlocal-formfactors-p-to-p_TEST \
	nonlocal-formfactors-p-to-v_TEST \
	b-to-kstar-charmonium_TEST \
	b-to-k-charmonium_TEST
XFAIL_TESTS = \
	exclusive-b-to-s-dilepton-large-recoil_TEST # One of the QCDF integrals has a bug in the imaginary part
LDADD = \
	$(top_builddir)/test/libeostest.a \
	libeosrarebdecays.la \
	$(top_builddir)/eos/utils/libeosutils.la \
	$(top_builddir)/eos/libeos.la

check_PROGRAMS = $(TESTS)
bremsstrahlung_TEST_SOURCES = bremsstrahlung_TEST.cc

charm_loops_TEST_SOURCES = charm-loops_TEST.cc

em_contributions_TEST_SOURCES = em-contributions_TEST.cc

exclusive_b_to_dilepton_TEST_SOURCES = exclusive-b-to-dilepton_TEST.cc

exclusive_b_to_s_dilepton_low_recoil_TEST_SOURCES = exclusive-b-to-s-dilepton-low-recoil_TEST.cc

exclusive_b_to_s_dilepton_large_recoil_TEST_SOURCES = exclusive-b-to-s-dilepton-large-recoil_TEST.cc

exclusive_b_to_s_gamma_TEST_SOURCES = exclusive-b-to-s-gamma_TEST.cc

inclusive_b_to_s_dilepton_TEST_SOURCES = inclusive-b-to-s-dilepton_TEST.cc

inclusive_b_to_s_gamma_TEST_SOURCES = inclusive-b-to-s-gamma_TEST.cc

hard_scattering_TEST_SOURCES = hard-scattering_TEST.cc

lambda_b_to_lambda_dilepton_TEST_SOURCES = lambda-b-to-lambda-dilepton_TEST.cc

long_distance_TEST_SOURCES = long-distance_TEST.cc

qcdf_integrals_TEST_SOURCES = qcdf_integrals_TEST.cc

nonlocal_formfactors_p_to_p_TEST_SOURCES = nonlocal-formfactors-p-to-p_TEST.cc

nonlocal_formfactors_p_to_v_TEST_SOURCES = nonlocal-formfactors-p-to-v_TEST.cc

b_to_kstar_charmonium_TEST_SOURCES = b-to-kstar-charmonium_TEST.cc

b_to_k_charmonium_TEST_SOURCES = b-to-k-charmonium_TEST.cc