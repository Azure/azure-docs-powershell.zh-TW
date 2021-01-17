---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: 2326551a2b6a03e1904e8d0d90663ee796ccaa46
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449012"
---
# <span data-ttu-id="a183e-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="a183e-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="a183e-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a183e-102">SYNOPSIS</span></span>
<span data-ttu-id="a183e-103"> (ANF) 卷中建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="a183e-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="a183e-104">句法</span><span class="sxs-lookup"><span data-stu-id="a183e-104">SYNTAX</span></span>

### <span data-ttu-id="a183e-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a183e-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a183e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a183e-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a183e-107">說明</span><span class="sxs-lookup"><span data-stu-id="a183e-107">DESCRIPTION</span></span>
<span data-ttu-id="a183e-108">**新的-AzNetAppFilesVolume** Cmdlet 會建立 ANF 的音量。</span><span class="sxs-lookup"><span data-stu-id="a183e-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="a183e-109">示例</span><span class="sxs-lookup"><span data-stu-id="a183e-109">EXAMPLES</span></span>

### <span data-ttu-id="a183e-110">範例1：建立 ANF 體積</span><span class="sxs-lookup"><span data-stu-id="a183e-110">Example 1: Create an ANF volume</span></span>
```
PS C:\>New-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -l "westus2" -CreationToken "MyAnfVolume" -UsageThreshold 1099511627776 -ServiceLevel "Premium" -SubnetId "/subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/MySubNetName"

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 1099511627776
ProvisioningState : Succeeded
SubnetId          : /subscriptions/f557b96d-2308-4a18-aae1-b8f7e7e70cc7/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyVnetName/subnets/default
```

<span data-ttu-id="a183e-111">這個命令會在「MyAnfPool」池中建立新的 ANF 音量「MyAnfVolume」。</span><span class="sxs-lookup"><span data-stu-id="a183e-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="a183e-112">參數</span><span class="sxs-lookup"><span data-stu-id="a183e-112">PARAMETERS</span></span>

