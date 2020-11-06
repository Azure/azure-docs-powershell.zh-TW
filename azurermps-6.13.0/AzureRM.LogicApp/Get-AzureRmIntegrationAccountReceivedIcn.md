---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/get-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Get-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: b9defadc92619d136c82302203d296d6b71318ee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93448394"
---
# <span data-ttu-id="79902-101">Get-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="79902-101">Get-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="79902-102">摘要</span><span class="sxs-lookup"><span data-stu-id="79902-102">SYNOPSIS</span></span>
<span data-ttu-id="79902-103">這個 Cmdlet 會針對每個協定和控制編號值來檢索特定接收的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="79902-103">This cmdlet retrieves a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79902-104">句法</span><span class="sxs-lookup"><span data-stu-id="79902-104">SYNTAX</span></span>

```
Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="79902-105">說明</span><span class="sxs-lookup"><span data-stu-id="79902-105">DESCRIPTION</span></span>
<span data-ttu-id="79902-106">這個 Cmdlet 是用來在災害復原案例中使用，以驗證收到的交換控制號碼是否存在，以及選擇是否要移除該實體與 Remove AzureRmIntegrationAccountReceivedIcn。</span><span class="sxs-lookup"><span data-stu-id="79902-106">This cmdlet is meant to be used in disaster recovery scenarios to validate the presence of a received interchange control number and optionally to remove that entity with Remove-AzureRmIntegrationAccountReceivedIcn.</span></span>
<span data-ttu-id="79902-107">請提供 "-AgreementType" 參數，以指定要傳回的 X12 或 Edifact 控制編號</span><span class="sxs-lookup"><span data-stu-id="79902-107">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="79902-108">示例</span><span class="sxs-lookup"><span data-stu-id="79902-108">EXAMPLES</span></span>

### <span data-ttu-id="79902-109">範例1</span><span class="sxs-lookup"><span data-stu-id="79902-109">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="79902-110">這個命令會透過 [協定名稱] 和 [控制編號] 值來取得 [X12 整合] 帳戶收到的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="79902-110">This command gets the X12 integration account received interchange control number by agreement name and control number value.</span></span>

### <span data-ttu-id="79902-111">範例2</span><span class="sxs-lookup"><span data-stu-id="79902-111">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
ControlNumber            : 000000641
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed: False
```

<span data-ttu-id="79902-112">這個命令會透過 [合約名稱] 和 [控制編號] 值來取得已收到交換控制編號的 Edifact 整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="79902-112">This command gets the Edifact integration account received interchange control number by agreement name and control number value.</span></span>

## <span data-ttu-id="79902-113">參數</span><span class="sxs-lookup"><span data-stu-id="79902-113">PARAMETERS</span></span>

### <span data-ttu-id="79902-114">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="79902-114">-AgreementName</span></span>
<span data-ttu-id="79902-115">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="79902-115">The integration account agreement name.</span></span>

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

### <span data-ttu-id="79902-116">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="79902-116">-AgreementType</span></span>
<span data-ttu-id="79902-117">整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="79902-117">The integration account agreement type.</span></span>

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

### <span data-ttu-id="79902-118">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="79902-118">-ControlNumberValue</span></span>
<span data-ttu-id="79902-119">[整合帳戶控制編號] 值。</span><span class="sxs-lookup"><span data-stu-id="79902-119">The integration account control number value.</span></span>

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

### <span data-ttu-id="79902-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79902-120">-DefaultProfile</span></span>
<span data-ttu-id="79902-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="79902-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79902-122">-名稱</span><span class="sxs-lookup"><span data-stu-id="79902-122">-Name</span></span>
<span data-ttu-id="79902-123">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="79902-123">The integration account name.</span></span>

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

### <span data-ttu-id="79902-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79902-124">-ResourceGroupName</span></span>
<span data-ttu-id="79902-125">整合帳戶資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="79902-125">The integration account resource group name.</span></span>

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

### <span data-ttu-id="79902-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79902-126">CommonParameters</span></span>
<span data-ttu-id="79902-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="79902-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79902-128">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="79902-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79902-129">輸入</span><span class="sxs-lookup"><span data-stu-id="79902-129">INPUTS</span></span>

### <span data-ttu-id="79902-130">System.object</span><span class="sxs-lookup"><span data-stu-id="79902-130">System.String</span></span>

## <span data-ttu-id="79902-131">輸出</span><span class="sxs-lookup"><span data-stu-id="79902-131">OUTPUTS</span></span>

### <span data-ttu-id="79902-132">IntegrationAccountControlNumber （LogicApp）。</span><span class="sxs-lookup"><span data-stu-id="79902-132">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="79902-133">筆記</span><span class="sxs-lookup"><span data-stu-id="79902-133">NOTES</span></span>

## <span data-ttu-id="79902-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="79902-134">RELATED LINKS</span></span>

[<span data-ttu-id="79902-135">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="79902-135">Set-AzureRmIntegrationAccountReceivedIcn</span></span>](./Set-AzureRmIntegrationAccountReceivedIcn.md)

[<span data-ttu-id="79902-136">移除-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="79902-136">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>](./Remove-AzureRmIntegrationAccountReceivedIcn.md)
