---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/27/2020
ms.locfileid: "94141579"
---
# <span data-ttu-id="54fe1-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="54fe1-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="54fe1-102">摘要</span><span class="sxs-lookup"><span data-stu-id="54fe1-102">SYNOPSIS</span></span>
<span data-ttu-id="54fe1-103">移除 [整合] 帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="54fe1-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="54fe1-104">句法</span><span class="sxs-lookup"><span data-stu-id="54fe1-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54fe1-105">說明</span><span class="sxs-lookup"><span data-stu-id="54fe1-105">DESCRIPTION</span></span>
<span data-ttu-id="54fe1-106">**AzIntegrationAccountAgreement** Cmdlet 會從 Azure 資源群組中移除整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="54fe1-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="54fe1-107">指定整合帳戶名稱、資源群組名稱和協定名稱。</span><span class="sxs-lookup"><span data-stu-id="54fe1-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="54fe1-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="54fe1-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="54fe1-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="54fe1-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="54fe1-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="54fe1-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="54fe1-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="54fe1-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="54fe1-112">示例</span><span class="sxs-lookup"><span data-stu-id="54fe1-112">EXAMPLES</span></span>

### <span data-ttu-id="54fe1-113">範例1：依名稱移除整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="54fe1-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="54fe1-114">這個命令會移除名為 IntegrationAccountAgreement06 的整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="54fe1-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="54fe1-115">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54fe1-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="54fe1-116">參數</span><span class="sxs-lookup"><span data-stu-id="54fe1-116">PARAMETERS</span></span>

### <span data-ttu-id="54fe1-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="54fe1-117">-AgreementName</span></span>
<span data-ttu-id="54fe1-118">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="54fe1-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="54fe1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54fe1-119">-DefaultProfile</span></span>
<span data-ttu-id="54fe1-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="54fe1-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54fe1-121">-Force</span><span class="sxs-lookup"><span data-stu-id="54fe1-121">-Force</span></span>
<span data-ttu-id="54fe1-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="54fe1-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="54fe1-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="54fe1-123">-Name</span></span>
<span data-ttu-id="54fe1-124">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="54fe1-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="54fe1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54fe1-125">-ResourceGroupName</span></span>
<span data-ttu-id="54fe1-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="54fe1-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="54fe1-127">-確認</span><span class="sxs-lookup"><span data-stu-id="54fe1-127">-Confirm</span></span>
<span data-ttu-id="54fe1-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="54fe1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54fe1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54fe1-129">-WhatIf</span></span>
<span data-ttu-id="54fe1-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="54fe1-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54fe1-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="54fe1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54fe1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54fe1-132">CommonParameters</span></span>
<span data-ttu-id="54fe1-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="54fe1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54fe1-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="54fe1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54fe1-135">輸入</span><span class="sxs-lookup"><span data-stu-id="54fe1-135">INPUTS</span></span>

### <span data-ttu-id="54fe1-136">System.object</span><span class="sxs-lookup"><span data-stu-id="54fe1-136">System.String</span></span>

## <span data-ttu-id="54fe1-137">輸出</span><span class="sxs-lookup"><span data-stu-id="54fe1-137">OUTPUTS</span></span>

### <span data-ttu-id="54fe1-138">System.void</span><span class="sxs-lookup"><span data-stu-id="54fe1-138">System.Void</span></span>

## <span data-ttu-id="54fe1-139">筆記</span><span class="sxs-lookup"><span data-stu-id="54fe1-139">NOTES</span></span>

## <span data-ttu-id="54fe1-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="54fe1-140">RELATED LINKS</span></span>

[<span data-ttu-id="54fe1-141">AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="54fe1-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="54fe1-142">新-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="54fe1-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="54fe1-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="54fe1-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


