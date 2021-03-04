---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: b6354a88f7363d1dfff72f6513f17be0f144f97c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908638"
---
# <span data-ttu-id="c879b-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="c879b-101">New-AzBlueprint</span></span>

## <span data-ttu-id="c879b-102">簡介</span><span class="sxs-lookup"><span data-stu-id="c879b-102">SYNOPSIS</span></span>
<span data-ttu-id="c879b-103">建立新藍圖定義，並將其儲存在指定的訂閱或管理群組中。</span><span class="sxs-lookup"><span data-stu-id="c879b-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="c879b-104">語法</span><span class="sxs-lookup"><span data-stu-id="c879b-104">SYNTAX</span></span>

### <span data-ttu-id="c879b-105">CreateBlueprintBySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="c879b-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c879b-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c879b-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c879b-107">描述</span><span class="sxs-lookup"><span data-stu-id="c879b-107">DESCRIPTION</span></span>
<span data-ttu-id="c879b-108">建立新藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="c879b-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="c879b-109">例子</span><span class="sxs-lookup"><span data-stu-id="c879b-109">EXAMPLES</span></span>

### <span data-ttu-id="c879b-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="c879b-110">Example 1</span></span>
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="c879b-111">在指定的訂閱中建立新藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="c879b-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="c879b-112">參數</span><span class="sxs-lookup"><span data-stu-id="c879b-112">PARAMETERS</span></span>

### <span data-ttu-id="c879b-113">-藍圖檔</span><span class="sxs-lookup"><span data-stu-id="c879b-113">-BlueprintFile</span></span>
<span data-ttu-id="c879b-114">藍圖 JSON 檔案在磁片上的路徑。</span><span class="sxs-lookup"><span data-stu-id="c879b-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c879b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c879b-115">-DefaultProfile</span></span>
<span data-ttu-id="c879b-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="c879b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c879b-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="c879b-117">-ManagementGroupId</span></span>
<span data-ttu-id="c879b-118">儲存藍圖定義的管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="c879b-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c879b-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="c879b-119">-Name</span></span>
<span data-ttu-id="c879b-120">藍圖定義名稱。</span><span class="sxs-lookup"><span data-stu-id="c879b-120">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c879b-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c879b-121">-SubscriptionId</span></span>
<span data-ttu-id="c879b-122">已儲存或將會儲存藍圖定義的訂閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="c879b-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c879b-123">-確認</span><span class="sxs-lookup"><span data-stu-id="c879b-123">-Confirm</span></span>
<span data-ttu-id="c879b-124">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="c879b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c879b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c879b-125">-WhatIf</span></span>
<span data-ttu-id="c879b-126">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="c879b-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c879b-127">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="c879b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c879b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c879b-128">CommonParameters</span></span>
<span data-ttu-id="c879b-129">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="c879b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c879b-130">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c879b-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c879b-131">輸入</span><span class="sxs-lookup"><span data-stu-id="c879b-131">INPUTS</span></span>

### <span data-ttu-id="c879b-132">System.String</span><span class="sxs-lookup"><span data-stu-id="c879b-132">System.String</span></span>

## <span data-ttu-id="c879b-133">輸出</span><span class="sxs-lookup"><span data-stu-id="c879b-133">OUTPUTS</span></span>

### <span data-ttu-id="c879b-134">Microsoft.Azure.Commands.藍圖.models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="c879b-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="c879b-135">筆記</span><span class="sxs-lookup"><span data-stu-id="c879b-135">NOTES</span></span>

## <span data-ttu-id="c879b-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="c879b-136">RELATED LINKS</span></span>
