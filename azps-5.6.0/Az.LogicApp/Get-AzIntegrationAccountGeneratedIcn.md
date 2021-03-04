---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/get-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: b6bf2c126a1009d824ab8bae1ea2e2031459d876
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904074"
---
# <span data-ttu-id="a315a-101">Get-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="a315a-101">Get-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="a315a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="a315a-102">SYNOPSIS</span></span>
<span data-ttu-id="a315a-103">此 Cmdlet 會根據協定，從產生的交換控制項編號中，取回目前的值。</span><span class="sxs-lookup"><span data-stu-id="a315a-103">This cmdlet retrieves the current value of the generated interchange control number per agreement.</span></span>

## <span data-ttu-id="a315a-104">語法</span><span class="sxs-lookup"><span data-stu-id="a315a-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> [-AgreementName <String>]
 [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a315a-105">描述</span><span class="sxs-lookup"><span data-stu-id="a315a-105">DESCRIPTION</span></span>
<span data-ttu-id="a315a-106">此 Cmdlet 旨在用於災害復原案例，以取回產生的交換控制項編號目前的值，以便使用 Set-Az ScenarioAccountGeneratedIcn 回寫增加的值。</span><span class="sxs-lookup"><span data-stu-id="a315a-106">This cmdlet is meant to be used in disaster recovery scenarios to retrieve the current value of the generated interchange control number so to write back an increased value with Set-AzIntegrationAccountGeneratedIcn.</span></span>
<span data-ttu-id="a315a-107">交換控制號碼應該增加，以避免在作用中地區發生災害時，無法複製到被動區域的數位重複的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="a315a-107">The interchange control number should be increased to avoid duplicate interchange control numbers for the numbers that could not yet be replicated to the passive region when the disaster happened in the active region.</span></span>
<span data-ttu-id="a315a-108">請提供 "-AgreementType" 參數，以指定要傳回 X12 或 Edifact 控制項編號</span><span class="sxs-lookup"><span data-stu-id="a315a-108">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="a315a-109">例子</span><span class="sxs-lookup"><span data-stu-id="a315a-109">EXAMPLES</span></span>

### <span data-ttu-id="a315a-110">範例 1</span><span class="sxs-lookup"><span data-stu-id="a315a-110">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="a315a-111">此命令會根據協定名稱，獲得整合帳戶產生的 X12 交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="a315a-111">This command gets the integration account generated X12 interchange control number by agreement name.</span></span> <span data-ttu-id="a315a-112">請確定指定的協定類型為 "X12"</span><span class="sxs-lookup"><span data-stu-id="a315a-112">Please make sure agreement specified is of type "X12"</span></span>

### <span data-ttu-id="a315a-113">範例 2</span><span class="sxs-lookup"><span data-stu-id="a315a-113">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement"
ControlNumber            : 1000
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="a315a-114">此命令會以協定名稱獲得整合帳戶產生的 Edifact 交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="a315a-114">This command gets the integration account generated Edifact interchange control number by agreement name.</span></span> <span data-ttu-id="a315a-115">請確定指定的協定類型為"Edifact"</span><span class="sxs-lookup"><span data-stu-id="a315a-115">Please make sure agreement specified is of type "Edifact"</span></span>

### <span data-ttu-id="a315a-116">範例 3</span><span class="sxs-lookup"><span data-stu-id="a315a-116">Example 3</span></span>
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

<span data-ttu-id="a315a-117">此命令會根據整合帳戶名稱，獲得所有產生的 X12 交換控制項編號。</span><span class="sxs-lookup"><span data-stu-id="a315a-117">This command gets all the generated X12 interchange control numbers by integration account name.</span></span>

## <span data-ttu-id="a315a-118">參數</span><span class="sxs-lookup"><span data-stu-id="a315a-118">PARAMETERS</span></span>

### <span data-ttu-id="a315a-119">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="a315a-119">-AgreementName</span></span>
<span data-ttu-id="a315a-120">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="a315a-120">The integration account agreement name.</span></span>

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

### <span data-ttu-id="a315a-121">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="a315a-121">-AgreementType</span></span>
<span data-ttu-id="a315a-122">整合帳戶協定類型。</span><span class="sxs-lookup"><span data-stu-id="a315a-122">The integration account agreement type.</span></span>

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

### <span data-ttu-id="a315a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a315a-123">-DefaultProfile</span></span>
<span data-ttu-id="a315a-124">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="a315a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a315a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="a315a-125">-Name</span></span>
<span data-ttu-id="a315a-126">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="a315a-126">The integration account name.</span></span>

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

### <span data-ttu-id="a315a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a315a-127">-ResourceGroupName</span></span>
<span data-ttu-id="a315a-128">整合帳戶資源組名。</span><span class="sxs-lookup"><span data-stu-id="a315a-128">The integration account resource group name.</span></span>

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

### <span data-ttu-id="a315a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a315a-129">CommonParameters</span></span>
<span data-ttu-id="a315a-130">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="a315a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a315a-131">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="a315a-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a315a-132">輸入</span><span class="sxs-lookup"><span data-stu-id="a315a-132">INPUTS</span></span>

### <span data-ttu-id="a315a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="a315a-133">System.String</span></span>

## <span data-ttu-id="a315a-134">輸出</span><span class="sxs-lookup"><span data-stu-id="a315a-134">OUTPUTS</span></span>

### <span data-ttu-id="a315a-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="a315a-135">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="a315a-136">筆記</span><span class="sxs-lookup"><span data-stu-id="a315a-136">NOTES</span></span>

## <span data-ttu-id="a315a-137">相關連結</span><span class="sxs-lookup"><span data-stu-id="a315a-137">RELATED LINKS</span></span>

[<span data-ttu-id="a315a-138">Set-AzCountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="a315a-138">Set-AzIntegrationAccountGeneratedIcn</span></span>](./Set-AzIntegrationAccountGeneratedIcn.md)

