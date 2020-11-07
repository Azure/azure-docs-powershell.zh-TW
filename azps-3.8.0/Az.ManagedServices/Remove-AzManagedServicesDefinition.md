---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: ffebb4e3fca417c896939bb54ed1c0af1c42f7fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797141"
---
# <span data-ttu-id="037c4-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="037c4-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="037c4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="037c4-102">SYNOPSIS</span></span>
<span data-ttu-id="037c4-103">刪除註冊定義。</span><span class="sxs-lookup"><span data-stu-id="037c4-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="037c4-104">句法</span><span class="sxs-lookup"><span data-stu-id="037c4-104">SYNTAX</span></span>

### <span data-ttu-id="037c4-105">預設 (預設) </span><span class="sxs-lookup"><span data-stu-id="037c4-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition -Id <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="037c4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="037c4-106">ByResourceId</span></span>
```
Remove-AzManagedServicesDefinition -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="037c4-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="037c4-107">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="037c4-108">說明</span><span class="sxs-lookup"><span data-stu-id="037c4-108">DESCRIPTION</span></span>
<span data-ttu-id="037c4-109">刪除註冊定義。</span><span class="sxs-lookup"><span data-stu-id="037c4-109">Deletes the registration definition.</span></span>

## <span data-ttu-id="037c4-110">示例</span><span class="sxs-lookup"><span data-stu-id="037c4-110">EXAMPLES</span></span>

### <span data-ttu-id="037c4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="037c4-111">Example 1</span></span>
```powershell
PS C:\> Remove-RegistrationDefinition -Id 0513b566-cab0-4fef-9b53-a285cd33389f
```

<span data-ttu-id="037c4-112">移除已知其識別碼的註冊定義。</span><span class="sxs-lookup"><span data-stu-id="037c4-112">Removes the registration definition given it identifier.</span></span>

### <span data-ttu-id="037c4-113">範例2</span><span class="sxs-lookup"><span data-stu-id="037c4-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesDefinition -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/11b7c937-c5c1-4dd1-9a77-204591f93fcd

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
11b7c937-c5c1-4dd1-9a77-204591f93fcd bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="037c4-114">在已知完全限定的資源識別碼的情況下，移除註冊定義。</span><span class="sxs-lookup"><span data-stu-id="037c4-114">Removes the registration definition given the fully qualified resource id.</span></span> 

### <span data-ttu-id="037c4-115">範例3</span><span class="sxs-lookup"><span data-stu-id="037c4-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName 572e1807-b80b-4401-9128-1968f432a5ad -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> Remove-AzManagedServicesDefinition -InputObject $def

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
eee59839-119f-453f-adec-4a72a8687125 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="037c4-116">刪除指定物件的註冊定義。</span><span class="sxs-lookup"><span data-stu-id="037c4-116">Deletes the registration definition given the object.</span></span>

## <span data-ttu-id="037c4-117">參數</span><span class="sxs-lookup"><span data-stu-id="037c4-117">PARAMETERS</span></span>

### <span data-ttu-id="037c4-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="037c4-118">-AsJob</span></span>
<span data-ttu-id="037c4-119">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="037c4-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="037c4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="037c4-120">-DefaultProfile</span></span>
<span data-ttu-id="037c4-121">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="037c4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="037c4-122">-識別碼</span><span class="sxs-lookup"><span data-stu-id="037c4-122">-Id</span></span>
<span data-ttu-id="037c4-123">[註冊定義識別碼]。</span><span class="sxs-lookup"><span data-stu-id="037c4-123">The registration definition identifier.</span></span>

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

### <span data-ttu-id="037c4-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="037c4-124">-InputObject</span></span>
<span data-ttu-id="037c4-125">[註冊定義物件]。</span><span class="sxs-lookup"><span data-stu-id="037c4-125">The registration definition object.</span></span>

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

### <span data-ttu-id="037c4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="037c4-126">-ResourceId</span></span>
<span data-ttu-id="037c4-127">登記定義的 ResourceId</span><span class="sxs-lookup"><span data-stu-id="037c4-127">ResourceId of the registration definition</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="037c4-128">-確認</span><span class="sxs-lookup"><span data-stu-id="037c4-128">-Confirm</span></span>
<span data-ttu-id="037c4-129">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="037c4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="037c4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="037c4-130">-WhatIf</span></span>
<span data-ttu-id="037c4-131">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="037c4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="037c4-132">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="037c4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="037c4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="037c4-133">CommonParameters</span></span>
<span data-ttu-id="037c4-134">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="037c4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="037c4-135">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="037c4-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="037c4-136">輸入</span><span class="sxs-lookup"><span data-stu-id="037c4-136">INPUTS</span></span>

### <span data-ttu-id="037c4-137">所有</span><span class="sxs-lookup"><span data-stu-id="037c4-137">None</span></span>

## <span data-ttu-id="037c4-138">輸出</span><span class="sxs-lookup"><span data-stu-id="037c4-138">OUTPUTS</span></span>

### <span data-ttu-id="037c4-139">PSRegistrationDefinition （ManagedServices）的</span><span class="sxs-lookup"><span data-stu-id="037c4-139">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="037c4-140">筆記</span><span class="sxs-lookup"><span data-stu-id="037c4-140">NOTES</span></span>

## <span data-ttu-id="037c4-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="037c4-141">RELATED LINKS</span></span>
