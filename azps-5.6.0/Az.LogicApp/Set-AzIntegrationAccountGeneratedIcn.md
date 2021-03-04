---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
online version: https://docs.microsoft.com/powershell/module/az.logicapp/set-azintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: 4c91ced490226901a45e0eacb7caa204daa20558
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101908125"
---
# <span data-ttu-id="6e4a5-101">Set-AzIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="6e4a5-101">Set-AzIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="6e4a5-102">簡介</span><span class="sxs-lookup"><span data-stu-id="6e4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="6e4a5-103">更新 Azure 資源群組中 (ICN) 整合帳戶產生的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

## <span data-ttu-id="6e4a5-104">語法</span><span class="sxs-lookup"><span data-stu-id="6e4a5-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e4a5-105">描述</span><span class="sxs-lookup"><span data-stu-id="6e4a5-105">DESCRIPTION</span></span>
<span data-ttu-id="6e4a5-106">此Set-AzIntegrationAccountGeneratedIcn Cmdlet 會更新現有的整合帳戶產生的交換控制編號 (ICN) ，並會返回代表整合帳戶產生的交換控制項編號的物件。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-106">The Set-AzIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="6e4a5-107">使用此 Cmdlet 更新整合帳戶產生的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="6e4a5-108">您可以指定整合帳戶名稱、資源組名和協定名稱，以更新整合帳戶產生的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="6e4a5-109">您無法使用此命令建立新整合帳戶產生的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="6e4a5-110">若要使用動態參數，只要在命令中輸入參數，或輸入連字號 (-) 以表示參數名稱，然後重複按 TAB 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6e4a5-111">如果您錯過所需的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="6e4a5-112">在命令列中指定的範本參數檔案值優先于範本參數物件的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="6e4a5-113">請提供 "-AgreementType" 參數，以指定要傳回 X12 或 Edifact 控制項編號</span><span class="sxs-lookup"><span data-stu-id="6e4a5-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="6e4a5-114">例子</span><span class="sxs-lookup"><span data-stu-id="6e4a5-114">EXAMPLES</span></span>

### <span data-ttu-id="6e4a5-115">範例 1</span><span class="sxs-lookup"><span data-stu-id="6e4a5-115">Example 1</span></span>
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

<span data-ttu-id="6e4a5-116">此命令會針對特定整合帳戶協定，獲得整合帳戶產生的 X12 交換控制編號，增加其值 100，然後回寫更新的值。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="6e4a5-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="6e4a5-117">Example 2</span></span>
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

<span data-ttu-id="6e4a5-118">此命令會針對特定整合帳戶協定，獲得整合帳戶產生的 EdifactCountAgreement 交換控制編號，增加其值 100，然後回寫更新的值。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="6e4a5-119">參數</span><span class="sxs-lookup"><span data-stu-id="6e4a5-119">PARAMETERS</span></span>

### <span data-ttu-id="6e4a5-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="6e4a5-120">-AgreementName</span></span>
<span data-ttu-id="6e4a5-121">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="6e4a5-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="6e4a5-122">-AgreementType</span></span>
<span data-ttu-id="6e4a5-123">整合帳戶協定類型。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="6e4a5-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="6e4a5-124">-ControlNumber</span></span>
<span data-ttu-id="6e4a5-125">產生的控制項編號新值。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="6e4a5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e4a5-126">-DefaultProfile</span></span>
<span data-ttu-id="6e4a5-127">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="6e4a5-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e4a5-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="6e4a5-128">-Name</span></span>
<span data-ttu-id="6e4a5-129">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-129">The integration account name.</span></span>

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

### <span data-ttu-id="6e4a5-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e4a5-130">-ResourceGroupName</span></span>
<span data-ttu-id="6e4a5-131">整合帳戶資源組名。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="6e4a5-132">-確認</span><span class="sxs-lookup"><span data-stu-id="6e4a5-132">-Confirm</span></span>
<span data-ttu-id="6e4a5-133">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e4a5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e4a5-134">-WhatIf</span></span>
<span data-ttu-id="6e4a5-135">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6e4a5-136">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e4a5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e4a5-137">CommonParameters</span></span>
<span data-ttu-id="6e4a5-138">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e4a5-139">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="6e4a5-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e4a5-140">輸入</span><span class="sxs-lookup"><span data-stu-id="6e4a5-140">INPUTS</span></span>

### <span data-ttu-id="6e4a5-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6e4a5-141">System.String</span></span>

## <span data-ttu-id="6e4a5-142">輸出</span><span class="sxs-lookup"><span data-stu-id="6e4a5-142">OUTPUTS</span></span>

### <span data-ttu-id="6e4a5-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span><span class="sxs-lookup"><span data-stu-id="6e4a5-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="6e4a5-144">筆記</span><span class="sxs-lookup"><span data-stu-id="6e4a5-144">NOTES</span></span>

## <span data-ttu-id="6e4a5-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="6e4a5-145">RELATED LINKS</span></span>

[<span data-ttu-id="6e4a5-146">Get-AzCountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="6e4a5-146">Get-AzIntegrationAccountGeneratedIcn</span></span>](./Get-AzIntegrationAccountGeneratedIcn.md)

