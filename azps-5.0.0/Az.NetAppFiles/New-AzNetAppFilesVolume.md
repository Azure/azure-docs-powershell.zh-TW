---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/new-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/New-AzNetAppFilesVolume.md
ms.openlocfilehash: dce91ee25cac4a716dc604e38f1ac38e5a3f3f1d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139835"
---
# <span data-ttu-id="36ade-101">New-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="36ade-101">New-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="36ade-102">摘要</span><span class="sxs-lookup"><span data-stu-id="36ade-102">SYNOPSIS</span></span>
<span data-ttu-id="36ade-103"> (ANF) 卷中建立新的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="36ade-103">Creates a new Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="36ade-104">句法</span><span class="sxs-lookup"><span data-stu-id="36ade-104">SYNTAX</span></span>

### <span data-ttu-id="36ade-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="36ade-105">ByFieldsParameterSet (Default)</span></span>
```
New-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String> -PoolName <String>
 -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String> [-VolumeType <String>]
 -ServiceLevel <String> [-SnapshotId <String>] [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36ade-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="36ade-106">ByParentObjectParameterSet</span></span>
```
New-AzNetAppFilesVolume -Name <String> -UsageThreshold <Int64> -SubnetId <String> -CreationToken <String>
 -ServiceLevel <String> [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>]
 [-ReplicationObject <PSNetAppFilesReplicationObject>] [-ProtocolType <String[]>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36ade-107">說明</span><span class="sxs-lookup"><span data-stu-id="36ade-107">DESCRIPTION</span></span>
<span data-ttu-id="36ade-108">**新的-AzNetAppFilesVolume** Cmdlet 會建立 ANF 的音量。</span><span class="sxs-lookup"><span data-stu-id="36ade-108">The **New-AzNetAppFilesVolume** cmdlet creates an ANF volume.</span></span>

## <span data-ttu-id="36ade-109">示例</span><span class="sxs-lookup"><span data-stu-id="36ade-109">EXAMPLES</span></span>

### <span data-ttu-id="36ade-110">範例1：建立 ANF 體積</span><span class="sxs-lookup"><span data-stu-id="36ade-110">Example 1: Create an ANF volume</span></span>
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

<span data-ttu-id="36ade-111">這個命令會在「MyAnfPool」池中建立新的 ANF 音量「MyAnfVolume」。</span><span class="sxs-lookup"><span data-stu-id="36ade-111">This command creates the new ANF volume "MyAnfVolume" within the pool "MyAnfPool".</span></span>

## <span data-ttu-id="36ade-112">參數</span><span class="sxs-lookup"><span data-stu-id="36ade-112">PARAMETERS</span></span>

### <span data-ttu-id="36ade-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="36ade-113">-AccountName</span></span>
<span data-ttu-id="36ade-114">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="36ade-114">The name of the ANF account</span></span>

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

### <span data-ttu-id="36ade-115">-CreationToken</span><span class="sxs-lookup"><span data-stu-id="36ade-115">-CreationToken</span></span>
<span data-ttu-id="36ade-116">卷的唯一檔路徑</span><span class="sxs-lookup"><span data-stu-id="36ade-116">A unique file path for the volume</span></span>

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

### <span data-ttu-id="36ade-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36ade-117">-DefaultProfile</span></span>
<span data-ttu-id="36ade-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="36ade-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36ade-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="36ade-119">-ExportPolicy</span></span>
<span data-ttu-id="36ade-120">代表匯出原則的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="36ade-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="36ade-121">-位置</span><span class="sxs-lookup"><span data-stu-id="36ade-121">-Location</span></span>
<span data-ttu-id="36ade-122">資源的位置</span><span class="sxs-lookup"><span data-stu-id="36ade-122">The location of the resource</span></span>

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

### <span data-ttu-id="36ade-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="36ade-123">-Name</span></span>
<span data-ttu-id="36ade-124">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="36ade-124">The name of the ANF volume</span></span>

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

### <span data-ttu-id="36ade-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="36ade-125">-PoolName</span></span>
<span data-ttu-id="36ade-126">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="36ade-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="36ade-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="36ade-127">-PoolObject</span></span>
<span data-ttu-id="36ade-128">新的 volume 物件集區</span><span class="sxs-lookup"><span data-stu-id="36ade-128">The pool for the new volume object</span></span>

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

### <span data-ttu-id="36ade-129">-ProtocolType</span><span class="sxs-lookup"><span data-stu-id="36ade-129">-ProtocolType</span></span>
<span data-ttu-id="36ade-130">代表匯出原則的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="36ade-130">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="36ade-131">-ReplicationObject</span><span class="sxs-lookup"><span data-stu-id="36ade-131">-ReplicationObject</span></span>
<span data-ttu-id="36ade-132">代表複製物件的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="36ade-132">A hashtable array which represents the replication object</span></span>

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

### <span data-ttu-id="36ade-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36ade-133">-ResourceGroupName</span></span>
<span data-ttu-id="36ade-134">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="36ade-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="36ade-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="36ade-135">-ServiceLevel</span></span>
<span data-ttu-id="36ade-136">ANF 容量的服務層級</span><span class="sxs-lookup"><span data-stu-id="36ade-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="36ade-137">-SnapshotId</span><span class="sxs-lookup"><span data-stu-id="36ade-137">-SnapshotId</span></span>
<span data-ttu-id="36ade-138">從快照建立音量。</span><span class="sxs-lookup"><span data-stu-id="36ade-138">Create volume from a snapshot.</span></span> <span data-ttu-id="36ade-139">用來識別快照的 UUID v4 或資源識別碼</span><span class="sxs-lookup"><span data-stu-id="36ade-139">UUID v4 or resource identifier used to identify the Snapshot</span></span>

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

### <span data-ttu-id="36ade-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="36ade-140">-SubnetId</span></span>
<span data-ttu-id="36ade-141">委派子網的 Azure 資源 URI</span><span class="sxs-lookup"><span data-stu-id="36ade-141">The Azure Resource URI for a delegated subnet</span></span>

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

### <span data-ttu-id="36ade-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="36ade-142">-Tag</span></span>
<span data-ttu-id="36ade-143">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="36ade-143">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="36ade-144">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="36ade-144">-UsageThreshold</span></span>
<span data-ttu-id="36ade-145">檔案系統允許的儲存配額上限（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="36ade-145">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="36ade-146">-VolumeType</span><span class="sxs-lookup"><span data-stu-id="36ade-146">-VolumeType</span></span>
<span data-ttu-id="36ade-147">ANF 體積類型</span><span class="sxs-lookup"><span data-stu-id="36ade-147">The type of the ANF volume</span></span>

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

### <span data-ttu-id="36ade-148">-確認</span><span class="sxs-lookup"><span data-stu-id="36ade-148">-Confirm</span></span>
<span data-ttu-id="36ade-149">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="36ade-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36ade-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36ade-150">-WhatIf</span></span>
<span data-ttu-id="36ade-151">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="36ade-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36ade-152">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="36ade-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36ade-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36ade-153">CommonParameters</span></span>
<span data-ttu-id="36ade-154">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="36ade-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36ade-155">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="36ade-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36ade-156">輸入</span><span class="sxs-lookup"><span data-stu-id="36ade-156">INPUTS</span></span>

### <span data-ttu-id="36ade-157">System.object</span><span class="sxs-lookup"><span data-stu-id="36ade-157">System.String</span></span>

### <span data-ttu-id="36ade-158">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="36ade-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

## <span data-ttu-id="36ade-159">輸出</span><span class="sxs-lookup"><span data-stu-id="36ade-159">OUTPUTS</span></span>

### <span data-ttu-id="36ade-160">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="36ade-160">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="36ade-161">筆記</span><span class="sxs-lookup"><span data-stu-id="36ade-161">NOTES</span></span>

## <span data-ttu-id="36ade-162">相關連結</span><span class="sxs-lookup"><span data-stu-id="36ade-162">RELATED LINKS</span></span>
