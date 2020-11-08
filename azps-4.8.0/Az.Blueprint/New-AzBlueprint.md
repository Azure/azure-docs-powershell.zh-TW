---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 790a74ef5a296dbc90e9c1db16678b8c1bacf071
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969924"
---
# <span data-ttu-id="ff4c3-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="ff4c3-101">New-AzBlueprint</span></span>

## <span data-ttu-id="ff4c3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ff4c3-102">SYNOPSIS</span></span>
<span data-ttu-id="ff4c3-103">建立新的藍圖定義，並將它儲存在指定的訂閱或管理群組中。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="ff4c3-104">句法</span><span class="sxs-lookup"><span data-stu-id="ff4c3-104">SYNTAX</span></span>

### <span data-ttu-id="ff4c3-105">CreateBlueprintBySubscription (預設) </span><span class="sxs-lookup"><span data-stu-id="ff4c3-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff4c3-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="ff4c3-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff4c3-107">說明</span><span class="sxs-lookup"><span data-stu-id="ff4c3-107">DESCRIPTION</span></span>
<span data-ttu-id="ff4c3-108">建立新的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="ff4c3-109">示例</span><span class="sxs-lookup"><span data-stu-id="ff4c3-109">EXAMPLES</span></span>

### <span data-ttu-id="ff4c3-110">範例1</span><span class="sxs-lookup"><span data-stu-id="ff4c3-110">Example 1</span></span>
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

<span data-ttu-id="ff4c3-111">在指定的訂閱中建立新的藍圖定義。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="ff4c3-112">參數</span><span class="sxs-lookup"><span data-stu-id="ff4c3-112">PARAMETERS</span></span>

### <span data-ttu-id="ff4c3-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="ff4c3-113">-BlueprintFile</span></span>
<span data-ttu-id="ff4c3-114">磁片上藍圖 JSON 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="ff4c3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff4c3-115">-DefaultProfile</span></span>
<span data-ttu-id="ff4c3-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff4c3-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ff4c3-117">-ManagementGroupId</span></span>
<span data-ttu-id="ff4c3-118">已儲存藍圖定義或將要儲存的管理群組識別碼。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="ff4c3-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="ff4c3-119">-Name</span></span>
<span data-ttu-id="ff4c3-120">藍圖定義名稱。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="ff4c3-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ff4c3-121">-SubscriptionId</span></span>
<span data-ttu-id="ff4c3-122">藍圖定義或將要儲存的訂閱 Id。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="ff4c3-123">-確認</span><span class="sxs-lookup"><span data-stu-id="ff4c3-123">-Confirm</span></span>
<span data-ttu-id="ff4c3-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff4c3-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff4c3-125">-WhatIf</span></span>
<span data-ttu-id="ff4c3-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff4c3-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff4c3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff4c3-128">CommonParameters</span></span>
<span data-ttu-id="ff4c3-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff4c3-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="ff4c3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff4c3-131">輸入</span><span class="sxs-lookup"><span data-stu-id="ff4c3-131">INPUTS</span></span>

### <span data-ttu-id="ff4c3-132">System.object</span><span class="sxs-lookup"><span data-stu-id="ff4c3-132">System.String</span></span>

## <span data-ttu-id="ff4c3-133">輸出</span><span class="sxs-lookup"><span data-stu-id="ff4c3-133">OUTPUTS</span></span>

### <span data-ttu-id="ff4c3-134">PSBlueprint 中的 [.]</span><span class="sxs-lookup"><span data-stu-id="ff4c3-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="ff4c3-135">筆記</span><span class="sxs-lookup"><span data-stu-id="ff4c3-135">NOTES</span></span>

## <span data-ttu-id="ff4c3-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="ff4c3-136">RELATED LINKS</span></span>