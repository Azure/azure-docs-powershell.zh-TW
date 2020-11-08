---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzAlertRule.md
ms.openlocfilehash: 23b4c81e7c999301ccb535435911a9413ae4ef16
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93970428"
---
# <span data-ttu-id="cf9fa-101">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="cf9fa-101">Remove-AzAlertRule</span></span>

## <span data-ttu-id="cf9fa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cf9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="cf9fa-103">移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-103">Removes an alert rule.</span></span>

## <span data-ttu-id="cf9fa-104">句法</span><span class="sxs-lookup"><span data-stu-id="cf9fa-104">SYNTAX</span></span>

```
Remove-AzAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cf9fa-105">說明</span><span class="sxs-lookup"><span data-stu-id="cf9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="cf9fa-106">**AzAlertRule** Cmdlet 會移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-106">The **Remove-AzAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="cf9fa-107">您必須指定警示規則的名稱以及指派給它的資源群組。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="cf9fa-108">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="cf9fa-109">示例</span><span class="sxs-lookup"><span data-stu-id="cf9fa-109">EXAMPLES</span></span>

### <span data-ttu-id="cf9fa-110">範例1：移除警示規則</span><span class="sxs-lookup"><span data-stu-id="cf9fa-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="cf9fa-111">這個命令會在資源群組中移除名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則，預設為 [Web-CentralUS]。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="cf9fa-112">參數</span><span class="sxs-lookup"><span data-stu-id="cf9fa-112">PARAMETERS</span></span>

### <span data-ttu-id="cf9fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cf9fa-113">-DefaultProfile</span></span>
<span data-ttu-id="cf9fa-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cf9fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cf9fa-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="cf9fa-115">-Name</span></span>
<span data-ttu-id="cf9fa-116">指定要移除之警示規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="cf9fa-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cf9fa-117">-ResourceGroupName</span></span>
<span data-ttu-id="cf9fa-118">指定警示規則之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="cf9fa-119">-確認</span><span class="sxs-lookup"><span data-stu-id="cf9fa-119">-Confirm</span></span>
<span data-ttu-id="cf9fa-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cf9fa-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cf9fa-121">-WhatIf</span></span>
<span data-ttu-id="cf9fa-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cf9fa-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cf9fa-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cf9fa-124">CommonParameters</span></span>
<span data-ttu-id="cf9fa-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cf9fa-126">如需詳細資訊，請參閱 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)。</span><span class="sxs-lookup"><span data-stu-id="cf9fa-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cf9fa-127">輸入</span><span class="sxs-lookup"><span data-stu-id="cf9fa-127">INPUTS</span></span>

### <span data-ttu-id="cf9fa-128">System.object</span><span class="sxs-lookup"><span data-stu-id="cf9fa-128">System.String</span></span>

## <span data-ttu-id="cf9fa-129">輸出</span><span class="sxs-lookup"><span data-stu-id="cf9fa-129">OUTPUTS</span></span>

### <span data-ttu-id="cf9fa-130">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="cf9fa-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="cf9fa-131">筆記</span><span class="sxs-lookup"><span data-stu-id="cf9fa-131">NOTES</span></span>

## <span data-ttu-id="cf9fa-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="cf9fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="cf9fa-133">附加 AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="cf9fa-133">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="cf9fa-134">附加 AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="cf9fa-134">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="cf9fa-135">AzAlertHistory</span><span class="sxs-lookup"><span data-stu-id="cf9fa-135">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="cf9fa-136">AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="cf9fa-136">Get-AzAlertRule</span></span>](./Get-AzAlertRule.md)


