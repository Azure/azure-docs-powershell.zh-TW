---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: b7947f4224c667ed8332b0f3206588dda49fd1af
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905941"
---
# <span data-ttu-id="14029-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="14029-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="14029-102">簡介</span><span class="sxs-lookup"><span data-stu-id="14029-102">SYNOPSIS</span></span>
<span data-ttu-id="14029-103">根據提供的選擇性 (更新 Azure NetApp 檔案) ANF 檔案的音量。</span><span class="sxs-lookup"><span data-stu-id="14029-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="14029-104">語法</span><span class="sxs-lookup"><span data-stu-id="14029-104">SYNTAX</span></span>

### <span data-ttu-id="14029-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="14029-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="14029-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14029-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14029-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14029-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14029-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="14029-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14029-109">描述</span><span class="sxs-lookup"><span data-stu-id="14029-109">DESCRIPTION</span></span>
<span data-ttu-id="14029-110">**Update-AzNetAppFilesVolume** Cmdlet 會更新 ANF 音量。</span><span class="sxs-lookup"><span data-stu-id="14029-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="14029-111">例子</span><span class="sxs-lookup"><span data-stu-id="14029-111">EXAMPLES</span></span>

### <span data-ttu-id="14029-112">範例 1：更新 ANF 音量</span><span class="sxs-lookup"><span data-stu-id="14029-112">Example 1: Update an ANF volume</span></span>
```
PS C:\>Update-AzNetAppFilesVolume -ResourceGroupName "MyRG" -l "westus2" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume" -UsageThreshold Size

Output:

Location          : westus2
Id                : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.NetApp/netAppAccounts/MyAnfAccount/capacityPools/MyAnfPool/volumes/MyAnfVolume
Name              : MyAnfAccount/MyAnfPool/MyAnfVolume
Type              : Microsoft.NetApp/netAppAccounts/capacityPools/volumes
Tags              :
FileSystemId      : 3e2773a7-2a72-d003-0637-1a8b1fa3eaaf
CreationToken     : MyAnfVolume
ServiceLevel      : Premium
UsageThreshold    : 2199023255552
ProvisioningState : Succeeded
SubnetId          : /subscriptions/subsId/resourceGroups/MyRG/providers/Microsoft.Network/virtualNetworks/MyRG-vnet/subnets/default
```

<span data-ttu-id="14029-113">此命令會以新的 UsageThreshold 大小更新 ANF 音量 「MyAnfVolume」。</span><span class="sxs-lookup"><span data-stu-id="14029-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="14029-114">參數</span><span class="sxs-lookup"><span data-stu-id="14029-114">PARAMETERS</span></span>

### <span data-ttu-id="14029-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="14029-115">-AccountName</span></span>
<span data-ttu-id="14029-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="14029-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="14029-117">-備份</span><span class="sxs-lookup"><span data-stu-id="14029-117">-Backup</span></span>
<span data-ttu-id="14029-118">代表備份物件的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="14029-118">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="14029-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14029-119">-DefaultProfile</span></span>
<span data-ttu-id="14029-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="14029-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14029-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="14029-121">-ExportPolicy</span></span>
<span data-ttu-id="14029-122">代表匯出策略的雜湊表陣列</span><span class="sxs-lookup"><span data-stu-id="14029-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="14029-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14029-123">-InputObject</span></span>
<span data-ttu-id="14029-124">要更新的音量物件</span><span class="sxs-lookup"><span data-stu-id="14029-124">The volume object to update</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14029-125">-位置</span><span class="sxs-lookup"><span data-stu-id="14029-125">-Location</span></span>
<span data-ttu-id="14029-126">資源的位置</span><span class="sxs-lookup"><span data-stu-id="14029-126">The location of the resource</span></span>

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

### <span data-ttu-id="14029-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="14029-127">-Name</span></span>
<span data-ttu-id="14029-128">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="14029-128">The name of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14029-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="14029-129">-PoolName</span></span>
<span data-ttu-id="14029-130">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="14029-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="14029-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="14029-131">-PoolObject</span></span>
<span data-ttu-id="14029-132">包含要更新之卷的集中物件</span><span class="sxs-lookup"><span data-stu-id="14029-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="14029-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14029-133">-ResourceGroupName</span></span>
<span data-ttu-id="14029-134">ANF 帳戶的資源群組</span><span class="sxs-lookup"><span data-stu-id="14029-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="14029-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14029-135">-ResourceId</span></span>
<span data-ttu-id="14029-136">ANF 音量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="14029-136">The resource id of the ANF volume</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="14029-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="14029-137">-ServiceLevel</span></span>
<span data-ttu-id="14029-138">ANF 音量的服務等級</span><span class="sxs-lookup"><span data-stu-id="14029-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="14029-139">-標記</span><span class="sxs-lookup"><span data-stu-id="14029-139">-Tag</span></span>
<span data-ttu-id="14029-140">代表資源標記的雜湊表</span><span class="sxs-lookup"><span data-stu-id="14029-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="14029-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="14029-141">-ThroughputMibps</span></span>
<span data-ttu-id="14029-142">此音量可達到的最大 Mibps 輸送量</span><span class="sxs-lookup"><span data-stu-id="14029-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="14029-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="14029-143">-UsageThreshold</span></span>
<span data-ttu-id="14029-144">檔案系統允許的最大儲存配額 ，以位元組為單位</span><span class="sxs-lookup"><span data-stu-id="14029-144">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14029-145">-確認</span><span class="sxs-lookup"><span data-stu-id="14029-145">-Confirm</span></span>
<span data-ttu-id="14029-146">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="14029-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14029-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14029-147">-WhatIf</span></span>
<span data-ttu-id="14029-148">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="14029-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14029-149">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="14029-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14029-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14029-150">CommonParameters</span></span>
<span data-ttu-id="14029-151">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="14029-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14029-152">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14029-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14029-153">輸入</span><span class="sxs-lookup"><span data-stu-id="14029-153">INPUTS</span></span>

### <span data-ttu-id="14029-154">System.String</span><span class="sxs-lookup"><span data-stu-id="14029-154">System.String</span></span>

### <span data-ttu-id="14029-155">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="14029-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="14029-156">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="14029-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="14029-157">輸出</span><span class="sxs-lookup"><span data-stu-id="14029-157">OUTPUTS</span></span>

### <span data-ttu-id="14029-158">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="14029-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="14029-159">筆記</span><span class="sxs-lookup"><span data-stu-id="14029-159">NOTES</span></span>

## <span data-ttu-id="14029-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="14029-160">RELATED LINKS</span></span>
