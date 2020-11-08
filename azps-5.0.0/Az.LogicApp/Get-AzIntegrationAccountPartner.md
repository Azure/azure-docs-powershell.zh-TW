---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 6E84E26F-8150-41F8-8823-CEED05619A75
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/get-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Get-AzIntegrationAccountPartner.md
ms.openlocfilehash: cf6d2f4da1803e5c9403803ea7231b55c13d7243
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141614"
---
# <span data-ttu-id="4c1ec-101">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="4c1ec-101">Get-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="4c1ec-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4c1ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4c1ec-103">取得整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-103">Gets integration account partners.</span></span>

## <span data-ttu-id="4c1ec-104">句法</span><span class="sxs-lookup"><span data-stu-id="4c1ec-104">SYNTAX</span></span>

```
Get-AzIntegrationAccountPartner [-ResourceGroupName <String>] [-Name <String>] [-PartnerName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c1ec-105">說明</span><span class="sxs-lookup"><span data-stu-id="4c1ec-105">DESCRIPTION</span></span>
<span data-ttu-id="4c1ec-106">**AzIntegrationAccountPartner** Cmdlet 會從資源群組取得整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-106">The **Get-AzIntegrationAccountPartner** cmdlet gets integration account partners from a resource group.</span></span>
<span data-ttu-id="4c1ec-107">指定整合帳戶名稱、資源群組名稱，以及合作夥伴名稱。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="4c1ec-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4c1ec-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4c1ec-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4c1ec-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4c1ec-112">示例</span><span class="sxs-lookup"><span data-stu-id="4c1ec-112">EXAMPLES</span></span>

### <span data-ttu-id="4c1ec-113">範例1：取得整合帳戶合作夥伴</span><span class="sxs-lookup"><span data-stu-id="4c1ec-113">Example 1: Get an integration account partner</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner22"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="4c1ec-114">這個命令會取得名為 IntegrationAccountPartner22 的整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-114">This command gets the integration account partner named IntegrationAccountPartner22.</span></span>

### <span data-ttu-id="4c1ec-115">範例2：使用整合帳戶名稱取得整合帳戶合作夥伴</span><span class="sxs-lookup"><span data-stu-id="4c1ec-115">Example 2: Get an integration account partners by using an integration account name</span></span>
```
PS C:\>Get-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31"
Id                 : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/TestIntegrationAccount/partners/IntegrationAccountPartner31
Name               : IntegrationAccountPartner31
Type               : Microsoft.Logic/integrationAccounts/partners
PartnerType        : B2B
CreatedTime        : 3/24/2016 8:46:05 PM
ChangedTime        : 3/24/2016 8:47:47 PM
BusinessIdentities : {"Qualifier":"CC","Value":"FF"}
Metadata           :
```

<span data-ttu-id="4c1ec-116">這個命令會取得名為 IntegrationAccount31 之整合帳戶的整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-116">This command gets the integration account partners for the integration account named IntegrationAccount31.</span></span>

## <span data-ttu-id="4c1ec-117">參數</span><span class="sxs-lookup"><span data-stu-id="4c1ec-117">PARAMETERS</span></span>

### <span data-ttu-id="4c1ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c1ec-118">-DefaultProfile</span></span>
<span data-ttu-id="4c1ec-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4c1ec-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c1ec-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="4c1ec-120">-Name</span></span>
<span data-ttu-id="4c1ec-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c1ec-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="4c1ec-122">-PartnerName</span></span>
<span data-ttu-id="4c1ec-123">指定整合帳戶合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="4c1ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c1ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="4c1ec-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-125">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c1ec-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c1ec-126">CommonParameters</span></span>
<span data-ttu-id="4c1ec-127">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c1ec-128">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c1ec-129">輸入</span><span class="sxs-lookup"><span data-stu-id="4c1ec-129">INPUTS</span></span>

### <span data-ttu-id="4c1ec-130">System.object</span><span class="sxs-lookup"><span data-stu-id="4c1ec-130">System.String</span></span>

## <span data-ttu-id="4c1ec-131">輸出</span><span class="sxs-lookup"><span data-stu-id="4c1ec-131">OUTPUTS</span></span>

### <span data-ttu-id="4c1ec-132">IntegrationAccountPartner 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="4c1ec-132">Microsoft.Azure.Management.Logic.Models.IntegrationAccountPartner</span></span>

## <span data-ttu-id="4c1ec-133">筆記</span><span class="sxs-lookup"><span data-stu-id="4c1ec-133">NOTES</span></span>

## <span data-ttu-id="4c1ec-134">相關連結</span><span class="sxs-lookup"><span data-stu-id="4c1ec-134">RELATED LINKS</span></span>

[<span data-ttu-id="4c1ec-135">新-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="4c1ec-135">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="4c1ec-136">移除-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="4c1ec-136">Remove-AzIntegrationAccountPartner</span></span>](./Remove-AzIntegrationAccountPartner.md)

[<span data-ttu-id="4c1ec-137">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="4c1ec-137">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


