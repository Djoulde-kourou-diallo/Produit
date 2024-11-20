# Voiture 


package Devoir;

public class Voiture {
	private String marque;
	private String modelle;
	private int annee;
	private static int nbVoitures = 0;
	
	public Voiture(String marque, String modelle, int annee) {
		this.marque = marque;
		this.modelle = modelle;
		this.annee = annee;
		nbVoitures = getNbVoitures() + 1;
		}
	public static int getNbVoitures() {
		return nbVoitures;
	}
	
	public void affiche() {
		System.out.println("Marque :" + marque);
		System.out.println("Modelle :" + modelle);
		System.out.println("Année :" + annee);
}
	
	public static void main(String[] args) {
		Voiture V1 = new Voiture("TOOTA", "Drogba", 2023);
		Voiture V2 = new Voiture("TOOTA", "Corrola", 2022);
		Voiture V3 = new Voiture("TOOTA", "RV4", 2024);
		
		V1.affiche();
		V2.affiche();
		V3.affiche();
		System.out.println("Nombre total des voitures :" + Voiture.getNbVoitures());
	}

}