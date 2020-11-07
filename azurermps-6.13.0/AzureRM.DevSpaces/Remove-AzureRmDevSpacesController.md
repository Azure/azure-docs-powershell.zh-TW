---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/remove-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
ms.openlocfilehash: e242ba95330ac102fbfbcecf6f28326adb29a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625581"
---
# <span data-ttu-id="38f70-101">Remove-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="38f70-101">Remove-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="38f70-102">摘要</span><span class="sxs-lookup"><span data-stu-id="38f70-102">SYNOPSIS</span></span>
<span data-ttu-id="38f70-103">刪除 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="38f70-103">Delete a DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38f70-104">句法</span><span class="sxs-lookup"><span data-stu-id="38f70-104">SYNTAX</span></span>

### <span data-ttu-id="38f70-105">DevSpacesControllerNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="38f70-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38f70-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38f70-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38f70-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38f70-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38f70-108">說明</span><span class="sxs-lookup"><span data-stu-id="38f70-108">DESCRIPTION</span></span>
<span data-ttu-id="38f70-109">刪除 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="38f70-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="38f70-110">示例</span><span class="sxs-lookup"><span data-stu-id="38f70-110">EXAMPLES</span></span>

### <span data-ttu-id="38f70-111">範例1</span><span class="sxs-lookup"><span data-stu-id="38f70-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="38f70-112">刪除一個名為 devSpaceControllerName 的 DevSpaces 控制器。</span><span class="sxs-lookup"><span data-stu-id="38f70-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="38f70-113">參數</span><span class="sxs-lookup"><span data-stu-id="38f70-113">PARAMETERS</span></span>

### <span data-ttu-id="38f70-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38f70-114">-AsJob</span></span>
<span data-ttu-id="38f70-115">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="38f70-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="38f70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f70-116">-DefaultProfile</span></span>
<span data-ttu-id="38f70-117">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="38f70-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38f70-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38f70-118">-InputObject</span></span>
<span data-ttu-id="38f70-119">PSController 物件，通常是透過管線傳遞。</span><span class="sxs-lookup"><span data-stu-id="38f70-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="38f70-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="38f70-120">-Name</span></span>
<span data-ttu-id="38f70-121">DevSpaces 控制器名稱。</span><span class="sxs-lookup"><span data-stu-id="38f70-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="38f70-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38f70-122">-PassThru</span></span>
<span data-ttu-id="38f70-123">如果刪除成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="38f70-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="38f70-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38f70-124">-ResourceGroupName</span></span>
<span data-ttu-id="38f70-125">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="38f70-125">Resource group name</span></span>

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

### <span data-ttu-id="38f70-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38f70-126">-ResourceId</span></span>
<span data-ttu-id="38f70-127">DevSpaces 資源識別碼</span><span class="sxs-lookup"><span data-stu-id="38f70-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="38f70-128">-確認</span><span class="sxs-lookup"><span data-stu-id="38f70-128">-Confirm</span></span>
<span data-ttu-id="38f70-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="38f70-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38f70-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38f70-130">-WhatIf</span></span>
<span data-ttu-id="38f70-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="38f70-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38f70-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="38f70-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38f70-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f70-133">CommonParameters</span></span>
<span data-ttu-id="38f70-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="38f70-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f70-135">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="38f70-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f70-136">輸入</span><span class="sxs-lookup"><span data-stu-id="38f70-136">INPUTS</span></span>

### <span data-ttu-id="38f70-137">System.object</span><span class="sxs-lookup"><span data-stu-id="38f70-137">System.String</span></span>

### <span data-ttu-id="38f70-138">PSController 中的 DevSpaces。</span><span class="sxs-lookup"><span data-stu-id="38f70-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="38f70-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="38f70-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="38f70-140">輸出</span><span class="sxs-lookup"><span data-stu-id="38f70-140">OUTPUTS</span></span>

### <span data-ttu-id="38f70-141">System.object</span><span class="sxs-lookup"><span data-stu-id="38f70-141">System.Boolean</span></span>

## <span data-ttu-id="38f70-142">筆記</span><span class="sxs-lookup"><span data-stu-id="38f70-142">NOTES</span></span>

## <span data-ttu-id="38f70-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="38f70-143">RELATED LINKS</span></span>
