---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 61a24b5ec7e63ce9a3059257cf1772c4e15d100b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905021"
---
# <span data-ttu-id="5423d-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="5423d-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="5423d-102">簡介</span><span class="sxs-lookup"><span data-stu-id="5423d-102">SYNOPSIS</span></span>
<span data-ttu-id="5423d-103">移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="5423d-103">Removes an alert rule.</span></span>

## <span data-ttu-id="5423d-104">語法</span><span class="sxs-lookup"><span data-stu-id="5423d-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5423d-105">描述</span><span class="sxs-lookup"><span data-stu-id="5423d-105">DESCRIPTION</span></span>
<span data-ttu-id="5423d-106">**Remove-AzAlertRule** Cmdlet 會移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="5423d-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="5423d-107">您必須指定警示規則的名稱，以及指派給該規則的資源群組。</span><span class="sxs-lookup"><span data-stu-id="5423d-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="5423d-108">此 Cmdlet 實做 ShouldProcess 模式，即實際建立、修改或移除資源之前，可能會向使用者要求確認。</span><span class="sxs-lookup"><span data-stu-id="5423d-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="5423d-109">例子</span><span class="sxs-lookup"><span data-stu-id="5423d-109">EXAMPLES</span></span>

### <span data-ttu-id="5423d-110">範例 1：移除警示規則</span><span class="sxs-lookup"><span data-stu-id="5423d-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="5423d-111">此命令會移除資源群組 Default-Web-CentralUS 中名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則。</span><span class="sxs-lookup"><span data-stu-id="5423d-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="5423d-112">參數</span><span class="sxs-lookup"><span data-stu-id="5423d-112">PARAMETERS</span></span>

### <span data-ttu-id="5423d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5423d-113">-DefaultProfile</span></span>
<span data-ttu-id="5423d-114">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="5423d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5423d-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="5423d-115">-Name</span></span>
<span data-ttu-id="5423d-116">指定要移除的警示規則名稱。</span><span class="sxs-lookup"><span data-stu-id="5423d-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5423d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5423d-117">-ResourceGroupName</span></span>
<span data-ttu-id="5423d-118">指定警示規則的資源組名。</span><span class="sxs-lookup"><span data-stu-id="5423d-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5423d-119">-確認</span><span class="sxs-lookup"><span data-stu-id="5423d-119">-Confirm</span></span>
<span data-ttu-id="5423d-120">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="5423d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5423d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5423d-121">-WhatIf</span></span>
<span data-ttu-id="5423d-122">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5423d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5423d-123">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5423d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5423d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5423d-124">CommonParameters</span></span>
<span data-ttu-id="5423d-125">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="5423d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5423d-126">詳細資訊[請參閱about_CommonParameters。](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5423d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5423d-127">輸入</span><span class="sxs-lookup"><span data-stu-id="5423d-127">INPUTS</span></span>

### <span data-ttu-id="5423d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="5423d-128">System.String</span></span>

## <span data-ttu-id="5423d-129">輸出</span><span class="sxs-lookup"><span data-stu-id="5423d-129">OUTPUTS</span></span>

### <span data-ttu-id="5423d-130">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5423d-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="5423d-131">筆記</span><span class="sxs-lookup"><span data-stu-id="5423d-131">NOTES</span></span>

## <span data-ttu-id="5423d-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="5423d-132">RELATED LINKS</span></span>

[<span data-ttu-id="5423d-133">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="5423d-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="5423d-134">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="5423d-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="5423d-135">Get-AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="5423d-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="5423d-136">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="5423d-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)


