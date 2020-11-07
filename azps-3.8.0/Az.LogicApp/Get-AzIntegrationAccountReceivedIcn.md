---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: d7c6e5cfc1462e0ae807c9cdddb2d743a7608738
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93797626"
---
# <span data-ttu-id="05279-101">Get-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="05279-101">Get-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="05279-102">摘要</span><span class="sxs-lookup"><span data-stu-id="05279-102">SYNOPSIS</span></span>
<span data-ttu-id="05279-103">這個 Cmdlet 會針對每個協定和控制編號值來檢索特定接收的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="05279-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="05279-104">句法</span><span class="sxs-lookup"><span data-stu-id="05279-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="05279-105">說明</span><span class="sxs-lookup"><span data-stu-id="05279-105">DESCRIPTION</span></span>
<span data-ttu-id="05279-106">這個 Cmdlet 是用來在災害復原案例中使用，以驗證收到的交換控制號碼是否存在，以及選擇是否要移除該實體與 Remove AzIntegrationAccountReceivedIcn。</span><span class="sxs-lookup"><span data-stu-id="05279-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="05279-107">請提供 "-AgreementType" 參數，以指定要傳回的 X12 或 Edifact 控制編號</span><span class="sxs-lookup"><span data-stu-id="05279-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="05279-108">示例</span><span class="sxs-lookup"><span data-stu-id="05279-108">EXAMPLES</span></span>

### <span data-ttu-id="05279-109">範例1</span><span class="sxs-lookup"><span data-stu-id="05279-109">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="05279-110">這個命令會透過 [協定名稱] 和 [控制編號] 值來取得 [X12 整合] 帳戶收到的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="05279-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="05279-111">範例2</span><span class="sxs-lookup"><span data-stu-id="05279-111">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="05279-112">這個命令會透過 [合約名稱] 和 [控制編號] 值來取得已收到交換控制編號的 Edifact 整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="05279-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="05279-113">參數</span><span class="sxs-lookup"><span data-stu-id="05279-113">PARAMETERS</span></span>

### <span data-ttu-id="05279-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="05279-114">-AgreementName</span></span>
<span data-ttu-id="05279-115">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="05279-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="05279-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="05279-116">-AgreementType</span></span>
<span data-ttu-id="05279-117">整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="05279-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="05279-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="05279-118">-ControlNumberValue</span></span>
<span data-ttu-id="05279-119">[整合帳戶控制編號] 值。</span><span class="sxs-lookup"><span data-stu-id="05279-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="05279-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05279-120">-DefaultProfile</span></span>
<span data-ttu-id="05279-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="05279-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05279-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="05279-122">-Name</span></span>
<span data-ttu-id="05279-123">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="05279-123">The integration account name.</span></span>

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

### <span data-ttu-id="05279-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05279-124">-ResourceGroupName</span></span>
<span data-ttu-id="05279-125">整合帳戶資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="05279-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="05279-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05279-126">CommonParameters</span></span>
<span data-ttu-id="05279-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="05279-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05279-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="05279-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05279-129">輸入</span><span class="sxs-lookup"><span data-stu-id="05279-129">INPUTS</span></span>

### <span data-ttu-id="05279-130">System.object</span><span class="sxs-lookup"><span data-stu-id="05279-130">System.String</span></span>

## <span data-ttu-id="05279-131">輸出</span><span class="sxs-lookup"><span data-stu-id="05279-131">OUTPUTS</span></span>

### <span data-ttu-id="05279-132">IntegrationAccountControlNumber （LogicApp）。</span><span class="sxs-lookup"><span data-stu-id="05279-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="05279-133">筆記</span><span class="sxs-lookup"><span data-stu-id="05279-133">NOTES</span></span>

## <span data-ttu-id="05279-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="05279-134">RELATED LINKS</span></span>

[<span data-ttu-id="05279-135">Set-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="05279-135">Set-AzIntegrationAccountReceivedIcn</span></span>](./Set-AzIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="05279-136">移除-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="05279-136">Remove-AzIntegrationAccountReceivedIcn</span></span>](./Remove-AzIntegrationAccountReceivedIcn.md)
