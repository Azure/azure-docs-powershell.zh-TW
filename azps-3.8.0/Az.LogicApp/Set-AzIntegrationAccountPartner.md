---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 9B3B6AD4-C37C-4877-9864-9FB2E3B0BDAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountPartner.md
ms.openlocfilehash: ac66c1d28c53224fedb18000db86557c8290d41a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93956366"
---
# <span data-ttu-id="f7e19-101">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f7e19-101">Set-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="f7e19-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f7e19-102">SYNOPSIS</span></span>
<span data-ttu-id="f7e19-103">修改整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="f7e19-103">Modifies an integration account partner.</span></span>

## <span data-ttu-id="f7e19-104">句法</span><span class="sxs-lookup"><span data-stu-id="f7e19-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-PartnerType <String>] [-BusinessIdentities <Object>] [-Metadata <Object>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7e19-105">說明</span><span class="sxs-lookup"><span data-stu-id="f7e19-105">DESCRIPTION</span></span>
<span data-ttu-id="f7e19-106">**AzIntegrationAccountPartner** Cmdlet 會修改整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="f7e19-106">The **Set-AzIntegrationAccountPartner** cmdlet modifies an integration account partner.</span></span>
<span data-ttu-id="f7e19-107">這個 Cmdlet 會傳回代表整合帳戶合作夥伴的物件。</span><span class="sxs-lookup"><span data-stu-id="f7e19-107">This cmdlet returns an object that represents the integration account partner.</span></span>
<span data-ttu-id="f7e19-108">指定整合帳戶名稱、資源群組名稱，以及合作夥伴名稱。</span><span class="sxs-lookup"><span data-stu-id="f7e19-108">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="f7e19-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="f7e19-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f7e19-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="f7e19-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f7e19-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="f7e19-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f7e19-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="f7e19-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f7e19-113">示例</span><span class="sxs-lookup"><span data-stu-id="f7e19-113">EXAMPLES</span></span>

### <span data-ttu-id="f7e19-114">範例1：修改整合帳戶合作夥伴</span><span class="sxs-lookup"><span data-stu-id="f7e19-114">Example 1: Modify an integration account partner</span></span>
```
PS C:\>Set-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22" -PartnerType "B2B" -BusinessIdentities $BusinessIdentities
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/partners/IntegrationAccountPartner1
Name               : IntegrationAccountPartner1
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/26/2016 7:29:30 PM
ChangedTime        : 3/26/2016 7:29:30 PM
BusinessIdentities : [{"Qualifier":"ZZ","Value":"AA"},{"Qualifier":"XX","Value":"GG"}]
Metadata
```

<span data-ttu-id="f7e19-115">這個命令會修改指定資源群組中名為 IntegrationAccountPartner22 的整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="f7e19-115">This command modify the integration account partner named IntegrationAccountPartner22 in the specified resource group.</span></span>

## <span data-ttu-id="f7e19-116">參數</span><span class="sxs-lookup"><span data-stu-id="f7e19-116">PARAMETERS</span></span>

### <span data-ttu-id="f7e19-117">-BusinessIdentities</span><span class="sxs-lookup"><span data-stu-id="f7e19-117">-BusinessIdentities</span></span>
<span data-ttu-id="f7e19-118">指定整合帳戶合作夥伴的商業身分識別。</span><span class="sxs-lookup"><span data-stu-id="f7e19-118">Specifies business identities for the integration account partner.</span></span>
<span data-ttu-id="f7e19-119">指定雜湊資料表。</span><span class="sxs-lookup"><span data-stu-id="f7e19-119">Specify a hash table.</span></span>

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

### <span data-ttu-id="f7e19-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7e19-120">-DefaultProfile</span></span>
<span data-ttu-id="f7e19-121">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="f7e19-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7e19-122">-Force</span><span class="sxs-lookup"><span data-stu-id="f7e19-122">-Force</span></span>
<span data-ttu-id="f7e19-123">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f7e19-123">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f7e19-124">-中繼資料</span><span class="sxs-lookup"><span data-stu-id="f7e19-124">-Metadata</span></span>
<span data-ttu-id="f7e19-125">指定合作夥伴的中繼資料物件。</span><span class="sxs-lookup"><span data-stu-id="f7e19-125">Specifies a metadata object for the partner.</span></span>

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

### <span data-ttu-id="f7e19-126">-名稱</span><span class="sxs-lookup"><span data-stu-id="f7e19-126">-Name</span></span>
<span data-ttu-id="f7e19-127">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7e19-127">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="f7e19-128">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="f7e19-128">-PartnerName</span></span>
<span data-ttu-id="f7e19-129">指定整合帳戶合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7e19-129">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="f7e19-130">-PartnerType</span><span class="sxs-lookup"><span data-stu-id="f7e19-130">-PartnerType</span></span>
<span data-ttu-id="f7e19-131">指定整合帳戶的類型。</span><span class="sxs-lookup"><span data-stu-id="f7e19-131">Specifies the type of the integration account.</span></span>
<span data-ttu-id="f7e19-132">此參數支援類型 B2B。</span><span class="sxs-lookup"><span data-stu-id="f7e19-132">This parameter supports the type B2B.</span></span>

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

### <span data-ttu-id="f7e19-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7e19-133">-ResourceGroupName</span></span>
<span data-ttu-id="f7e19-134">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f7e19-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f7e19-135">-確認</span><span class="sxs-lookup"><span data-stu-id="f7e19-135">-Confirm</span></span>
<span data-ttu-id="f7e19-136">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f7e19-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7e19-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7e19-137">-WhatIf</span></span>
<span data-ttu-id="f7e19-138">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f7e19-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7e19-139">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f7e19-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7e19-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7e19-140">CommonParameters</span></span>
<span data-ttu-id="f7e19-141">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f7e19-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7e19-142">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f7e19-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7e19-143">輸入</span><span class="sxs-lookup"><span data-stu-id="f7e19-143">INPUTS</span></span>

### <span data-ttu-id="f7e19-144">System.object</span><span class="sxs-lookup"><span data-stu-id="f7e19-144">System.String</span></span>

## <span data-ttu-id="f7e19-145">輸出</span><span class="sxs-lookup"><span data-stu-id="f7e19-145">OUTPUTS</span></span>

### <span data-ttu-id="f7e19-146">IntegrationAccountPartner 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="f7e19-146">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="f7e19-147">筆記</span><span class="sxs-lookup"><span data-stu-id="f7e19-147">NOTES</span></span>

## <span data-ttu-id="f7e19-148">相關連結</span><span class="sxs-lookup"><span data-stu-id="f7e19-148">RELATED LINKS</span></span>

[<span data-ttu-id="f7e19-149">AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f7e19-149">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f7e19-150">新-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f7e19-150">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="f7e19-151">移除-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="f7e19-151">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)


