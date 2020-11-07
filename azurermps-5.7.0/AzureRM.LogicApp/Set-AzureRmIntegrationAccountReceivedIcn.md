---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountreceivedicn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountReceivedIcn.md
ms.openlocfilehash: 533013be3a878e946b9ff5e44826ad5a7bd6415d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93625468"
---
# <span data-ttu-id="aabea-101">Set-AzureRmIntegrationAccountReceivedIcn</span><span class="sxs-lookup"><span data-stu-id="aabea-101">Set-AzureRmIntegrationAccountReceivedIcn</span></span>

## <span data-ttu-id="aabea-102">摘要</span><span class="sxs-lookup"><span data-stu-id="aabea-102">SYNOPSIS</span></span>
<span data-ttu-id="aabea-103">更新在 Azure 資源群組中 (ICN) 的整合帳戶收到的交換控制編號。</span><span class="sxs-lookup"><span data-stu-id="aabea-103">Updates the integration account received interchange control number (ICN) in the Azure resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aabea-104">句法</span><span class="sxs-lookup"><span data-stu-id="aabea-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountReceivedIcn -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -ControlNumberValue <String> -IsMessageProcessingFailed <Boolean> [-AgreementType <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aabea-105">說明</span><span class="sxs-lookup"><span data-stu-id="aabea-105">DESCRIPTION</span></span>
<span data-ttu-id="aabea-106">Set-AzureRmIntegrationAccountGeneratedIcn Cmdlet 會更新現有的整合帳戶， (ICN) 傳回交換控制編號，並傳回代表整合帳戶收到的交換控制編號的物件。</span><span class="sxs-lookup"><span data-stu-id="aabea-106">The Set-AzureRmIntegrationAccountGeneratedIcn cmdlet updates an existing integration account received interchange control number (ICN) and returns an object that represents the integration account received interchange control number.</span></span>
<span data-ttu-id="aabea-107">使用此 Cmdlet 來更新整合帳戶收到的交換控制編號的訊息處理狀態。</span><span class="sxs-lookup"><span data-stu-id="aabea-107">Use this cmdlet to update an integration account received interchange control number's message processing status.</span></span>
<span data-ttu-id="aabea-108">您可以透過指定整合帳戶名稱、資源群組名稱、協定名稱、控制編號值和郵件處理狀態，來更新已收到交換控制編號的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="aabea-108">You can update an integration account received interchange control number by specifying the integration account name, resource group name, agreement name, control number value and message processing status.</span></span>
<span data-ttu-id="aabea-109">您無法使用此命令來建立新的整合帳戶（已收到交換控制編號）。</span><span class="sxs-lookup"><span data-stu-id="aabea-109">You cannot create a new integration account received interchange control number with this command.</span></span>
<span data-ttu-id="aabea-110">若要使用動態參數，只要在命令中輸入，或輸入連字號符號 ( ) ，即可指定參數名稱，然後重複按 TAB 鍵，以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="aabea-110">To use the dynamic parameters, just type them in the command, or type a hyphen sign(-) to indicate a parameter name and then press the TAB key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="aabea-111">如果您遺漏了必要的範本參數，此 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="aabea-111">If you miss a required template parameter, the cmdlet prompts you for the value.</span></span>
<span data-ttu-id="aabea-112">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="aabea-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="aabea-113">請提供 "-AgreementType" 參數，以指定要傳回的 X12 或 Edifact 控制編號</span><span class="sxs-lookup"><span data-stu-id="aabea-113">Please do provide the "-AgreementType" parameter to specify whether X12 or Edifact control numbers to return</span></span>

## <span data-ttu-id="aabea-114">示例</span><span class="sxs-lookup"><span data-stu-id="aabea-114">EXAMPLES</span></span>

### <span data-ttu-id="aabea-115">範例1</span><span class="sxs-lookup"><span data-stu-id="aabea-115">Example 1</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "X12" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "X12IntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="aabea-116">這個命令會更新整合帳戶已收到特定整合帳戶合約的 X12 交換控制編號，以及郵件處理狀態失敗的值。</span><span class="sxs-lookup"><span data-stu-id="aabea-116">This command updates the integration account received X12 interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

### <span data-ttu-id="aabea-117">範例2</span><span class="sxs-lookup"><span data-stu-id="aabea-117">Example 2</span></span>
```
PS C:\> Set-AzureRmIntegrationAccountGeneratedIcn -AgreementType "Edifact" -ResourceGroupName "ResourceGroup1" -Name "IntegrationAccount1" -AgreementName "EdifactIntegrationAccountAgreement" -ControlNumber "123" -IsMessageProcessingFailed $true
ControlNumber             : 1100
ControlNumberChangedTime  : 2/15/2017 12:36:00 AM
IsMessageProcessingFailed : True
```

<span data-ttu-id="aabea-118">這個命令會更新整合帳戶針對特定整合帳戶合約接收的 Edifact 交換控制編號，以及郵件處理狀態失敗的值。</span><span class="sxs-lookup"><span data-stu-id="aabea-118">This command updates the integration account received Edifact interchange control number for a specific integration account agreement and value with message processing status failed.</span></span>

## <span data-ttu-id="aabea-119">參數</span><span class="sxs-lookup"><span data-stu-id="aabea-119">PARAMETERS</span></span>

### <span data-ttu-id="aabea-120">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="aabea-120">-AgreementName</span></span>
<span data-ttu-id="aabea-121">整合帳戶協定名稱。</span><span class="sxs-lookup"><span data-stu-id="aabea-121">The integration account agreement name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-122">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="aabea-122">-AgreementType</span></span>
<span data-ttu-id="aabea-123">整合帳戶協定類型 (X12 或 Edifact) 。</span><span class="sxs-lookup"><span data-stu-id="aabea-123">The integration account agreement type (X12 or Edifact).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: MessageType
Accepted values: X12, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-124">-ControlNumberValue</span><span class="sxs-lookup"><span data-stu-id="aabea-124">-ControlNumberValue</span></span>
<span data-ttu-id="aabea-125">[整合帳戶控制編號] 值。</span><span class="sxs-lookup"><span data-stu-id="aabea-125">The integration account control number value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aabea-126">-DefaultProfile</span></span>
<span data-ttu-id="aabea-127">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="aabea-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-128">-IsMessageProcessingFailed</span><span class="sxs-lookup"><span data-stu-id="aabea-128">-IsMessageProcessingFailed</span></span>
<span data-ttu-id="aabea-129">收到的郵件處理狀態。</span><span class="sxs-lookup"><span data-stu-id="aabea-129">The received message processing status.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-130">-名稱</span><span class="sxs-lookup"><span data-stu-id="aabea-130">-Name</span></span>
<span data-ttu-id="aabea-131">整合帳戶名稱。</span><span class="sxs-lookup"><span data-stu-id="aabea-131">The integration account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aabea-132">-ResourceGroupName</span></span>
<span data-ttu-id="aabea-133">整合帳戶資源組名稱。</span><span class="sxs-lookup"><span data-stu-id="aabea-133">The integration account resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-134">-確認</span><span class="sxs-lookup"><span data-stu-id="aabea-134">-Confirm</span></span>
<span data-ttu-id="aabea-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="aabea-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aabea-136">-WhatIf</span></span>
<span data-ttu-id="aabea-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="aabea-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aabea-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="aabea-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aabea-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aabea-139">CommonParameters</span></span>
<span data-ttu-id="aabea-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="aabea-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aabea-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="aabea-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aabea-142">輸入</span><span class="sxs-lookup"><span data-stu-id="aabea-142">INPUTS</span></span>

### <span data-ttu-id="aabea-143">System.object</span><span class="sxs-lookup"><span data-stu-id="aabea-143">System.String</span></span>

## <span data-ttu-id="aabea-144">輸出</span><span class="sxs-lookup"><span data-stu-id="aabea-144">OUTPUTS</span></span>

### <span data-ttu-id="aabea-145">IntegrationAccountControlNumber （LogicApp）。</span><span class="sxs-lookup"><span data-stu-id="aabea-145">Microsoft.Azure.Commands.LogicApp.Utilities.IntegrationAccountControlNumber</span></span>

## <span data-ttu-id="aabea-146">筆記</span><span class="sxs-lookup"><span data-stu-id="aabea-146">NOTES</span></span>

## <span data-ttu-id="aabea-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="aabea-147">RELATED LINKS</span></span>

<span data-ttu-id="aabea-148">[AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md) 
[移除-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span><span class="sxs-lookup"><span data-stu-id="aabea-148">[Get-AzureRmIntegrationAccountReceivedIcn](./Get-AzureRmIntegrationAccountReceivedIcn.md)
[Remove-AzureRmIntegrationAccountReceivedIcn](./Remove-AzureRmIntegrationAccountReceivedIcn.md)</span></span>
