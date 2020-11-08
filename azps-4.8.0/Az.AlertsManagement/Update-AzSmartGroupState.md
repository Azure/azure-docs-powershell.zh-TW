---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969470"
---
# <span data-ttu-id="450df-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="450df-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="450df-102">摘要</span><span class="sxs-lookup"><span data-stu-id="450df-102">SYNOPSIS</span></span>
<span data-ttu-id="450df-103">更新智慧群組狀態</span><span class="sxs-lookup"><span data-stu-id="450df-103">Updates smart group state</span></span>

## <span data-ttu-id="450df-104">句法</span><span class="sxs-lookup"><span data-stu-id="450df-104">SYNTAX</span></span>

### <span data-ttu-id="450df-105">BySmartGroupId (預設) </span><span class="sxs-lookup"><span data-stu-id="450df-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="450df-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="450df-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="450df-107">說明</span><span class="sxs-lookup"><span data-stu-id="450df-107">DESCRIPTION</span></span>
<span data-ttu-id="450df-108">**更新-AzSmartGroupState** Cmdlet 會更新智慧群組狀態。</span><span class="sxs-lookup"><span data-stu-id="450df-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="450df-109">示例</span><span class="sxs-lookup"><span data-stu-id="450df-109">EXAMPLES</span></span>

### <span data-ttu-id="450df-110">範例1</span><span class="sxs-lookup"><span data-stu-id="450df-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="450df-111">這個 Cmdlet 會將智慧群組狀態更新為 Acknowleged。</span><span class="sxs-lookup"><span data-stu-id="450df-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="450df-112">參數</span><span class="sxs-lookup"><span data-stu-id="450df-112">PARAMETERS</span></span>

### <span data-ttu-id="450df-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450df-113">-DefaultProfile</span></span>
<span data-ttu-id="450df-114">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="450df-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="450df-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="450df-115">-InputObject</span></span>
<span data-ttu-id="450df-116">從管線輸入物件。</span><span class="sxs-lookup"><span data-stu-id="450df-116">Input object from pipeline.</span></span>

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

### <span data-ttu-id="450df-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="450df-117">-SmartGroupId</span></span>
<span data-ttu-id="450df-118">智慧群組的智慧群組/ResourceId 的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="450df-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

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

### <span data-ttu-id="450df-119">-State</span><span class="sxs-lookup"><span data-stu-id="450df-119">-State</span></span>
<span data-ttu-id="450df-120">已更新的智慧群組狀態</span><span class="sxs-lookup"><span data-stu-id="450df-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="450df-121">-確認</span><span class="sxs-lookup"><span data-stu-id="450df-121">-Confirm</span></span>
<span data-ttu-id="450df-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="450df-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="450df-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450df-123">-WhatIf</span></span>
<span data-ttu-id="450df-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="450df-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="450df-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="450df-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="450df-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450df-126">CommonParameters</span></span>
<span data-ttu-id="450df-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="450df-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450df-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="450df-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450df-129">輸入</span><span class="sxs-lookup"><span data-stu-id="450df-129">INPUTS</span></span>

### <span data-ttu-id="450df-130">所有</span><span class="sxs-lookup"><span data-stu-id="450df-130">None</span></span>

## <span data-ttu-id="450df-131">輸出</span><span class="sxs-lookup"><span data-stu-id="450df-131">OUTPUTS</span></span>

### <span data-ttu-id="450df-132">AlertsManagement. OutputModels. PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="450df-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="450df-133">筆記</span><span class="sxs-lookup"><span data-stu-id="450df-133">NOTES</span></span>

## <span data-ttu-id="450df-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="450df-134">RELATED LINKS</span></span>
