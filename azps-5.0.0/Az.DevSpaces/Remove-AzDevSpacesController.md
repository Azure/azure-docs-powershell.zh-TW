---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94137009"
---
# <span data-ttu-id="febd1-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="febd1-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="febd1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="febd1-102">SYNOPSIS</span></span>
<span data-ttu-id="febd1-103">刪除 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="febd1-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="febd1-104">句法</span><span class="sxs-lookup"><span data-stu-id="febd1-104">SYNTAX</span></span>

### <span data-ttu-id="febd1-105">DevSpacesControllerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="febd1-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="febd1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="febd1-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="febd1-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="febd1-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="febd1-108">說明</span><span class="sxs-lookup"><span data-stu-id="febd1-108">DESCRIPTION</span></span>
<span data-ttu-id="febd1-109">刪除 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="febd1-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="febd1-110">示例</span><span class="sxs-lookup"><span data-stu-id="febd1-110">EXAMPLES</span></span>

### <span data-ttu-id="febd1-111">範例1</span><span class="sxs-lookup"><span data-stu-id="febd1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="febd1-112">刪除一個名為 devSpaceControllerName 的 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="febd1-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="febd1-113">參數</span><span class="sxs-lookup"><span data-stu-id="febd1-113">PARAMETERS</span></span>

### <span data-ttu-id="febd1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="febd1-114">-AsJob</span></span>
<span data-ttu-id="febd1-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="febd1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="febd1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="febd1-116">-DefaultProfile</span></span>
<span data-ttu-id="febd1-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="febd1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="febd1-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="febd1-118">-InputObject</span></span>
<span data-ttu-id="febd1-119">PSController 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="febd1-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="febd1-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="febd1-120">-Name</span></span>
<span data-ttu-id="febd1-121">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="febd1-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="febd1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="febd1-122">-PassThru</span></span>
<span data-ttu-id="febd1-123">如果刪除成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="febd1-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="febd1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="febd1-124">-ResourceGroupName</span></span>
<span data-ttu-id="febd1-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="febd1-125">Resource group name</span></span>

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

### <span data-ttu-id="febd1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="febd1-126">-ResourceId</span></span>
<span data-ttu-id="febd1-127">DevSpaces 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="febd1-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="febd1-128">-確認</span><span class="sxs-lookup"><span data-stu-id="febd1-128">-Confirm</span></span>
<span data-ttu-id="febd1-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="febd1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="febd1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="febd1-130">-WhatIf</span></span>
<span data-ttu-id="febd1-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="febd1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="febd1-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="febd1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="febd1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="febd1-133">CommonParameters</span></span>
<span data-ttu-id="febd1-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="febd1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="febd1-135">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="febd1-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="febd1-136">輸入</span><span class="sxs-lookup"><span data-stu-id="febd1-136">INPUTS</span></span>

### <span data-ttu-id="febd1-137">System.object</span><span class="sxs-lookup"><span data-stu-id="febd1-137">System.String</span></span>

### <span data-ttu-id="febd1-138">PSController 中的 DevSpaces。</span><span class="sxs-lookup"><span data-stu-id="febd1-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="febd1-139">輸出</span><span class="sxs-lookup"><span data-stu-id="febd1-139">OUTPUTS</span></span>

### <span data-ttu-id="febd1-140">System.object</span><span class="sxs-lookup"><span data-stu-id="febd1-140">System.Boolean</span></span>

## <span data-ttu-id="febd1-141">筆記</span><span class="sxs-lookup"><span data-stu-id="febd1-141">NOTES</span></span>

## <span data-ttu-id="febd1-142">相關連結</span><span class="sxs-lookup"><span data-stu-id="febd1-142">RELATED LINKS</span></span>