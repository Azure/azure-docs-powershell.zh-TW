---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountReceivedIcn.md
ms.openlocfilehash: a87ccecbba21479c24a2defd2d7443f66184a799
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101904405"
---
# <span data-ttu-id="daf81-101">Remove-AzIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="daf81-101">Remove-AzIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="daf81-102">簡介</span><span class="sxs-lookup"><span data-stu-id="daf81-102">SYNOPSIS</span></span>
<span data-ttu-id="daf81-103">此 Cmdlet 會移除每個協定的特定接收交換控制項編號及控制項編號值。</span><span class="sxs-lookup"><span data-stu-id="daf81-103">This cmdlet removes a specific received interchange control number per agreement and control number value.</span></span>

## <span data-ttu-id="daf81-104">語法</span><span class="sxs-lookup"><span data-stu-id="daf81-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="daf81-105">描述</span><span class="sxs-lookup"><span data-stu-id="daf81-105">DESCRIPTION</span></span>
<span data-ttu-id="daf81-106">此 Cmdlet 旨在用於災害復原案例，以從整合帳戶移除收到的交換控制編號，讓 B2B 連接器在啟用重複數位偵測時，可以再次處理郵件。</span><span class="sxs-lookup"><span data-stu-id="daf81-106">This cmdlet is meant to be used in disaster recovery scenarios to remove a received interchange control number from the integration account so that the B2B connector may process again the message when duplicate number detection is enabled.</span></span>
<span data-ttu-id="daf81-107">在少數情況下，接收的交換控制號碼可能在發生災害前和 B2B 連接器拒絕交換之前保留為錯誤。</span><span class="sxs-lookup"><span data-stu-id="daf81-107">In rare occasions the received interchange control number may be reserved shortly before a disaster and before the B2B connector rejects the interchange as erroneous.</span></span>
<span data-ttu-id="daf81-108">在這類情況下，作業可能會想要讓修復網站在有效負載修正之後，再次處理相同的交換。</span><span class="sxs-lookup"><span data-stu-id="daf81-108">In such occasions the operation may want to enable the recovery site to process again the same interchange after its payload is corrected.</span></span>
<span data-ttu-id="daf81-109">請提供 "-AgreementType" 參數，以指定要傳回 X12 或 Edifact 控制項編號</span><span class="sxs-lookup"><span data-stu-id="daf81-109">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="daf81-110">例子</span><span class="sxs-lookup"><span data-stu-id="daf81-110">EXAMPLES</span></span>

### <span data-ttu-id="daf81-111">範例 1</span><span class="sxs-lookup"><span data-stu-id="daf81-111">Example 1</span></span>
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

<span data-ttu-id="daf81-112">嘗試取得接收的 X12 交換控制項編號，其中的內容不是有效的格式。</span><span class="sxs-lookup"><span data-stu-id="daf81-112">Attempts to get a received X12 interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="daf81-113">移除收到的 X12 交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="daf81-113">Removes the received X12 interchange control number.</span></span>
<span data-ttu-id="daf81-114">嘗試再次取得，以確認已收到的 X12 交換控制號碼已移除。</span><span class="sxs-lookup"><span data-stu-id="daf81-114">Confirms the received X12 interchange control number was removed by attempting to get it again.</span></span>

### <span data-ttu-id="daf81-115">範例 2</span><span class="sxs-lookup"><span data-stu-id="daf81-115">Example 2</span></span>
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

<span data-ttu-id="daf81-116">嘗試取得收到的 Edifact 交換控制項編號，其中的內容不是有效格式。</span><span class="sxs-lookup"><span data-stu-id="daf81-116">Attempts to get a received Edifact interchange control number which content is not in a valid format.</span></span>
<span data-ttu-id="daf81-117">移除收到的 Edifact 交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="daf81-117">Removes the received Edifact interchange control number.</span></span>
<span data-ttu-id="daf81-118">嘗試再次取得，以確認已收到的 Edifact 交換控制編號已移除。</span><span class="sxs-lookup"><span data-stu-id="daf81-118">Confirms the received Edifact interchange control number was removed by attempting to get it again.</span></span>

## <span data-ttu-id="daf81-119">參數</span><span class="sxs-lookup"><span data-stu-id="daf81-119">PARAMETERS</span></span>

### <span data-ttu-id="daf81-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="daf81-120">-AgreementName</span></span>
<span data-ttu-id="daf81-121">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="daf81-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="daf81-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="daf81-122">-AgreementType</span></span>
<span data-ttu-id="daf81-123">整合帳戶協定類型。</span><span class="sxs-lookup"><span data-stu-id="daf81-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="daf81-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="daf81-124">-ControlNumberValue</span></span>
<span data-ttu-id="daf81-125">整合帳戶控制項數位值。</span><span class="sxs-lookup"><span data-stu-id="daf81-125">The integration account control number value.</span></span>

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

### <span data-ttu-id="daf81-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="daf81-126">-DefaultProfile</span></span>
<span data-ttu-id="daf81-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="daf81-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="daf81-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="daf81-128">-Name</span></span>
<span data-ttu-id="daf81-129">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="daf81-129">The integration account name.</span></span>

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

### <span data-ttu-id="daf81-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="daf81-130">-ResourceGroupName</span></span>
<span data-ttu-id="daf81-131">整合帳戶資源組名。</span><span class="sxs-lookup"><span data-stu-id="daf81-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="daf81-132">-確認</span><span class="sxs-lookup"><span data-stu-id="daf81-132">-Confirm</span></span>
<span data-ttu-id="daf81-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="daf81-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="daf81-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="daf81-134">-WhatIf</span></span>
<span data-ttu-id="daf81-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="daf81-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="daf81-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="daf81-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="daf81-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf81-137">CommonParameters</span></span>
<span data-ttu-id="daf81-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="daf81-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf81-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="daf81-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf81-140">輸入</span><span class="sxs-lookup"><span data-stu-id="daf81-140">INPUTS</span></span>

### <span data-ttu-id="daf81-141">System.String</span><span class="sxs-lookup"><span data-stu-id="daf81-141">System.String</span></span>

## <span data-ttu-id="daf81-142">輸出</span><span class="sxs-lookup"><span data-stu-id="daf81-142">OUTPUTS</span></span>

### <span data-ttu-id="daf81-143">System.Void</span><span class="sxs-lookup"><span data-stu-id="daf81-143">System.Void</span></span>

## <span data-ttu-id="daf81-144">筆記</span><span class="sxs-lookup"><span data-stu-id="daf81-144">NOTES</span></span>

## <span data-ttu-id="daf81-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="daf81-145">RELATED LINKS</span></span>

<span data-ttu-id="daf81-146">[Get-AzCountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md) 
[Set-AzCountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="daf81-146">[Get-AzIntegrationAccountReceivedIcn](./Get-AzIntegrationAccountReceivedIcn.md)
[Set-AzIntegrationAccountReceivedIcn](./Set-AzIntegrationAccountReceivedIcn.md)</span></span>

