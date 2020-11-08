---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: fa02d7ffc23706564b8b6fe118f12525829b27f8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/13/2020
ms.locfileid: "93971022"
---
# <span data-ttu-id="f5080-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="f5080-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="f5080-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5080-102">SYNOPSIS</span></span>
<span data-ttu-id="f5080-103">更新 Azure 資源群組中 (ICN) 的整合帳戶產生的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="f5080-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="f5080-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5080-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5080-105">說明</span><span class="sxs-lookup"><span data-stu-id="f5080-105">DESCRIPTION</span></span>
<span data-ttu-id="f5080-106">Set-AzIntegrationAccountGeneratedIcn Cmdlet 會更新現有的整合帳戶， (ICN) 產生交換控制編號，並傳回代表整合帳戶產生的交換控制編號的物件。</span><span class="sxs-lookup"><span data-stu-id="f5080-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="f5080-107">使用此 Cmdlet 來更新產生交換控制編號的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="f5080-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="f5080-108">您可以指定整合帳戶名稱、資源群組名稱和協定名稱，以更新產生交換控制編號的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="f5080-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="f5080-109">您無法使用此命令建立新的整合帳戶產生的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="f5080-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="f5080-110">若要使用動態參數，只要在命令中輸入，或輸入連字號符號 ( ) ，即可指定參數名稱，然後重複按 TAB 鍵，以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="f5080-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f5080-111">如果您遺漏了必要的範本參數，此 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="f5080-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="f5080-112">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="f5080-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="f5080-113">請提供 "-AgreementType" 參數，以指定要傳回的 X12 或 Edifact 控制編號</span><span class="sxs-lookup"><span data-stu-id="f5080-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="f5080-114">示例</span><span class="sxs-lookup"><span data-stu-id="f5080-114">EXAMPLES</span></span>

### <span data-ttu-id="f5080-115">範例1</span><span class="sxs-lookup"><span data-stu-id="f5080-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="f5080-116">這個命令會取得整合帳戶為特定整合帳戶協定產生的 X12 交換控制編號，並將其值增加100，然後寫回更新後的值。</span><span class="sxs-lookup"><span data-stu-id="f5080-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="f5080-117">範例2</span><span class="sxs-lookup"><span data-stu-id="f5080-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="f5080-118">這個命令會取得整合帳戶針對特定整合帳戶協定產生的 EdifactIntegrationAccountAgreement 交換控制編號，並將其值增加至100，然後寫回更新後的值。</span><span class="sxs-lookup"><span data-stu-id="f5080-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="f5080-119">參數</span><span class="sxs-lookup"><span data-stu-id="f5080-119">PARAMETERS</span></span>

### <span data-ttu-id="f5080-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="f5080-120">-AgreementName</span></span>
<span data-ttu-id="f5080-121">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="f5080-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="f5080-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="f5080-122">-AgreementType</span></span>
<span data-ttu-id="f5080-123">整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="f5080-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="f5080-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="f5080-124">-ControlNumber</span></span>
<span data-ttu-id="f5080-125">產生的控制項編號新值。</span><span class="sxs-lookup"><span data-stu-id="f5080-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="f5080-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5080-126">-DefaultProfile</span></span>
<span data-ttu-id="f5080-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f5080-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f5080-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5080-128">-Name</span></span>
<span data-ttu-id="f5080-129">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="f5080-129">The integration account name.</span></span>

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

### <span data-ttu-id="f5080-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5080-130">-ResourceGroupName</span></span>
<span data-ttu-id="f5080-131">整合帳戶資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="f5080-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="f5080-132">-確認</span><span class="sxs-lookup"><span data-stu-id="f5080-132">-Confirm</span></span>
<span data-ttu-id="f5080-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5080-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5080-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5080-134">-WhatIf</span></span>
<span data-ttu-id="f5080-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5080-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5080-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5080-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5080-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5080-137">CommonParameters</span></span>
<span data-ttu-id="f5080-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5080-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5080-139">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5080-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5080-140">輸入</span><span class="sxs-lookup"><span data-stu-id="f5080-140">INPUTS</span></span>

### <span data-ttu-id="f5080-141">System.object</span><span class="sxs-lookup"><span data-stu-id="f5080-141">System.String</span></span>

## <span data-ttu-id="f5080-142">輸出</span><span class="sxs-lookup"><span data-stu-id="f5080-142">OUTPUTS</span></span>

### <span data-ttu-id="f5080-143">IntegrationAccountControlNumber （LogicApp）。</span><span class="sxs-lookup"><span data-stu-id="f5080-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="f5080-144">筆記</span><span class="sxs-lookup"><span data-stu-id="f5080-144">NOTES</span></span>

## <span data-ttu-id="f5080-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5080-145">RELATED LINKS</span></span>

[<span data-ttu-id="f5080-146">AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="f5080-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)
