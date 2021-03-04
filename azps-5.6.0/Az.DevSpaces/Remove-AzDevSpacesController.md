---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: fa535876524961dc8e7a05ca3acc5fa007f759fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906226"
---
# <span data-ttu-id="94334-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="94334-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="94334-102">簡介</span><span class="sxs-lookup"><span data-stu-id="94334-102">SYNOPSIS</span></span>
<span data-ttu-id="94334-103">刪除 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="94334-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="94334-104">語法</span><span class="sxs-lookup"><span data-stu-id="94334-104">SYNTAX</span></span>

### <span data-ttu-id="94334-105">DevSpacesControllerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="94334-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94334-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="94334-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94334-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="94334-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="94334-108">描述</span><span class="sxs-lookup"><span data-stu-id="94334-108">DESCRIPTION</span></span>
<span data-ttu-id="94334-109">刪除 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="94334-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="94334-110">例子</span><span class="sxs-lookup"><span data-stu-id="94334-110">EXAMPLES</span></span>

### <span data-ttu-id="94334-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="94334-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="94334-112">刪除 DevSpaces 控制器，名稱為 devSpaceControllerName。</span><span class="sxs-lookup"><span data-stu-id="94334-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="94334-113">參數</span><span class="sxs-lookup"><span data-stu-id="94334-113">PARAMETERS</span></span>

### <span data-ttu-id="94334-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="94334-114">-AsJob</span></span>
<span data-ttu-id="94334-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="94334-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="94334-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94334-116">-DefaultProfile</span></span>
<span data-ttu-id="94334-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="94334-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94334-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94334-118">-InputObject</span></span>
<span data-ttu-id="94334-119">PSController 物件，通常會通過管線。</span><span class="sxs-lookup"><span data-stu-id="94334-119">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="94334-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="94334-120">-Name</span></span>
<span data-ttu-id="94334-121">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="94334-121">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94334-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="94334-122">-PassThru</span></span>
<span data-ttu-id="94334-123">如果刪除成功，則返回 True</span><span class="sxs-lookup"><span data-stu-id="94334-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="94334-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94334-124">-ResourceGroupName</span></span>
<span data-ttu-id="94334-125">資源組名</span><span class="sxs-lookup"><span data-stu-id="94334-125">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="94334-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94334-126">-ResourceId</span></span>
<span data-ttu-id="94334-127">DevSpaces 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="94334-127">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94334-128">-確認</span><span class="sxs-lookup"><span data-stu-id="94334-128">-Confirm</span></span>
<span data-ttu-id="94334-129">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="94334-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94334-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94334-130">-WhatIf</span></span>
<span data-ttu-id="94334-131">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="94334-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="94334-132">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="94334-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94334-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94334-133">CommonParameters</span></span>
<span data-ttu-id="94334-134">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="94334-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94334-135">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="94334-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94334-136">輸入</span><span class="sxs-lookup"><span data-stu-id="94334-136">INPUTS</span></span>

### <span data-ttu-id="94334-137">System.String</span><span class="sxs-lookup"><span data-stu-id="94334-137">System.String</span></span>

### <span data-ttu-id="94334-138">Microsoft.Azure.Commands.DevSpaces.models.PSController</span><span class="sxs-lookup"><span data-stu-id="94334-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="94334-139">輸出</span><span class="sxs-lookup"><span data-stu-id="94334-139">OUTPUTS</span></span>

### <span data-ttu-id="94334-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="94334-140">System.Boolean</span></span>

## <span data-ttu-id="94334-141">筆記</span><span class="sxs-lookup"><span data-stu-id="94334-141">NOTES</span></span>

## <span data-ttu-id="94334-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="94334-142">RELATED LINKS</span></span>
