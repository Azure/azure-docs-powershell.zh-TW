---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 0dffb7a99e29ea4cc595cad1b5b92450e83289f4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "94127776"
---
# <span data-ttu-id="8416c-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="8416c-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="8416c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="8416c-102">SYNOPSIS</span></span>
<span data-ttu-id="8416c-103">這個 Cmdlet 會針對每個協定檢索產生的交換控制編號的目前值。</span><span class="sxs-lookup"><span data-stu-id="8416c-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="8416c-104">句法</span><span class="sxs-lookup"><span data-stu-id="8416c-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8416c-105">說明</span><span class="sxs-lookup"><span data-stu-id="8416c-105">DESCRIPTION</span></span>
<span data-ttu-id="8416c-106">這個 Cmdlet 是用來在災害復原案例中用來檢索所產生交換控制編號的目前值，以便使用 AzIntegrationAccountGeneratedIcn 寫回增加的值。</span><span class="sxs-lookup"><span data-stu-id="8416c-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="8416c-107">應增加交換控制編號，以避免在使用中區域發生災難時，無法複製到被動區域之數位的重複交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="8416c-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="8416c-108">請提供 "-AgreementType" 參數，以指定要傳回的 X12 或 Edifact 控制編號</span><span class="sxs-lookup"><span data-stu-id="8416c-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="8416c-109">示例</span><span class="sxs-lookup"><span data-stu-id="8416c-109">EXAMPLES</span></span>

### <span data-ttu-id="8416c-110">範例1</span><span class="sxs-lookup"><span data-stu-id="8416c-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="8416c-111">這個命令會根據協定名稱，取得整合帳戶產生的 X12 交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="8416c-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="8416c-112">請確定指定的協定類型為 "X12"</span><span class="sxs-lookup"><span data-stu-id="8416c-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="8416c-113">範例2</span><span class="sxs-lookup"><span data-stu-id="8416c-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="8416c-114">這個命令會根據協定名稱，透過 [整合] 帳戶產生的 Edifact 交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="8416c-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="8416c-115">請確定指定的合約為 "Edifact" 類型</span><span class="sxs-lookup"><span data-stu-id="8416c-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="8416c-116">範例3</span><span class="sxs-lookup"><span data-stu-id="8416c-116">Example 3</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1"
ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement1
IsMessageProcessingFailed:

ControlNumber            : 1000
ControlNumberChangedTime : 2/22/2017 8:05:41 PM
AgreementName            : X12IntegrationAccountAgreement2
IsMessageProcessingFailed:

ControlNumber            : No generated control number was found for this agreement.
ControlNumberChangedTime : 1/1/0001 12:00:00 AM
AgreementName            : X12IntegrationAccountAgreement3
IsMessageProcessingFailed:
```

<span data-ttu-id="8416c-117">這個命令會透過整合帳戶名稱來取得所有產生的 X12 交換控制號碼。</span><span class="sxs-lookup"><span data-stu-id="8416c-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="8416c-118">參數</span><span class="sxs-lookup"><span data-stu-id="8416c-118">PARAMETERS</span></span>

### <span data-ttu-id="8416c-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="8416c-119">-AgreementName</span></span>
<span data-ttu-id="8416c-120">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="8416c-120">The integration account agreement name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8416c-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="8416c-121">-AgreementType</span></span>
<span data-ttu-id="8416c-122">整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="8416c-122">The integration account agreement type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8416c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8416c-123">-DefaultProfile</span></span>
<span data-ttu-id="8416c-124">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="8416c-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8416c-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="8416c-125">-Name</span></span>
<span data-ttu-id="8416c-126">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="8416c-126">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8416c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8416c-127">-ResourceGroupName</span></span>
<span data-ttu-id="8416c-128">整合帳戶資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="8416c-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="8416c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8416c-129">CommonParameters</span></span>
<span data-ttu-id="8416c-130">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="8416c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8416c-131">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="8416c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8416c-132">輸入</span><span class="sxs-lookup"><span data-stu-id="8416c-132">INPUTS</span></span>

### <span data-ttu-id="8416c-133">System.object</span><span class="sxs-lookup"><span data-stu-id="8416c-133">System.String</span></span>

## <span data-ttu-id="8416c-134">輸出</span><span class="sxs-lookup"><span data-stu-id="8416c-134">OUTPUTS</span></span>

### <span data-ttu-id="8416c-135">IntegrationAccountControlNumber （LogicApp）。</span><span class="sxs-lookup"><span data-stu-id="8416c-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="8416c-136">筆記</span><span class="sxs-lookup"><span data-stu-id="8416c-136">NOTES</span></span>

## <span data-ttu-id="8416c-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="8416c-137">RELATED LINKS</span></span>

[<span data-ttu-id="8416c-138">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="8416c-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)
