---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountAgreement.md
ms.openlocfilehash: ac0e5e89706e648d714e3f09ebad5dee7d7b4416
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94140399"
---
# <span data-ttu-id="680ae-101">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="680ae-101">Set-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="680ae-102">摘要</span><span class="sxs-lookup"><span data-stu-id="680ae-102">SYNOPSIS</span></span>
<span data-ttu-id="680ae-103">修改整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="680ae-103">Modifies an integration account agreement.</span></span>

## <span data-ttu-id="680ae-104">句法</span><span class="sxs-lookup"><span data-stu-id="680ae-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="680ae-105">說明</span><span class="sxs-lookup"><span data-stu-id="680ae-105">DESCRIPTION</span></span>
<span data-ttu-id="680ae-106">**AzIntegrationAccountAgreement** Cmdlet 會修改整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="680ae-106">The **Set-AzIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="680ae-107">這個 Cmdlet 會傳回代表整合帳戶協定的物件。</span><span class="sxs-lookup"><span data-stu-id="680ae-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="680ae-108">指定整合帳戶名稱、資源群組名稱和協定名稱。</span><span class="sxs-lookup"><span data-stu-id="680ae-108">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="680ae-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="680ae-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="680ae-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="680ae-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="680ae-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="680ae-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="680ae-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="680ae-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="680ae-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="680ae-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="680ae-114">示例</span><span class="sxs-lookup"><span data-stu-id="680ae-114">EXAMPLES</span></span>

### <span data-ttu-id="680ae-115">範例1：更新整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="680ae-115">Example 1: Update an integration account agreement</span></span>
```powershell
PS C:\>Set-AzIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="680ae-116">這個命令會更新指定 Azure 資源群組中的整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="680ae-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

### <span data-ttu-id="680ae-117">範例2</span><span class="sxs-lookup"><span data-stu-id="680ae-117">Example 2</span></span>

<span data-ttu-id="680ae-118">修改整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="680ae-118">Modifies an integration account agreement.</span></span> <span data-ttu-id="680ae-119"> (自動生成) </span><span class="sxs-lookup"><span data-stu-id="680ae-119">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzIntegrationAccountAgreement -AgreementContentFilePath 'C:\temp\AgreementContent.json' -AgreementName 'IntegrationAccountAgreement06' -GuestIdentityQualifier 'BB' -GuestIdentityQualifierValue <String> -GuestPartner 'GuestPartner' -HostIdentityQualifier 'AA' -HostIdentityQualifierValue <String> -HostPartner 'HostPartner' -Metadata <Object> -Name 'IntegrationAccount31' -ResourceGroupName 'ResourceGroup11'
```

## <span data-ttu-id="680ae-120">參數</span><span class="sxs-lookup"><span data-stu-id="680ae-120">PARAMETERS</span></span>

### <span data-ttu-id="680ae-121">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="680ae-121">-AgreementContent</span></span>
<span data-ttu-id="680ae-122">指定協定內容（在 JavaScript 物件符號中， (JSON) 格式）。</span><span class="sxs-lookup"><span data-stu-id="680ae-122">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="680ae-123">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="680ae-123">-AgreementContentFilePath</span></span>
<span data-ttu-id="680ae-124">指定合約之協定內容的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="680ae-124">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="680ae-125">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="680ae-125">-AgreementName</span></span>
<span data-ttu-id="680ae-126">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="680ae-126">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="680ae-127">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="680ae-127">-AgreementType</span></span>
<span data-ttu-id="680ae-128">指定整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="680ae-128">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="680ae-129">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="680ae-129">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="680ae-130">X12</span><span class="sxs-lookup"><span data-stu-id="680ae-130">X12</span></span> 
- <span data-ttu-id="680ae-131">AS2</span><span class="sxs-lookup"><span data-stu-id="680ae-131">AS2</span></span>
- <span data-ttu-id="680ae-132">Edifact</span><span class="sxs-lookup"><span data-stu-id="680ae-132">Edifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="680ae-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="680ae-133">-DefaultProfile</span></span>
<span data-ttu-id="680ae-134">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="680ae-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="680ae-135">-Force</span><span class="sxs-lookup"><span data-stu-id="680ae-135">-Force</span></span>
<span data-ttu-id="680ae-136">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="680ae-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="680ae-137">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="680ae-137">-GuestIdentityQualifier</span></span>
<span data-ttu-id="680ae-138">指定來賓合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="680ae-138">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="680ae-139">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="680ae-139">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="680ae-140">[整合帳戶協定來賓身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="680ae-140">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="680ae-141">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="680ae-141">-GuestPartner</span></span>
<span data-ttu-id="680ae-142">指定來賓合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="680ae-142">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="680ae-143">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="680ae-143">-HostIdentityQualifier</span></span>
<span data-ttu-id="680ae-144">指定主機合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="680ae-144">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="680ae-145">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="680ae-145">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="680ae-146">[整合帳戶協定主機身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="680ae-146">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="680ae-147">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="680ae-147">-HostPartner</span></span>
<span data-ttu-id="680ae-148">指定主機夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="680ae-148">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="680ae-149">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="680ae-149">-Metadata</span></span>
<span data-ttu-id="680ae-150">指定協定的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="680ae-150">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="680ae-151">-名稱</span><span class="sxs-lookup"><span data-stu-id="680ae-151">-Name</span></span>
<span data-ttu-id="680ae-152">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="680ae-152">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="680ae-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="680ae-153">-ResourceGroupName</span></span>
<span data-ttu-id="680ae-154">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="680ae-154">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="680ae-155">-確認</span><span class="sxs-lookup"><span data-stu-id="680ae-155">-Confirm</span></span>
<span data-ttu-id="680ae-156">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="680ae-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="680ae-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="680ae-157">-WhatIf</span></span>
<span data-ttu-id="680ae-158">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="680ae-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="680ae-159">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="680ae-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="680ae-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="680ae-160">CommonParameters</span></span>
<span data-ttu-id="680ae-161">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="680ae-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="680ae-162">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="680ae-162">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="680ae-163">輸入</span><span class="sxs-lookup"><span data-stu-id="680ae-163">INPUTS</span></span>

### <span data-ttu-id="680ae-164">System.object</span><span class="sxs-lookup"><span data-stu-id="680ae-164">System.String</span></span>

## <span data-ttu-id="680ae-165">輸出</span><span class="sxs-lookup"><span data-stu-id="680ae-165">OUTPUTS</span></span>

### <span data-ttu-id="680ae-166">IntegrationAccountAgreement 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="680ae-166">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="680ae-167">筆記</span><span class="sxs-lookup"><span data-stu-id="680ae-167">NOTES</span></span>

## <span data-ttu-id="680ae-168">相關連結</span><span class="sxs-lookup"><span data-stu-id="680ae-168">RELATED LINKS</span></span>

[<span data-ttu-id="680ae-169">AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="680ae-169">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="680ae-170">新-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="680ae-170">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="680ae-171">移除-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="680ae-171">Remove-AzIntegrationAccountAgreement</span></span>](./Remove-AzIntegrationAccountAgreement.md)

