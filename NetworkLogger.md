```cs
using System;
using System.Runtime.CompilerServices;
using EFT;
using UnityEngine.Networking;

// Token: 0x02000FCC RID: 4044
public abstract class GClass1120
{
	// Token: 0x17000B3F RID: 2879
	// (get) Token: 0x06005E60 RID: 24160 RVA: 0x000DA87C File Offset: 0x000D8A7C
	// (set) Token: 0x06005E61 RID: 24161 RVA: 0x000DA883 File Offset: 0x000D8A83
	internal static NetworkConnection NetworkConnection_0 { get; set; }

	// Token: 0x17000B40 RID: 2880
	// (get) Token: 0x06005E62 RID: 24162 RVA: 0x000DA88B File Offset: 0x000D8A8B
	// (set) Token: 0x06005E63 RID: 24163 RVA: 0x000DA892 File Offset: 0x000D8A92
	public static ENetLogsLevel LogsLevel { get; set; }

	// Token: 0x06005E64 RID: 24164 RVA: 0x0028010C File Offset: 0x0027E30C
	public static void Trace(string message, params string[] context)
	{
		GClass1120.LogsLevel = ENetLogsLevel.None;
	}

	// Token: 0x06005E65 RID: 24165 RVA: 0x0028010C File Offset: 0x0027E30C
	public static void Trace(byte tracerId, string message, params string[] context)
	{
		GClass1120.LogsLevel = ENetLogsLevel.None;
	}

	// Token: 0x06005E66 RID: 24166 RVA: 0x00280120 File Offset: 0x0027E320
	public static void Trace(ETraceCode code, params string[] context)
	{
		GClass1120.LogsLevel = ENetLogsLevel.None;
	}

	// Token: 0x06005E67 RID: 24167 RVA: 0x00280120 File Offset: 0x0027E320
	public static void Trace(byte tracerId, ETraceCode code, params string[] context)
	{
		GClass1120.LogsLevel = ENetLogsLevel.None;
	}

	// Token: 0x06005E68 RID: 24168 RVA: 0x0028010C File Offset: 0x0027E30C
	public static void TraceError(string message, params string[] context)
	{
		GClass1120.LogsLevel = ENetLogsLevel.None;
	}

	// Token: 0x06005E69 RID: 24169 RVA: 0x0028010C File Offset: 0x0027E30C
	public static void TraceError(byte tracerId, string message, params string[] context)
	{
		GClass1120.LogsLevel = ENetLogsLevel.None;
	}

	// Token: 0x06005E6A RID: 24170 RVA: 0x00280120 File Offset: 0x0027E320
	public static void TraceError(ETraceCode code, params string[] context)
	{
		GClass1120.LogsLevel = ENetLogsLevel.None;
	}

	// Token: 0x06005E6B RID: 24171 RVA: 0x00280120 File Offset: 0x0027E320
	public static void TraceError(byte tracerId, ETraceCode code, params string[] context)
	{
		GClass1120.LogsLevel = ENetLogsLevel.None;
	}

	// Token: 0x06005E6C RID: 24172 RVA: 0x000A1638 File Offset: 0x0009F838
	protected GClass1120()
	{
	}

	// Token: 0x04005B5D RID: 23389
	[CompilerGenerated]
	private static NetworkConnection networkConnection_0;

	// Token: 0x04005B5E RID: 23390
	[CompilerGenerated]
	private static ENetLogsLevel enetLogsLevel_0;
}
```