### <span data-ttu-id="a183e-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a183e-113">-AccountName</span></span>
<span data-ttu-id="a183e-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="a183e-114">The name of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-115">-備份</span><span class="sxs-lookup"><span data-stu-id="a183e-115">-Backup</span></span>
<span data-ttu-id="a183e-116">代表備份物件的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="a183e-116">A hashtable array which represents the backup object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeBackupProperties
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="a183e-117">-BackupId</span></span>
<span data-ttu-id="a183e-118">[備份識別碼]。</span><span class="sxs-lookup"><span data-stu-id="a183e-118">Backup ID.</span></span> <span data-ttu-id="a183e-119">用於識別備份的 UUID v4 或資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a183e-119">UUID v4 or resource identifier used to identify the Backup</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="a183e-120">-CreationToken</span></span>
<span data-ttu-id="a183e-121">卷的唯一檔路徑</span><span class="sxs-lookup"><span data-stu-id="a183e-121">A unique file path for the volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a183e-122">-DefaultProfile</span></span>
<span data-ttu-id="a183e-123">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a183e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="a183e-124">-ExportPolicy</span></span>
<span data-ttu-id="a183e-125">代表匯出原則的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="a183e-125">A hashtable array which represents the export policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeExportPolicy
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="a183e-126">-KerberosEnabled</span></span>
<span data-ttu-id="a183e-127">描述是否已啟用某個卷 Kerberos</span><span class="sxs-lookup"><span data-stu-id="a183e-127">Describe if a volume is Kerberos Enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-128">-位置</span><span class="sxs-lookup"><span data-stu-id="a183e-128">-Location</span></span>
<span data-ttu-id="a183e-129">資源的位置</span><span class="sxs-lookup"><span data-stu-id="a183e-129">The location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="a183e-130">-Name</span></span>
<span data-ttu-id="a183e-131">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="a183e-131">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="a183e-132">-PoolName</span></span>
<span data-ttu-id="a183e-133">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="a183e-133">The name of the ANF pool</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="a183e-134">-PoolObject</span></span>
<span data-ttu-id="a183e-135">新的 volume 物件集區</span><span class="sxs-lookup"><span data-stu-id="a183e-135">The pool for the new volume object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="a183e-136">-ProtocolType</span></span>
<span data-ttu-id="a183e-137">代表匯出原則的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="a183e-137">A hashtable array which represents the export policy</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="a183e-138">-ReplicationObject</span></span>
<span data-ttu-id="a183e-139">代表複製物件的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="a183e-139">A hashtable array which represents the replication object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesReplicationObject
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a183e-140">-ResourceGroupName</span></span>
<span data-ttu-id="a183e-141">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="a183e-141">The resource group of the ANF account</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="a183e-142">-SecurityStyle</span></span>
<span data-ttu-id="a183e-143">Volume 的安全性樣式。</span><span class="sxs-lookup"><span data-stu-id="a183e-143">The security style of volume.</span></span> <span data-ttu-id="a183e-144">可能的值包括： "ntfs"、"unix"</span><span class="sxs-lookup"><span data-stu-id="a183e-144">Possible values include: 'ntfs', 'unix'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="a183e-145">-ServiceLevel</span></span>
<span data-ttu-id="a183e-146">ANF 容量的服務層級</span><span class="sxs-lookup"><span data-stu-id="a183e-146">The service level of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-147">-快照</span><span class="sxs-lookup"><span data-stu-id="a183e-147">-Snapshot</span></span>
<span data-ttu-id="a183e-148">代表快照物件的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="a183e-148">A hashtable array which represents the snapshot object</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolumeSnapshot
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="a183e-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="a183e-150">如果已啟用 (true) 則會包含唯讀的快照目錄，提供每個卷快照的存取權 (預設為 true) </span><span class="sxs-lookup"><span data-stu-id="a183e-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="a183e-151">-SnapshotId</span></span>
<span data-ttu-id="a183e-152">從快照建立音量。</span><span class="sxs-lookup"><span data-stu-id="a183e-152">Create volume from a snapshot.</span></span> <span data-ttu-id="a183e-153">用來識別快照的 UUID v4 或資源識別碼</span><span class="sxs-lookup"><span data-stu-id="a183e-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-154">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="a183e-154">-SubnetId</span></span>
<span data-ttu-id="a183e-155">委派子網的 Azure 資源 URI</span><span class="sxs-lookup"><span data-stu-id="a183e-155">The Azure Resource URI for a delegated subnet</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="a183e-156">-Tag</span></span>
<span data-ttu-id="a183e-157">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="a183e-157">A hashtable which represents resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="a183e-158">-ThroughputMibps</span></span>
<span data-ttu-id="a183e-159">此磁片量可達到的 Mibps 中的最大輸送量</span><span class="sxs-lookup"><span data-stu-id="a183e-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="a183e-160">-UsageThreshold</span></span>
<span data-ttu-id="a183e-161">檔案系統允許的儲存配額上限（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="a183e-161">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Int64
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="a183e-162">-VolumeType</span></span>
<span data-ttu-id="a183e-163">ANF 體積類型</span><span class="sxs-lookup"><span data-stu-id="a183e-163">The type of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-164">-確認</span><span class="sxs-lookup"><span data-stu-id="a183e-164">-Confirm</span></span>
<span data-ttu-id="a183e-165">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a183e-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a183e-166">-WhatIf</span></span>
<span data-ttu-id="a183e-167">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a183e-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a183e-168">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a183e-168">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a183e-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a183e-169">CommonParameters</span></span>
<span data-ttu-id="a183e-170">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a183e-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a183e-171">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="a183e-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a183e-172">輸入</span><span class="sxs-lookup"><span data-stu-id="a183e-172">INPUTS</span></span>

### <span data-ttu-id="a183e-173">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="a183e-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="a183e-174">輸出</span><span class="sxs-lookup"><span data-stu-id="a183e-174">OUTPUTS</span></span>

### <span data-ttu-id="a183e-175">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="a183e-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="a183e-176">筆記</span><span class="sxs-lookup"><span data-stu-id="a183e-176">NOTES</span></span>

## <span data-ttu-id="a183e-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="a183e-177">RELATED LINKS</span></span>
