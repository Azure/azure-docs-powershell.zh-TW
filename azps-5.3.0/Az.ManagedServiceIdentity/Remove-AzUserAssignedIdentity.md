---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 4e133ef82e61d34e4e2915a37cc3f0e0d1e61382
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98436486"
---
# <span data-ttu-id="85495-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="85495-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="85495-102">摘要</span><span class="sxs-lookup"><span data-stu-id="85495-102">SYNOPSIS</span></span>
<span data-ttu-id="85495-103">移除指派身分識別的使用者。</span><span class="sxs-lookup"><span data-stu-id="85495-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="85495-104">句法</span><span class="sxs-lookup"><span data-stu-id="85495-104">SYNTAX</span></span>

### <span data-ttu-id="85495-105">ResourceGroupAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="85495-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85495-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85495-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85495-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85495-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85495-108">說明</span><span class="sxs-lookup"><span data-stu-id="85495-108">DESCRIPTION</span></span>
<span data-ttu-id="85495-109">[ **移除-AzUserAssignedIdentity** ] 會刪除指定的使用者指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="85495-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="85495-110">示例</span><span class="sxs-lookup"><span data-stu-id="85495-110">EXAMPLES</span></span>

### <span data-ttu-id="85495-111">範例1</span><span class="sxs-lookup"><span data-stu-id="85495-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="85495-112">這個範例 Cmdlet 會刪除 [資源群組 **PSRG**] 下的 [身分識別 **ID1** ]。</span><span class="sxs-lookup"><span data-stu-id="85495-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="85495-113">滿足</span><span class="sxs-lookup"><span data-stu-id="85495-113">True</span></span>

## <span data-ttu-id="85495-114">參數</span><span class="sxs-lookup"><span data-stu-id="85495-114">PARAMETERS</span></span>

### <span data-ttu-id="85495-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85495-115">-AsJob</span></span>
<span data-ttu-id="85495-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="85495-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85495-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85495-117">-DefaultProfile</span></span>
<span data-ttu-id="85495-118">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="85495-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85495-119">-Force</span><span class="sxs-lookup"><span data-stu-id="85495-119">-Force</span></span>
<span data-ttu-id="85495-120">{{Fill Force 描述}}</span><span class="sxs-lookup"><span data-stu-id="85495-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="85495-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85495-121">-InputObject</span></span>
<span data-ttu-id="85495-122">身分識別物件。</span><span class="sxs-lookup"><span data-stu-id="85495-122">The Identity object.</span></span>

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

### <span data-ttu-id="85495-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="85495-123">-Name</span></span>
<span data-ttu-id="85495-124">身分識別名稱。</span><span class="sxs-lookup"><span data-stu-id="85495-124">The Identity name.</span></span>

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

### <span data-ttu-id="85495-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85495-125">-ResourceGroupName</span></span>
<span data-ttu-id="85495-126">資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="85495-126">The resource group name.</span></span>

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

### <span data-ttu-id="85495-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85495-127">-ResourceId</span></span>
<span data-ttu-id="85495-128">身分識別的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="85495-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="85495-129">-確認</span><span class="sxs-lookup"><span data-stu-id="85495-129">-Confirm</span></span>
<span data-ttu-id="85495-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="85495-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85495-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85495-131">-WhatIf</span></span>
<span data-ttu-id="85495-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="85495-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85495-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="85495-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85495-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85495-134">CommonParameters</span></span>
<span data-ttu-id="85495-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="85495-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85495-136">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="85495-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85495-137">輸入</span><span class="sxs-lookup"><span data-stu-id="85495-137">INPUTS</span></span>

### <span data-ttu-id="85495-138">PsUserAssignedIdentity 中的 ManagedServiceIdentity。</span><span class="sxs-lookup"><span data-stu-id="85495-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="85495-139">System.object</span><span class="sxs-lookup"><span data-stu-id="85495-139">System.String</span></span>

## <span data-ttu-id="85495-140">輸出</span><span class="sxs-lookup"><span data-stu-id="85495-140">OUTPUTS</span></span>

### <span data-ttu-id="85495-141">System.object</span><span class="sxs-lookup"><span data-stu-id="85495-141">System.Boolean</span></span>

## <span data-ttu-id="85495-142">筆記</span><span class="sxs-lookup"><span data-stu-id="85495-142">NOTES</span></span>

## <span data-ttu-id="85495-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="85495-143">RELATED LINKS</span></span>
