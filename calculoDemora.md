Class Viaje {
    private Integer destinoInicial;
    private Integer destinoFinal;
    private List<Parada> paradas;
    private boolean avisarParada;
    private Float demoraAproxMins;

    public void calcularDemoraAproxMins(CalculadorDistancia calculadorDistancia, CalculadorDemora calculadorDemora) {

        Float demora = 0;
        Float distanciaEnMetros = 0;

        if (avisarParada) {
            distanciaEnMetros = calculadorDistancia.distanciaEnMetrosEntre(this.destinoInicial, paradas.get(0).getUbicacion());
            demora += calculadorDemora.demoraAproxMins(distanciaEnMetros);
            
            for (int i = 0; i < paradas.size() - 1; i++) {
                distanciaEnMetros = calculadorDistancia.distanciaEnMetrosEntre(paradas.get(i).getUbicacion(), paradas.get(i+1).getUbicacion());
                demora += calculadorDemora.demoraAproxMins(distanciaEnMetros);
            }

        } else {
            distanciaEnMetros = calculadorDistancia.distanciaEnMetrosEntre(this.destinoInicial, this.destinoFinal);
            demora = calculadorDemora.demoraAproxMins(distanciaEnMetros); 
        }

        this.demoraAproxMins = demora;
    }
}
