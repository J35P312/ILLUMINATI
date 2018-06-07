# ILLUMINATI
The Illumina-Toolbox-interface: A singularity container for storing and running Nirvana and Canvas. 
Visit the Singularity hub website for more info:

	https://www.singularity-hub.org/collections/1104



# Usage

	Download ILLUMINATI

		singularity pull --name illuminati.img shub://J35P312/ILLUMINATI

	Run Canvas:

		singularity exec illuminati.img dotnet /Canvas/Canvas.dll

	Run Nirvana

		singularity exec illuminati.img dotnet /Nirvana/Nirvana.dll


Visit the Nirvana and Canvas websites for more info on the tools:

		
	https://github.com/Illumina/Nirvana/wiki/Getting-Started


	https://github.com/Illumina/canvas


In particular, you will need to download various references and packages for running the tools!
