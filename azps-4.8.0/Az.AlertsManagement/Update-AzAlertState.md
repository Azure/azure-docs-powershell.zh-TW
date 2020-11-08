---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 4ba238f75fa1e39daf2309a1ceda1aed323ff47d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93969476"
---
# <span data-ttu-id="d25c1-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="d25c1-101">Update-AzAlertState</span></span>

## <span data-ttu-id="d25c1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d25c1-102">SYNOPSIS</span></span>
<span data-ttu-id="d25c1-103">更新提醒狀態</span><span class="sxs-lookup"><span data-stu-id="d25c1-103">Updates alert state</span></span>

## <span data-ttu-id="d25c1-104">句法</span><span class="sxs-lookup"><span data-stu-id="d25c1-104">SYNTAX</span></span>

### <span data-ttu-id="d25c1-105">ByAlertId (預設) </span><span class="sxs-lookup"><span data-stu-id="d25c1-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d25c1-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d25c1-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d25c1-107">說明</span><span class="sxs-lookup"><span data-stu-id="d25c1-107">DESCRIPTION</span></span>
<span data-ttu-id="d25c1-108">**更新-AzAlertState** Cmdlet 會更新警報狀態。</span><span class="sxs-lookup"><span data-stu-id="d25c1-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="d25c1-109">示例</span><span class="sxs-lookup"><span data-stu-id="d25c1-109">EXAMPLES</span></span>

### <span data-ttu-id="d25c1-110">範例1</span><span class="sxs-lookup"><span data-stu-id="d25c1-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="d25c1-111">這個 Cmdlet 會將警報狀態更新為 [已關閉]。</span><span class="sxs-lookup"><span data-stu-id="d25c1-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="d25c1-112">參數</span><span class="sxs-lookup"><span data-stu-id="d25c1-112">PARAMETERS</span></span>

### <span data-ttu-id="d25c1-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="d25c1-113">-AlertId</span></span>
<span data-ttu-id="d25c1-114">警示/警示的唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="d25c1-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAlertId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25c1-115">-DefaultProfile</span></span>
<span data-ttu-id="d25c1-116">用於與 Azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="d25c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d25c1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d25c1-117">-InputObject</span></span>
<span data-ttu-id="d25c1-118">從管線輸入物件。</span><span class="sxs-lookup"><span data-stu-id="d25c1-118">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d25c1-119">-State</span><span class="sxs-lookup"><span data-stu-id="d25c1-119">-State</span></span>
<span data-ttu-id="d25c1-120">已更新的警示狀態</span><span class="sxs-lookup"><span data-stu-id="d25c1-120">Updated Alert State</span></span>

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

### <span data-ttu-id="d25c1-121">-確認</span><span class="sxs-lookup"><span data-stu-id="d25c1-121">-Confirm</span></span>
<span data-ttu-id="d25c1-122">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d25c1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d25c1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d25c1-123">-WhatIf</span></span>
<span data-ttu-id="d25c1-124">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d25c1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d25c1-125">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d25c1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d25c1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25c1-126">CommonParameters</span></span>
<span data-ttu-id="d25c1-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d25c1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25c1-128">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="d25c1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25c1-129">輸入</span><span class="sxs-lookup"><span data-stu-id="d25c1-129">INPUTS</span></span>

### <span data-ttu-id="d25c1-130">所有</span><span class="sxs-lookup"><span data-stu-id="d25c1-130">None</span></span>

## <span data-ttu-id="d25c1-131">輸出</span><span class="sxs-lookup"><span data-stu-id="d25c1-131">OUTPUTS</span></span>

### <span data-ttu-id="d25c1-132">AlertsManagement. OutputModels. PSAlert</span><span class="sxs-lookup"><span data-stu-id="d25c1-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="d25c1-133">筆記</span><span class="sxs-lookup"><span data-stu-id="d25c1-133">NOTES</span></span>

## <span data-ttu-id="d25c1-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="d25c1-134">RELATED LINKS</span></span>
