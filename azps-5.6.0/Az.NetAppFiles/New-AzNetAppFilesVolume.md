---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: c92e1b2536fab3584ebdf7f63b75bf264ff3eae4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906021"
---
# <span data-ttu-id="39809-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="39809-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="39809-102">簡介</span><span class="sxs-lookup"><span data-stu-id="39809-102">SYNOPSIS</span></span>
<span data-ttu-id="39809-103">在 ANF 卷 (建立) Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="39809-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="39809-104">語法</span><span class="sxs-lookup"><span data-stu-id="39809-104">SYNTAX</span></span>

### <span data-ttu-id="39809-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="39809-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-BackupId <String>] [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="39809-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="39809-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-Snapshot <PSNetAppFilesVolumeSnapshot>]
 [-Backup <PSNetAppFilesVolumeBackupProperties>] [-ProtocolType <String[]>] [-SnapshotDirectoryVisible]
 [-SecurityStyle <String>] [-ThroughputMibps <Double>] [-KerberosEnabled] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="39809-107">描述</span><span class="sxs-lookup"><span data-stu-id="39809-107">DESCRIPTION</span></span>
<span data-ttu-id="39809-108">**New-AzNetAppFilesVolume** Cmdlet 會建立 ANF 音量。</span><span class="sxs-lookup"><span data-stu-id="39809-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="39809-109">例子</span><span class="sxs-lookup"><span data-stu-id="39809-109">EXAMPLES</span></span>

### <span data-ttu-id="39809-110">範例 1：建立 ANF 音量</span><span class="sxs-lookup"><span data-stu-id="39809-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="39809-111">此命令在 「MyAnfPool」的集中建立新的 ANF 音量 「MyAnfVolume」。</span><span class="sxs-lookup"><span data-stu-id="39809-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="39809-112">參數</span><span class="sxs-lookup"><span data-stu-id="39809-112">PARAMETERS</span></span>

### <span data-ttu-id="39809-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="39809-113">-AccountName</span></span>
<span data-ttu-id="39809-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="39809-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="39809-115">-備份</span><span class="sxs-lookup"><span data-stu-id="39809-115">-Backup</span></span>
<span data-ttu-id="39809-116">代表備份物件的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="39809-116">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="39809-117">-BackupId</span><span class="sxs-lookup"><span data-stu-id="39809-117">-BackupId</span></span>
<span data-ttu-id="39809-118">備份識別碼。</span><span class="sxs-lookup"><span data-stu-id="39809-118">Backup ID.</span></span> <span data-ttu-id="39809-119">用來識別備份的 UUID v4 或資源識別碼</span><span class="sxs-lookup"><span data-stu-id="39809-119">UUID v4 or resource identifier used to identify the Backup</span></span>

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

### <span data-ttu-id="39809-120">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="39809-120">-CreationToken</span></span>
<span data-ttu-id="39809-121">音量的唯一檔案路徑</span><span class="sxs-lookup"><span data-stu-id="39809-121">A unique file path for the volume</span></span>

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

### <span data-ttu-id="39809-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="39809-122">-DefaultProfile</span></span>
<span data-ttu-id="39809-123">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="39809-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="39809-124">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="39809-124">-ExportPolicy</span></span>
<span data-ttu-id="39809-125">代表匯出策略的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="39809-125">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="39809-126">-KerberosEnabled</span><span class="sxs-lookup"><span data-stu-id="39809-126">-KerberosEnabled</span></span>
<span data-ttu-id="39809-127">描述音量是否已啟用 Kerberos</span><span class="sxs-lookup"><span data-stu-id="39809-127">Describe if a volume is Kerberos Enabled</span></span>

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

### <span data-ttu-id="39809-128">-位置</span><span class="sxs-lookup"><span data-stu-id="39809-128">-Location</span></span>
<span data-ttu-id="39809-129">資源的位置</span><span class="sxs-lookup"><span data-stu-id="39809-129">The location of the resource</span></span>

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

### <span data-ttu-id="39809-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="39809-130">-Name</span></span>
<span data-ttu-id="39809-131">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="39809-131">The name of the ANF volume</span></span>

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

### <span data-ttu-id="39809-132">-PoolName</span><span class="sxs-lookup"><span data-stu-id="39809-132">-PoolName</span></span>
<span data-ttu-id="39809-133">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="39809-133">The name of the ANF pool</span></span>

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

### <span data-ttu-id="39809-134">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="39809-134">-PoolObject</span></span>
<span data-ttu-id="39809-135">新卷積物件的區</span><span class="sxs-lookup"><span data-stu-id="39809-135">The pool for the new volume object</span></span>

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

