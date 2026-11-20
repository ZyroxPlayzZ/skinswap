package dev.skinswap.mixin;

import dev.skinswap.SkinManager;
import net.minecraft.client.network.PlayerListEntry;
import net.minecraft.entity.player.SkinTextures;
import org.spongepowered.asm.mixin.Mixin;
import org.spongepowered.asm.mixin.injection.At;
import org.spongepowered.asm.mixin.injection.Inject;
import org.spongepowered.asm.mixin.injection.callback.CallbackInfoReturnable;

@Mixin(PlayerListEntry.class)
public class PlayerListEntryMixin {
    @Inject(method = "getSkinTextures", at = @At("RETURN"), cancellable = true)
    private void skinswap$override(CallbackInfoReturnable<SkinTextures> cir) {
        SkinTextures custom = SkinManager.apply(cir.getReturnValue(), (PlayerListEntry) (Object) this);
        if (custom != null) {
            cir.setReturnValue(custom);
        }
    }
}
