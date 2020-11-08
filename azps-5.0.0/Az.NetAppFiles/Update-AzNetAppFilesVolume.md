---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: c28b53fcd9b65198554f34cacd6f628d977e703a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94139829"
---
# <span data-ttu-id="7f823-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="7f823-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="7f823-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7f823-102">SYNOPSIS</span></span>
<span data-ttu-id="7f823-103">根據提供的選擇性修飾符，更新 (ANF) 盤案的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="7f823-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="7f823-104">句法</span><span class="sxs-lookup"><span data-stu-id="7f823-104">SYNTAX</span></span>

### <span data-ttu-id="7f823-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="7f823-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f823-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f823-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -PoolObject <PSNetAppFilesPool>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f823-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f823-107">ByResourceIdParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f823-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f823-108">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>]
 [-ExportPolicy <PSNetAppFilesVolumeExportPolicy>] [-Tag <Hashtable>] -InputObject <PSNetAppFilesVolume>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f823-109">說明</span><span class="sxs-lookup"><span data-stu-id="7f823-109">DESCRIPTION</span></span>
<span data-ttu-id="7f823-110">**更新-AzNetAppFilesVolume** Cmdlet 會更新 ANF 的音量。</span><span class="sxs-lookup"><span data-stu-id="7f823-110">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="7f823-111">示例</span><span class="sxs-lookup"><span data-stu-id="7f823-111">EXAMPLES</span></span>

### <span data-ttu-id="7f823-112">範例1：更新 ANF 的音量</span><span class="sxs-lookup"><span data-stu-id="7f823-112">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="7f823-113">這個命令會使用新的 UsageThreshold 大小來更新 ANF volume "MyAnfVolume"。</span><span class="sxs-lookup"><span data-stu-id="7f823-113">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="7f823-114">參數</span><span class="sxs-lookup"><span data-stu-id="7f823-114">PARAMETERS</span></span>

### <span data-ttu-id="7f823-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7f823-115">-AccountName</span></span>
<span data-ttu-id="7f823-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="7f823-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="7f823-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f823-117">-DefaultProfile</span></span>
<span data-ttu-id="7f823-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="7f823-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f823-119">-ExportPolicy</span><span class="sxs-lookup"><span data-stu-id="7f823-119">-ExportPolicy</span></span>
<span data-ttu-id="7f823-120">代表匯出原則的 hashtable 陣列</span><span class="sxs-lookup"><span data-stu-id="7f823-120">A hashtable array which represents the export policy</span></span>

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

### <span data-ttu-id="7f823-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7f823-121">-InputObject</span></span>
<span data-ttu-id="7f823-122">要更新的卷物件</span><span class="sxs-lookup"><span data-stu-id="7f823-122">The volume object to update</span></span>

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

### <span data-ttu-id="7f823-123">-位置</span><span class="sxs-lookup"><span data-stu-id="7f823-123">-Location</span></span>
<span data-ttu-id="7f823-124">資源的位置</span><span class="sxs-lookup"><span data-stu-id="7f823-124">The location of the resource</span></span>

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

### <span data-ttu-id="7f823-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="7f823-125">-Name</span></span>
<span data-ttu-id="7f823-126">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="7f823-126">The name of the ANF volume</span></span>

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

### <span data-ttu-id="7f823-127">-PoolName</span><span class="sxs-lookup"><span data-stu-id="7f823-127">-PoolName</span></span>
<span data-ttu-id="7f823-128">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="7f823-128">The name of the ANF pool</span></span>

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

### <span data-ttu-id="7f823-129">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="7f823-129">-PoolObject</span></span>
<span data-ttu-id="7f823-130">包含要更新之卷的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="7f823-130">The pool object containing the volume to update</span></span>

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

### <span data-ttu-id="7f823-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f823-131">-ResourceGroupName</span></span>
<span data-ttu-id="7f823-132">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="7f823-132">The resource group of the ANF account</span></span>

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

### <span data-ttu-id="7f823-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f823-133">-ResourceId</span></span>
<span data-ttu-id="7f823-134">ANF 體積的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="7f823-134">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="7f823-135">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="7f823-135">-ServiceLevel</span></span>
<span data-ttu-id="7f823-136">ANF 容量的服務層級</span><span class="sxs-lookup"><span data-stu-id="7f823-136">The service level of the ANF volume</span></span>

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

### <span data-ttu-id="7f823-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="7f823-137">-Tag</span></span>
<span data-ttu-id="7f823-138">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="7f823-138">A hashtable which represents resource tags</span></span>

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

### <span data-ttu-id="7f823-139">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="7f823-139">-UsageThreshold</span></span>
<span data-ttu-id="7f823-140">檔案系統允許的儲存配額上限（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="7f823-140">The maximum storage quota allowed for a file system in bytes</span></span>

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

### <span data-ttu-id="7f823-141">-確認</span><span class="sxs-lookup"><span data-stu-id="7f823-141">-Confirm</span></span>
<span data-ttu-id="7f823-142">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7f823-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f823-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f823-143">-WhatIf</span></span>
<span data-ttu-id="7f823-144">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7f823-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f823-145">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7f823-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f823-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f823-146">CommonParameters</span></span>
<span data-ttu-id="7f823-147">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7f823-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f823-148">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="7f823-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f823-149">輸入</span><span class="sxs-lookup"><span data-stu-id="7f823-149">INPUTS</span></span>

### <span data-ttu-id="7f823-150">System.object</span><span class="sxs-lookup"><span data-stu-id="7f823-150">System.String</span></span>

### <span data-ttu-id="7f823-151">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="7f823-151">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="7f823-152">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="7f823-152">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7f823-153">輸出</span><span class="sxs-lookup"><span data-stu-id="7f823-153">OUTPUTS</span></span>

### <span data-ttu-id="7f823-154">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="7f823-154">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="7f823-155">筆記</span><span class="sxs-lookup"><span data-stu-id="7f823-155">NOTES</span></span>

## <span data-ttu-id="7f823-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="7f823-156">RELATED LINKS</span></span>