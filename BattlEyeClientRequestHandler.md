```cs
using System;
using System.Runtime.CompilerServices;
using System.Threading.Tasks;
using BattlEye;

// Token: 0x02000EF4 RID: 3828
internal sealed class Class923 : IBattlEyeClientRequestHandler
{
	// Token: 0x17000A9C RID: 2716
	// (get) Token: 0x060058E1 RID: 22753 RVA: 0x000D77EA File Offset: 0x000D59EA
	// (set) Token: 0x060058E2 RID: 22754 RVA: 0x000D77F2 File Offset: 0x000D59F2
	public bool Succeed { get; private set; }

	// Token: 0x17000A9D RID: 2717
	// (get) Token: 0x060058E3 RID: 22755 RVA: 0x000D77FB File Offset: 0x000D59FB
	// (set) Token: 0x060058E4 RID: 22756 RVA: 0x000D7803 File Offset: 0x000D5A03
	public string Error { get; private set; }

	// Token: 0x060058E5 RID: 22757 RVA: 0x0027097C File Offset: 0x0026EB7C
	public async Task RunValidation(BEClient.LogDelegate logDelegate)
	{
		this.Succeed = true;
	}

	// Token: 0x060058E6 RID: 22758 RVA: 0x000D780C File Offset: 0x000D5A0C
	void IBattlEyeClientRequestHandler.OnRequestRestart(BEClient.ERestartReason reason)
	{
		this.nullable_0 = new BEClient.ERestartReason?(reason);
	}

	// Token: 0x060058E7 RID: 22759 RVA: 0x000A1F19 File Offset: 0x000A0119
	void IBattlEyeClientRequestHandler.OnSendPacket(byte[] bePacket)
	{
	}

	// Token: 0x0400578E RID: 22414
	private const int int_0 = 10;

	// Token: 0x0400578F RID: 22415
	private BEClient.ERestartReason? nullable_0;

	// Token: 0x04005790 RID: 22416
	[CompilerGenerated]
	private bool bool_0;

	// Token: 0x04005791 RID: 22417
	[CompilerGenerated]
	private string string_0;
}
```
