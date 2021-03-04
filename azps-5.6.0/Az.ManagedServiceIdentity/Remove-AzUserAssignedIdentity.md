---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 83280df19363285ab23ca1e27441a491a783b03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904650"
---
# <span data-ttu-id="f6221-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f6221-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="f6221-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f6221-102">SYNOPSIS</span></span>
<span data-ttu-id="f6221-103">移除使用者指派的身分識別。</span><span class="sxs-lookup"><span data-stu-id="f6221-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="f6221-104">語法</span><span class="sxs-lookup"><span data-stu-id="f6221-104">SYNTAX</span></span>

### <span data-ttu-id="f6221-105">ResourceGroupAndNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="f6221-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6221-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6221-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6221-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6221-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6221-108">描述</span><span class="sxs-lookup"><span data-stu-id="f6221-108">DESCRIPTION</span></span>
<span data-ttu-id="f6221-109">**Remove-AzUserAssignedIdentity 會** 刪除指定的使用者指派身分識別。</span><span class="sxs-lookup"><span data-stu-id="f6221-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="f6221-110">例子</span><span class="sxs-lookup"><span data-stu-id="f6221-110">EXAMPLES</span></span>

### <span data-ttu-id="f6221-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="f6221-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="f6221-112">此範例 Cmdlet 會刪除資源群組 PSRG **下的身分\*\*\*\*識別識別碼1。**</span><span class="sxs-lookup"><span data-stu-id="f6221-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="f6221-113">真</span><span class="sxs-lookup"><span data-stu-id="f6221-113">True</span></span>

## <span data-ttu-id="f6221-114">參數</span><span class="sxs-lookup"><span data-stu-id="f6221-114">PARAMETERS</span></span>

### <span data-ttu-id="f6221-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6221-115">-AsJob</span></span>
<span data-ttu-id="f6221-116">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="f6221-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6221-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6221-117">-DefaultProfile</span></span>
<span data-ttu-id="f6221-118">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f6221-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6221-119">-強制</span><span class="sxs-lookup"><span data-stu-id="f6221-119">-Force</span></span>
<span data-ttu-id="f6221-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="f6221-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="f6221-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6221-121">-InputObject</span></span>
<span data-ttu-id="f6221-122">身分識別物件。</span><span class="sxs-lookup"><span data-stu-id="f6221-122">The Identity object.</span></span>

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

### <span data-ttu-id="f6221-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="f6221-123">-Name</span></span>
<span data-ttu-id="f6221-124">身分識別名稱。</span><span class="sxs-lookup"><span data-stu-id="f6221-124">The Identity name.</span></span>

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

### <span data-ttu-id="f6221-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6221-125">-ResourceGroupName</span></span>
<span data-ttu-id="f6221-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f6221-126">The resource group name.</span></span>

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

### <span data-ttu-id="f6221-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6221-127">-ResourceId</span></span>
<span data-ttu-id="f6221-128">身分識別的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6221-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="f6221-129">-確認</span><span class="sxs-lookup"><span data-stu-id="f6221-129">-Confirm</span></span>
<span data-ttu-id="f6221-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f6221-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6221-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6221-131">-WhatIf</span></span>
<span data-ttu-id="f6221-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f6221-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6221-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f6221-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6221-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6221-134">CommonParameters</span></span>
<span data-ttu-id="f6221-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f6221-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6221-136">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="f6221-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6221-137">輸入</span><span class="sxs-lookup"><span data-stu-id="f6221-137">INPUTS</span></span>

### <span data-ttu-id="f6221-138">Microsoft.Azure.Commands.ManagedServiceIdentity.models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f6221-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="f6221-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f6221-139">System.String</span></span>

## <span data-ttu-id="f6221-140">輸出</span><span class="sxs-lookup"><span data-stu-id="f6221-140">OUTPUTS</span></span>

### <span data-ttu-id="f6221-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f6221-141">System.Boolean</span></span>

## <span data-ttu-id="f6221-142">筆記</span><span class="sxs-lookup"><span data-stu-id="f6221-142">NOTES</span></span>

## <span data-ttu-id="f6221-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="f6221-143">RELATED LINKS</span></span>
