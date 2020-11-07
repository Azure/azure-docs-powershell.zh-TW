---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 88661e132e6f40f4bb8e90fac339ddf1946085c2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93624298"
---
# <span data-ttu-id="07540-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="07540-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="07540-102">摘要</span><span class="sxs-lookup"><span data-stu-id="07540-102">SYNOPSIS</span></span>
<span data-ttu-id="07540-103">移除 [整合] 帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="07540-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="07540-104">句法</span><span class="sxs-lookup"><span data-stu-id="07540-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07540-105">說明</span><span class="sxs-lookup"><span data-stu-id="07540-105">DESCRIPTION</span></span>
<span data-ttu-id="07540-106">**AzureRmIntegrationAccountAgreement** Cmdlet 會從 Azure 資源群組中移除整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="07540-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="07540-107">指定整合帳戶名稱、資源群組名稱和協定名稱。</span><span class="sxs-lookup"><span data-stu-id="07540-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="07540-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="07540-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="07540-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="07540-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="07540-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="07540-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="07540-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="07540-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="07540-112">示例</span><span class="sxs-lookup"><span data-stu-id="07540-112">EXAMPLES</span></span>

### <span data-ttu-id="07540-113">範例1：依名稱移除整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="07540-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="07540-114">這個命令會移除名為 IntegrationAccountAgreement06 的整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="07540-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="07540-115">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="07540-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="07540-116">參數</span><span class="sxs-lookup"><span data-stu-id="07540-116">PARAMETERS</span></span>

### <span data-ttu-id="07540-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="07540-117">-AgreementName</span></span>
<span data-ttu-id="07540-118">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="07540-118">Specifies the name of the integration account agreement.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07540-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07540-119">-DefaultProfile</span></span>
<span data-ttu-id="07540-120">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="07540-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07540-121">-Force</span><span class="sxs-lookup"><span data-stu-id="07540-121">-Force</span></span>
<span data-ttu-id="07540-122">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="07540-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07540-123">-名稱</span><span class="sxs-lookup"><span data-stu-id="07540-123">-Name</span></span>
<span data-ttu-id="07540-124">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="07540-124">Specifies the name of an integration account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07540-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07540-125">-ResourceGroupName</span></span>
<span data-ttu-id="07540-126">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="07540-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="07540-127">-確認</span><span class="sxs-lookup"><span data-stu-id="07540-127">-Confirm</span></span>
<span data-ttu-id="07540-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="07540-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07540-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07540-129">-WhatIf</span></span>
<span data-ttu-id="07540-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="07540-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07540-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="07540-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07540-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07540-132">CommonParameters</span></span>
<span data-ttu-id="07540-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="07540-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07540-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="07540-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07540-135">輸入</span><span class="sxs-lookup"><span data-stu-id="07540-135">INPUTS</span></span>

### <span data-ttu-id="07540-136">所有</span><span class="sxs-lookup"><span data-stu-id="07540-136">None</span></span>
<span data-ttu-id="07540-137">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="07540-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="07540-138">輸出</span><span class="sxs-lookup"><span data-stu-id="07540-138">OUTPUTS</span></span>

## <span data-ttu-id="07540-139">筆記</span><span class="sxs-lookup"><span data-stu-id="07540-139">NOTES</span></span>

## <span data-ttu-id="07540-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="07540-140">RELATED LINKS</span></span>

[<span data-ttu-id="07540-141">AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="07540-141">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="07540-142">新-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="07540-142">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="07540-143">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="07540-143">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


