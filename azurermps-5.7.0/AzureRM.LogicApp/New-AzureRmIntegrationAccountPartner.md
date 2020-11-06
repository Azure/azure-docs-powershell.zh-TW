---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/new-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/New-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 470a400721d911e09c7bed4e51eb6cef39a1dafa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450584"
---
# <span data-ttu-id="6b9d2-101">New-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6b9d2-101">New-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="6b9d2-102">摘要</span><span class="sxs-lookup"><span data-stu-id="6b9d2-102">SYNOPSIS</span></span>
<span data-ttu-id="6b9d2-103">建立整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-103">Creates an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b9d2-104">句法</span><span class="sxs-lookup"><span data-stu-id="6b9d2-104">SYNTAX</span></span>

```
New-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b9d2-105">說明</span><span class="sxs-lookup"><span data-stu-id="6b9d2-105">DESCRIPTION</span></span>
<span data-ttu-id="6b9d2-106">**新的-AzureRmIntegrationAccountPartner** Cmdlet 會建立整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-106">The **New-AzureRmIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="6b9d2-107">這個 Cmdlet 會傳回代表整合帳戶合作夥伴的物件。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="6b9d2-108">指定整合帳戶名稱、資源群組名稱、合作夥伴名稱和合作夥伴身分識別。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>

<span data-ttu-id="6b9d2-109">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>

<span data-ttu-id="6b9d2-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="6b9d2-111">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="6b9d2-112">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="6b9d2-113">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="6b9d2-114">示例</span><span class="sxs-lookup"><span data-stu-id="6b9d2-114">EXAMPLES</span></span>

### <span data-ttu-id="6b9d2-115">範例1：建立整合帳戶合作夥伴</span><span class="sxs-lookup"><span data-stu-id="6b9d2-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="6b9d2-116">這個命令會在指定的資源群組中，建立名為 IntegrationAccountPartner22 的整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="6b9d2-117">參數</span><span class="sxs-lookup"><span data-stu-id="6b9d2-117">PARAMETERS</span></span>

### <span data-ttu-id="6b9d2-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="6b9d2-118">-BusinessIdentities</span></span>
<span data-ttu-id="6b9d2-119">指定整合帳戶合作夥伴的商業身分識別。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="6b9d2-120">指定雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-120">Specify a hash table.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b9d2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b9d2-121">-DefaultProfile</span></span>
<span data-ttu-id="6b9d2-122">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="6b9d2-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b9d2-123">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="6b9d2-123">-Metadata</span></span>
<span data-ttu-id="6b9d2-124">指定合作夥伴的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-124">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="6b9d2-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="6b9d2-125">-Name</span></span>
<span data-ttu-id="6b9d2-126">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="6b9d2-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="6b9d2-127">-PartnerName</span></span>
<span data-ttu-id="6b9d2-128">指定整合帳戶合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="6b9d2-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="6b9d2-129">-PartnerType</span></span>
<span data-ttu-id="6b9d2-130">指定整合帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="6b9d2-131">此參數支援類型 B2B。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-131">This parameter supports the type B2B.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b9d2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b9d2-132">-ResourceGroupName</span></span>
<span data-ttu-id="6b9d2-133">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6b9d2-134">-確認</span><span class="sxs-lookup"><span data-stu-id="6b9d2-134">-Confirm</span></span>
<span data-ttu-id="6b9d2-135">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b9d2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b9d2-136">-WhatIf</span></span>
<span data-ttu-id="6b9d2-137">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b9d2-138">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b9d2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b9d2-139">CommonParameters</span></span>
<span data-ttu-id="6b9d2-140">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b9d2-141">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b9d2-142">輸入</span><span class="sxs-lookup"><span data-stu-id="6b9d2-142">INPUTS</span></span>

### <span data-ttu-id="6b9d2-143">所有</span><span class="sxs-lookup"><span data-stu-id="6b9d2-143">None</span></span>
<span data-ttu-id="6b9d2-144">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6b9d2-145">輸出</span><span class="sxs-lookup"><span data-stu-id="6b9d2-145">OUTPUTS</span></span>

### <span data-ttu-id="6b9d2-146">IntegrationAccountPartner 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="6b9d2-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="6b9d2-147">筆記</span><span class="sxs-lookup"><span data-stu-id="6b9d2-147">NOTES</span></span>

## <span data-ttu-id="6b9d2-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="6b9d2-148">RELATED LINKS</span></span>

[<span data-ttu-id="6b9d2-149">AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6b9d2-149">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="6b9d2-150">移除-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6b9d2-150">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="6b9d2-151">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="6b9d2-151">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


