---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountAgreement.md
ms.openlocfilehash: 63241b764576e06166e293f17717b26c4dcbe3d8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93452484"
---
# <span data-ttu-id="f5f53-101">Remove-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f5f53-101">Remove-AzureRmIntegrationAccountAgreement</span></span>

## <span data-ttu-id="f5f53-102">摘要</span><span class="sxs-lookup"><span data-stu-id="f5f53-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f53-103">移除 [整合] 帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="f5f53-103">Removes an integration account agreement.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5f53-104">句法</span><span class="sxs-lookup"><span data-stu-id="f5f53-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5f53-105">說明</span><span class="sxs-lookup"><span data-stu-id="f5f53-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f53-106">**AzureRmIntegrationAccountAgreement** Cmdlet 會從 Azure 資源群組中移除整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="f5f53-106">The **Remove-AzureRmIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="f5f53-107">指定整合帳戶名稱、資源群組名稱和協定名稱。</span><span class="sxs-lookup"><span data-stu-id="f5f53-107">Specify the integration account name, resource group name, and agreement name.</span></span>

<span data-ttu-id="f5f53-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="f5f53-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f5f53-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="f5f53-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f5f53-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="f5f53-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f5f53-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="f5f53-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f5f53-112">示例</span><span class="sxs-lookup"><span data-stu-id="f5f53-112">EXAMPLES</span></span>

### <span data-ttu-id="f5f53-113">範例1：依名稱移除整合帳戶協定</span><span class="sxs-lookup"><span data-stu-id="f5f53-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="f5f53-114">這個命令會移除名為 IntegrationAccountAgreement06 的整合帳戶協定。</span><span class="sxs-lookup"><span data-stu-id="f5f53-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="f5f53-115">該命令不會提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5f53-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="f5f53-116">參數</span><span class="sxs-lookup"><span data-stu-id="f5f53-116">PARAMETERS</span></span>

### <span data-ttu-id="f5f53-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="f5f53-117">-AgreementName</span></span>
<span data-ttu-id="f5f53-118">指定整合帳戶協定的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5f53-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="f5f53-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f5f53-119">-Force</span></span>
<span data-ttu-id="f5f53-120">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="f5f53-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f5f53-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="f5f53-121">-Name</span></span>
<span data-ttu-id="f5f53-122">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5f53-122">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="f5f53-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5f53-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5f53-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5f53-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f5f53-125">-確認</span><span class="sxs-lookup"><span data-stu-id="f5f53-125">-Confirm</span></span>
<span data-ttu-id="f5f53-126">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="f5f53-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5f53-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5f53-127">-WhatIf</span></span>
<span data-ttu-id="f5f53-128">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="f5f53-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f5f53-129">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="f5f53-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5f53-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f53-130">-DefaultProfile</span></span>
<span data-ttu-id="f5f53-131">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱。</span><span class="sxs-lookup"><span data-stu-id="f5f53-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5f53-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f53-132">CommonParameters</span></span>
<span data-ttu-id="f5f53-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="f5f53-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f53-134">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="f5f53-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f53-135">輸入</span><span class="sxs-lookup"><span data-stu-id="f5f53-135">INPUTS</span></span>

## <span data-ttu-id="f5f53-136">輸出</span><span class="sxs-lookup"><span data-stu-id="f5f53-136">OUTPUTS</span></span>

## <span data-ttu-id="f5f53-137">筆記</span><span class="sxs-lookup"><span data-stu-id="f5f53-137">NOTES</span></span>

## <span data-ttu-id="f5f53-138">相關連結</span><span class="sxs-lookup"><span data-stu-id="f5f53-138">RELATED LINKS</span></span>

[<span data-ttu-id="f5f53-139">AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f5f53-139">Get-AzureRmIntegrationAccountAgreement</span></span>](./Get-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="f5f53-140">新-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f5f53-140">New-AzureRmIntegrationAccountAgreement</span></span>](./New-AzureRmIntegrationAccountAgreement.md)

[<span data-ttu-id="f5f53-141">Set-AzureRmIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="f5f53-141">Set-AzureRmIntegrationAccountAgreement</span></span>](./Set-AzureRmIntegrationAccountAgreement.md)


