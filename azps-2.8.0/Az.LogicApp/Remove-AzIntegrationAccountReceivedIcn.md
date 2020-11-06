---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 416a5991be227364e4374d3e4c0e64caa3095b9e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611971"
---
# <span data-ttu-id="1ce4c-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="1ce4c-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="1ce4c-102">摘要</span><span class="sxs-lookup"><span data-stu-id="1ce4c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ce4c-103">這個 Cmdlet 會移除每個協定與控制編號值的特定接收交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="1ce4c-104">句法</span><span class="sxs-lookup"><span data-stu-id="1ce4c-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ce4c-105">說明</span><span class="sxs-lookup"><span data-stu-id="1ce4c-105">DESCRIPTION</span></span>
<span data-ttu-id="1ce4c-106">這個 Cmdlet 是用來在災害復原案例中，從整合帳戶中移除接收到的交換控制編號，讓 B2B 連接器在啟用重複的數位檢測時也可以再次處理訊息。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="1ce4c-107">在少數情況下，收到的交換控制號碼可能會在災難之前保留，在 B2B 連接器拒絕交換是錯誤的之前。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="1ce4c-108">在這種情況下，該作業可能會想要讓恢復網站在其負載得到修正之後，再次處理相同的交換。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="1ce4c-109">請提供 "-AgreementType" 參數，以指定要傳回的 X12 或 Edifact 控制編號</span><span class="sxs-lookup"><span data-stu-id="1ce4c-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="1ce4c-110">示例</span><span class="sxs-lookup"><span data-stu-id="1ce4c-110">EXAMPLES</span></span>

### <span data-ttu-id="1ce4c-111">範例1</span><span class="sxs-lookup"><span data-stu-id="1ce4c-111">Example 1</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'X12AgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "X12" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "X12AgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'X12-ICN-X12AgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="1ce4c-112">嘗試取得已收到的 X12 交換控制編號內容格式不正確。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="1ce4c-113">移除接收的 X12 交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="1ce4c-114">再次嘗試再次取得，以確認接收到的 X12 交換控制編號已移除。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="1ce4c-115">範例2</span><span class="sxs-lookup"><span data-stu-id="1ce4c-115">Example 2</span></span>
```
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The existing received control number '000000641' for agreement 'EdifactAgreementName' is not in a valid format.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], PSInvalidOperationException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand

PS C:\> Remove-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
PS C:\> Get-AzIntegrationAccountReceivedIcn -AgreementType "Edifact" -ResourceGroupName "groupName" -Name "accountName" -AgreementName "EdifactAgreementName" -ControlNumberValue "000000641"
Get-AzIntegrationAccountReceivedIcn : The session 'Edifact-ICN-EdifactAgreementName-000000641' could not be found in integration account 'accountName'.
At line:1 char:1
+ Get-AzIntegrationAccountReceivedIcn -ResourceGroupName "groupName ...
+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : CloseError: (:) [Get-AzIntegrationAccountReceivedIcn], CloudException
    + FullyQualifiedErrorId : Microsoft.Azure.Commands.LogicApp.Cmdlets.GetAzureIntegrationAccountReceivedIcnCommand
```

<span data-ttu-id="1ce4c-116">嘗試取得所收到的 Edifact 交換控制編號內容不是有效格式。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="1ce4c-117">移除接收的 Edifact 交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="1ce4c-118">再次嘗試再次取得所接收的 Edifact 交換控制編號，以確認已移除。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="1ce4c-119">參數</span><span class="sxs-lookup"><span data-stu-id="1ce4c-119">PARAMETERS</span></span>

### <span data-ttu-id="1ce4c-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="1ce4c-120">-AgreementName</span></span>
<span data-ttu-id="1ce4c-121">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="1ce4c-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="1ce4c-122">-AgreementType</span></span>
<span data-ttu-id="1ce4c-123">整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="1ce4c-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="1ce4c-124">-ControlNumberValue</span></span>
<span data-ttu-id="1ce4c-125">[整合帳戶控制編號] 值。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="1ce4c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ce4c-126">-DefaultProfile</span></span>
<span data-ttu-id="1ce4c-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="1ce4c-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1ce4c-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="1ce4c-128">-Name</span></span>
<span data-ttu-id="1ce4c-129">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-129">The integration account name.</span></span>

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

### <span data-ttu-id="1ce4c-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ce4c-130">-ResourceGroupName</span></span>
<span data-ttu-id="1ce4c-131">整合帳戶資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="1ce4c-132">-確認</span><span class="sxs-lookup"><span data-stu-id="1ce4c-132">-Confirm</span></span>
<span data-ttu-id="1ce4c-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ce4c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ce4c-134">-WhatIf</span></span>
<span data-ttu-id="1ce4c-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1ce4c-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ce4c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ce4c-137">CommonParameters</span></span>
<span data-ttu-id="1ce4c-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ce4c-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="1ce4c-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ce4c-140">輸入</span><span class="sxs-lookup"><span data-stu-id="1ce4c-140">INPUTS</span></span>

### <span data-ttu-id="1ce4c-141">System.object</span><span class="sxs-lookup"><span data-stu-id="1ce4c-141">System.String</span></span>

## <span data-ttu-id="1ce4c-142">輸出</span><span class="sxs-lookup"><span data-stu-id="1ce4c-142">OUTPUTS</span></span>

### <span data-ttu-id="1ce4c-143">System.void</span><span class="sxs-lookup"><span data-stu-id="1ce4c-143">System.Void</span></span>

## <span data-ttu-id="1ce4c-144">筆記</span><span class="sxs-lookup"><span data-stu-id="1ce4c-144">NOTES</span></span>

## <span data-ttu-id="1ce4c-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="1ce4c-145">RELATED LINKS</span></span>

<span data-ttu-id="1ce4c-146">[AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="1ce4c-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

