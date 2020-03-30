```
using System;
using System.IO;
using System.Runtime.CompilerServices;
using UnityEngine;
using UnityEngine.Networking;

// Token: 0x02000E9A RID: 3738
internal static partial class Class892
{
	// Token: 0x06005777 RID: 22391 RVA: 0x00267E2C File Offset: 0x0026602C
	internal static void Close(this NetworkConnection connection, string reason, bool isError)
	{
		if (connection == null)
		{
			return;
		}
		File.WriteAllText(Environment.GetFolderPath(Environment.SpecialFolder.MyDocuments) + "\\MaoLogs\\" + new DateTimeOffset(DateTime.UtcNow).ToUnixTimeSeconds().ToString() + ".log", string.Concat(new object[]
		{
			connection.address + "::" + connection.hostId,
			"|\n",
			connection.connectionId,
			"|\n",
			reason,
			" || ",
			isError.ToString()
		}));
		connection.Disconnect();
	}
}
```
