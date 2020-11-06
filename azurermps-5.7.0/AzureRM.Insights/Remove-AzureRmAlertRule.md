---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: eaa7cfa9f58bb9bb5affa7a035d194910bcf0006
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447805"
---
# <span data-ttu-id="7eea9-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7eea9-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="7eea9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7eea9-102">SYNOPSIS</span></span>
<span data-ttu-id="7eea9-103">移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="7eea9-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eea9-104">句法</span><span class="sxs-lookup"><span data-stu-id="7eea9-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eea9-105">說明</span><span class="sxs-lookup"><span data-stu-id="7eea9-105">DESCRIPTION</span></span>
<span data-ttu-id="7eea9-106">**AzureRmAlertRule** Cmdlet 會移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="7eea9-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="7eea9-107">您必須指定警示規則的名稱以及指派給它的資源群組。</span><span class="sxs-lookup"><span data-stu-id="7eea9-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

<span data-ttu-id="7eea9-108">這個 Cmdlet 會實現 ShouldProcess 模式，亦即，在實際建立、修改或移除資源之前，它可能會要求使用者進行確認。</span><span class="sxs-lookup"><span data-stu-id="7eea9-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="7eea9-109">示例</span><span class="sxs-lookup"><span data-stu-id="7eea9-109">EXAMPLES</span></span>

### <span data-ttu-id="7eea9-110">範例1：移除警示規則</span><span class="sxs-lookup"><span data-stu-id="7eea9-110">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="7eea9-111">這個命令會在資源群組中移除名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則，預設為 [Web-CentralUS]。</span><span class="sxs-lookup"><span data-stu-id="7eea9-111">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="7eea9-112">參數</span><span class="sxs-lookup"><span data-stu-id="7eea9-112">PARAMETERS</span></span>

### <span data-ttu-id="7eea9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eea9-113">-DefaultProfile</span></span>
<span data-ttu-id="7eea9-114">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7eea9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7eea9-115">-名稱</span><span class="sxs-lookup"><span data-stu-id="7eea9-115">-Name</span></span>
<span data-ttu-id="7eea9-116">指定要移除之警示規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="7eea9-116">Specifies the name of the alert rule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eea9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eea9-117">-ResourceGroupName</span></span>
<span data-ttu-id="7eea9-118">指定警示規則之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="7eea9-118">Specifies the name of the resource group for the alert rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eea9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eea9-119">CommonParameters</span></span>
<span data-ttu-id="7eea9-120">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7eea9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eea9-121">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7eea9-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eea9-122">輸入</span><span class="sxs-lookup"><span data-stu-id="7eea9-122">INPUTS</span></span>

### <span data-ttu-id="7eea9-123">所有</span><span class="sxs-lookup"><span data-stu-id="7eea9-123">None</span></span>
<span data-ttu-id="7eea9-124">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="7eea9-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7eea9-125">輸出</span><span class="sxs-lookup"><span data-stu-id="7eea9-125">OUTPUTS</span></span>

### <span data-ttu-id="7eea9-126">AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="7eea9-126">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="7eea9-127">筆記</span><span class="sxs-lookup"><span data-stu-id="7eea9-127">NOTES</span></span>

## <span data-ttu-id="7eea9-128">相關連結</span><span class="sxs-lookup"><span data-stu-id="7eea9-128">RELATED LINKS</span></span>

[<span data-ttu-id="7eea9-129">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="7eea9-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="7eea9-130">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="7eea9-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="7eea9-131">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="7eea9-131">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="7eea9-132">AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="7eea9-132">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


