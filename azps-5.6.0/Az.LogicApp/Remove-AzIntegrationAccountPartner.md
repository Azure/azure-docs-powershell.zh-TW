---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: 4c50f7de3d3748f254d87910fc8c55bb0ba8fc22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101905385"
---
# <span data-ttu-id="b8a2f-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b8a2f-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="b8a2f-102">簡介</span><span class="sxs-lookup"><span data-stu-id="b8a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="b8a2f-103">移除整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="b8a2f-104">語法</span><span class="sxs-lookup"><span data-stu-id="b8a2f-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8a2f-105">描述</span><span class="sxs-lookup"><span data-stu-id="b8a2f-105">DESCRIPTION</span></span>
<span data-ttu-id="b8a2f-106">**Remove-Az方AccountPartner Cmdlet** 會從資源群組移除整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="b8a2f-107">指定整合帳戶名稱、資源組名和合作夥伴名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="b8a2f-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="b8a2f-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="b8a2f-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="b8a2f-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="b8a2f-112">例子</span><span class="sxs-lookup"><span data-stu-id="b8a2f-112">EXAMPLES</span></span>

### <span data-ttu-id="b8a2f-113">範例 1：移除整合帳戶合作夥伴</span><span class="sxs-lookup"><span data-stu-id="b8a2f-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="b8a2f-114">此命令會移除名為 IntegrationAccountPartner1 的整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="b8a2f-115">參數</span><span class="sxs-lookup"><span data-stu-id="b8a2f-115">PARAMETERS</span></span>

### <span data-ttu-id="b8a2f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8a2f-116">-DefaultProfile</span></span>
<span data-ttu-id="b8a2f-117">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="b8a2f-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b8a2f-118">-強制</span><span class="sxs-lookup"><span data-stu-id="b8a2f-118">-Force</span></span>
<span data-ttu-id="b8a2f-119">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b8a2f-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="b8a2f-120">-Name</span></span>
<span data-ttu-id="b8a2f-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="b8a2f-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="b8a2f-122">-PartnerName</span></span>
<span data-ttu-id="b8a2f-123">指定整合帳戶合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="b8a2f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8a2f-124">-ResourceGroupName</span></span>
<span data-ttu-id="b8a2f-125">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="b8a2f-126">-確認</span><span class="sxs-lookup"><span data-stu-id="b8a2f-126">-Confirm</span></span>
<span data-ttu-id="b8a2f-127">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8a2f-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8a2f-128">-WhatIf</span></span>
<span data-ttu-id="b8a2f-129">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b8a2f-130">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8a2f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8a2f-131">CommonParameters</span></span>
<span data-ttu-id="b8a2f-132">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8a2f-133">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="b8a2f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8a2f-134">輸入</span><span class="sxs-lookup"><span data-stu-id="b8a2f-134">INPUTS</span></span>

### <span data-ttu-id="b8a2f-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b8a2f-135">System.String</span></span>

## <span data-ttu-id="b8a2f-136">輸出</span><span class="sxs-lookup"><span data-stu-id="b8a2f-136">OUTPUTS</span></span>

### <span data-ttu-id="b8a2f-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="b8a2f-137">System.Void</span></span>

## <span data-ttu-id="b8a2f-138">筆記</span><span class="sxs-lookup"><span data-stu-id="b8a2f-138">NOTES</span></span>

## <span data-ttu-id="b8a2f-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="b8a2f-139">RELATED LINKS</span></span>

[<span data-ttu-id="b8a2f-140">Get-Az方AccountPartner</span><span class="sxs-lookup"><span data-stu-id="b8a2f-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="b8a2f-141">New-AzCountAccountPartner</span><span class="sxs-lookup"><span data-stu-id="b8a2f-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="b8a2f-142">Set-Az方AccountPartner</span><span class="sxs-lookup"><span data-stu-id="b8a2f-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


