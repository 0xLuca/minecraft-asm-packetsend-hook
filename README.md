# Minecraft ASM hook for sending packets

## Usage

Copy these three files into your labymod addon source, set the transformer to `yourpackage.transformer.NetHandlerPlayClientTransformer`.

Everytime the client wants to send a packet to the server, the `shouldSendPacket` method from PacketHandler.java is called. Do stuff here, returning true means the packet is being sent to the server, not if false.

## Troubleshoot

If the asm packages could not be found, add this package to you build.gradle: https://search.maven.org/search?q=g:org.ow2.asm%20AND%20a:asm
