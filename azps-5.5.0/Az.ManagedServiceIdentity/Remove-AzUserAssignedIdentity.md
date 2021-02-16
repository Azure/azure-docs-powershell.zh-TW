---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100132763"
---
# <span data-ttu-id="93e66-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="93e66-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="93e66-102">摘要</span><span class="sxs-lookup"><span data-stu-id="93e66-102">SYNOPSIS</span></span>
<span data-ttu-id="93e66-103">移除指派身分識別的使用者。</span><span class="sxs-lookup"><span data-stu-id="93e66-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="93e66-104">句法</span><span class="sxs-lookup"><span data-stu-id="93e66-104">SYNTAX</span></span>

### <span data-ttu-id="93e66-105">ResourceGroupAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="93e66-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e66-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93e66-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93e66-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93e66-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93e66-108">說明</span><span class="sxs-lookup"><span data-stu-id="93e66-108">DESCRIPTION</span></span>
<span data-ttu-id="93e66-109">[ **移除-AzUserAssignedIdentity** ] 會刪除指定的使用者指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="93e66-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="93e66-110">示例</span><span class="sxs-lookup"><span data-stu-id="93e66-110">EXAMPLES</span></span>

### <span data-ttu-id="93e66-111">範例1</span><span class="sxs-lookup"><span data-stu-id="93e66-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="93e66-112">這個範例 Cmdlet 會刪除 [資源群組 **PSRG**] 下的 [身分識別 **ID1** ]。</span><span class="sxs-lookup"><span data-stu-id="93e66-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="93e66-113">滿足</span><span class="sxs-lookup"><span data-stu-id="93e66-113">True</span></span>

## <span data-ttu-id="93e66-114">參數</span><span class="sxs-lookup"><span data-stu-id="93e66-114">PARAMETERS</span></span>

### <span data-ttu-id="93e66-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93e66-115">-AsJob</span></span>
<span data-ttu-id="93e66-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="93e66-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93e66-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e66-117">-DefaultProfile</span></span>
<span data-ttu-id="93e66-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="93e66-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93e66-119">-Force</span><span class="sxs-lookup"><span data-stu-id="93e66-119">-Force</span></span>
<span data-ttu-id="93e66-120">{{Fill Force 描述}}</span><span class="sxs-lookup"><span data-stu-id="93e66-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="93e66-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93e66-121">-InputObject</span></span>
<span data-ttu-id="93e66-122">身分識別物件。</span><span class="sxs-lookup"><span data-stu-id="93e66-122">The Identity object.</span></span>

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

### <span data-ttu-id="93e66-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="93e66-123">-Name</span></span>
<span data-ttu-id="93e66-124">身分識別名稱。</span><span class="sxs-lookup"><span data-stu-id="93e66-124">The Identity name.</span></span>

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

### <span data-ttu-id="93e66-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e66-125">-ResourceGroupName</span></span>
<span data-ttu-id="93e66-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="93e66-126">The resource group name.</span></span>

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

### <span data-ttu-id="93e66-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="93e66-127">-ResourceId</span></span>
<span data-ttu-id="93e66-128">身分識別的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="93e66-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="93e66-129">-確認</span><span class="sxs-lookup"><span data-stu-id="93e66-129">-Confirm</span></span>
<span data-ttu-id="93e66-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="93e66-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93e66-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93e66-131">-WhatIf</span></span>
<span data-ttu-id="93e66-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="93e66-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93e66-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="93e66-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93e66-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e66-134">CommonParameters</span></span>
<span data-ttu-id="93e66-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="93e66-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e66-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="93e66-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e66-137">輸入</span><span class="sxs-lookup"><span data-stu-id="93e66-137">INPUTS</span></span>

### <span data-ttu-id="93e66-138">PsUserAssignedIdentity 中的 ManagedServiceIdentity。</span><span class="sxs-lookup"><span data-stu-id="93e66-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="93e66-139">System.object</span><span class="sxs-lookup"><span data-stu-id="93e66-139">System.String</span></span>

## <span data-ttu-id="93e66-140">輸出</span><span class="sxs-lookup"><span data-stu-id="93e66-140">OUTPUTS</span></span>

### <span data-ttu-id="93e66-141">System.object</span><span class="sxs-lookup"><span data-stu-id="93e66-141">System.Boolean</span></span>

## <span data-ttu-id="93e66-142">筆記</span><span class="sxs-lookup"><span data-stu-id="93e66-142">NOTES</span></span>

## <span data-ttu-id="93e66-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="93e66-143">RELATED LINKS</span></span>
