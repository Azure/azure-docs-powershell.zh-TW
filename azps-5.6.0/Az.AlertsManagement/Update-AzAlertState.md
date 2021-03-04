---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/powershell/module/az.alertsmanagement/update-azalertstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzAlertState.md
ms.openlocfilehash: 1ab5abc4af394647fd1438ed79cebb739daaca94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101910330"
---
# <span data-ttu-id="3f462-101">Update-AzAlertState</span><span class="sxs-lookup"><span data-stu-id="3f462-101">Update-AzAlertState</span></span>

## <span data-ttu-id="3f462-102">簡介</span><span class="sxs-lookup"><span data-stu-id="3f462-102">SYNOPSIS</span></span>
<span data-ttu-id="3f462-103">更新通知狀態</span><span class="sxs-lookup"><span data-stu-id="3f462-103">Updates alert state</span></span>

## <span data-ttu-id="3f462-104">語法</span><span class="sxs-lookup"><span data-stu-id="3f462-104">SYNTAX</span></span>

### <span data-ttu-id="3f462-105">ByAlertId (預設) </span><span class="sxs-lookup"><span data-stu-id="3f462-105">ByAlertId (Default)</span></span>
```
Update-AzAlertState -AlertId <String> -State <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f462-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="3f462-106">ByInputObject</span></span>
```
Update-AzAlertState -State <String> -InputObject <PSAlert> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f462-107">描述</span><span class="sxs-lookup"><span data-stu-id="3f462-107">DESCRIPTION</span></span>
<span data-ttu-id="3f462-108">**Update-AzAlertState** Cmdlet 會更新警示狀態。</span><span class="sxs-lookup"><span data-stu-id="3f462-108">**Update-AzAlertState** cmdlet updates alert state.</span></span>

## <span data-ttu-id="3f462-109">例子</span><span class="sxs-lookup"><span data-stu-id="3f462-109">EXAMPLES</span></span>

### <span data-ttu-id="3f462-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="3f462-110">Example 1</span></span>
```powershell
PS C:\> Update-AzAlertState -AlertId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Closed"
```

<span data-ttu-id="3f462-111">此 Cmdlet 將通知狀態更新為關閉。</span><span class="sxs-lookup"><span data-stu-id="3f462-111">This cmdlet updates the alert state to Closed.</span></span>

## <span data-ttu-id="3f462-112">參數</span><span class="sxs-lookup"><span data-stu-id="3f462-112">PARAMETERS</span></span>

### <span data-ttu-id="3f462-113">-AlertId</span><span class="sxs-lookup"><span data-stu-id="3f462-113">-AlertId</span></span>
<span data-ttu-id="3f462-114">警示的唯一識別碼/ ResourceId 警示。</span><span class="sxs-lookup"><span data-stu-id="3f462-114">Unique Identifier of Alert / ResourceId of alert.</span></span>

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

### <span data-ttu-id="3f462-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f462-115">-DefaultProfile</span></span>
<span data-ttu-id="3f462-116">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱。</span><span class="sxs-lookup"><span data-stu-id="3f462-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f462-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f462-117">-InputObject</span></span>
<span data-ttu-id="3f462-118">來自管線的輸入物件。</span><span class="sxs-lookup"><span data-stu-id="3f462-118">Input object from pipeline.</span></span>

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

### <span data-ttu-id="3f462-119">-State</span><span class="sxs-lookup"><span data-stu-id="3f462-119">-State</span></span>
<span data-ttu-id="3f462-120">已更新通知狀態</span><span class="sxs-lookup"><span data-stu-id="3f462-120">Updated Alert State</span></span>

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

### <span data-ttu-id="3f462-121">-確認</span><span class="sxs-lookup"><span data-stu-id="3f462-121">-Confirm</span></span>
<span data-ttu-id="3f462-122">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="3f462-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f462-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f462-123">-WhatIf</span></span>
<span data-ttu-id="3f462-124">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3f462-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f462-125">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3f462-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f462-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f462-126">CommonParameters</span></span>
<span data-ttu-id="3f462-127">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="3f462-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f462-128">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f462-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f462-129">輸入</span><span class="sxs-lookup"><span data-stu-id="3f462-129">INPUTS</span></span>

### <span data-ttu-id="3f462-130">沒有</span><span class="sxs-lookup"><span data-stu-id="3f462-130">None</span></span>

## <span data-ttu-id="3f462-131">輸出</span><span class="sxs-lookup"><span data-stu-id="3f462-131">OUTPUTS</span></span>

### <span data-ttu-id="3f462-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span><span class="sxs-lookup"><span data-stu-id="3f462-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSAlert</span></span>

## <span data-ttu-id="3f462-133">筆記</span><span class="sxs-lookup"><span data-stu-id="3f462-133">NOTES</span></span>

## <span data-ttu-id="3f462-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="3f462-134">RELATED LINKS</span></span>
