---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: bfbcfe06acbfefefcd754a7ad541ebafe31bae7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93453440"
---
# <span data-ttu-id="5482f-101">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5482f-101">Set-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="5482f-102">摘要</span><span class="sxs-lookup"><span data-stu-id="5482f-102">SYNOPSIS</span></span>
<span data-ttu-id="5482f-103">修改整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="5482f-103">Modifies an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5482f-104">句法</span><span class="sxs-lookup"><span data-stu-id="5482f-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5482f-105">說明</span><span class="sxs-lookup"><span data-stu-id="5482f-105">DESCRIPTION</span></span>
<span data-ttu-id="5482f-106">**AzureRmIntegrationAccountAgreement** Cmdlet 會修改整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="5482f-106">The **Set-AzureRmIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="5482f-107">這個 Cmdlet 會傳回代表整合帳戶協定的物件。</span><span class="sxs-lookup"><span data-stu-id="5482f-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="5482f-108">指定整合帳戶名稱、資源群組名稱和協定名稱。</span><span class="sxs-lookup"><span data-stu-id="5482f-108">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="5482f-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="5482f-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="5482f-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="5482f-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="5482f-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="5482f-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="5482f-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="5482f-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="5482f-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="5482f-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="5482f-114">示例</span><span class="sxs-lookup"><span data-stu-id="5482f-114">EXAMPLES</span></span>

### <span data-ttu-id="5482f-115">範例1：更新整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="5482f-115">Example 1: Update an integration account agreement</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountAgreement -Name "IntegrationAccount31"-ResourceGroupName "ResourceGroup11" -AgreementName "IntegrationAccountAgreement06" -AgreementType "X12" -GuestPartner "GuestPartner" -HostPartner "HostPartner" -GuestIdentityQualifier "BB" -HostIdentityQualifier "AA" -AgreementContentFilePath "C:\temp\AgreementContent.json"
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

<span data-ttu-id="5482f-116">這個命令會更新指定 Azure 資源群組中的整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="5482f-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="5482f-117">參數</span><span class="sxs-lookup"><span data-stu-id="5482f-117">PARAMETERS</span></span>

### <span data-ttu-id="5482f-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="5482f-118">-AgreementContent</span></span>
<span data-ttu-id="5482f-119">指定協定內容（在 JavaScript 物件符號中， (JSON) 格式）。</span><span class="sxs-lookup"><span data-stu-id="5482f-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

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

### <span data-ttu-id="5482f-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="5482f-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="5482f-121">指定合約之協定內容的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="5482f-121">Specifies the file path of agreement content for the agreement.</span></span>

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

### <span data-ttu-id="5482f-122">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="5482f-122">-AgreementName</span></span>
<span data-ttu-id="5482f-123">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="5482f-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="5482f-124">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="5482f-124">-AgreementType</span></span>
<span data-ttu-id="5482f-125">指定整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="5482f-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="5482f-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="5482f-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5482f-127">X12</span><span class="sxs-lookup"><span data-stu-id="5482f-127">X12</span></span> 
- <span data-ttu-id="5482f-128">AS2</span><span class="sxs-lookup"><span data-stu-id="5482f-128">AS2</span></span>
- <span data-ttu-id="5482f-129">Edifact</span><span class="sxs-lookup"><span data-stu-id="5482f-129">Edifact</span></span>

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

### <span data-ttu-id="5482f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="5482f-130">-Force</span></span>
<span data-ttu-id="5482f-131">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="5482f-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5482f-132">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="5482f-132">-GuestIdentityQualifier</span></span>
<span data-ttu-id="5482f-133">指定來賓合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="5482f-133">Specifies a name business identity qualifier for the guest partner.</span></span>

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

### <span data-ttu-id="5482f-134">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="5482f-134">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="5482f-135">[整合帳戶協定來賓身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="5482f-135">The integration account agreement guest identity qualifier value.</span></span>

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

### <span data-ttu-id="5482f-136">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="5482f-136">-GuestPartner</span></span>
<span data-ttu-id="5482f-137">指定來賓合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="5482f-137">Specifies the name of the guest partner.</span></span>

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

### <span data-ttu-id="5482f-138">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="5482f-138">-HostIdentityQualifier</span></span>
<span data-ttu-id="5482f-139">指定主機合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="5482f-139">Specifies a name business identity qualifier for the host partner.</span></span>

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

### <span data-ttu-id="5482f-140">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="5482f-140">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="5482f-141">[整合帳戶協定主機身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="5482f-141">The integration account agreement host identity qualifier value.</span></span>

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

### <span data-ttu-id="5482f-142">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="5482f-142">-HostPartner</span></span>
<span data-ttu-id="5482f-143">指定主機夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="5482f-143">Specifies the name of the host partner.</span></span>

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

### <span data-ttu-id="5482f-144">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="5482f-144">-Metadata</span></span>
<span data-ttu-id="5482f-145">指定協定的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="5482f-145">Specifies a metadata object for the agreement.</span></span>

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

### <span data-ttu-id="5482f-146">-名稱</span><span class="sxs-lookup"><span data-stu-id="5482f-146">-Name</span></span>
<span data-ttu-id="5482f-147">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="5482f-147">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="5482f-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5482f-148">-ResourceGroupName</span></span>
<span data-ttu-id="5482f-149">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="5482f-149">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="5482f-150">-確認</span><span class="sxs-lookup"><span data-stu-id="5482f-150">-Confirm</span></span>
<span data-ttu-id="5482f-151">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="5482f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5482f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5482f-152">-WhatIf</span></span>
<span data-ttu-id="5482f-153">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="5482f-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5482f-154">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="5482f-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5482f-155">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5482f-155">-DefaultProfile</span></span>
<span data-ttu-id="5482f-156">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="5482f-156">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5482f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5482f-157">CommonParameters</span></span>
<span data-ttu-id="5482f-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="5482f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5482f-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="5482f-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5482f-160">輸入</span><span class="sxs-lookup"><span data-stu-id="5482f-160">INPUTS</span></span>

## <span data-ttu-id="5482f-161">輸出</span><span class="sxs-lookup"><span data-stu-id="5482f-161">OUTPUTS</span></span>

### <span data-ttu-id="5482f-162">IntegrationAccountAgreement 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="5482f-162">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="5482f-163">筆記</span><span class="sxs-lookup"><span data-stu-id="5482f-163">NOTES</span></span>

## <span data-ttu-id="5482f-164">相關連結</span><span class="sxs-lookup"><span data-stu-id="5482f-164">RELATED LINKS</span></span>

[<span data-ttu-id="5482f-165">AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5482f-165">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="5482f-166">新-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5482f-166">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="5482f-167">移除-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="5482f-167">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)

