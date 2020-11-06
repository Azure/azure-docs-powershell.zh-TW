---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/set-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: e8bf71ec58273e89ad8f32e65c9c110205239dd2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93456188"
---
# <span data-ttu-id="d72b0-101">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d72b0-101">Set-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="d72b0-102">摘要</span><span class="sxs-lookup"><span data-stu-id="d72b0-102">SYNOPSIS</span></span>
<span data-ttu-id="d72b0-103">修改整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="d72b0-103">Modifies an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d72b0-104">句法</span><span class="sxs-lookup"><span data-stu-id="d72b0-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d72b0-105">說明</span><span class="sxs-lookup"><span data-stu-id="d72b0-105">DESCRIPTION</span></span>
<span data-ttu-id="d72b0-106">**AzureRmIntegrationAccountPartner** Cmdlet 會修改整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="d72b0-106">The **Set-AzureRmIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="d72b0-107">這個 Cmdlet 會傳回代表整合帳戶合作夥伴的物件。</span><span class="sxs-lookup"><span data-stu-id="d72b0-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="d72b0-108">指定整合帳戶名稱、資源群組名稱，以及合作夥伴名稱。</span><span class="sxs-lookup"><span data-stu-id="d72b0-108">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="d72b0-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="d72b0-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d72b0-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="d72b0-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d72b0-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="d72b0-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d72b0-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="d72b0-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d72b0-113">示例</span><span class="sxs-lookup"><span data-stu-id="d72b0-113">EXAMPLES</span></span>

### <span data-ttu-id="d72b0-114">範例1：修改整合帳戶合作夥伴</span><span class="sxs-lookup"><span data-stu-id="d72b0-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="d72b0-115">這個命令會修改指定資源群組中名為 IntegrationAccountPartner22 的整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="d72b0-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="d72b0-116">參數</span><span class="sxs-lookup"><span data-stu-id="d72b0-116">PARAMETERS</span></span>

### <span data-ttu-id="d72b0-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="d72b0-117">-BusinessIdentities</span></span>
<span data-ttu-id="d72b0-118">指定整合帳戶合作夥伴的商業身分識別。</span><span class="sxs-lookup"><span data-stu-id="d72b0-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="d72b0-119">指定雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="d72b0-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="d72b0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d72b0-120">-DefaultProfile</span></span>
<span data-ttu-id="d72b0-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="d72b0-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d72b0-122">-Force</span><span class="sxs-lookup"><span data-stu-id="d72b0-122">-Force</span></span>
<span data-ttu-id="d72b0-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="d72b0-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d72b0-124">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="d72b0-124">-Metadata</span></span>
<span data-ttu-id="d72b0-125">指定合作夥伴的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="d72b0-125">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="d72b0-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="d72b0-126">-Name</span></span>
<span data-ttu-id="d72b0-127">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="d72b0-127">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="d72b0-128">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="d72b0-128">-PartnerName</span></span>
<span data-ttu-id="d72b0-129">指定整合帳戶合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="d72b0-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="d72b0-130">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="d72b0-130">-PartnerType</span></span>
<span data-ttu-id="d72b0-131">指定整合帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="d72b0-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="d72b0-132">此參數支援類型 B2B。</span><span class="sxs-lookup"><span data-stu-id="d72b0-132">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="d72b0-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d72b0-133">-ResourceGroupName</span></span>
<span data-ttu-id="d72b0-134">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="d72b0-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="d72b0-135">-確認</span><span class="sxs-lookup"><span data-stu-id="d72b0-135">-Confirm</span></span>
<span data-ttu-id="d72b0-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="d72b0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d72b0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d72b0-137">-WhatIf</span></span>
<span data-ttu-id="d72b0-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="d72b0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d72b0-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="d72b0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d72b0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d72b0-140">CommonParameters</span></span>
<span data-ttu-id="d72b0-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="d72b0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d72b0-142">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="d72b0-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d72b0-143">輸入</span><span class="sxs-lookup"><span data-stu-id="d72b0-143">INPUTS</span></span>

### <span data-ttu-id="d72b0-144">所有</span><span class="sxs-lookup"><span data-stu-id="d72b0-144">None</span></span>
<span data-ttu-id="d72b0-145">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="d72b0-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d72b0-146">輸出</span><span class="sxs-lookup"><span data-stu-id="d72b0-146">OUTPUTS</span></span>

### <span data-ttu-id="d72b0-147">IntegrationAccountPartner 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="d72b0-147">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="d72b0-148">筆記</span><span class="sxs-lookup"><span data-stu-id="d72b0-148">NOTES</span></span>

## <span data-ttu-id="d72b0-149">相關連結</span><span class="sxs-lookup"><span data-stu-id="d72b0-149">RELATED LINKS</span></span>

[<span data-ttu-id="d72b0-150">AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d72b0-150">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="d72b0-151">新-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d72b0-151">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="d72b0-152">移除-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="d72b0-152">Remove-AzureRmIntegrationAccountPartner</span></span>](./Remove-AzureRmIntegrationAccountPartner.md)


