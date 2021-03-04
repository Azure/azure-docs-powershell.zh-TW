---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 2B5FC268-4888-4AEB-B125-7263CF2E4DCD
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountPartner.md
ms.openlocfilehash: 7b07a07dc99efa7f0f3fdb150c902b86b374181e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101903593"
---
# <span data-ttu-id="b613a-101">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b613a-101">New-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="b613a-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b613a-102">SYNOPSIS</span></span>
<span data-ttu-id="b613a-103">建立整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="b613a-103">Creates an integration account partner.</span></span>

## <span data-ttu-id="b613a-104">語法</span><span class="sxs-lookup"><span data-stu-id="b613a-104">SYNTAX</span></span>

```
New-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] -BusinessIdentities <Object> [-Metadata <Object>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b613a-105">描述</span><span class="sxs-lookup"><span data-stu-id="b613a-105">DESCRIPTION</span></span>
<span data-ttu-id="b613a-106">**New-Az方AccountPartner** Cmdlet 會建立整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="b613a-106">The **New-AzIntegrationAccountPartner** cmdlet creates an integration account partner.</span></span>
<span data-ttu-id="b613a-107">此 Cmdlet 會返回代表整合帳戶合作夥伴的物件。</span><span class="sxs-lookup"><span data-stu-id="b613a-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="b613a-108">指定整合帳戶名稱、資源組名、合作夥伴名稱和合作夥伴身分。</span><span class="sxs-lookup"><span data-stu-id="b613a-108">Specify the integration account name, resource group name, partner name, and partner identities.</span></span>
<span data-ttu-id="b613a-109">在命令列中指定的範本參數檔案值優先于範本參數物件的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="b613a-109">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="b613a-110">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="b613a-110">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b613a-111">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="b613a-111">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b613a-112">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="b613a-112">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b613a-113">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="b613a-113">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b613a-114">例子</span><span class="sxs-lookup"><span data-stu-id="b613a-114">EXAMPLES</span></span>

### <span data-ttu-id="b613a-115">範例 1：建立整合帳戶合作夥伴</span><span class="sxs-lookup"><span data-stu-id="b613a-115">Example 1: Create an integration account partner</span></span>
```
PS C:\>New-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata           :
```

<span data-ttu-id="b613a-116">此命令會建立指定資源群組中名為 IntegrationAccountPartner22 的整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="b613a-116">This command creates the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="b613a-117">參數</span><span class="sxs-lookup"><span data-stu-id="b613a-117">PARAMETERS</span></span>

### <span data-ttu-id="b613a-118">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="b613a-118">-BusinessIdentities</span></span>
<span data-ttu-id="b613a-119">指定整合帳戶合作夥伴的企業身分。</span><span class="sxs-lookup"><span data-stu-id="b613a-119">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="b613a-120">指定雜湊表格。</span><span class="sxs-lookup"><span data-stu-id="b613a-120">Specify a hash table.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b613a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b613a-121">-DefaultProfile</span></span>
<span data-ttu-id="b613a-122">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b613a-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b613a-123">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="b613a-123">-Metadata</span></span>
<span data-ttu-id="b613a-124">指定合作夥伴的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="b613a-124">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="b613a-125">-名稱</span><span class="sxs-lookup"><span data-stu-id="b613a-125">-Name</span></span>
<span data-ttu-id="b613a-126">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b613a-126">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b613a-127">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="b613a-127">-PartnerName</span></span>
<span data-ttu-id="b613a-128">指定整合帳戶合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="b613a-128">Specifies a name for the integration account partner.</span></span>

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

### <span data-ttu-id="b613a-129">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="b613a-129">-PartnerType</span></span>
<span data-ttu-id="b613a-130">指定整合帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="b613a-130">Specifies the type of the integration account.</span></span>
<span data-ttu-id="b613a-131">此參數支援 B2B 類型。</span><span class="sxs-lookup"><span data-stu-id="b613a-131">This parameter supports the type B2B.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: B2B

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b613a-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b613a-132">-ResourceGroupName</span></span>
<span data-ttu-id="b613a-133">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b613a-133">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b613a-134">-確認</span><span class="sxs-lookup"><span data-stu-id="b613a-134">-Confirm</span></span>
<span data-ttu-id="b613a-135">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b613a-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b613a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b613a-136">-WhatIf</span></span>
<span data-ttu-id="b613a-137">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b613a-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b613a-138">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b613a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b613a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b613a-139">CommonParameters</span></span>
<span data-ttu-id="b613a-140">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b613a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b613a-141">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b613a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b613a-142">輸入</span><span class="sxs-lookup"><span data-stu-id="b613a-142">INPUTS</span></span>

### <span data-ttu-id="b613a-143">System.String</span><span class="sxs-lookup"><span data-stu-id="b613a-143">System.String</span></span>

## <span data-ttu-id="b613a-144">輸出</span><span class="sxs-lookup"><span data-stu-id="b613a-144">OUTPUTS</span></span>

### <span data-ttu-id="b613a-145">Microsoft.Azure.management.Logic.models.IntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b613a-145">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="b613a-146">筆記</span><span class="sxs-lookup"><span data-stu-id="b613a-146">NOTES</span></span>

## <span data-ttu-id="b613a-147">相關連結</span><span class="sxs-lookup"><span data-stu-id="b613a-147">RELATED LINKS</span></span>

[<span data-ttu-id="b613a-148">Get-Az方AccountPartner</span><span class="sxs-lookup"><span data-stu-id="b613a-148">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="b613a-149">Remove-Az方AccountPartner</span><span class="sxs-lookup"><span data-stu-id="b613a-149">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="b613a-150">Set-Az方AccountPartner</span><span class="sxs-lookup"><span data-stu-id="b613a-150">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


