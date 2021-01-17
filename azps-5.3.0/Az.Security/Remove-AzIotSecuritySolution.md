---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Remove-AzIotSecuritySolution
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Remove-AzIotSecuritySolution.md
ms.openlocfilehash: 42e483a9783a919dfe45425357052df2389cc8b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286508"
---
# <span data-ttu-id="9b514-101">Remove-AzIotSecuritySolution</span><span class="sxs-lookup"><span data-stu-id="9b514-101">Remove-AzIotSecuritySolution</span></span>

## <span data-ttu-id="9b514-102">摘要</span><span class="sxs-lookup"><span data-stu-id="9b514-102">SYNOPSIS</span></span>
<span data-ttu-id="9b514-103">刪除 IoT 安全解決方案</span><span class="sxs-lookup"><span data-stu-id="9b514-103">Delete IoT security solution</span></span>

## <span data-ttu-id="9b514-104">句法</span><span class="sxs-lookup"><span data-stu-id="9b514-104">SYNTAX</span></span>

### <span data-ttu-id="9b514-105">ResourceGroupLevelResource (預設) </span><span class="sxs-lookup"><span data-stu-id="9b514-105">ResourceGroupLevelResource (Default)</span></span>
```
Remove-AzIotSecuritySolution -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b514-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b514-106">ResourceId</span></span>
```
Remove-AzIotSecuritySolution -ResourceId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b514-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="9b514-107">InputObject</span></span>
```
Remove-AzIotSecuritySolution -InputObject <PSIotSecuritySolution> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9b514-108">說明</span><span class="sxs-lookup"><span data-stu-id="9b514-108">DESCRIPTION</span></span>
<span data-ttu-id="9b514-109">Remove-AzIotSecuritySolution Cmdlet 會刪除特定的 iot 安全性方案。</span><span class="sxs-lookup"><span data-stu-id="9b514-109">The Remove-AzIotSecuritySolution cmdlet deletes a specific iot security solution.</span></span> <span data-ttu-id="9b514-110">IoT 安全解決方案會從 IoT 裝置和 IoT 中樞收集安全性資料和事件，以協助防範及偵測威脅。</span><span class="sxs-lookup"><span data-stu-id="9b514-110">The IoT security solution collects security data and events from iot devices and iot hub to help prevent and detect threats.</span></span>

## <span data-ttu-id="9b514-111">示例</span><span class="sxs-lookup"><span data-stu-id="9b514-111">EXAMPLES</span></span>

### <span data-ttu-id="9b514-112">範例1</span><span class="sxs-lookup"><span data-stu-id="9b514-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotSecuritySolution -Name "MySample" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="9b514-113">刪除含有資源群組 "MyResourceGroup" 的 IoT 安全解決方案 "MySample"</span><span class="sxs-lookup"><span data-stu-id="9b514-113">Delete IoT security solution "MySample" with resource group "MyResourceGroup"</span></span>

## <span data-ttu-id="9b514-114">參數</span><span class="sxs-lookup"><span data-stu-id="9b514-114">PARAMETERS</span></span>

### <span data-ttu-id="9b514-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b514-115">-DefaultProfile</span></span>
<span data-ttu-id="9b514-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="9b514-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b514-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9b514-117">-InputObject</span></span>
<span data-ttu-id="9b514-118">輸入物件。</span><span class="sxs-lookup"><span data-stu-id="9b514-118">Input Object.</span></span>

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

### <span data-ttu-id="9b514-119">-名稱</span><span class="sxs-lookup"><span data-stu-id="9b514-119">-Name</span></span>
<span data-ttu-id="9b514-120">資源名稱。</span><span class="sxs-lookup"><span data-stu-id="9b514-120">Resource name.</span></span>

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

### <span data-ttu-id="9b514-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b514-121">-PassThru</span></span>
<span data-ttu-id="9b514-122">傳回操作是否成功。</span><span class="sxs-lookup"><span data-stu-id="9b514-122">Return whether the operation was successful.</span></span>

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

### <span data-ttu-id="9b514-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b514-123">-ResourceGroupName</span></span>
<span data-ttu-id="9b514-124">資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="9b514-124">Resource group name.</span></span>

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

### <span data-ttu-id="9b514-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9b514-125">-ResourceId</span></span>
<span data-ttu-id="9b514-126">您想要在其上喚醒命令的安全性資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="9b514-126">ID of the security resource that you want to invoke the command on.</span></span>

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

### <span data-ttu-id="9b514-127">-確認</span><span class="sxs-lookup"><span data-stu-id="9b514-127">-Confirm</span></span>
<span data-ttu-id="9b514-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="9b514-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b514-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b514-129">-WhatIf</span></span>
<span data-ttu-id="9b514-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="9b514-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b514-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="9b514-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b514-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b514-132">CommonParameters</span></span>
<span data-ttu-id="9b514-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="9b514-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b514-134">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="9b514-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b514-135">輸入</span><span class="sxs-lookup"><span data-stu-id="9b514-135">INPUTS</span></span>

### <span data-ttu-id="9b514-136">System.object</span><span class="sxs-lookup"><span data-stu-id="9b514-136">System.String</span></span>

### <span data-ttu-id="9b514-137">PSIotSecuritySolution 中的 IotSecuritySolutions （Security..。</span><span class="sxs-lookup"><span data-stu-id="9b514-137">Microsoft.Azure.Commands.Security.Models.IotSecuritySolutions.PSIotSecuritySolution</span></span>

## <span data-ttu-id="9b514-138">輸出</span><span class="sxs-lookup"><span data-stu-id="9b514-138">OUTPUTS</span></span>

### <span data-ttu-id="9b514-139">System.object</span><span class="sxs-lookup"><span data-stu-id="9b514-139">System.Boolean</span></span>

## <span data-ttu-id="9b514-140">筆記</span><span class="sxs-lookup"><span data-stu-id="9b514-140">NOTES</span></span>

## <span data-ttu-id="9b514-141">相關連結</span><span class="sxs-lookup"><span data-stu-id="9b514-141">RELATED LINKS</span></span>
