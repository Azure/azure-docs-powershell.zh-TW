---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: da98138060b0c06e09a56b375c64f530ea8e51f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101909945"
---
# <span data-ttu-id="f11b2-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f11b2-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="f11b2-102">簡介</span><span class="sxs-lookup"><span data-stu-id="f11b2-102">SYNOPSIS</span></span>
<span data-ttu-id="f11b2-103">刪除 IoT 安全性解決方案</span><span class="sxs-lookup"><span data-stu-id="f11b2-103">Delete IoT security solution</span></span>

## <span data-ttu-id="f11b2-104">語法</span><span class="sxs-lookup"><span data-stu-id="f11b2-104">SYNTAX</span></span>

### <span data-ttu-id="f11b2-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="f11b2-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f11b2-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="f11b2-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f11b2-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="f11b2-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f11b2-108">描述</span><span class="sxs-lookup"><span data-stu-id="f11b2-108">DESCRIPTION</span></span>
<span data-ttu-id="f11b2-109">Cmdlet Remove-AzIotSecuritySolution刪除特定的 iot 安全性解決方案。</span><span class="sxs-lookup"><span data-stu-id="f11b2-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="f11b2-110">IoT 安全性解決方案會收集 iot 裝置和 iot 中樞的安全性資料和事件，協助防範和偵測威脅。</span><span class="sxs-lookup"><span data-stu-id="f11b2-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="f11b2-111">例子</span><span class="sxs-lookup"><span data-stu-id="f11b2-111">EXAMPLES</span></span>

### <span data-ttu-id="f11b2-112">範例 1</span><span class="sxs-lookup"><span data-stu-id="f11b2-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f11b2-113">使用資源群組 "MyResourceGroup" 刪除 IoT 安全性解決方案 「MySample」</span><span class="sxs-lookup"><span data-stu-id="f11b2-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="f11b2-114">參數</span><span class="sxs-lookup"><span data-stu-id="f11b2-114">PARAMETERS</span></span>

### <span data-ttu-id="f11b2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f11b2-115">-DefaultProfile</span></span>
<span data-ttu-id="f11b2-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="f11b2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f11b2-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f11b2-117">-InputObject</span></span>
<span data-ttu-id="f11b2-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="f11b2-118">Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f11b2-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="f11b2-119">-Name</span></span>
<span data-ttu-id="f11b2-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="f11b2-120">Resource name.</span></span>

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

### <span data-ttu-id="f11b2-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f11b2-121">-PassThru</span></span>
<span data-ttu-id="f11b2-122">返回作業是否成功。</span><span class="sxs-lookup"><span data-stu-id="f11b2-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="f11b2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f11b2-123">-ResourceGroupName</span></span>
<span data-ttu-id="f11b2-124">資源組名。</span><span class="sxs-lookup"><span data-stu-id="f11b2-124">Resource group name.</span></span>

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

### <span data-ttu-id="f11b2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f11b2-125">-ResourceId</span></span>
<span data-ttu-id="f11b2-126">這是要調用命令之安全性資源的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f11b2-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="f11b2-127">-確認</span><span class="sxs-lookup"><span data-stu-id="f11b2-127">-Confirm</span></span>
<span data-ttu-id="f11b2-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="f11b2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f11b2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f11b2-129">-WhatIf</span></span>
<span data-ttu-id="f11b2-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f11b2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f11b2-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f11b2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f11b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f11b2-132">CommonParameters</span></span>
<span data-ttu-id="f11b2-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="f11b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f11b2-134">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f11b2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f11b2-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f11b2-135">INPUTS</span></span>

### <span data-ttu-id="f11b2-136">System.String</span><span class="sxs-lookup"><span data-stu-id="f11b2-136">System.String</span></span>

### <span data-ttu-id="f11b2-137">Microsoft.Azure.Commands.Security.models.IotSecuritySolutions.PSIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="f11b2-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="f11b2-138">輸出</span><span class="sxs-lookup"><span data-stu-id="f11b2-138">OUTPUTS</span></span>

### <span data-ttu-id="f11b2-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f11b2-139">System.Boolean</span></span>

## <span data-ttu-id="f11b2-140">筆記</span><span class="sxs-lookup"><span data-stu-id="f11b2-140">NOTES</span></span>

## <span data-ttu-id="f11b2-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="f11b2-141">RELATED LINKS</span></span>
