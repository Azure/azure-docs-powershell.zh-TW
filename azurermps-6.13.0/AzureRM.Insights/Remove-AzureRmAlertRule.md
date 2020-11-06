---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: bca70877b8821b06e6662f334120f126328f4451
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455328"
---
# <span data-ttu-id="1a8ce-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="1a8ce-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="1a8ce-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1a8ce-102">SYNOPSIS</span></span>
<span data-ttu-id="1a8ce-103">移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a8ce-104">句法</span><span class="sxs-lookup"><span data-stu-id="1a8ce-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a8ce-105">說明</span><span class="sxs-lookup"><span data-stu-id="1a8ce-105">DESCRIPTION</span></span>
<span data-ttu-id="1a8ce-106">**AzureRmAlertRule** Cmdlet 會移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="1a8ce-107">您必須指定警示規則的名稱以及指派給它的資源群組。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>
<span data-ttu-id="1a8ce-108">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="1a8ce-109">示例</span><span class="sxs-lookup"><span data-stu-id="1a8ce-109">EXAMPLES</span></span>

### <span data-ttu-id="1a8ce-110">範例1：移除警示規則</span><span class="sxs-lookup"><span data-stu-id="1a8ce-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="1a8ce-111">這個命令會在資源群組中移除名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則，預設為 [Web-CentralUS]。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="1a8ce-112">參數</span><span class="sxs-lookup"><span data-stu-id="1a8ce-112">PARAMETERS</span></span>

### <span data-ttu-id="1a8ce-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a8ce-113">-DefaultProfile</span></span>
<span data-ttu-id="1a8ce-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1a8ce-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a8ce-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="1a8ce-115">-Name</span></span>
<span data-ttu-id="1a8ce-116">指定要移除之警示規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-116">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="1a8ce-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a8ce-117">-ResourceGroupName</span></span>
<span data-ttu-id="1a8ce-118">指定警示規則之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-118">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="1a8ce-119">-確認</span><span class="sxs-lookup"><span data-stu-id="1a8ce-119">-Confirm</span></span>
<span data-ttu-id="1a8ce-120">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a8ce-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a8ce-121">-WhatIf</span></span>
<span data-ttu-id="1a8ce-122">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a8ce-123">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a8ce-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a8ce-124">CommonParameters</span></span>
<span data-ttu-id="1a8ce-125">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a8ce-126">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1a8ce-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a8ce-127">輸入</span><span class="sxs-lookup"><span data-stu-id="1a8ce-127">INPUTS</span></span>

### <span data-ttu-id="1a8ce-128">System.object</span><span class="sxs-lookup"><span data-stu-id="1a8ce-128">System.String</span></span>

## <span data-ttu-id="1a8ce-129">輸出</span><span class="sxs-lookup"><span data-stu-id="1a8ce-129">OUTPUTS</span></span>

### <span data-ttu-id="1a8ce-130">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1a8ce-130">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1a8ce-131">筆記</span><span class="sxs-lookup"><span data-stu-id="1a8ce-131">NOTES</span></span>

## <span data-ttu-id="1a8ce-132">相關連結</span><span class="sxs-lookup"><span data-stu-id="1a8ce-132">RELATED LINKS</span></span>

[<span data-ttu-id="1a8ce-133">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="1a8ce-133">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="1a8ce-134">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="1a8ce-134">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="1a8ce-135">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="1a8ce-135">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="1a8ce-136">AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="1a8ce-136">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


