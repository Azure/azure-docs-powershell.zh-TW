---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 5f7e0f26461780b30dbe2b80c79bad8231590e7d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101917817"
---
# <span data-ttu-id="0c8a9-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="0c8a9-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="0c8a9-102">簡介</span><span class="sxs-lookup"><span data-stu-id="0c8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8a9-103">更新智慧型群組狀態</span><span class="sxs-lookup"><span data-stu-id="0c8a9-103">Updates smart group state</span></span>

## <span data-ttu-id="0c8a9-104">語法</span><span class="sxs-lookup"><span data-stu-id="0c8a9-104">SYNTAX</span></span>

### <span data-ttu-id="0c8a9-105">BySmartGroupId (預設) </span><span class="sxs-lookup"><span data-stu-id="0c8a9-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0c8a9-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0c8a9-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c8a9-107">描述</span><span class="sxs-lookup"><span data-stu-id="0c8a9-107">DESCRIPTION</span></span>
<span data-ttu-id="0c8a9-108">**Update-AzSmartGroupState** Cmdlet 會更新智慧型群組狀態。</span><span class="sxs-lookup"><span data-stu-id="0c8a9-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="0c8a9-109">例子</span><span class="sxs-lookup"><span data-stu-id="0c8a9-109">EXAMPLES</span></span>

### <span data-ttu-id="0c8a9-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="0c8a9-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="0c8a9-111">此 Cmdlet 會更新智慧組狀態至確認。</span><span class="sxs-lookup"><span data-stu-id="0c8a9-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="0c8a9-112">參數</span><span class="sxs-lookup"><span data-stu-id="0c8a9-112">PARAMETERS</span></span>

### <span data-ttu-id="0c8a9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c8a9-113">-DefaultProfile</span></span>
<span data-ttu-id="0c8a9-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="0c8a9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c8a9-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0c8a9-115">-InputObject</span></span>
<span data-ttu-id="0c8a9-116">來自管線的輸入物件。</span><span class="sxs-lookup"><span data-stu-id="0c8a9-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0c8a9-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="0c8a9-117">-SmartGroupId</span></span>
<span data-ttu-id="0c8a9-118">智慧組的唯一識別碼/智慧群組的 ResourceId。</span><span class="sxs-lookup"><span data-stu-id="0c8a9-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c8a9-119">-State</span><span class="sxs-lookup"><span data-stu-id="0c8a9-119">-State</span></span>
<span data-ttu-id="0c8a9-120">已更新智慧型群組狀態</span><span class="sxs-lookup"><span data-stu-id="0c8a9-120">Updated Smart group State</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c8a9-121">-確認</span><span class="sxs-lookup"><span data-stu-id="0c8a9-121">-Confirm</span></span>
<span data-ttu-id="0c8a9-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="0c8a9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c8a9-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c8a9-123">-WhatIf</span></span>
<span data-ttu-id="0c8a9-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0c8a9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c8a9-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0c8a9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c8a9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8a9-126">CommonParameters</span></span>
<span data-ttu-id="0c8a9-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="0c8a9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8a9-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c8a9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8a9-129">輸入</span><span class="sxs-lookup"><span data-stu-id="0c8a9-129">INPUTS</span></span>

### <span data-ttu-id="0c8a9-130">沒有</span><span class="sxs-lookup"><span data-stu-id="0c8a9-130">None</span></span>

## <span data-ttu-id="0c8a9-131">輸出</span><span class="sxs-lookup"><span data-stu-id="0c8a9-131">OUTPUTS</span></span>

### <span data-ttu-id="0c8a9-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="0c8a9-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="0c8a9-133">筆記</span><span class="sxs-lookup"><span data-stu-id="0c8a9-133">NOTES</span></span>

## <span data-ttu-id="0c8a9-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="0c8a9-134">RELATED LINKS</span></span>
