---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 10cd1993acccf45e39a1b192f44b715b06f6d1d0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2020
ms.locfileid: "93787117"
---
# <span data-ttu-id="0d53d-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0d53d-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="0d53d-102">摘要</span><span class="sxs-lookup"><span data-stu-id="0d53d-102">SYNOPSIS</span></span>
<span data-ttu-id="0d53d-103">建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="0d53d-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="0d53d-104">句法</span><span class="sxs-lookup"><span data-stu-id="0d53d-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d53d-105">說明</span><span class="sxs-lookup"><span data-stu-id="0d53d-105">DESCRIPTION</span></span>
<span data-ttu-id="0d53d-106">**新的-AzIntegrationAccountAgreement** Cmdlet 會建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="0d53d-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="0d53d-107">這個 Cmdlet 會傳回代表整合帳戶協定的物件。</span><span class="sxs-lookup"><span data-stu-id="0d53d-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="0d53d-108">指定整合帳戶名稱、資源組名稱、協定名稱、類型、合作夥伴名稱、合作夥伴限定詞及協定內容。</span><span class="sxs-lookup"><span data-stu-id="0d53d-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="0d53d-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="0d53d-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="0d53d-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="0d53d-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0d53d-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="0d53d-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0d53d-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="0d53d-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0d53d-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="0d53d-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0d53d-114">示例</span><span class="sxs-lookup"><span data-stu-id="0d53d-114">EXAMPLES</span></span>

### <span data-ttu-id="0d53d-115">範例1：建立整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="0d53d-115">Example 1: Create a integration account agreement</span></span>
```
PS C:\>New-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
Id                     : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/agreements/IntegrationAccountAgreement06
Name                   : IntegrationAccountAgreement06
Type                   : Microsoft.Logic/integrationAccounts/agreements
CreatedTime            : 3/26/2016 6:43:52 PM
ChangedTime            : 3/26/2016 6:43:52 PM
AgreementType          : X12
HostPartner            : HostPartner
GuestPartner           : GuestPartner
HostIdentityQualifier  : AA
HostIdentityValue      : AA
GuestIdentityQualifier : BB
GuestIdentityValue     : BB
Content                : {"AS2":null,"X12":{"ReceiveAgreement":{"SenderBusinessIdentity":{"Qualifier":"AA","Value":"AA"},"ReceiverBusinessIdentity":{"Qualifier":"ZZ","Valu
                         e":"ZZ"},"ProtocolSettings":{"ValidationSettings":{"ValidateCharacterSet":true,"CheckDuplicateInterchangeControlNumber":false,"InterchangeControlN

                         . . .
```

<span data-ttu-id="0d53d-116">這個命令會在指定的 Azure 資源群組中建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="0d53d-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="0d53d-117">參數</span><span class="sxs-lookup"><span data-stu-id="0d53d-117">PARAMETERS</span></span>

### <span data-ttu-id="0d53d-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="0d53d-118">-AgreementContent</span></span>
<span data-ttu-id="0d53d-119">指定協定內容（在 JavaScript 物件符號中， (JSON) 格式）。</span><span class="sxs-lookup"><span data-stu-id="0d53d-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="0d53d-120">請指定此參數或 *AgreementContentFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="0d53d-120">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d53d-121">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="0d53d-121">-AgreementContentFilePath</span></span>
<span data-ttu-id="0d53d-122">指定合約之協定內容的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="0d53d-122">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="0d53d-123">請指定此參數或 *AgreementContent* 參數。</span><span class="sxs-lookup"><span data-stu-id="0d53d-123">Specify either this parameter or the *AgreementContent* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d53d-124">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="0d53d-124">-AgreementName</span></span>
<span data-ttu-id="0d53d-125">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d53d-125">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="0d53d-126">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="0d53d-126">-AgreementType</span></span>
<span data-ttu-id="0d53d-127">指定整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="0d53d-127">Specifies the integration account agreement type.</span></span> <span data-ttu-id="0d53d-128">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="0d53d-128">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0d53d-129">X12</span><span class="sxs-lookup"><span data-stu-id="0d53d-129">X12</span></span> 
- <span data-ttu-id="0d53d-130">AS2</span><span class="sxs-lookup"><span data-stu-id="0d53d-130">AS2</span></span>
- <span data-ttu-id="0d53d-131">Edifact</span><span class="sxs-lookup"><span data-stu-id="0d53d-131">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d53d-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d53d-132">-DefaultProfile</span></span>
<span data-ttu-id="0d53d-133">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="0d53d-133">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0d53d-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="0d53d-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="0d53d-135">指定來賓合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="0d53d-135">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="0d53d-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="0d53d-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="0d53d-137">[整合帳戶協定來賓身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="0d53d-137">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="0d53d-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="0d53d-138">-GuestPartner</span></span>
<span data-ttu-id="0d53d-139">指定來賓合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d53d-139">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="0d53d-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="0d53d-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="0d53d-141">指定主機合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="0d53d-141">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="0d53d-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="0d53d-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="0d53d-143">[整合帳戶協定主機身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="0d53d-143">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="0d53d-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="0d53d-144">-HostPartner</span></span>
<span data-ttu-id="0d53d-145">指定主機夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d53d-145">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="0d53d-146">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="0d53d-146">-Metadata</span></span>
<span data-ttu-id="0d53d-147">指定協定的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="0d53d-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d53d-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="0d53d-148">-Name</span></span>
<span data-ttu-id="0d53d-149">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d53d-149">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d53d-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d53d-150">-ResourceGroupName</span></span>
<span data-ttu-id="0d53d-151">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="0d53d-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0d53d-152">-確認</span><span class="sxs-lookup"><span data-stu-id="0d53d-152">-Confirm</span></span>
<span data-ttu-id="0d53d-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="0d53d-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d53d-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d53d-154">-WhatIf</span></span>
<span data-ttu-id="0d53d-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="0d53d-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d53d-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="0d53d-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d53d-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d53d-157">CommonParameters</span></span>
<span data-ttu-id="0d53d-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="0d53d-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d53d-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="0d53d-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d53d-160">輸入</span><span class="sxs-lookup"><span data-stu-id="0d53d-160">INPUTS</span></span>

### <span data-ttu-id="0d53d-161">System.object</span><span class="sxs-lookup"><span data-stu-id="0d53d-161">System.String</span></span>

## <span data-ttu-id="0d53d-162">輸出</span><span class="sxs-lookup"><span data-stu-id="0d53d-162">OUTPUTS</span></span>

### <span data-ttu-id="0d53d-163">IntegrationAccountAgreement 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="0d53d-163">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="0d53d-164">筆記</span><span class="sxs-lookup"><span data-stu-id="0d53d-164">NOTES</span></span>

## <span data-ttu-id="0d53d-165">相關連結</span><span class="sxs-lookup"><span data-stu-id="0d53d-165">RELATED LINKS</span></span>

[<span data-ttu-id="0d53d-166">AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0d53d-166">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="0d53d-167">移除-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0d53d-167">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="0d53d-168">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="0d53d-168">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


