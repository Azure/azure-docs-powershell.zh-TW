---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: ccf76449bf2f7e904cbfe6e2507e067df7661dae
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93622880"
---
# <span data-ttu-id="52ed8-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="52ed8-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="52ed8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="52ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="52ed8-103">從訂閱中移除藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="52ed8-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="52ed8-104">句法</span><span class="sxs-lookup"><span data-stu-id="52ed8-104">SYNTAX</span></span>

### <span data-ttu-id="52ed8-105">DeleteBlueprintAssignmentByName (預設) </span><span class="sxs-lookup"><span data-stu-id="52ed8-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52ed8-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="52ed8-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52ed8-107">說明</span><span class="sxs-lookup"><span data-stu-id="52ed8-107">DESCRIPTION</span></span>
<span data-ttu-id="52ed8-108">移除已指派給訂閱的藍圖。</span><span class="sxs-lookup"><span data-stu-id="52ed8-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="52ed8-109">示例</span><span class="sxs-lookup"><span data-stu-id="52ed8-109">EXAMPLES</span></span>

### <span data-ttu-id="52ed8-110">範例1</span><span class="sxs-lookup"><span data-stu-id="52ed8-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="52ed8-111">從指定的訂閱中移除名稱指定的藍圖作業。</span><span class="sxs-lookup"><span data-stu-id="52ed8-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="52ed8-112">在執行命令前，Cmdlet 會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52ed8-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="52ed8-113">參數</span><span class="sxs-lookup"><span data-stu-id="52ed8-113">PARAMETERS</span></span>

### <span data-ttu-id="52ed8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52ed8-114">-DefaultProfile</span></span>
<span data-ttu-id="52ed8-115">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="52ed8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52ed8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="52ed8-116">-InputObject</span></span>
<span data-ttu-id="52ed8-117">藍圖指派物件。</span><span class="sxs-lookup"><span data-stu-id="52ed8-117">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52ed8-118">-名稱</span><span class="sxs-lookup"><span data-stu-id="52ed8-118">-Name</span></span>
<span data-ttu-id="52ed8-119">藍圖作業名稱。</span><span class="sxs-lookup"><span data-stu-id="52ed8-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ed8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52ed8-120">-PassThru</span></span>
<span data-ttu-id="52ed8-121">{{Fill PassThru 描述}}</span><span class="sxs-lookup"><span data-stu-id="52ed8-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="52ed8-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="52ed8-122">-SubscriptionId</span></span>
<span data-ttu-id="52ed8-123">已部署藍圖指派的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="52ed8-123">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52ed8-124">-確認</span><span class="sxs-lookup"><span data-stu-id="52ed8-124">-Confirm</span></span>
<span data-ttu-id="52ed8-125">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="52ed8-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ed8-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ed8-126">-WhatIf</span></span>
<span data-ttu-id="52ed8-127">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="52ed8-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52ed8-128">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="52ed8-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ed8-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ed8-129">CommonParameters</span></span>
<span data-ttu-id="52ed8-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="52ed8-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ed8-131">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="52ed8-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ed8-132">輸入</span><span class="sxs-lookup"><span data-stu-id="52ed8-132">INPUTS</span></span>

### <span data-ttu-id="52ed8-133">System.object</span><span class="sxs-lookup"><span data-stu-id="52ed8-133">System.String</span></span>

### <span data-ttu-id="52ed8-134">PSBlueprintAssignment [] （[]）</span><span class="sxs-lookup"><span data-stu-id="52ed8-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="52ed8-135">輸出</span><span class="sxs-lookup"><span data-stu-id="52ed8-135">OUTPUTS</span></span>

### <span data-ttu-id="52ed8-136">System.object</span><span class="sxs-lookup"><span data-stu-id="52ed8-136">System.Object</span></span>
## <span data-ttu-id="52ed8-137">筆記</span><span class="sxs-lookup"><span data-stu-id="52ed8-137">NOTES</span></span>

## <span data-ttu-id="52ed8-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="52ed8-138">RELATED LINKS</span></span>