### <span data-ttu-id="39809-136">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="39809-136">-ProtocolType</span></span>
<span data-ttu-id="39809-137">代表匯出策略的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="39809-137">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="39809-138">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="39809-138">-ReplicationObject</span></span>
<span data-ttu-id="39809-139">代表複製物件的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="39809-139">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="39809-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="39809-140">-ResourceGroupName</span></span>
<span data-ttu-id="39809-141">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="39809-141">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="39809-142">-SecurityStyle</span><span class="sxs-lookup"><span data-stu-id="39809-142">-SecurityStyle</span></span>
<span data-ttu-id="39809-143">音量的安全性樣式。</span><span class="sxs-lookup"><span data-stu-id="39809-143">The security style of volume.</span></span> <span data-ttu-id="39809-144">可能的值包括：'ntfs'， 'unix'</span><span class="sxs-lookup"><span data-stu-id="39809-144">Possible values include: 'ntfs', 'unix'</span></span>

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

### <span data-ttu-id="39809-145">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="39809-145">-ServiceLevel</span></span>
<span data-ttu-id="39809-146">ANF 音量的服務等級</span><span class="sxs-lookup"><span data-stu-id="39809-146">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="39809-147">-快照</span><span class="sxs-lookup"><span data-stu-id="39809-147">-Snapshot</span></span>
<span data-ttu-id="39809-148">代表快照物件的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="39809-148">A hashtable array which represents the snapshot object</span></span>

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

### <span data-ttu-id="39809-149">-SnapshotDirectoryVisible</span><span class="sxs-lookup"><span data-stu-id="39809-149">-SnapshotDirectoryVisible</span></span>
<span data-ttu-id="39809-150">如果已啟用 (true) ，該卷會包含唯讀 .snapshot 目錄，提供每個卷的快照存取權 (預設為 true) </span><span class="sxs-lookup"><span data-stu-id="39809-150">If enabled (true) the volume will contain a read-only .snapshot directory which provides access to each of the volume's snapshots (default to true)</span></span>

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

### <span data-ttu-id="39809-151">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="39809-151">-SnapshotId</span></span>
<span data-ttu-id="39809-152">從快照建立大量。</span><span class="sxs-lookup"><span data-stu-id="39809-152">Create volume from a snapshot.</span></span> <span data-ttu-id="39809-153">用來識別快照的 UUID v4 或資源識別碼</span><span class="sxs-lookup"><span data-stu-id="39809-153">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="39809-154">-子網Id</span><span class="sxs-lookup"><span data-stu-id="39809-154">-SubnetId</span></span>
<span data-ttu-id="39809-155">委派子網的 Azure 資源 URI</span><span class="sxs-lookup"><span data-stu-id="39809-155">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="39809-156">-標記</span><span class="sxs-lookup"><span data-stu-id="39809-156">-Tag</span></span>
<span data-ttu-id="39809-157">代表資源標記的雜湊表</span><span class="sxs-lookup"><span data-stu-id="39809-157">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="39809-158">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="39809-158">-ThroughputMibps</span></span>
<span data-ttu-id="39809-159">此音量可達到的最大 Mibps 輸送量</span><span class="sxs-lookup"><span data-stu-id="39809-159">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="39809-160">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="39809-160">-UsageThreshold</span></span>
<span data-ttu-id="39809-161">檔案系統允許的最大儲存配額 ，以位元組為單位</span><span class="sxs-lookup"><span data-stu-id="39809-161">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="39809-162">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="39809-162">-VolumeType</span></span>
<span data-ttu-id="39809-163">ANF 音量的類型</span><span class="sxs-lookup"><span data-stu-id="39809-163">The type of the ANF volume</span></span>

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

### <span data-ttu-id="39809-164">-確認</span><span class="sxs-lookup"><span data-stu-id="39809-164">-Confirm</span></span>
<span data-ttu-id="39809-165">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="39809-165">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="39809-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="39809-166">-WhatIf</span></span>
<span data-ttu-id="39809-167">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="39809-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="39809-168">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="39809-168">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="39809-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39809-169">CommonParameters</span></span>
<span data-ttu-id="39809-170">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="39809-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39809-171">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="39809-171">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39809-172">輸入</span><span class="sxs-lookup"><span data-stu-id="39809-172">INPUTS</span></span>

### <span data-ttu-id="39809-173">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="39809-173">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="39809-174">輸出</span><span class="sxs-lookup"><span data-stu-id="39809-174">OUTPUTS</span></span>

### <span data-ttu-id="39809-175">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="39809-175">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="39809-176">筆記</span><span class="sxs-lookup"><span data-stu-id="39809-176">NOTES</span></span>

## <span data-ttu-id="39809-177">相關連結</span><span class="sxs-lookup"><span data-stu-id="39809-177">RELATED LINKS</span></span>
