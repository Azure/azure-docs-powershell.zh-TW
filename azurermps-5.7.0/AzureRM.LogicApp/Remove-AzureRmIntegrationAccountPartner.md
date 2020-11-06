---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.logicapp/remove-azurermintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountPartner.md
ms.openlocfilehash: 29eb57e7c076499f105bec9e2400091ac11b09fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93447075"
---
# <span data-ttu-id="40880-101">Remove-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="40880-101">Remove-AzureRmIntegrationAccountPartner</span></span>

## <span data-ttu-id="40880-102">摘要</span><span class="sxs-lookup"><span data-stu-id="40880-102">SYNOPSIS</span></span>
<span data-ttu-id="40880-103">移除整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="40880-103">Removes an integration account partner.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="40880-104">句法</span><span class="sxs-lookup"><span data-stu-id="40880-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40880-105">說明</span><span class="sxs-lookup"><span data-stu-id="40880-105">DESCRIPTION</span></span>
<span data-ttu-id="40880-106">**AzureRmIntegrationAccountPartner** Cmdlet 會從資源群組中移除整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="40880-106">The **Remove-AzureRmIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="40880-107">指定整合帳戶名稱、資源群組名稱，以及合作夥伴名稱。</span><span class="sxs-lookup"><span data-stu-id="40880-107">Specify the integration account name, resource group name, and partner name.</span></span>

<span data-ttu-id="40880-108">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="40880-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="40880-109">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="40880-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="40880-110">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="40880-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="40880-111">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="40880-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="40880-112">示例</span><span class="sxs-lookup"><span data-stu-id="40880-112">EXAMPLES</span></span>

### <span data-ttu-id="40880-113">範例1：移除整合帳戶合作夥伴</span><span class="sxs-lookup"><span data-stu-id="40880-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="40880-114">這個命令會移除名為 IntegrationAccountPartner1 的整合帳戶合作夥伴。</span><span class="sxs-lookup"><span data-stu-id="40880-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="40880-115">參數</span><span class="sxs-lookup"><span data-stu-id="40880-115">PARAMETERS</span></span>

### <span data-ttu-id="40880-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40880-116">-DefaultProfile</span></span>
<span data-ttu-id="40880-117">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="40880-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="40880-118">-Force</span><span class="sxs-lookup"><span data-stu-id="40880-118">-Force</span></span>
<span data-ttu-id="40880-119">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="40880-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="40880-120">-名稱</span><span class="sxs-lookup"><span data-stu-id="40880-120">-Name</span></span>
<span data-ttu-id="40880-121">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="40880-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="40880-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="40880-122">-PartnerName</span></span>
<span data-ttu-id="40880-123">指定整合帳戶合作夥伴的名稱。</span><span class="sxs-lookup"><span data-stu-id="40880-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="40880-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40880-124">-ResourceGroupName</span></span>
<span data-ttu-id="40880-125">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="40880-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="40880-126">-確認</span><span class="sxs-lookup"><span data-stu-id="40880-126">-Confirm</span></span>
<span data-ttu-id="40880-127">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="40880-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40880-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40880-128">-WhatIf</span></span>
<span data-ttu-id="40880-129">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="40880-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40880-130">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="40880-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40880-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40880-131">CommonParameters</span></span>
<span data-ttu-id="40880-132">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="40880-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40880-133">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="40880-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40880-134">輸入</span><span class="sxs-lookup"><span data-stu-id="40880-134">INPUTS</span></span>

### <span data-ttu-id="40880-135">所有</span><span class="sxs-lookup"><span data-stu-id="40880-135">None</span></span>
<span data-ttu-id="40880-136">這個 Cmdlet 不接受任何輸入。</span><span class="sxs-lookup"><span data-stu-id="40880-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="40880-137">輸出</span><span class="sxs-lookup"><span data-stu-id="40880-137">OUTPUTS</span></span>

## <span data-ttu-id="40880-138">筆記</span><span class="sxs-lookup"><span data-stu-id="40880-138">NOTES</span></span>

## <span data-ttu-id="40880-139">相關連結</span><span class="sxs-lookup"><span data-stu-id="40880-139">RELATED LINKS</span></span>

[<span data-ttu-id="40880-140">AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="40880-140">Get-AzureRmIntegrationAccountPartner</span></span>](./Get-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="40880-141">新-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="40880-141">New-AzureRmIntegrationAccountPartner</span></span>](./New-AzureRmIntegrationAccountPartner.md)

[<span data-ttu-id="40880-142">Set-AzureRmIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="40880-142">Set-AzureRmIntegrationAccountPartner</span></span>](./Set-AzureRmIntegrationAccountPartner.md)


