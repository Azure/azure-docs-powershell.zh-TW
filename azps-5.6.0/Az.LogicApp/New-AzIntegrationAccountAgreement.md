---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: B8998AAA-05FC-4029-A284-B64E23326B22
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 82fb412cca4642881ff6a84ede1f2c722c6d5086
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101916531"
---
# <span data-ttu-id="b7300-101">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b7300-101">New-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="b7300-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b7300-102">SYNOPSIS</span></span>
<span data-ttu-id="b7300-103">建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="b7300-103">Creates an integration account agreement.</span></span>

## <span data-ttu-id="b7300-104">語法</span><span class="sxs-lookup"><span data-stu-id="b7300-104">SYNTAX</span></span>

```
New-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 -AgreementType <String> -GuestPartner <String> -HostPartner <String> -GuestIdentityQualifier <String>
 -GuestIdentityQualifierValue <String> -HostIdentityQualifier <String> -HostIdentityQualifierValue <String>
 [-AgreementContent <String>] [-AgreementContentFilePath <String>] [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7300-105">描述</span><span class="sxs-lookup"><span data-stu-id="b7300-105">DESCRIPTION</span></span>
<span data-ttu-id="b7300-106">**New-AzEmentAccountAgreement** Cmdlet 會建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="b7300-106">The **New-AzIntegrationAccountAgreement** cmdlet creates an integration account agreement.</span></span>
<span data-ttu-id="b7300-107">此 Cmdlet 會返回代表整合帳戶協定的物件。</span><span class="sxs-lookup"><span data-stu-id="b7300-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="b7300-108">指定整合帳戶名稱、資源組名、協定名稱、類型、合作夥伴名稱、合作夥伴限定詞及協定內容。</span><span class="sxs-lookup"><span data-stu-id="b7300-108">Specify the integration account name, resource group name, agreement name, type, partner name, partner qualifiers, and agreement content.</span></span>
<span data-ttu-id="b7300-109">在命令列中指定的範本參數檔案值優先于範本參數物件的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="b7300-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="b7300-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="b7300-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b7300-111">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="b7300-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b7300-112">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="b7300-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b7300-113">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="b7300-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b7300-114">例子</span><span class="sxs-lookup"><span data-stu-id="b7300-114">EXAMPLES</span></span>

### <span data-ttu-id="b7300-115">範例 1：建立整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="b7300-115">Example 1: Create a integration account agreement</span></span>
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

<span data-ttu-id="b7300-116">此命令會建立指定 Azure 資源群組中的整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="b7300-116">This command creates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="b7300-117">範例 2</span><span class="sxs-lookup"><span data-stu-id="b7300-117">Example 2</span></span>

<span data-ttu-id="b7300-118">建立整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="b7300-118">Creates an integration account agreement.</span></span> <span data-ttu-id="b7300-119"> (自動) </span><span class="sxs-lookup"><span data-stu-id="b7300-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzIntegrationAccountAgreement -AgreementContent <String> -AgreementName 'IntegrationAccountAgreement06' -AgreementType X12 -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="b7300-120">參數</span><span class="sxs-lookup"><span data-stu-id="b7300-120">PARAMETERS</span></span>

### <span data-ttu-id="b7300-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="b7300-121">-AgreementContent</span></span>
<span data-ttu-id="b7300-122">指定協定在 JavaScript 物件標記法中 (JSON) 格式。</span><span class="sxs-lookup"><span data-stu-id="b7300-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>
<span data-ttu-id="b7300-123">指定此參數或 *AgreementContentFilePath* 參數。</span><span class="sxs-lookup"><span data-stu-id="b7300-123">Specify either this parameter or the *AgreementContentFilePath* parameter.</span></span>

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

### <span data-ttu-id="b7300-124">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="b7300-124">-AgreementContentFilePath</span></span>
<span data-ttu-id="b7300-125">指定協定內容的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="b7300-125">Specifies the file path of agreement content for the agreement.</span></span>
<span data-ttu-id="b7300-126">指定此參數或 *AgreementContent 參數* 。</span><span class="sxs-lookup"><span data-stu-id="b7300-126">Specify either this parameter or the *AgreementContent* parameter.</span></span>

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

### <span data-ttu-id="b7300-127">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="b7300-127">-AgreementName</span></span>
<span data-ttu-id="b7300-128">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7300-128">Specifies a name for the integration account agreement.</span></span>

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

### <span data-ttu-id="b7300-129">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="b7300-129">-AgreementType</span></span>
<span data-ttu-id="b7300-130">指定整合帳戶協定類型。</span><span class="sxs-lookup"><span data-stu-id="b7300-130">Specifies the integration account agreement type.</span></span> <span data-ttu-id="b7300-131">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="b7300-131">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="b7300-132">X12</span><span class="sxs-lookup"><span data-stu-id="b7300-132">X12</span></span> 
- <span data-ttu-id="b7300-133">AS2</span><span class="sxs-lookup"><span data-stu-id="b7300-133">AS2</span></span>
- <span data-ttu-id="b7300-134">Edifact</span><span class="sxs-lookup"><span data-stu-id="b7300-134">Edifact</span></span>

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

### <span data-ttu-id="b7300-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7300-135">-DefaultProfile</span></span>
<span data-ttu-id="b7300-136">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b7300-136">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7300-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="b7300-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="b7300-138">指定來賓合作夥伴的名稱商務身分識別識別。</span><span class="sxs-lookup"><span data-stu-id="b7300-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="b7300-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="b7300-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="b7300-140">整合帳戶協定來賓身分識別識別值。</span><span class="sxs-lookup"><span data-stu-id="b7300-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="b7300-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="b7300-141">-GuestPartner</span></span>
<span data-ttu-id="b7300-142">指定來賓合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7300-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="b7300-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="b7300-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="b7300-144">指定主機合作夥伴的名稱商務身分識別。</span><span class="sxs-lookup"><span data-stu-id="b7300-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="b7300-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="b7300-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="b7300-146">整合帳戶協定主機身分識別識別識別值。</span><span class="sxs-lookup"><span data-stu-id="b7300-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="b7300-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="b7300-147">-HostPartner</span></span>
<span data-ttu-id="b7300-148">指定主機合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7300-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="b7300-149">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="b7300-149">-Metadata</span></span>
<span data-ttu-id="b7300-150">指定協定的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="b7300-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="b7300-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="b7300-151">-Name</span></span>
<span data-ttu-id="b7300-152">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7300-152">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="b7300-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7300-153">-ResourceGroupName</span></span>
<span data-ttu-id="b7300-154">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b7300-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b7300-155">-確認</span><span class="sxs-lookup"><span data-stu-id="b7300-155">-Confirm</span></span>
<span data-ttu-id="b7300-156">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b7300-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7300-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7300-157">-WhatIf</span></span>
<span data-ttu-id="b7300-158">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b7300-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7300-159">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b7300-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7300-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7300-160">CommonParameters</span></span>
<span data-ttu-id="b7300-161">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b7300-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7300-162">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b7300-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7300-163">輸入</span><span class="sxs-lookup"><span data-stu-id="b7300-163">INPUTS</span></span>

### <span data-ttu-id="b7300-164">System.String</span><span class="sxs-lookup"><span data-stu-id="b7300-164">System.String</span></span>

## <span data-ttu-id="b7300-165">輸出</span><span class="sxs-lookup"><span data-stu-id="b7300-165">OUTPUTS</span></span>

### <span data-ttu-id="b7300-166">Microsoft.Azure.management.Logic.models.IntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b7300-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="b7300-167">筆記</span><span class="sxs-lookup"><span data-stu-id="b7300-167">NOTES</span></span>

## <span data-ttu-id="b7300-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="b7300-168">RELATED LINKS</span></span>

[<span data-ttu-id="b7300-169">Get-AzEmentAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b7300-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="b7300-170">Remove-AzEmentAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b7300-170">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="b7300-171">Set-AzEmentAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="b7300-171">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


