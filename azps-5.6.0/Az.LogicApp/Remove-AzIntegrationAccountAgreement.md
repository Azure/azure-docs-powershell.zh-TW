---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: cd15a6f132360bba973e9361cf2f6e98c9bf24f8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "101906157"
---
# <span data-ttu-id="afd57-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="afd57-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="afd57-102">簡介</span><span class="sxs-lookup"><span data-stu-id="afd57-102">SYNOPSIS</span></span>
<span data-ttu-id="afd57-103">移除整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="afd57-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="afd57-104">語法</span><span class="sxs-lookup"><span data-stu-id="afd57-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd57-105">描述</span><span class="sxs-lookup"><span data-stu-id="afd57-105">DESCRIPTION</span></span>
<span data-ttu-id="afd57-106">**Remove-AzEmentAccountAgreement Cmdlet** 會從 Azure 資源群組移除整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="afd57-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="afd57-107">指定整合帳戶名稱、資源組名和協定名稱。</span><span class="sxs-lookup"><span data-stu-id="afd57-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="afd57-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="afd57-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="afd57-109">若要使用動態參數，請于命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="afd57-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="afd57-110">若要探索動態參數的名稱，在 Cmdlet 名稱之後輸入連字號 (-) ，然後重複按 Tab 鍵以迴圈流覽可用的參數。</span><span class="sxs-lookup"><span data-stu-id="afd57-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="afd57-111">如果您省略必要的範本參數，Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="afd57-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="afd57-112">例子</span><span class="sxs-lookup"><span data-stu-id="afd57-112">EXAMPLES</span></span>

### <span data-ttu-id="afd57-113">範例 1：根據名稱移除整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="afd57-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="afd57-114">此命令會移除名為 IntegrationAccountAgreement06 的整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="afd57-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="afd57-115">命令不會提示您確認。</span><span class="sxs-lookup"><span data-stu-id="afd57-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="afd57-116">參數</span><span class="sxs-lookup"><span data-stu-id="afd57-116">PARAMETERS</span></span>

### <span data-ttu-id="afd57-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="afd57-117">-AgreementName</span></span>
<span data-ttu-id="afd57-118">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="afd57-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="afd57-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd57-119">-DefaultProfile</span></span>
<span data-ttu-id="afd57-120">用於與 Azure 通訊的認證、帳戶、租使用者和訂閱</span><span class="sxs-lookup"><span data-stu-id="afd57-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="afd57-121">-強制</span><span class="sxs-lookup"><span data-stu-id="afd57-121">-Force</span></span>
<span data-ttu-id="afd57-122">強制執行命令，但不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="afd57-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="afd57-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="afd57-123">-Name</span></span>
<span data-ttu-id="afd57-124">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="afd57-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="afd57-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="afd57-125">-ResourceGroupName</span></span>
<span data-ttu-id="afd57-126">指定資源組的名稱。</span><span class="sxs-lookup"><span data-stu-id="afd57-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="afd57-127">-確認</span><span class="sxs-lookup"><span data-stu-id="afd57-127">-Confirm</span></span>
<span data-ttu-id="afd57-128">執行 Cmdlet 之前，提示您確認。</span><span class="sxs-lookup"><span data-stu-id="afd57-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afd57-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd57-129">-WhatIf</span></span>
<span data-ttu-id="afd57-130">顯示 Cmdlet 執行時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="afd57-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="afd57-131">不會執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="afd57-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afd57-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd57-132">CommonParameters</span></span>
<span data-ttu-id="afd57-133">此 Cmdlet 支援常見的參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-Verbose、-WarningAction 和 -WarningVariable。</span><span class="sxs-lookup"><span data-stu-id="afd57-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd57-134">詳細資訊請參閱 http://go.microsoft.com/fwlink/?LinkID=113216) about_CommonParameters (。</span><span class="sxs-lookup"><span data-stu-id="afd57-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd57-135">輸入</span><span class="sxs-lookup"><span data-stu-id="afd57-135">INPUTS</span></span>

### <span data-ttu-id="afd57-136">System.String</span><span class="sxs-lookup"><span data-stu-id="afd57-136">System.String</span></span>

## <span data-ttu-id="afd57-137">輸出</span><span class="sxs-lookup"><span data-stu-id="afd57-137">OUTPUTS</span></span>

### <span data-ttu-id="afd57-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="afd57-138">System.Void</span></span>

## <span data-ttu-id="afd57-139">筆記</span><span class="sxs-lookup"><span data-stu-id="afd57-139">NOTES</span></span>

## <span data-ttu-id="afd57-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="afd57-140">RELATED LINKS</span></span>

[<span data-ttu-id="afd57-141">Get-AzEmentAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="afd57-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="afd57-142">New-AzEmentAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="afd57-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="afd57-143">Set-AzEmentAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="afd57-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


