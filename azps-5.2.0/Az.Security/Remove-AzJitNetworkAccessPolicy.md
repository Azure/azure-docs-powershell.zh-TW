---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzJitNetworkAccessPolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzJitNetworkAccessPolicy.md
ms.openlocfilehash: 484fa890f672435d0add2ba7b30325d03dab91f8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/08/2020
ms.locfileid: "98277659"
---
# <span data-ttu-id="9e018-101">Remove-AzJitNetworkAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9e018-101">Remove-AzJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="9e018-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9e018-102">SYNOPSIS</span></span>
<span data-ttu-id="9e018-103">刪除 JIT 網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="9e018-103">Deletes a JIT network access policy.</span></span>

## <span data-ttu-id="9e018-104">句法</span><span class="sxs-lookup"><span data-stu-id="9e018-104">SYNTAX</span></span>

### <span data-ttu-id="9e018-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="9e018-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceGroupName <String> -Location <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e018-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e018-106">ResourceId</span></span>
```
Remove-AzJitNetworkAccessPolicy -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e018-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9e018-107">InputObject</span></span>
```
Remove-AzJitNetworkAccessPolicy -InputObject <PSSecurityJitNetworkAccessPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e018-108">說明</span><span class="sxs-lookup"><span data-stu-id="9e018-108">DESCRIPTION</span></span>
<span data-ttu-id="9e018-109">刪除即時網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="9e018-109">Deletes a Just In Time network access policy.</span></span>
<span data-ttu-id="9e018-110">在此動作之後，使用者將無法在已刪除原則內設定的 Vm 上要求暫時的網路連線。</span><span class="sxs-lookup"><span data-stu-id="9e018-110">After this action a user will not be able to request temporary network connection on the VMs that were configured inside the deleted policy.</span></span>

## <span data-ttu-id="9e018-111">示例</span><span class="sxs-lookup"><span data-stu-id="9e018-111">EXAMPLES</span></span>

### <span data-ttu-id="9e018-112">範例1</span><span class="sxs-lookup"><span data-stu-id="9e018-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzJitNetworkAccessPolicy -ResourceGroupName "myService1" -Location "centralus" -Name "default"
```

<span data-ttu-id="9e018-113">刪除即時網路存取原則。</span><span class="sxs-lookup"><span data-stu-id="9e018-113">Deletes a Just In Time network access policy.</span></span>

## <span data-ttu-id="9e018-114">參數</span><span class="sxs-lookup"><span data-stu-id="9e018-114">PARAMETERS</span></span>

### <span data-ttu-id="9e018-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e018-115">-DefaultProfile</span></span>
<span data-ttu-id="9e018-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9e018-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e018-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9e018-117">-InputObject</span></span>
<span data-ttu-id="9e018-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="9e018-118">Input Object.</span></span>

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

### <span data-ttu-id="9e018-119">-位置</span><span class="sxs-lookup"><span data-stu-id="9e018-119">-Location</span></span>
<span data-ttu-id="9e018-120">位於.</span><span class="sxs-lookup"><span data-stu-id="9e018-120">Location.</span></span>

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

### <span data-ttu-id="9e018-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="9e018-121">-Name</span></span>
<span data-ttu-id="9e018-122">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9e018-122">Resource name.</span></span>

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

### <span data-ttu-id="9e018-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e018-123">-PassThru</span></span>
<span data-ttu-id="9e018-124">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="9e018-124">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9e018-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e018-125">-ResourceGroupName</span></span>
<span data-ttu-id="9e018-126">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9e018-126">Resource group name.</span></span>

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

### <span data-ttu-id="9e018-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9e018-127">-ResourceId</span></span>
<span data-ttu-id="9e018-128">[資源識別碼]。</span><span class="sxs-lookup"><span data-stu-id="9e018-128">Resource ID.</span></span>

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

### <span data-ttu-id="9e018-129">-確認</span><span class="sxs-lookup"><span data-stu-id="9e018-129">-Confirm</span></span>
<span data-ttu-id="9e018-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9e018-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e018-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e018-131">-WhatIf</span></span>
<span data-ttu-id="9e018-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9e018-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9e018-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9e018-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e018-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e018-134">CommonParameters</span></span>
<span data-ttu-id="9e018-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9e018-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e018-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9e018-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e018-137">輸入</span><span class="sxs-lookup"><span data-stu-id="9e018-137">INPUTS</span></span>

### <span data-ttu-id="9e018-138">System.object</span><span class="sxs-lookup"><span data-stu-id="9e018-138">System.String</span></span>

### <span data-ttu-id="9e018-139">PSSecurityJitNetworkAccessPolicy 中的 JitNetworkAccessPolicies （Security..。</span><span class="sxs-lookup"><span data-stu-id="9e018-139">Microsoft.Azure.Commands.Security.Models.JitNetworkAccessPolicies.PSSecurityJitNetworkAccessPolicy</span></span>

## <span data-ttu-id="9e018-140">輸出</span><span class="sxs-lookup"><span data-stu-id="9e018-140">OUTPUTS</span></span>

### <span data-ttu-id="9e018-141">System.object</span><span class="sxs-lookup"><span data-stu-id="9e018-141">System.Boolean</span></span>

## <span data-ttu-id="9e018-142">筆記</span><span class="sxs-lookup"><span data-stu-id="9e018-142">NOTES</span></span>

## <span data-ttu-id="9e018-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="9e018-143">RELATED LINKS</span></span>
