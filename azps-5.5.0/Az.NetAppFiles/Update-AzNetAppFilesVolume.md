---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: 2d3b212ea24c9dda665d2e2ec2516f25a59318b2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100140559"
---
# <span data-ttu-id="454d8-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="454d8-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="454d8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="454d8-102">SYNOPSIS</span></span>
<span data-ttu-id="454d8-103">根據提供的選擇性修飾符，更新 (ANF) 盤案的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="454d8-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="454d8-104">句法</span><span class="sxs-lookup"><span data-stu-id="454d8-104">SYNTAX</span></span>

### <span data-ttu-id="454d8-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="454d8-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="454d8-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="454d8-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="454d8-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="454d8-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="454d8-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="454d8-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Backup <PSNetAppFilesVolumeBackupProperties>]
 [-ThroughputMibps <Double>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="454d8-109">說明</span><span class="sxs-lookup"><span data-stu-id="454d8-109">DESCRIPTION</span></span>
<span data-ttu-id="454d8-110">**更新-AzNetAppFilesVolume** Cmdlet 會更新 ANF 的音量。</span><span class="sxs-lookup"><span data-stu-id="454d8-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="454d8-111">示例</span><span class="sxs-lookup"><span data-stu-id="454d8-111">EXAMPLES</span></span>

### <span data-ttu-id="454d8-112">範例1：更新 ANF 的音量</span><span class="sxs-lookup"><span data-stu-id="454d8-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="454d8-113">這個命令會使用新的 UsageThreshold 大小來更新 ANF volume "MyAnfVolume"。</span><span class="sxs-lookup"><span data-stu-id="454d8-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="454d8-114">參數</span><span class="sxs-lookup"><span data-stu-id="454d8-114">PARAMETERS</span></span>

### <span data-ttu-id="454d8-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="454d8-115">-AccountName</span></span>
<span data-ttu-id="454d8-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="454d8-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="454d8-117">-備份</span><span class="sxs-lookup"><span data-stu-id="454d8-117">-Backup</span></span>
<span data-ttu-id="454d8-118">代表備份物件的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="454d8-118">A hashtable array which represents the backup object</span></span>

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

### <span data-ttu-id="454d8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="454d8-119">-DefaultProfile</span></span>
<span data-ttu-id="454d8-120">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="454d8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="454d8-121">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="454d8-121">-ExportPolicy</span></span>
<span data-ttu-id="454d8-122">代表匯出原則的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="454d8-122">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="454d8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="454d8-123">-InputObject</span></span>
<span data-ttu-id="454d8-124">要更新的卷物件</span><span class="sxs-lookup"><span data-stu-id="454d8-124">The volume object to update</span></span>

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

### <span data-ttu-id="454d8-125">-位置</span><span class="sxs-lookup"><span data-stu-id="454d8-125">-Location</span></span>
<span data-ttu-id="454d8-126">資源的位置</span><span class="sxs-lookup"><span data-stu-id="454d8-126">The location of the resource</span></span>

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

### <span data-ttu-id="454d8-127">-名稱</span><span class="sxs-lookup"><span data-stu-id="454d8-127">-Name</span></span>
<span data-ttu-id="454d8-128">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="454d8-128">The name of the ANF volume</span></span>

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

### <span data-ttu-id="454d8-129">-PoolName</span><span class="sxs-lookup"><span data-stu-id="454d8-129">-PoolName</span></span>
<span data-ttu-id="454d8-130">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="454d8-130">The name of the ANF pool</span></span>

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

### <span data-ttu-id="454d8-131">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="454d8-131">-PoolObject</span></span>
<span data-ttu-id="454d8-132">包含要更新之卷的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="454d8-132">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="454d8-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="454d8-133">-ResourceGroupName</span></span>
<span data-ttu-id="454d8-134">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="454d8-134">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="454d8-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="454d8-135">-ResourceId</span></span>
<span data-ttu-id="454d8-136">ANF 體積的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="454d8-136">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="454d8-137">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="454d8-137">-ServiceLevel</span></span>
<span data-ttu-id="454d8-138">ANF 容量的服務層級</span><span class="sxs-lookup"><span data-stu-id="454d8-138">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="454d8-139">-Tag</span><span class="sxs-lookup"><span data-stu-id="454d8-139">-Tag</span></span>
<span data-ttu-id="454d8-140">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="454d8-140">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="454d8-141">-ThroughputMibps</span><span class="sxs-lookup"><span data-stu-id="454d8-141">-ThroughputMibps</span></span>
<span data-ttu-id="454d8-142">此磁片量可達到的 Mibps 中的最大輸送量</span><span class="sxs-lookup"><span data-stu-id="454d8-142">Maximum throughput in Mibps that can be achieved by this volume</span></span>

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

### <span data-ttu-id="454d8-143">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="454d8-143">-UsageThreshold</span></span>
<span data-ttu-id="454d8-144">檔案系統允許的儲存配額上限（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="454d8-144">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="454d8-145">-確認</span><span class="sxs-lookup"><span data-stu-id="454d8-145">-Confirm</span></span>
<span data-ttu-id="454d8-146">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="454d8-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="454d8-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="454d8-147">-WhatIf</span></span>
<span data-ttu-id="454d8-148">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="454d8-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="454d8-149">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="454d8-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="454d8-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="454d8-150">CommonParameters</span></span>
<span data-ttu-id="454d8-151">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="454d8-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="454d8-152">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="454d8-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="454d8-153">輸入</span><span class="sxs-lookup"><span data-stu-id="454d8-153">INPUTS</span></span>

### <span data-ttu-id="454d8-154">System.object</span><span class="sxs-lookup"><span data-stu-id="454d8-154">System.String</span></span>

### <span data-ttu-id="454d8-155">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="454d8-155">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="454d8-156">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="454d8-156">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="454d8-157">輸出</span><span class="sxs-lookup"><span data-stu-id="454d8-157">OUTPUTS</span></span>

### <span data-ttu-id="454d8-158">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="454d8-158">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="454d8-159">筆記</span><span class="sxs-lookup"><span data-stu-id="454d8-159">NOTES</span></span>

## <span data-ttu-id="454d8-160">相關連結</span><span class="sxs-lookup"><span data-stu-id="454d8-160">RELATED LINKS</span></span>
