---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountgeneratedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountGeneratedIcn.md
ms.openlocfilehash: b002ca0dca3f3974af8cd05e8ae7c7babf2af486
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93455264"
---
# <span data-ttu-id="205d9-101">Set-AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="205d9-101">Set-AzureRmIntegrationAccountGeneratedIcn</span></span>

## <span data-ttu-id="205d9-102">摘要</span><span class="sxs-lookup"><span data-stu-id="205d9-102">SYNOPSIS</span></span>
<span data-ttu-id="205d9-103">更新 Azure 資源群組中 (ICN) 的整合帳戶產生的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="205d9-103">Updates the integration account generated interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="205d9-104">句法</span><span class="sxs-lookup"><span data-stu-id="205d9-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumber <String> [-AgreementType <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="205d9-105">說明</span><span class="sxs-lookup"><span data-stu-id="205d9-105">DESCRIPTION</span></span>
<span data-ttu-id="205d9-106">Set-AzureRmIntegrationAccountGeneratedIcn Cmdlet 會更新現有的整合帳戶， (ICN) 產生交換控制編號，並傳回代表整合帳戶產生的交換控制編號的物件。</span><span class="sxs-lookup"><span data-stu-id="205d9-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account generated interchange control number (ICN) and returns an object that represents the integration account generated interchange control number.</span></span>
<span data-ttu-id="205d9-107">使用此 Cmdlet 來更新產生交換控制編號的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="205d9-107">Use this cmdlet to update an integration account generated interchange control number.</span></span>
<span data-ttu-id="205d9-108">您可以指定整合帳戶名稱、資源群組名稱和協定名稱，以更新產生交換控制編號的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="205d9-108">You can update an integration account generated interchange control number by specifying the integration account name, resource group name and agreement name.</span></span>
<span data-ttu-id="205d9-109">您無法使用此命令建立新的整合帳戶產生的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="205d9-109">You cannot create a new integration account generated interchange control number with this command.</span></span>
<span data-ttu-id="205d9-110">若要使用動態參數，只要在命令中輸入，或輸入連字號符號 ( ) ，即可指定參數名稱，然後重複按 TAB 鍵，以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="205d9-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="205d9-111">如果您遺漏了必要的範本參數，此 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="205d9-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="205d9-112">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="205d9-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="205d9-113">請提供 "-AgreementType" 參數，以指定要傳回的 X12 或 Edifact 控制編號</span><span class="sxs-lookup"><span data-stu-id="205d9-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="205d9-114">示例</span><span class="sxs-lookup"><span data-stu-id="205d9-114">EXAMPLES</span></span>

### <span data-ttu-id="205d9-115">範例1</span><span class="sxs-lookup"><span data-stu-id="205d9-115">Example 1</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "X12IntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType X12 -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="205d9-116">這個命令會取得整合帳戶為特定整合帳戶協定產生的 X12 交換控制編號，並將其值增加100，然後寫回更新後的值。</span><span class="sxs-lookup"><span data-stu-id="205d9-116">This command gets the integration account generated X12 interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

### <span data-ttu-id="205d9-117">範例2</span><span class="sxs-lookup"><span data-stu-id="205d9-117">Example 2</span></span>
```
PS C:\> $resourceGroup.ResourceGroupName = "ResourceGroup1"
PS C:\> $integrationAccountName = "IntegrationAccount1"
PS C:\> $integrationAccountAgreementName = "EdifactIntegrationAccountAgreement"
PS C:\> $initialControlNumber = Get-AzureRmIntegrationAccountGeneratedIcn -AgreementType EdifactIntegrationAccountAgreement -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName
PS C:\> $incrementedControlNumberValue = [convert]::ToString([convert]::ToInt32($initialControlNumber.ControlNumber, 10) + 100, 10)
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -ResourceGroupName $resourceGroup.ResourceGroupName -Name $integrationAccountName -AgreementName $integrationAccountAgreementName -ControlNumber $incrementedControlNumberValue
ControlNumber            : 1100
ControlNumberChangedTime : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed:
```

<span data-ttu-id="205d9-118">這個命令會取得整合帳戶針對特定整合帳戶協定產生的 EdifactIntegrationAccountAgreement 交換控制編號，並將其值增加至100，然後寫回更新後的值。</span><span class="sxs-lookup"><span data-stu-id="205d9-118">This command gets the integration account generated EdifactIntegrationAccountAgreement interchange control number for a specific integration account agreement, increase its value by 100 then writes back the updated value.</span></span>

## <span data-ttu-id="205d9-119">參數</span><span class="sxs-lookup"><span data-stu-id="205d9-119">PARAMETERS</span></span>

### <span data-ttu-id="205d9-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="205d9-120">-AgreementName</span></span>
<span data-ttu-id="205d9-121">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="205d9-121">The integration account agreement name.</span></span>

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

### <span data-ttu-id="205d9-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="205d9-122">-AgreementType</span></span>
<span data-ttu-id="205d9-123">整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="205d9-123">The integration account agreement type.</span></span>

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

### <span data-ttu-id="205d9-124">-ControlNumber</span><span class="sxs-lookup"><span data-stu-id="205d9-124">-ControlNumber</span></span>
<span data-ttu-id="205d9-125">產生的控制項編號新值。</span><span class="sxs-lookup"><span data-stu-id="205d9-125">The generated control number new value.</span></span>

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

### <span data-ttu-id="205d9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="205d9-126">-DefaultProfile</span></span>
<span data-ttu-id="205d9-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="205d9-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="205d9-128">-名稱</span><span class="sxs-lookup"><span data-stu-id="205d9-128">-Name</span></span>
<span data-ttu-id="205d9-129">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="205d9-129">The integration account name.</span></span>

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

### <span data-ttu-id="205d9-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="205d9-130">-ResourceGroupName</span></span>
<span data-ttu-id="205d9-131">整合帳戶資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="205d9-131">The integration account resource group name.</span></span>

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

### <span data-ttu-id="205d9-132">-確認</span><span class="sxs-lookup"><span data-stu-id="205d9-132">-Confirm</span></span>
<span data-ttu-id="205d9-133">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="205d9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="205d9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="205d9-134">-WhatIf</span></span>
<span data-ttu-id="205d9-135">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="205d9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="205d9-136">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="205d9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="205d9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="205d9-137">CommonParameters</span></span>
<span data-ttu-id="205d9-138">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="205d9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="205d9-139">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="205d9-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="205d9-140">輸入</span><span class="sxs-lookup"><span data-stu-id="205d9-140">INPUTS</span></span>

### <span data-ttu-id="205d9-141">System.object</span><span class="sxs-lookup"><span data-stu-id="205d9-141">System.String</span></span>

## <span data-ttu-id="205d9-142">輸出</span><span class="sxs-lookup"><span data-stu-id="205d9-142">OUTPUTS</span></span>

### <span data-ttu-id="205d9-143">IntegrationAccountControlNumber （LogicApp）。</span><span class="sxs-lookup"><span data-stu-id="205d9-143">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="205d9-144">筆記</span><span class="sxs-lookup"><span data-stu-id="205d9-144">NOTES</span></span>

## <span data-ttu-id="205d9-145">相關連結</span><span class="sxs-lookup"><span data-stu-id="205d9-145">RELATED LINKS</span></span>

[<span data-ttu-id="205d9-146">AzureRmIntegrationAccountGeneratedIcn</span><span class="sxs-lookup"><span data-stu-id="205d9-146">Get-AzureRmIntegrationAccountGeneratedIcn</span></span>](./Get-AzureRmIntegrationAccountGeneratedIcn.md)

