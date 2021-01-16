---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeShare.md
ms.openlocfilehash: 3f5855d329daba44b26e2c79cbc07608222db5f9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98286127"
---
# <span data-ttu-id="3aca4-101">Remove-AzStackEdgeShare</span><span class="sxs-lookup"><span data-stu-id="3aca4-101">Remove-AzStackEdgeShare</span></span>

## <span data-ttu-id="3aca4-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3aca4-102">SYNOPSIS</span></span>
<span data-ttu-id="3aca4-103">從裝置移除共用。</span><span class="sxs-lookup"><span data-stu-id="3aca4-103">Removes a share from the device.</span></span>

## <span data-ttu-id="3aca4-104">句法</span><span class="sxs-lookup"><span data-stu-id="3aca4-104">SYNTAX</span></span>

### <span data-ttu-id="3aca4-105">DeleteByNameParameterSet (預設) </span><span class="sxs-lookup"><span data-stu-id="3aca4-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeShare [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aca4-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aca4-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeShare [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3aca4-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3aca4-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeShare [-InputObject] <PSStackEdgeShare> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3aca4-108">說明</span><span class="sxs-lookup"><span data-stu-id="3aca4-108">DESCRIPTION</span></span>
<span data-ttu-id="3aca4-109">**AzStackEdgeEdgeShare** Cmdlet 會移除堆疊邊緣裝置的關聯邊緣共用。</span><span class="sxs-lookup"><span data-stu-id="3aca4-109">The **Remove-AzStackEdgeEdgeShare** cmdlet removes the associated edge shares for a Stack Edge device.</span></span>

## <span data-ttu-id="3aca4-110">示例</span><span class="sxs-lookup"><span data-stu-id="3aca4-110">EXAMPLES</span></span>

### <span data-ttu-id="3aca4-111">範例1</span><span class="sxs-lookup"><span data-stu-id="3aca4-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeShare -ResourceGroupName resourceGroupName -DeviceName deviceName -Name shareName
```

## <span data-ttu-id="3aca4-112">參數</span><span class="sxs-lookup"><span data-stu-id="3aca4-112">PARAMETERS</span></span>

### <span data-ttu-id="3aca4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3aca4-113">-AsJob</span></span>
<span data-ttu-id="3aca4-114">在背景中執行 Cmdlet</span><span class="sxs-lookup"><span data-stu-id="3aca4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3aca4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3aca4-115">-DefaultProfile</span></span>
<span data-ttu-id="3aca4-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="3aca4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3aca4-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3aca4-117">-DeviceName</span></span>
<span data-ttu-id="3aca4-118">裝置名稱</span><span class="sxs-lookup"><span data-stu-id="3aca4-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aca4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3aca4-119">-InputObject</span></span>
<span data-ttu-id="3aca4-120">輸入物件</span><span class="sxs-lookup"><span data-stu-id="3aca4-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeShare

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3aca4-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="3aca4-121">-Name</span></span>
<span data-ttu-id="3aca4-122">資源名稱</span><span class="sxs-lookup"><span data-stu-id="3aca4-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeShareName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aca4-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3aca4-123">-PassThru</span></span>
<span data-ttu-id="3aca4-124">如果成功，則傳回 true</span><span class="sxs-lookup"><span data-stu-id="3aca4-124">returns true if successful</span></span>

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

### <span data-ttu-id="3aca4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3aca4-125">-ResourceGroupName</span></span>
<span data-ttu-id="3aca4-126">資源群組名稱</span><span class="sxs-lookup"><span data-stu-id="3aca4-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aca4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aca4-127">-ResourceId</span></span>
<span data-ttu-id="3aca4-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3aca4-128">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3aca4-129">-確認</span><span class="sxs-lookup"><span data-stu-id="3aca4-129">-Confirm</span></span>
<span data-ttu-id="3aca4-130">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3aca4-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3aca4-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3aca4-131">-WhatIf</span></span>
<span data-ttu-id="3aca4-132">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3aca4-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3aca4-133">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3aca4-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3aca4-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3aca4-134">CommonParameters</span></span>
<span data-ttu-id="3aca4-135">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3aca4-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3aca4-136">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="3aca4-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3aca4-137">輸入</span><span class="sxs-lookup"><span data-stu-id="3aca4-137">INPUTS</span></span>

### <span data-ttu-id="3aca4-138">System.object</span><span class="sxs-lookup"><span data-stu-id="3aca4-138">System.String</span></span>

### <span data-ttu-id="3aca4-139">PSStackEdgeShare （StackEdge）的</span><span class="sxs-lookup"><span data-stu-id="3aca4-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeShare</span></span>

## <span data-ttu-id="3aca4-140">輸出</span><span class="sxs-lookup"><span data-stu-id="3aca4-140">OUTPUTS</span></span>

### <span data-ttu-id="3aca4-141">System.object</span><span class="sxs-lookup"><span data-stu-id="3aca4-141">System.Boolean</span></span>

## <span data-ttu-id="3aca4-142">筆記</span><span class="sxs-lookup"><span data-stu-id="3aca4-142">NOTES</span></span>

## <span data-ttu-id="3aca4-143">相關連結</span><span class="sxs-lookup"><span data-stu-id="3aca4-143">RELATED LINKS</span></span>
