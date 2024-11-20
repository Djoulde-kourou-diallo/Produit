package Devoir;

public class Produit {
   private String nom;
   private double prixHT;
   
   public static final double TVA = 0.20;
   
   public Produit (String nom, double prixHT) {
	   this.nom = nom;
	   this.prixHT = prixHT;
   }
   
   public double calculPrixTTC() {
   return prixHT * (1 + TVA);
   }
   
   public void affiche() {
	   System.out.println("Produit : " + nom);
	   System.out.println("Prix HT : " + prixHT + "GNF");
	   System.out.println("Prix TTC : " + calculPrixTTC() + "GNF");
   }
	public static void main(String[] args
{
Produit P1 = new Produit("Livre ",20.0);
		Produit P2 = new Produit("Ordinateur ",100000.0);
		P1.affiche();
		P2.affiche();
	}

}