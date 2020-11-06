---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4dea211f2a09823161c1c6551b1fa00ab018a855
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93611953"
---
# <span data-ttu-id="ef827-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="ef827-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="ef827-102">摘要</span><span class="sxs-lookup"><span data-stu-id="ef827-102">SYNOPSIS</span></span>
<span data-ttu-id="ef827-103">更新 Azure 資源群組中 (ICN) 的整合帳戶產生的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="ef827-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="ef827-104">句法</span><span class="sxs-lookup"><span data-stu-id="ef827-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef827-105">說明</span><span class="sxs-lookup"><span data-stu-id="ef827-105">DESCRIPTION</span></span>
<span data-ttu-id="ef827-106">Set-AzIntegrationAccountGeneratedIcn Cmdlet 會更新現有的整合帳戶， (ICN) 產生交換控制編號，並傳回代表整合帳戶產生的交換控制編號的物件。</span><span class="sxs-lookup"><span data-stu-id="ef827-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="ef827-107">使用此 Cmdlet 來更新產生交換控制編號的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="ef827-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="ef827-108">您可以指定整合帳戶名稱、資源群組名稱和協定名稱，以更新產生交換控制編號的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="ef827-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="ef827-109">您無法使用此命令建立新的整合帳戶產生的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="ef827-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="ef827-110">若要使用動態參數，只要在命令中輸入，或輸入連字號符號 ( ) ，即可指定參數名稱，然後重複按 TAB 鍵，以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="ef827-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ef827-111">如果您遺漏了必要的範本參數，此 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="ef827-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="ef827-112">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="ef827-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="ef827-113">請提供 "-AgreementType" 參數，以指定要傳回的 X12 或 Edifact 控制編號</span><span class="sxs-lookup"><span data-stu-id="ef827-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="ef827-114">示例</span><span class="sxs-lookup"><span data-stu-id="ef827-114">EXAMPLES</span></span>

### <span data-ttu-id="ef827-115">範例1</span><span class="sxs-lookup"><span data-stu-id="ef827-115">Example 1</span></span>
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

<span data-ttu-id="ef827-116">這個命令會取得整合帳戶為特定整合帳戶協定產生的 X12 交換控制編號，並將其值增加100，然後寫回更新後的值。</span><span class="sxs-lookup"><span data-stu-id="ef827-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="ef827-117">範例2</span><span class="sxs-lookup"><span data-stu-id="ef827-117">Example 2</span></span>
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

<span data-ttu-id="ef827-118">這個命令會取得整合帳戶針對特定整合帳戶協定產生的 EdifactIntegrationAccountAgreement 交換控制編號，並將其值增加至100，然後寫回更新後的值。</span><span class="sxs-lookup"><span data-stu-id="ef827-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="ef827-119">參數</span><span class="sxs-lookup"><span data-stu-id="ef827-119">PARAMETERS</span></span>

### <span data-ttu-id="ef827-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="ef827-120">-AgreementName</span></span>
<span data-ttu-id="ef827-121">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="ef827-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="ef827-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="ef827-122">-AgreementType</span></span>
<span data-ttu-id="ef827-123">整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="ef827-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="ef827-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="ef827-124">-ControlNumber</span></span>
<span data-ttu-id="ef827-125">產生的控制項編號新值。</span><span class="sxs-lookup"><span data-stu-id="ef827-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="ef827-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef827-126">-DefaultProfile</span></span>
<span data-ttu-id="ef827-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="ef827-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef827-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="ef827-128">-Name</span></span>
<span data-ttu-id="ef827-129">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="ef827-129">The integration account name.</span></span>

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

### <span data-ttu-id="ef827-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef827-130">-ResourceGroupName</span></span>
<span data-ttu-id="ef827-131">整合帳戶資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="ef827-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="ef827-132">-確認</span><span class="sxs-lookup"><span data-stu-id="ef827-132">-Confirm</span></span>
<span data-ttu-id="ef827-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="ef827-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef827-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef827-134">-WhatIf</span></span>
<span data-ttu-id="ef827-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="ef827-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef827-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ef827-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef827-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef827-137">CommonParameters</span></span>
<span data-ttu-id="ef827-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="ef827-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef827-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="ef827-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef827-140">輸入</span><span class="sxs-lookup"><span data-stu-id="ef827-140">INPUTS</span></span>

### <span data-ttu-id="ef827-141">System.object</span><span class="sxs-lookup"><span data-stu-id="ef827-141">System.String</span></span>

## <span data-ttu-id="ef827-142">輸出</span><span class="sxs-lookup"><span data-stu-id="ef827-142">OUTPUTS</span></span>

### <span data-ttu-id="ef827-143">IntegrationAccountControlNumber （LogicApp）。</span><span class="sxs-lookup"><span data-stu-id="ef827-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="ef827-144">筆記</span><span class="sxs-lookup"><span data-stu-id="ef827-144">NOTES</span></span>

## <span data-ttu-id="ef827-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="ef827-145">RELATED LINKS</span></span>

[<span data-ttu-id="ef827-146">AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="ef827-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

