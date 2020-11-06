---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 429c2eefb9c5ba69b829e292522d168939170e06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93449781"
---
# <span data-ttu-id="7d6f3-101">Remove-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="7d6f3-101">Remove-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="7d6f3-102">摘要</span><span class="sxs-lookup"><span data-stu-id="7d6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="7d6f3-103">這個 Cmdlet 會移除每個協定與控制編號值的特定接收交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d6f3-104">句法</span><span class="sxs-lookup"><span data-stu-id="7d6f3-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d6f3-105">說明</span><span class="sxs-lookup"><span data-stu-id="7d6f3-105">DESCRIPTION</span></span>
<span data-ttu-id="7d6f3-106">這個 Cmdlet 是用來在災害復原案例中，從整合帳戶中移除接收到的交換控制編號，讓 B2B 連接器在啟用重複的數位檢測時也可以再次處理訊息。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="7d6f3-107">在少數情況下，收到的交換控制號碼可能會在災難之前保留，在 B2B 連接器拒絕交換是錯誤的之前。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="7d6f3-108">在這種情況下，該作業可能會想要讓恢復網站在其負載得到修正之後，再次處理相同的交換。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="7d6f3-109">請提供 "-AgreementType" 參數，以指定要傳回的 X12 或 Edifact 控制編號</span><span class="sxs-lookup"><span data-stu-id="7d6f3-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="7d6f3-110">示例</span><span class="sxs-lookup"><span data-stu-id="7d6f3-110">EXAMPLES</span></span>

### <span data-ttu-id="7d6f3-111">範例1</span><span class="sxs-lookup"><span data-stu-id="7d6f3-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="7d6f3-112">嘗試取得已收到的 X12 交換控制編號內容格式不正確。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="7d6f3-113">移除接收的 X12 交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="7d6f3-114">再次嘗試再次取得，以確認接收到的 X12 交換控制編號已移除。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="7d6f3-115">範例2</span><span class="sxs-lookup"><span data-stu-id="7d6f3-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The existing recevied control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzureRmIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzureRmIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzureRmIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="7d6f3-116">嘗試取得所收到的 Edifact 交換控制編號內容不是有效格式。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="7d6f3-117">移除接收的 Edifact 交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="7d6f3-118">再次嘗試再次取得所接收的 Edifact 交換控制編號，以確認已移除。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="7d6f3-119">參數</span><span class="sxs-lookup"><span data-stu-id="7d6f3-119">PARAMETERS</span></span>

### <span data-ttu-id="7d6f3-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="7d6f3-120">-AgreementName</span></span>
<span data-ttu-id="7d6f3-121">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="7d6f3-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="7d6f3-122">-AgreementType</span></span>
<span data-ttu-id="7d6f3-123">整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="7d6f3-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="7d6f3-124">-ControlNumberValue</span></span>
<span data-ttu-id="7d6f3-125">[整合帳戶控制編號] 值。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="7d6f3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d6f3-126">-DefaultProfile</span></span>
<span data-ttu-id="7d6f3-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="7d6f3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d6f3-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="7d6f3-128">-Name</span></span>
<span data-ttu-id="7d6f3-129">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-129">The integration account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d6f3-130">-ResourceGroupName</span></span>
<span data-ttu-id="7d6f3-131">整合帳戶資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="7d6f3-132">-確認</span><span class="sxs-lookup"><span data-stu-id="7d6f3-132">-Confirm</span></span>
<span data-ttu-id="7d6f3-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d6f3-134">-WhatIf</span></span>
<span data-ttu-id="7d6f3-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d6f3-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d6f3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d6f3-137">CommonParameters</span></span>
<span data-ttu-id="7d6f3-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d6f3-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="7d6f3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d6f3-140">輸入</span><span class="sxs-lookup"><span data-stu-id="7d6f3-140">INPUTS</span></span>

### <span data-ttu-id="7d6f3-141">System.object</span><span class="sxs-lookup"><span data-stu-id="7d6f3-141">System.String</span></span>

## <span data-ttu-id="7d6f3-142">輸出</span><span class="sxs-lookup"><span data-stu-id="7d6f3-142">OUTPUTS</span></span>

### <span data-ttu-id="7d6f3-143">System.void</span><span class="sxs-lookup"><span data-stu-id="7d6f3-143">System.Void</span></span>

## <span data-ttu-id="7d6f3-144">筆記</span><span class="sxs-lookup"><span data-stu-id="7d6f3-144">NOTES</span></span>

## <span data-ttu-id="7d6f3-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="7d6f3-145">RELATED LINKS</span></span>

<span data-ttu-id="7d6f3-146">[AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
[Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="7d6f3-146">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Set-AzureRmIntegrationAccountReceivedIcn](./Set-AzureRmIntegrationAccountReceivedIcn.md)</span></span>

