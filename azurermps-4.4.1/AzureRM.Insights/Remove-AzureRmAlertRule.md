---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmAlertRule.md
ms.openlocfilehash: de0c1f8fa66b195452d7f2c9447189b4e925136b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453495"
---
# <span data-ttu-id="be43d-101">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="be43d-101">Remove-AzureRmAlertRule</span></span>

## <span data-ttu-id="be43d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="be43d-102">SYNOPSIS</span></span>
<span data-ttu-id="be43d-103">移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="be43d-103">Removes an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be43d-104">句法</span><span class="sxs-lookup"><span data-stu-id="be43d-104">SYNTAX</span></span>

```
Remove-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="be43d-105">說明</span><span class="sxs-lookup"><span data-stu-id="be43d-105">DESCRIPTION</span></span>
<span data-ttu-id="be43d-106">**AzureRmAlertRule** Cmdlet 會移除警示規則。</span><span class="sxs-lookup"><span data-stu-id="be43d-106">The **Remove-AzureRmAlertRule** cmdlet removes an alert rule.</span></span>
<span data-ttu-id="be43d-107">您必須指定警示規則的名稱以及指派給它的資源群組。</span><span class="sxs-lookup"><span data-stu-id="be43d-107">You must specify the name of the alert rule and the resource group to which it is assigned.</span></span>

## <span data-ttu-id="be43d-108">示例</span><span class="sxs-lookup"><span data-stu-id="be43d-108">EXAMPLES</span></span>

### <span data-ttu-id="be43d-109">範例1：移除警示規則</span><span class="sxs-lookup"><span data-stu-id="be43d-109">Example 1: Remove an alert rule</span></span>
```
PS C:\>Remove-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="be43d-110">這個命令會在資源群組中移除名為 myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 的警示規則，預設為 [Web-CentralUS]。</span><span class="sxs-lookup"><span data-stu-id="be43d-110">This command removes the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8 in the resource group Default-Web-CentralUS.</span></span>

## <span data-ttu-id="be43d-111">參數</span><span class="sxs-lookup"><span data-stu-id="be43d-111">PARAMETERS</span></span>

### <span data-ttu-id="be43d-112">-名稱</span><span class="sxs-lookup"><span data-stu-id="be43d-112">-Name</span></span>
<span data-ttu-id="be43d-113">指定要移除之警示規則的名稱。</span><span class="sxs-lookup"><span data-stu-id="be43d-113">Specifies the name of the alert rule to remove.</span></span>

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

### <span data-ttu-id="be43d-114">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="be43d-114">-ResourceGroup</span></span>
<span data-ttu-id="be43d-115">指定警示規則之資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="be43d-115">Specifies the name of the resource group for the alert rule.</span></span>

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

### <span data-ttu-id="be43d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be43d-116">-DefaultProfile</span></span>
<span data-ttu-id="be43d-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="be43d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be43d-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be43d-118">CommonParameters</span></span>
<span data-ttu-id="be43d-119">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="be43d-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be43d-120">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="be43d-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be43d-121">輸入</span><span class="sxs-lookup"><span data-stu-id="be43d-121">INPUTS</span></span>

## <span data-ttu-id="be43d-122">輸出</span><span class="sxs-lookup"><span data-stu-id="be43d-122">OUTPUTS</span></span>

### <span data-ttu-id="be43d-123">[System.object]. 清單 ' 1 [AzureOperationResponse]</span><span class="sxs-lookup"><span data-stu-id="be43d-123">System.Collections.Generic.List\`1[Microsoft.Azure.AzureOperationResponse]</span></span>

## <span data-ttu-id="be43d-124">筆記</span><span class="sxs-lookup"><span data-stu-id="be43d-124">NOTES</span></span>

## <span data-ttu-id="be43d-125">相關連結</span><span class="sxs-lookup"><span data-stu-id="be43d-125">RELATED LINKS</span></span>

[<span data-ttu-id="be43d-126">附加 AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="be43d-126">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="be43d-127">附加 AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="be43d-127">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="be43d-128">附加 AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="be43d-128">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="be43d-129">AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="be43d-129">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="be43d-130">AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="be43d-130">Get-AzureRmAlertRule</span></span>](./Get-AzureRmAlertRule.md)


