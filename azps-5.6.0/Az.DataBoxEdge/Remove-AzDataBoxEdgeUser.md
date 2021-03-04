---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 8c977c61f332ccdc927dd3f0e070d635e6095acf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909733"
---
# <span data-ttu-id="8a1b8-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8a1b8-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="8a1b8-102">簡介</span><span class="sxs-lookup"><span data-stu-id="8a1b8-102">SYNOPSIS</span></span>
<span data-ttu-id="8a1b8-103">移除裝置上的使用者。</span><span class="sxs-lookup"><span data-stu-id="8a1b8-103">Removes a user on a device.</span></span>

## <span data-ttu-id="8a1b8-104">語法</span><span class="sxs-lookup"><span data-stu-id="8a1b8-104">SYNTAX</span></span>

### <span data-ttu-id="8a1b8-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="8a1b8-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a1b8-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a1b8-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a1b8-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8a1b8-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a1b8-108">描述</span><span class="sxs-lookup"><span data-stu-id="8a1b8-108">DESCRIPTION</span></span>
<span data-ttu-id="8a1b8-109">**Remove-AzDataBoxEdgeUser** Cmdlet 會移除 Data Box Edge 裝置上的使用者。</span><span class="sxs-lookup"><span data-stu-id="8a1b8-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="8a1b8-110">僅支援建立類型 `Share` 使用者。</span><span class="sxs-lookup"><span data-stu-id="8a1b8-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="8a1b8-111">例子</span><span class="sxs-lookup"><span data-stu-id="8a1b8-111">EXAMPLES</span></span>

### <span data-ttu-id="8a1b8-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="8a1b8-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="8a1b8-113">參數</span><span class="sxs-lookup"><span data-stu-id="8a1b8-113">PARAMETERS</span></span>

### <span data-ttu-id="8a1b8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a1b8-114">-AsJob</span></span>
<span data-ttu-id="8a1b8-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="8a1b8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8a1b8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a1b8-116">-DefaultProfile</span></span>
<span data-ttu-id="8a1b8-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="8a1b8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a1b8-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8a1b8-118">-DeviceName</span></span>
<span data-ttu-id="8a1b8-119">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="8a1b8-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1b8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a1b8-120">-InputObject</span></span>
<span data-ttu-id="8a1b8-121">輸入物件</span><span class="sxs-lookup"><span data-stu-id="8a1b8-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a1b8-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="8a1b8-122">-Name</span></span>
<span data-ttu-id="8a1b8-123">使用者</span><span class="sxs-lookup"><span data-stu-id="8a1b8-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1b8-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8a1b8-124">-PassThru</span></span>
<span data-ttu-id="8a1b8-125">如果成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="8a1b8-125">returns true if successful</span></span>

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

### <span data-ttu-id="8a1b8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a1b8-126">-ResourceGroupName</span></span>
<span data-ttu-id="8a1b8-127">資源組名</span><span class="sxs-lookup"><span data-stu-id="8a1b8-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a1b8-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a1b8-128">-ResourceId</span></span>
<span data-ttu-id="8a1b8-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8a1b8-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a1b8-130">-確認</span><span class="sxs-lookup"><span data-stu-id="8a1b8-130">-Confirm</span></span>
<span data-ttu-id="8a1b8-131">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="8a1b8-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a1b8-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a1b8-132">-WhatIf</span></span>
<span data-ttu-id="8a1b8-133">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="8a1b8-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a1b8-134">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="8a1b8-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a1b8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a1b8-135">CommonParameters</span></span>
<span data-ttu-id="8a1b8-136">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="8a1b8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a1b8-137">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a1b8-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a1b8-138">輸入</span><span class="sxs-lookup"><span data-stu-id="8a1b8-138">INPUTS</span></span>

### <span data-ttu-id="8a1b8-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8a1b8-139">System.String</span></span>

### <span data-ttu-id="8a1b8-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="8a1b8-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="8a1b8-141">輸出</span><span class="sxs-lookup"><span data-stu-id="8a1b8-141">OUTPUTS</span></span>

### <span data-ttu-id="8a1b8-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="8a1b8-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="8a1b8-143">筆記</span><span class="sxs-lookup"><span data-stu-id="8a1b8-143">NOTES</span></span>

## <span data-ttu-id="8a1b8-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="8a1b8-144">RELATED LINKS</span></span>
