---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 7220304c4dbc234a3513d2dfc35e6d71180159e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101915226"
---
# <span data-ttu-id="162f9-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="162f9-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="162f9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="162f9-102">SYNOPSIS</span></span>
<span data-ttu-id="162f9-103">刪除 JIT 網路存取策略。</span><span class="sxs-lookup"><span data-stu-id="162f9-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="162f9-104">語法</span><span class="sxs-lookup"><span data-stu-id="162f9-104">SYNTAX</span></span>

### <span data-ttu-id="162f9-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="162f9-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="162f9-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="162f9-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="162f9-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="162f9-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="162f9-108">描述</span><span class="sxs-lookup"><span data-stu-id="162f9-108">DESCRIPTION</span></span>
<span data-ttu-id="162f9-109">刪除即時網路存取策略。</span><span class="sxs-lookup"><span data-stu-id="162f9-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="162f9-110">執行此動作之後，使用者將無法要求在已刪除之策略內所配置的虛擬機器上建立暫時網路連接。</span><span class="sxs-lookup"><span data-stu-id="162f9-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="162f9-111">例子</span><span class="sxs-lookup"><span data-stu-id="162f9-111">EXAMPLES</span></span>

### <span data-ttu-id="162f9-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="162f9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="162f9-113">刪除即時網路存取策略。</span><span class="sxs-lookup"><span data-stu-id="162f9-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="162f9-114">參數</span><span class="sxs-lookup"><span data-stu-id="162f9-114">PARAMETERS</span></span>

### <span data-ttu-id="162f9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="162f9-115">-DefaultProfile</span></span>
<span data-ttu-id="162f9-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="162f9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="162f9-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="162f9-117">-InputObject</span></span>
<span data-ttu-id="162f9-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="162f9-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="162f9-119">-位置</span><span class="sxs-lookup"><span data-stu-id="162f9-119">-Location</span></span>
<span data-ttu-id="162f9-120">位置。</span><span class="sxs-lookup"><span data-stu-id="162f9-120">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162f9-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="162f9-121">-Name</span></span>
<span data-ttu-id="162f9-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="162f9-122">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162f9-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="162f9-123">-PassThru</span></span>
<span data-ttu-id="162f9-124">返回作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="162f9-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="162f9-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="162f9-125">-ResourceGroupName</span></span>
<span data-ttu-id="162f9-126">資源組名。</span><span class="sxs-lookup"><span data-stu-id="162f9-126">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupLevelResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="162f9-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="162f9-127">-ResourceId</span></span>
<span data-ttu-id="162f9-128">jit Network Access Policy 資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="162f9-128">The resource id of the jit Network Access Policy resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="162f9-129">-確認</span><span class="sxs-lookup"><span data-stu-id="162f9-129">-Confirm</span></span>
<span data-ttu-id="162f9-130">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="162f9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="162f9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="162f9-131">-WhatIf</span></span>
<span data-ttu-id="162f9-132">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="162f9-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="162f9-133">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="162f9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="162f9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162f9-134">CommonParameters</span></span>
<span data-ttu-id="162f9-135">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="162f9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162f9-136">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="162f9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162f9-137">輸入</span><span class="sxs-lookup"><span data-stu-id="162f9-137">INPUTS</span></span>

### <span data-ttu-id="162f9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="162f9-138">System.String</span></span>

### <span data-ttu-id="162f9-139">Microsoft.Azure.Commands.Security.models.JitNetworkAccesssPolicies.PSSecurityJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="162f9-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="162f9-140">輸出</span><span class="sxs-lookup"><span data-stu-id="162f9-140">OUTPUTS</span></span>

### <span data-ttu-id="162f9-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="162f9-141">System.Boolean</span></span>

## <span data-ttu-id="162f9-142">筆記</span><span class="sxs-lookup"><span data-stu-id="162f9-142">NOTES</span></span>

## <span data-ttu-id="162f9-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="162f9-143">RELATED LINKS</span></span>
