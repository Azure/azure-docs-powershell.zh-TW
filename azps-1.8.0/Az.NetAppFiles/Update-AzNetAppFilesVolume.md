---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/en-us/powershell/module/az.netappfiles/update-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Update-AzNetAppFilesVolume.md
ms.openlocfilehash: ea943c490a87dd4c62752b97753971f0941ed3b9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622204"
---
# <span data-ttu-id="6e490-101">Update-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="6e490-101">Update-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="6e490-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6e490-102">SYNOPSIS</span></span>
<span data-ttu-id="6e490-103">根據提供的選擇性修飾符，更新 (ANF) 盤案的 Azure NetApp 檔案。</span><span class="sxs-lookup"><span data-stu-id="6e490-103">Updates an Azure NetApp Files (ANF) volume according to the optional modifiers provided.</span></span>

## <span data-ttu-id="6e490-104">句法</span><span class="sxs-lookup"><span data-stu-id="6e490-104">SYNTAX</span></span>

### <span data-ttu-id="6e490-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="6e490-105">ByFieldsParameterSet (Default)</span></span>
```
Update-AzNetAppFilesVolume -ResourceGroupName <String> -Location <String> -AccountName <String>
 -PoolName <String> -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e490-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e490-106">ByParentObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume -Name <String> [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -PoolObject <PSNetAppFilesPool> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6e490-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6e490-107">ByObjectParameterSet</span></span>
```
Update-AzNetAppFilesVolume [-UsageThreshold <Int64>] [-ServiceLevel <String>] [-Tag <Hashtable>]
 -InputObject <PSNetAppFilesVolume> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6e490-108">說明</span><span class="sxs-lookup"><span data-stu-id="6e490-108">DESCRIPTION</span></span>
<span data-ttu-id="6e490-109">**更新-AzNetAppFilesVolume** Cmdlet 會更新 ANF 的音量。</span><span class="sxs-lookup"><span data-stu-id="6e490-109">The **Update-AzNetAppFilesVolume** cmdlet updates an ANF volume.</span></span>

## <span data-ttu-id="6e490-110">示例</span><span class="sxs-lookup"><span data-stu-id="6e490-110">EXAMPLES</span></span>

### <span data-ttu-id="6e490-111">範例1：更新 ANF 的音量</span><span class="sxs-lookup"><span data-stu-id="6e490-111">Example 1: Update an ANF volume</span></span>
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

<span data-ttu-id="6e490-112">這個命令會使用新的 UsageThreshold 大小來更新 ANF volume "MyAnfVolume"。</span><span class="sxs-lookup"><span data-stu-id="6e490-112">This command updates the ANF volume "MyAnfVolume" with the new UsageThreshold size.</span></span>

## <span data-ttu-id="6e490-113">參數</span><span class="sxs-lookup"><span data-stu-id="6e490-113">PARAMETERS</span></span>

### <span data-ttu-id="6e490-114">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6e490-114">-AccountName</span></span>
<span data-ttu-id="6e490-115">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="6e490-115">The name of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e490-116">-DefaultProfile</span></span>
<span data-ttu-id="6e490-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="6e490-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e490-118">-InputObject</span></span>
<span data-ttu-id="6e490-119">要更新的卷物件</span><span class="sxs-lookup"><span data-stu-id="6e490-119">The volume object to update</span></span>

```yaml
Type: PSNetAppFilesVolume
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-120">-位置</span><span class="sxs-lookup"><span data-stu-id="6e490-120">-Location</span></span>
<span data-ttu-id="6e490-121">資源的位置</span><span class="sxs-lookup"><span data-stu-id="6e490-121">The location of the resource</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e490-122">-Name</span></span>
<span data-ttu-id="6e490-123">ANF 體積的名稱</span><span class="sxs-lookup"><span data-stu-id="6e490-123">The name of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet, ByParentObjectParameterSet
Aliases: VolumeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-124">-PoolName</span><span class="sxs-lookup"><span data-stu-id="6e490-124">-PoolName</span></span>
<span data-ttu-id="6e490-125">ANF 池的名稱</span><span class="sxs-lookup"><span data-stu-id="6e490-125">The name of the ANF pool</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-126">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="6e490-126">-PoolObject</span></span>
<span data-ttu-id="6e490-127">包含要更新之卷的 pool 物件</span><span class="sxs-lookup"><span data-stu-id="6e490-127">The pool object containing the volume to update</span></span>

```yaml
Type: PSNetAppFilesPool
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e490-128">-ResourceGroupName</span></span>
<span data-ttu-id="6e490-129">ANF 帳戶的 [資源] 群組</span><span class="sxs-lookup"><span data-stu-id="6e490-129">The resource group of the ANF account</span></span>

```yaml
Type: String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-130">-ServiceLevel</span><span class="sxs-lookup"><span data-stu-id="6e490-130">-ServiceLevel</span></span>
<span data-ttu-id="6e490-131">ANF 容量的服務層級</span><span class="sxs-lookup"><span data-stu-id="6e490-131">The service level of the ANF volume</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="6e490-132">-Tag</span></span>
<span data-ttu-id="6e490-133">代表資源標記的 hashtable</span><span class="sxs-lookup"><span data-stu-id="6e490-133">A hashtable which represents resource tags</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-134">-UsageThreshold</span><span class="sxs-lookup"><span data-stu-id="6e490-134">-UsageThreshold</span></span>
<span data-ttu-id="6e490-135">檔案系統允許的儲存配額上限（以位元組為單位）</span><span class="sxs-lookup"><span data-stu-id="6e490-135">The maximum storage quota allowed for a file system in bytes</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-136">-確認</span><span class="sxs-lookup"><span data-stu-id="6e490-136">-Confirm</span></span>
<span data-ttu-id="6e490-137">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6e490-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e490-138">-WhatIf</span></span>
<span data-ttu-id="6e490-139">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e490-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e490-140">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e490-140">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e490-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e490-141">CommonParameters</span></span>
<span data-ttu-id="6e490-142">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6e490-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6e490-143">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6e490-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e490-144">輸入</span><span class="sxs-lookup"><span data-stu-id="6e490-144">INPUTS</span></span>

### <span data-ttu-id="6e490-145">PSNetAppFilesPool 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="6e490-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="6e490-146">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="6e490-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6e490-147">輸出</span><span class="sxs-lookup"><span data-stu-id="6e490-147">OUTPUTS</span></span>

### <span data-ttu-id="6e490-148">PSNetAppFilesVolume 中的 NetAppFiles。</span><span class="sxs-lookup"><span data-stu-id="6e490-148">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="6e490-149">筆記</span><span class="sxs-lookup"><span data-stu-id="6e490-149">NOTES</span></span>

## <span data-ttu-id="6e490-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e490-150">RELATED LINKS</span></span>
