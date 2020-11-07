---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: ee4f24356c33aac0940a10905b52199bd06d2a47
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/21/2020
ms.locfileid: "93957325"
---
# <span data-ttu-id="3e535-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e535-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="3e535-102">摘要</span><span class="sxs-lookup"><span data-stu-id="3e535-102">SYNOPSIS</span></span>
<span data-ttu-id="3e535-103">移除整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="3e535-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="3e535-104">句法</span><span class="sxs-lookup"><span data-stu-id="3e535-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e535-105">說明</span><span class="sxs-lookup"><span data-stu-id="3e535-105">DESCRIPTION</span></span>
<span data-ttu-id="3e535-106">**AzIntegrationAccountPartner** Cmdlet 會從資源群組中移除整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="3e535-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="3e535-107">指定整合帳戶名稱、資源群組名稱，以及合作夥伴名稱。</span><span class="sxs-lookup"><span data-stu-id="3e535-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="3e535-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="3e535-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3e535-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="3e535-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3e535-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="3e535-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3e535-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="3e535-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3e535-112">示例</span><span class="sxs-lookup"><span data-stu-id="3e535-112">EXAMPLES</span></span>

### <span data-ttu-id="3e535-113">範例1：移除整合帳戶合作夥伴</span><span class="sxs-lookup"><span data-stu-id="3e535-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="3e535-114">這個命令會移除名為 IntegrationAccountPartner1 的整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="3e535-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="3e535-115">參數</span><span class="sxs-lookup"><span data-stu-id="3e535-115">PARAMETERS</span></span>

### <span data-ttu-id="3e535-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e535-116">-DefaultProfile</span></span>
<span data-ttu-id="3e535-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="3e535-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e535-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3e535-118">-Force</span></span>
<span data-ttu-id="3e535-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="3e535-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3e535-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="3e535-120">-Name</span></span>
<span data-ttu-id="3e535-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e535-121">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e535-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="3e535-122">-PartnerName</span></span>
<span data-ttu-id="3e535-123">指定整合帳戶合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e535-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="3e535-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e535-124">-ResourceGroupName</span></span>
<span data-ttu-id="3e535-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="3e535-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3e535-126">-確認</span><span class="sxs-lookup"><span data-stu-id="3e535-126">-Confirm</span></span>
<span data-ttu-id="3e535-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="3e535-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e535-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e535-128">-WhatIf</span></span>
<span data-ttu-id="3e535-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="3e535-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e535-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="3e535-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e535-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e535-131">CommonParameters</span></span>
<span data-ttu-id="3e535-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="3e535-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e535-133">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="3e535-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e535-134">輸入</span><span class="sxs-lookup"><span data-stu-id="3e535-134">INPUTS</span></span>

### <span data-ttu-id="3e535-135">System.object</span><span class="sxs-lookup"><span data-stu-id="3e535-135">System.String</span></span>

## <span data-ttu-id="3e535-136">輸出</span><span class="sxs-lookup"><span data-stu-id="3e535-136">OUTPUTS</span></span>

### <span data-ttu-id="3e535-137">System.void</span><span class="sxs-lookup"><span data-stu-id="3e535-137">System.Void</span></span>

## <span data-ttu-id="3e535-138">筆記</span><span class="sxs-lookup"><span data-stu-id="3e535-138">NOTES</span></span>

## <span data-ttu-id="3e535-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="3e535-139">RELATED LINKS</span></span>

[<span data-ttu-id="3e535-140">AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e535-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3e535-141">新-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e535-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="3e535-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="3e535-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


