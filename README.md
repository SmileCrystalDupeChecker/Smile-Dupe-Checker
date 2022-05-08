# Smile-Dupe-Checker
Dupe checker for Hypixel Skyblock
  @extrasmiles
   public final HashSet<String> getDupedUUIDs() {
      return dupedUUIDs;
   }
 
   @extrasmiles
   public final HashSet<String> getDirtyUUIDs() { // Gets Dirty UUIDs 
      return dirtyUUIDs;
   }
 
   @extrasmiles
   public final HashMap<String, Integer> getDupeChecking() {
      return dupeChecking;
   }
 
   public final boolean getInAuctionBrowser() {
      return inAuctionBrowser;
   }
 
   public final void setInAuctionBrowser(boolean <set-?>) { // In auction house
      inAuctionBrowser = var1;
   }
 
   @SubscribeEvent
   public final void onWindowChange(@NotNull GuiOpenEvent event) {
      Intrinsics.checkNotNullParameter(event, "event");
      if (!(event.gui instanceof GuiContainer)) {
         inAuctionBrowser = false; // Checks duped items everywhere
         dupeChecking.clear();
         extrasmiles.printDevMessage("Cleared dupe check", "dupecheck");
         extrasmiles.printDevMessage("Cleared auction", "dupecheck");
         if (event.gui instanceof && DevTools.duped.getToggle("dupecheck")) {
            dupedUUIDs.clear();
         }
 
      }
   }
 
