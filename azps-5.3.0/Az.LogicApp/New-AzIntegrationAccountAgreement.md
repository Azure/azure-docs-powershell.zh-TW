---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 190745ce8b09bf29b3cc3cbc07f35899732f97f0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/05/2021
ms.locfileid: "98449202"
---
# <span data-ttu-id="2b4b8-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="2b4b8-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="2b4b8-102">摘要</span><span class="sxs-lookup"><span data-stu-id="2b4b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4b8-103">建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="2b4b8-104">句法</span><span class="sxs-lookup"><span data-stu-id="2b4b8-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b4b8-105">說明</span><span class="sxs-lookup"><span data-stu-id="2b4b8-105">DESCRIPTION</span></span>
<span data-ttu-id="2b4b8-106">**新的-AzIntegrationAccountAgreement** Cmdlet 會建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="2b4b8-107">這個 Cmdlet 會傳回代表整合帳戶協定的物件。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="2b4b8-108">指定整合帳戶名稱、資源組名稱、協定名稱、類型、合作夥伴名稱、合作夥伴限定詞及協定內容。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="2b4b8-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="2b4b8-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="2b4b8-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="2b4b8-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="2b4b8-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="2b4b8-114">示例</span><span class="sxs-lookup"><span data-stu-id="2b4b8-114">EXAMPLES</span></span>

### <span data-ttu-id="2b4b8-115">範例1：建立整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="2b4b8-115">Example 1: Create a integration account agreement</span></span>
```powershell
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

<span data-ttu-id="2b4b8-116">這個命令會在指定的 Azure 資源群組中建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="2b4b8-117">範例2</span><span class="sxs-lookup"><span data-stu-id="2b4b8-117">Example 2</span></span>

<span data-ttu-id="2b4b8-118">建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-118">Creates an integration account agreement.</span></span> <span data-ttu-id="2b4b8-119"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="2b4b8-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="2b4b8-120">參數</span><span class="sxs-lookup"><span data-stu-id="2b4b8-120">PARAMETERS</span></span>

### <span data-ttu-id="2b4b8-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="2b4b8-121">-AgreementContent</span></span>
<span data-ttu-id="2b4b8-122">指定協定內容（在 JavaScript 物件符號中， (JSON) 格式）。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="2b4b8-123">請指定此參數或 *AgreementContentFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="2b4b8-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="2b4b8-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="2b4b8-125">指定合約之協定內容的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="2b4b8-126">請指定此參數或 *AgreementContent* 參數。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="2b4b8-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="2b4b8-127">-AgreementName</span></span>
<span data-ttu-id="2b4b8-128">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="2b4b8-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="2b4b8-129">-AgreementType</span></span>
<span data-ttu-id="2b4b8-130">指定整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="2b4b8-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="2b4b8-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2b4b8-132">X12</span><span class="sxs-lookup"><span data-stu-id="2b4b8-132">X12</span></span> 
- <span data-ttu-id="2b4b8-133">AS2</span><span class="sxs-lookup"><span data-stu-id="2b4b8-133">AS2</span></span>
- <span data-ttu-id="2b4b8-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="2b4b8-134">Edifact</span></span>

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

### <span data-ttu-id="2b4b8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b4b8-135">-DefaultProfile</span></span>
<span data-ttu-id="2b4b8-136">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="2b4b8-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2b4b8-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="2b4b8-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="2b4b8-138">指定來賓合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="2b4b8-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="2b4b8-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="2b4b8-140">[整合帳戶協定來賓身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="2b4b8-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="2b4b8-141">-GuestPartner</span></span>
<span data-ttu-id="2b4b8-142">指定來賓合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="2b4b8-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="2b4b8-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="2b4b8-144">指定主機合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="2b4b8-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="2b4b8-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="2b4b8-146">[整合帳戶協定主機身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="2b4b8-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="2b4b8-147">-HostPartner</span></span>
<span data-ttu-id="2b4b8-148">指定主機夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="2b4b8-149">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="2b4b8-149">-Metadata</span></span>
<span data-ttu-id="2b4b8-150">指定協定的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="2b4b8-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="2b4b8-151">-Name</span></span>
<span data-ttu-id="2b4b8-152">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="2b4b8-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b4b8-153">-ResourceGroupName</span></span>
<span data-ttu-id="2b4b8-154">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="2b4b8-155">-確認</span><span class="sxs-lookup"><span data-stu-id="2b4b8-155">-Confirm</span></span>
<span data-ttu-id="2b4b8-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b4b8-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b4b8-157">-WhatIf</span></span>
<span data-ttu-id="2b4b8-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b4b8-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b4b8-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4b8-160">CommonParameters</span></span>
<span data-ttu-id="2b4b8-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4b8-162">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4b8-163">輸入</span><span class="sxs-lookup"><span data-stu-id="2b4b8-163">INPUTS</span></span>

### <span data-ttu-id="2b4b8-164">System.object</span><span class="sxs-lookup"><span data-stu-id="2b4b8-164">System.String</span></span>

## <span data-ttu-id="2b4b8-165">輸出</span><span class="sxs-lookup"><span data-stu-id="2b4b8-165">OUTPUTS</span></span>

### <span data-ttu-id="2b4b8-166">IntegrationAccountAgreement 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="2b4b8-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="2b4b8-167">筆記</span><span class="sxs-lookup"><span data-stu-id="2b4b8-167">NOTES</span></span>

## <span data-ttu-id="2b4b8-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="2b4b8-168">RELATED LINKS</span></span>

[<span data-ttu-id="2b4b8-169">AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="2b4b8-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="2b4b8-170">移除-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="2b4b8-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="2b4b8-171">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="2b4b8-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


