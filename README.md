# comfortFoam
comfortFoam Tool for OpenFOAM

If you like to compiling under dev Version than you need to change the "Qr" to "qr" in:

    volScalarField Qr
    (
	IOobject
	(
        	"Qr",   // <---- for dev small qr
        	runTime.timeName(),
        	mesh,
        	IOobject::READ_IF_PRESENT,
        	IOobject::NO_WRITE
    	),
        mesh,
        dimensionedScalar("Qr", dimensionSet(0,0,0,0,0,0,0), 0.0)
    );


# compiling
compile with openfoam 2212 ESI version on WSL
create aliases for cohabiting versions
if permission issues : change FOAM_APPBIN into FOAM_USER_APPBIN in the Make/files file.”
