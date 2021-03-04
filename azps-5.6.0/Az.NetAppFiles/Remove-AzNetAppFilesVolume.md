---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NetAppFiles.dll-Help.xml
Module Name: Az.NetAppFiles
online version: https://docs.microsoft.com/powershell/module/az.netappfiles/remove-aznetappfilesvolume
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NetAppFiles/NetAppFiles/help/Remove-AzNetAppFilesVolume.md
ms.openlocfilehash: f53ca76da23620a37020a14877059aae4f4c9808
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905989"
---
# <span data-ttu-id="9b08e-101">Remove-AzNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9b08e-101">Remove-AzNetAppFilesVolume</span></span>

## <span data-ttu-id="9b08e-102">簡介</span><span class="sxs-lookup"><span data-stu-id="9b08e-102">SYNOPSIS</span></span>
<span data-ttu-id="9b08e-103">刪除 ANF 卷 (的 Azure NetApp) 檔案。</span><span class="sxs-lookup"><span data-stu-id="9b08e-103">Deletes an Azure NetApp Files (ANF) volume.</span></span>

## <span data-ttu-id="9b08e-104">語法</span><span class="sxs-lookup"><span data-stu-id="9b08e-104">SYNTAX</span></span>

### <span data-ttu-id="9b08e-105">ByFieldsParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="9b08e-105">ByFieldsParameterSet (Default)</span></span>
```
Remove-AzNetAppFilesVolume -ResourceGroupName <String> -AccountName <String> -PoolName <String> -Name <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b08e-106">ByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b08e-106">ByParentObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -Name <String> -PoolObject <PSNetAppFilesPool> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b08e-107">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b08e-107">ByResourceIdParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b08e-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9b08e-108">ByObjectParameterSet</span></span>
```
Remove-AzNetAppFilesVolume -InputObject <PSNetAppFilesVolume> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b08e-109">描述</span><span class="sxs-lookup"><span data-stu-id="9b08e-109">DESCRIPTION</span></span>
<span data-ttu-id="9b08e-110">**Remove-AzNetAppFilesVolume** Cmdlet 會刪除 ANF 音量。</span><span class="sxs-lookup"><span data-stu-id="9b08e-110">The **Remove-AzNetAppFilesVolume** cmdlet deletes an ANF volume.</span></span>

## <span data-ttu-id="9b08e-111">例子</span><span class="sxs-lookup"><span data-stu-id="9b08e-111">EXAMPLES</span></span>

### <span data-ttu-id="9b08e-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="9b08e-112">Example 1</span></span>
```
PS C:\>Remove-AzNetAppFilesVolume -ResourceGroupName "MyRG" -AccountName "MyAnfAccount" -PoolName "MyAnfPool" -Name "MyAnfVolume"
```

<span data-ttu-id="9b08e-113">此命令會刪除 ANF 音量 「MyAnfVolume」。</span><span class="sxs-lookup"><span data-stu-id="9b08e-113">This command deletes the ANF volume "MyAnfVolume".</span></span>

## <span data-ttu-id="9b08e-114">參數</span><span class="sxs-lookup"><span data-stu-id="9b08e-114">PARAMETERS</span></span>

### <span data-ttu-id="9b08e-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="9b08e-115">-AccountName</span></span>
<span data-ttu-id="9b08e-116">ANF 帳戶的名稱</span><span class="sxs-lookup"><span data-stu-id="9b08e-116">The name of the ANF account</span></span>

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

### <span data-ttu-id="9b08e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b08e-117">-DefaultProfile</span></span>
<span data-ttu-id="9b08e-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b08e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b08e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b08e-119">-InputObject</span></span>
<span data-ttu-id="9b08e-120">要移除的音量物件</span><span class="sxs-lookup"><span data-stu-id="9b08e-120">The volume object to remove</span></span>

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

### <span data-ttu-id="9b08e-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b08e-121">-Name</span></span>
<span data-ttu-id="9b08e-122">ANF 音量的名稱</span><span class="sxs-lookup"><span data-stu-id="9b08e-122">The name of the ANF volume</span></span>

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

### <span data-ttu-id="9b08e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b08e-123">-PassThru</span></span>
<span data-ttu-id="9b08e-124">返回指定的音量是否已成功移除</span><span class="sxs-lookup"><span data-stu-id="9b08e-124">Return whether the specified volume was successfully removed</span></span>

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

### <span data-ttu-id="9b08e-125">-PoolName</span><span class="sxs-lookup"><span data-stu-id="9b08e-125">-PoolName</span></span>
<span data-ttu-id="9b08e-126">ANF 組名</span><span class="sxs-lookup"><span data-stu-id="9b08e-126">The name of the ANF pool</span></span>

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

### <span data-ttu-id="9b08e-127">-PoolObject</span><span class="sxs-lookup"><span data-stu-id="9b08e-127">-PoolObject</span></span>
<span data-ttu-id="9b08e-128">包含要移除之卷的集中物件</span><span class="sxs-lookup"><span data-stu-id="9b08e-128">The pool object containing the volume to remove</span></span>

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

### <span data-ttu-id="9b08e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b08e-129">-ResourceGroupName</span></span>
<span data-ttu-id="9b08e-130">ANF 音量的資源群組</span><span class="sxs-lookup"><span data-stu-id="9b08e-130">The resource group of the ANF volume</span></span>

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

### <span data-ttu-id="9b08e-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b08e-131">-ResourceId</span></span>
<span data-ttu-id="9b08e-132">ANF 音量的資源識別碼</span><span class="sxs-lookup"><span data-stu-id="9b08e-132">The resource id of the ANF volume</span></span>

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

### <span data-ttu-id="9b08e-133">-確認</span><span class="sxs-lookup"><span data-stu-id="9b08e-133">-Confirm</span></span>
<span data-ttu-id="9b08e-134">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="9b08e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b08e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b08e-135">-WhatIf</span></span>
<span data-ttu-id="9b08e-136">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b08e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b08e-137">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b08e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b08e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b08e-138">CommonParameters</span></span>
<span data-ttu-id="9b08e-139">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="9b08e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b08e-140">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9b08e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b08e-141">輸入</span><span class="sxs-lookup"><span data-stu-id="9b08e-141">INPUTS</span></span>

### <span data-ttu-id="9b08e-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9b08e-142">System.String</span></span>

### <span data-ttu-id="9b08e-143">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesPool</span><span class="sxs-lookup"><span data-stu-id="9b08e-143">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesPool</span></span>

### <span data-ttu-id="9b08e-144">Microsoft.Azure.Commands.NetAppFiles.models.PSNetAppFilesVolume</span><span class="sxs-lookup"><span data-stu-id="9b08e-144">Microsoft.Azure.Commands.NetAppFiles.Models.PSNetAppFilesVolume</span></span>

## <span data-ttu-id="9b08e-145">輸出</span><span class="sxs-lookup"><span data-stu-id="9b08e-145">OUTPUTS</span></span>

### <span data-ttu-id="9b08e-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9b08e-146">System.Boolean</span></span>

## <span data-ttu-id="9b08e-147">筆記</span><span class="sxs-lookup"><span data-stu-id="9b08e-147">NOTES</span></span>

## <span data-ttu-id="9b08e-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b08e-148">RELATED LINKS</span></span>
