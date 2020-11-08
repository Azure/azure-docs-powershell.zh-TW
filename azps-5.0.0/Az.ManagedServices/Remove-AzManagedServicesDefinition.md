---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 2b81a1983bb89af48115ead85c3392cc3d762734
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94138778"
---
# <span data-ttu-id="56d9c-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="56d9c-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="56d9c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="56d9c-102">SYNOPSIS</span></span>
<span data-ttu-id="56d9c-103">刪除註冊定義。</span><span class="sxs-lookup"><span data-stu-id="56d9c-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="56d9c-104">句法</span><span class="sxs-lookup"><span data-stu-id="56d9c-104">SYNTAX</span></span>

### <span data-ttu-id="56d9c-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="56d9c-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="56d9c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="56d9c-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d9c-107">說明</span><span class="sxs-lookup"><span data-stu-id="56d9c-107">DESCRIPTION</span></span>
<span data-ttu-id="56d9c-108">刪除註冊定義。</span><span class="sxs-lookup"><span data-stu-id="56d9c-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="56d9c-109">示例</span><span class="sxs-lookup"><span data-stu-id="56d9c-109">EXAMPLES</span></span>

### <span data-ttu-id="56d9c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="56d9c-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="56d9c-111">在預設範圍中，以名稱移除註冊定義。</span><span class="sxs-lookup"><span data-stu-id="56d9c-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="56d9c-112">範例2</span><span class="sxs-lookup"><span data-stu-id="56d9c-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="56d9c-113">刪除已知輸入物件的註冊定義。</span><span class="sxs-lookup"><span data-stu-id="56d9c-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="56d9c-114">參數</span><span class="sxs-lookup"><span data-stu-id="56d9c-114">PARAMETERS</span></span>

### <span data-ttu-id="56d9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d9c-115">-DefaultProfile</span></span>
<span data-ttu-id="56d9c-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="56d9c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56d9c-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56d9c-117">-InputObject</span></span>
<span data-ttu-id="56d9c-118">[註冊定義物件]。</span><span class="sxs-lookup"><span data-stu-id="56d9c-118">The registration definition object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="56d9c-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="56d9c-119">-Name</span></span>
<span data-ttu-id="56d9c-120">註冊定義的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="56d9c-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d9c-121">-範圍</span><span class="sxs-lookup"><span data-stu-id="56d9c-121">-Scope</span></span>
<span data-ttu-id="56d9c-122">已建立註冊定義的範圍。</span><span class="sxs-lookup"><span data-stu-id="56d9c-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d9c-123">-確認</span><span class="sxs-lookup"><span data-stu-id="56d9c-123">-Confirm</span></span>
<span data-ttu-id="56d9c-124">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="56d9c-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d9c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d9c-125">-WhatIf</span></span>
<span data-ttu-id="56d9c-126">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="56d9c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56d9c-127">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="56d9c-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56d9c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d9c-128">CommonParameters</span></span>
<span data-ttu-id="56d9c-129">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="56d9c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d9c-130">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="56d9c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d9c-131">輸入</span><span class="sxs-lookup"><span data-stu-id="56d9c-131">INPUTS</span></span>

### <span data-ttu-id="56d9c-132">PSRegistrationDefinition （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="56d9c-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="56d9c-133">輸出</span><span class="sxs-lookup"><span data-stu-id="56d9c-133">OUTPUTS</span></span>

### <span data-ttu-id="56d9c-134">System.void</span><span class="sxs-lookup"><span data-stu-id="56d9c-134">System.Void</span></span>
## <span data-ttu-id="56d9c-135">筆記</span><span class="sxs-lookup"><span data-stu-id="56d9c-135">NOTES</span></span>

## <span data-ttu-id="56d9c-136">相關連結</span><span class="sxs-lookup"><span data-stu-id="56d9c-136">RELATED LINKS</span></span>
