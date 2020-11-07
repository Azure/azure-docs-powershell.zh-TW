---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 5FDD6C6A-9F6A-44C3-B332-B528F648DFDB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 79ad0434a7918bbdf834b5917ed023cbbabf0525
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93623966"
---
# <span data-ttu-id="cb5de-101">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cb5de-101">Set-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="cb5de-102">摘要</span><span class="sxs-lookup"><span data-stu-id="cb5de-102">SYNOPSIS</span></span>
<span data-ttu-id="cb5de-103">修改整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="cb5de-103">Modifies an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb5de-104">句法</span><span class="sxs-lookup"><span data-stu-id="cb5de-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-AgreementType <String>] [-GuestPartner <String>] [-HostPartner <String>] [-GuestIdentityQualifier <String>]
 [-GuestIdentityQualifierValue <String>] [-HostIdentityQualifier <String>]
 [-HostIdentityQualifierValue <String>] [-AgreementContent <String>] [-AgreementContentFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb5de-105">說明</span><span class="sxs-lookup"><span data-stu-id="cb5de-105">DESCRIPTION</span></span>
<span data-ttu-id="cb5de-106">**AzureRmIntegrationAccountAgreement** Cmdlet 會修改整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="cb5de-106">The **Set-AzureRmIntegrationAccountAgreement** cmdlet modifies an integration account agreement.</span></span>
<span data-ttu-id="cb5de-107">這個 Cmdlet 會傳回代表整合帳戶協定的物件。</span><span class="sxs-lookup"><span data-stu-id="cb5de-107">This cmdlet returns an object that represents the integration account agreement.</span></span>
<span data-ttu-id="cb5de-108">指定整合帳戶名稱、資源群組名稱和協定名稱。</span><span class="sxs-lookup"><span data-stu-id="cb5de-108">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="cb5de-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="cb5de-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="cb5de-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="cb5de-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="cb5de-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="cb5de-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="cb5de-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="cb5de-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="cb5de-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="cb5de-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="cb5de-114">示例</span><span class="sxs-lookup"><span data-stu-id="cb5de-114">EXAMPLES</span></span>

### <span data-ttu-id="cb5de-115">範例1：更新整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="cb5de-115">Example 1: Update an integration account agreement</span></span>
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

<span data-ttu-id="cb5de-116">這個命令會更新指定 Azure 資源群組中的整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="cb5de-116">This command updates an integration account agreement in the specified Azure resource group.</span></span>

## <span data-ttu-id="cb5de-117">參數</span><span class="sxs-lookup"><span data-stu-id="cb5de-117">PARAMETERS</span></span>

### <span data-ttu-id="cb5de-118">-AgreementContent</span><span class="sxs-lookup"><span data-stu-id="cb5de-118">-AgreementContent</span></span>
<span data-ttu-id="cb5de-119">指定協定內容（在 JavaScript 物件符號中， (JSON) 格式）。</span><span class="sxs-lookup"><span data-stu-id="cb5de-119">Specifies agreement content, in JavaScript Object Notation (JSON) format, for the agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-120">-AgreementContentFilePath</span><span class="sxs-lookup"><span data-stu-id="cb5de-120">-AgreementContentFilePath</span></span>
<span data-ttu-id="cb5de-121">指定合約之協定內容的檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="cb5de-121">Specifies the file path of agreement content for the agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-122">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="cb5de-122">-AgreementName</span></span>
<span data-ttu-id="cb5de-123">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb5de-123">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="cb5de-124">-AgreementType</span><span class="sxs-lookup"><span data-stu-id="cb5de-124">-AgreementType</span></span>
<span data-ttu-id="cb5de-125">指定整合帳戶合約類型。</span><span class="sxs-lookup"><span data-stu-id="cb5de-125">Specifies the integration account agreement type.</span></span>
<span data-ttu-id="cb5de-126">此參數可接受的值為：</span><span class="sxs-lookup"><span data-stu-id="cb5de-126">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="cb5de-127">X12</span><span class="sxs-lookup"><span data-stu-id="cb5de-127">X12</span></span> 
- <span data-ttu-id="cb5de-128">AS2</span><span class="sxs-lookup"><span data-stu-id="cb5de-128">AS2</span></span>
- <span data-ttu-id="cb5de-129">Edifact</span><span class="sxs-lookup"><span data-stu-id="cb5de-129">Edifact</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: X12, AS2, Edifact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb5de-130">-DefaultProfile</span></span>
<span data-ttu-id="cb5de-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="cb5de-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb5de-132">-Force</span><span class="sxs-lookup"><span data-stu-id="cb5de-132">-Force</span></span>
<span data-ttu-id="cb5de-133">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="cb5de-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-134">-GuestIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="cb5de-134">-GuestIdentityQualifier</span></span>
<span data-ttu-id="cb5de-135">指定來賓合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="cb5de-135">Specifies a name business identity qualifier for the guest partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-136">-GuestIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="cb5de-136">-GuestIdentityQualifierValue</span></span>
<span data-ttu-id="cb5de-137">[整合帳戶協定來賓身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="cb5de-137">The integration account agreement guest identity qualifier value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-138">-GuestPartner</span><span class="sxs-lookup"><span data-stu-id="cb5de-138">-GuestPartner</span></span>
<span data-ttu-id="cb5de-139">指定來賓合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb5de-139">Specifies the name of the guest partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-140">-HostIdentityQualifier</span><span class="sxs-lookup"><span data-stu-id="cb5de-140">-HostIdentityQualifier</span></span>
<span data-ttu-id="cb5de-141">指定主機合作夥伴的名稱商業身分識別限定詞。</span><span class="sxs-lookup"><span data-stu-id="cb5de-141">Specifies a name business identity qualifier for the host partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-142">-HostIdentityQualifierValue</span><span class="sxs-lookup"><span data-stu-id="cb5de-142">-HostIdentityQualifierValue</span></span>
<span data-ttu-id="cb5de-143">[整合帳戶協定主機身分識別限定詞] 值。</span><span class="sxs-lookup"><span data-stu-id="cb5de-143">The integration account agreement host identity qualifier value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-144">-HostPartner</span><span class="sxs-lookup"><span data-stu-id="cb5de-144">-HostPartner</span></span>
<span data-ttu-id="cb5de-145">指定主機夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb5de-145">Specifies the name of the host partner.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-146">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="cb5de-146">-Metadata</span></span>
<span data-ttu-id="cb5de-147">指定協定的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="cb5de-147">Specifies a metadata object for the agreement.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-148">-名稱</span><span class="sxs-lookup"><span data-stu-id="cb5de-148">-Name</span></span>
<span data-ttu-id="cb5de-149">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb5de-149">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb5de-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb5de-150">-ResourceGroupName</span></span>
<span data-ttu-id="cb5de-151">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="cb5de-151">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cb5de-152">-確認</span><span class="sxs-lookup"><span data-stu-id="cb5de-152">-Confirm</span></span>
<span data-ttu-id="cb5de-153">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="cb5de-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb5de-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb5de-154">-WhatIf</span></span>
<span data-ttu-id="cb5de-155">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="cb5de-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb5de-156">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="cb5de-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb5de-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb5de-157">CommonParameters</span></span>
<span data-ttu-id="cb5de-158">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="cb5de-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb5de-159">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="cb5de-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb5de-160">輸入</span><span class="sxs-lookup"><span data-stu-id="cb5de-160">INPUTS</span></span>

### <span data-ttu-id="cb5de-161">所有</span><span class="sxs-lookup"><span data-stu-id="cb5de-161">None</span></span>
<span data-ttu-id="cb5de-162">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="cb5de-162">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cb5de-163">輸出</span><span class="sxs-lookup"><span data-stu-id="cb5de-163">OUTPUTS</span></span>

### <span data-ttu-id="cb5de-164">IntegrationAccountAgreement 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="cb5de-164">Microsoft.Azure.Management.Logic.Models.IntegrationAccountAgreement</span></span>

## <span data-ttu-id="cb5de-165">筆記</span><span class="sxs-lookup"><span data-stu-id="cb5de-165">NOTES</span></span>

## <span data-ttu-id="cb5de-166">相關連結</span><span class="sxs-lookup"><span data-stu-id="cb5de-166">RELATED LINKS</span></span>

[<span data-ttu-id="cb5de-167">AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cb5de-167">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="cb5de-168">新-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cb5de-168">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="cb5de-169">移除-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="cb5de-169">Remove-AzureRmIntegrationAccountAgreement</span></span>](./Remove-AzureRmIntegrationAccountAgreement.md)


