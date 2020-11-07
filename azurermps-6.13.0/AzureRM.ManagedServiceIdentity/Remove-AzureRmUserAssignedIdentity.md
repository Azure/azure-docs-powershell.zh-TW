---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 03d73ac28bc1869452ecc96b5c867fcbb8c372c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625805"
---
# <span data-ttu-id="a738d-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a738d-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="a738d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="a738d-102">SYNOPSIS</span></span>
<span data-ttu-id="a738d-103">移除指派身分識別的使用者。</span><span class="sxs-lookup"><span data-stu-id="a738d-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a738d-104">句法</span><span class="sxs-lookup"><span data-stu-id="a738d-104">SYNTAX</span></span>

### <span data-ttu-id="a738d-105">ResourceGroupAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="a738d-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a738d-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a738d-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a738d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a738d-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a738d-108">說明</span><span class="sxs-lookup"><span data-stu-id="a738d-108">DESCRIPTION</span></span>
<span data-ttu-id="a738d-109">[ **移除-AzureRmUserAssignedIdentity** ] 會刪除指定的使用者指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="a738d-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="a738d-110">示例</span><span class="sxs-lookup"><span data-stu-id="a738d-110">EXAMPLES</span></span>

### <span data-ttu-id="a738d-111">範例1</span><span class="sxs-lookup"><span data-stu-id="a738d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="a738d-112">這個範例 Cmdlet 會刪除 [資源群組 **PSRG** ] 下的 [身分識別 **ID1** ]。</span><span class="sxs-lookup"><span data-stu-id="a738d-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="a738d-113">滿足</span><span class="sxs-lookup"><span data-stu-id="a738d-113">True</span></span>

## <span data-ttu-id="a738d-114">參數</span><span class="sxs-lookup"><span data-stu-id="a738d-114">PARAMETERS</span></span>

### <span data-ttu-id="a738d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a738d-115">-AsJob</span></span>
<span data-ttu-id="a738d-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="a738d-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a738d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a738d-117">-DefaultProfile</span></span>
<span data-ttu-id="a738d-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="a738d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a738d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a738d-119">-Force</span></span>
<span data-ttu-id="a738d-120">{{Fill Force 描述}}</span><span class="sxs-lookup"><span data-stu-id="a738d-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="a738d-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a738d-121">-InputObject</span></span>
<span data-ttu-id="a738d-122">身分識別物件。</span><span class="sxs-lookup"><span data-stu-id="a738d-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a738d-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="a738d-123">-Name</span></span>
<span data-ttu-id="a738d-124">身分識別名稱。</span><span class="sxs-lookup"><span data-stu-id="a738d-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a738d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a738d-125">-ResourceGroupName</span></span>
<span data-ttu-id="a738d-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="a738d-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a738d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a738d-127">-ResourceId</span></span>
<span data-ttu-id="a738d-128">身分識別的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="a738d-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="a738d-129">-確認</span><span class="sxs-lookup"><span data-stu-id="a738d-129">-Confirm</span></span>
<span data-ttu-id="a738d-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="a738d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a738d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a738d-131">-WhatIf</span></span>
<span data-ttu-id="a738d-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="a738d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a738d-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="a738d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a738d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a738d-134">CommonParameters</span></span>
<span data-ttu-id="a738d-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="a738d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a738d-136">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="a738d-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a738d-137">輸入</span><span class="sxs-lookup"><span data-stu-id="a738d-137">INPUTS</span></span>

### <span data-ttu-id="a738d-138">PsUserAssignedIdentity 中的 ManagedServiceIdentity。</span><span class="sxs-lookup"><span data-stu-id="a738d-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>
<span data-ttu-id="a738d-139">參數： InputObject (ByValue) </span><span class="sxs-lookup"><span data-stu-id="a738d-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="a738d-140">System.object</span><span class="sxs-lookup"><span data-stu-id="a738d-140">System.String</span></span>

## <span data-ttu-id="a738d-141">輸出</span><span class="sxs-lookup"><span data-stu-id="a738d-141">OUTPUTS</span></span>

### <span data-ttu-id="a738d-142">System.object</span><span class="sxs-lookup"><span data-stu-id="a738d-142">System.Boolean</span></span>

## <span data-ttu-id="a738d-143">筆記</span><span class="sxs-lookup"><span data-stu-id="a738d-143">NOTES</span></span>

## <span data-ttu-id="a738d-144">相關連結</span><span class="sxs-lookup"><span data-stu-id="a738d-144">RELATED LINKS</span></span>
