---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilessnapshot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesSnapshot.md
ms.openlocfilehash: 340adf5b3114750212ad1e2458159f48a9dae91f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905993"
---
# <span data-ttu-id="d6f50-101">Remove-AzNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="d6f50-101">Remove-AzNetAppFilesSnapshot</span></span>

## <span data-ttu-id="d6f50-102">簡介</span><span class="sxs-lookup"><span data-stu-id="d6f50-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f50-103">刪除 ANF 快照 (Azure NetApp) 檔案。</span><span class="sxs-lookup"><span data-stu-id="d6f50-103">Deletes an Azure NetApp Files (ANF) snapshot.</span></span>

## <span data-ttu-id="d6f50-104">語法</span><span class="sxs-lookup"><span data-stu-id="d6f50-104">SYNTAX</span></span>

### <span data-ttu-id="d6f50-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="d6f50-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceGroupName <String> -AccountName <String> -PoolName <String>
 -VolumeName <String> -Name <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f50-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6f50-106">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f50-107">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6f50-107">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -VolumeObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d6f50-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d6f50-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesSnapshot -InputObject <PSNetAppFilesSnapshot> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d6f50-109">描述</span><span class="sxs-lookup"><span data-stu-id="d6f50-109">DESCRIPTION</span></span>
<span data-ttu-id="d6f50-110">**Remove-AzNetAppFilesSnapshot** Cmdlet 會刪除 ANF 快照。</span><span class="sxs-lookup"><span data-stu-id="d6f50-110">The **Remove-AzNetAppFilesSnapshot** cmdlet deletes an ANF snapshot.</span></span>

## <span data-ttu-id="d6f50-111">例子</span><span class="sxs-lookup"><span data-stu-id="d6f50-111">EXAMPLES</span></span>

### <span data-ttu-id="d6f50-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="d6f50-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesSnapshot -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -VolumeName "MyAnfVolume" -Name "MyAnfSnapshot"
```

<span data-ttu-id="d6f50-113">此命令會刪除 ANF 快照「MyAnfSnapshot」。</span><span class="sxs-lookup"><span data-stu-id="d6f50-113">This command deletes the ANF snapshot "MyAnfSnapshot".</span></span>

## <span data-ttu-id="d6f50-114">參數</span><span class="sxs-lookup"><span data-stu-id="d6f50-114">PARAMETERS</span></span>

### <span data-ttu-id="d6f50-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="d6f50-115">-AccountName</span></span>
<span data-ttu-id="d6f50-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="d6f50-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="d6f50-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f50-117">-DefaultProfile</span></span>
<span data-ttu-id="d6f50-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="d6f50-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6f50-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6f50-119">-InputObject</span></span>
<span data-ttu-id="d6f50-120">要移除的快照物件</span><span class="sxs-lookup"><span data-stu-id="d6f50-120">The snapshot object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f50-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="d6f50-121">-Name</span></span>
<span data-ttu-id="d6f50-122">ANF 快照的名稱</span><span class="sxs-lookup"><span data-stu-id="d6f50-122">The name of the ANF snapshot</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: SnapshotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f50-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d6f50-123">-PassThru</span></span>
<span data-ttu-id="d6f50-124">返回指定的音量是否已成功移除</span><span class="sxs-lookup"><span data-stu-id="d6f50-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="d6f50-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="d6f50-125">-PoolName</span></span>
<span data-ttu-id="d6f50-126">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="d6f50-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="d6f50-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f50-127">-ResourceGroupName</span></span>
<span data-ttu-id="d6f50-128">ANF 快照的資源群組</span><span class="sxs-lookup"><span data-stu-id="d6f50-128">The resource group of the ANF snapshot</span></span>

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

### <span data-ttu-id="d6f50-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f50-129">-ResourceId</span></span>
<span data-ttu-id="d6f50-130">ANF 快照的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="d6f50-130">The resource id of the ANF snapshot</span></span>

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

### <span data-ttu-id="d6f50-131">-VolumeName</span><span class="sxs-lookup"><span data-stu-id="d6f50-131">-VolumeName</span></span>
<span data-ttu-id="d6f50-132">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="d6f50-132">The name of the ANF volume</span></span>

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

### <span data-ttu-id="d6f50-133">-VolumeObject</span><span class="sxs-lookup"><span data-stu-id="d6f50-133">-VolumeObject</span></span>
<span data-ttu-id="d6f50-134">包含要移除之快照的卷積物件</span><span class="sxs-lookup"><span data-stu-id="d6f50-134">The volume object containing the snapshot to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume
Parameter Sets: ByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f50-135">-確認</span><span class="sxs-lookup"><span data-stu-id="d6f50-135">-Confirm</span></span>
<span data-ttu-id="d6f50-136">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="d6f50-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d6f50-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6f50-137">-WhatIf</span></span>
<span data-ttu-id="d6f50-138">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d6f50-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6f50-139">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d6f50-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d6f50-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f50-140">CommonParameters</span></span>
<span data-ttu-id="d6f50-141">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="d6f50-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f50-142">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6f50-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f50-143">輸入</span><span class="sxs-lookup"><span data-stu-id="d6f50-143">INPUTS</span></span>

### <span data-ttu-id="d6f50-144">System.String</span><span class="sxs-lookup"><span data-stu-id="d6f50-144">System.String</span></span>

### <span data-ttu-id="d6f50-145">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="d6f50-145">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

### <span data-ttu-id="d6f50-146">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesSnapshot</span><span class="sxs-lookup"><span data-stu-id="d6f50-146">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesSnapshot</span></span>

## <span data-ttu-id="d6f50-147">輸出</span><span class="sxs-lookup"><span data-stu-id="d6f50-147">OUTPUTS</span></span>

### <span data-ttu-id="d6f50-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d6f50-148">System.Boolean</span></span>

## <span data-ttu-id="d6f50-149">筆記</span><span class="sxs-lookup"><span data-stu-id="d6f50-149">NOTES</span></span>

## <span data-ttu-id="d6f50-150">相關連結</span><span class="sxs-lookup"><span data-stu-id="d6f50-150">RELATED LINKS</span></span>
