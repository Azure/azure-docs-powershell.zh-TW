---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 5F1A4FE0-CB57-45D3-9F08-879469A61E1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccount.md
ms.openlocfilehash: a3a3fc16b253235da82626ab6d827d074f05860d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/09/2021
ms.locfileid: "100136130"
---
# <span data-ttu-id="4f9bd-101">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4f9bd-101">New-AzIntegrationAccount</span></span>

## <span data-ttu-id="4f9bd-102">摘要</span><span class="sxs-lookup"><span data-stu-id="4f9bd-102">SYNOPSIS</span></span>
<span data-ttu-id="4f9bd-103">建立整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-103">Creates an integration account.</span></span>

## <span data-ttu-id="4f9bd-104">句法</span><span class="sxs-lookup"><span data-stu-id="4f9bd-104">SYNTAX</span></span>

```
New-AzIntegrationAccount -ResourceGroupName <String> -Name <String> -Location <String> [-Sku <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4f9bd-105">說明</span><span class="sxs-lookup"><span data-stu-id="4f9bd-105">DESCRIPTION</span></span>
<span data-ttu-id="4f9bd-106">**新的-AzIntegrationAccount** Cmdlet 會建立整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-106">The **New-AzIntegrationAccount** cmdlet creates an integration account.</span></span>
<span data-ttu-id="4f9bd-107">這個 Cmdlet 會傳回代表整合帳戶的物件。指定名稱、位置、資源群組名稱及 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-107">This cmdlet returns an object that represents the integration account.Specify a name, location, resource group name, and SKU name.</span></span>
<span data-ttu-id="4f9bd-108">您在命令列中指定的範本參數檔值優先于 template 參數物件中的範本參數值。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-108">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="4f9bd-109">此模組支援動態參數。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="4f9bd-110">若要使用動態參數，請在命令中輸入。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="4f9bd-111">若要探索動態參數的名稱，請在 Cmdlet 名稱後輸入連字號 ( ) ，然後重複按 Tab 鍵以迴圈顯示可用的參數。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="4f9bd-112">如果您省略必要的範本參數，則 Cmdlet 會提示您輸入值。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="4f9bd-113">示例</span><span class="sxs-lookup"><span data-stu-id="4f9bd-113">EXAMPLES</span></span>

### <span data-ttu-id="4f9bd-114">範例1：建立整合帳戶</span><span class="sxs-lookup"><span data-stu-id="4f9bd-114">Example 1: Create an integration account</span></span>
```
PS C:\>New-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Location "brazilsouth" -Sku "Standard"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="4f9bd-115">這個命令會在指定的資源群組中建立名為 IntegrationAccount31 的整合帳戶。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-115">This command creates an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="4f9bd-116">參數</span><span class="sxs-lookup"><span data-stu-id="4f9bd-116">PARAMETERS</span></span>

### <span data-ttu-id="4f9bd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f9bd-117">-DefaultProfile</span></span>
<span data-ttu-id="4f9bd-118">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="4f9bd-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4f9bd-119">-位置</span><span class="sxs-lookup"><span data-stu-id="4f9bd-119">-Location</span></span>
<span data-ttu-id="4f9bd-120">指定整合帳戶的位置。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-120">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="4f9bd-121">-名稱</span><span class="sxs-lookup"><span data-stu-id="4f9bd-121">-Name</span></span>
<span data-ttu-id="4f9bd-122">指定整合帳戶的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-122">Specifies a name for the integration account.</span></span>

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

### <span data-ttu-id="4f9bd-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f9bd-123">-ResourceGroupName</span></span>
<span data-ttu-id="4f9bd-124">指定資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4f9bd-125">-Sku</span><span class="sxs-lookup"><span data-stu-id="4f9bd-125">-Sku</span></span>
<span data-ttu-id="4f9bd-126">指定整合帳戶的 SKU 名稱。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-126">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f9bd-127">-確認</span><span class="sxs-lookup"><span data-stu-id="4f9bd-127">-Confirm</span></span>
<span data-ttu-id="4f9bd-128">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f9bd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f9bd-129">-WhatIf</span></span>
<span data-ttu-id="4f9bd-130">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f9bd-131">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f9bd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f9bd-132">CommonParameters</span></span>
<span data-ttu-id="4f9bd-133">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f9bd-134">如需詳細資訊，請參閱 about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f9bd-135">輸入</span><span class="sxs-lookup"><span data-stu-id="4f9bd-135">INPUTS</span></span>

### <span data-ttu-id="4f9bd-136">System.object</span><span class="sxs-lookup"><span data-stu-id="4f9bd-136">System.String</span></span>

## <span data-ttu-id="4f9bd-137">輸出</span><span class="sxs-lookup"><span data-stu-id="4f9bd-137">OUTPUTS</span></span>

### <span data-ttu-id="4f9bd-138">IntegrationAccount 的管理邏輯。</span><span class="sxs-lookup"><span data-stu-id="4f9bd-138">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="4f9bd-139">筆記</span><span class="sxs-lookup"><span data-stu-id="4f9bd-139">NOTES</span></span>

## <span data-ttu-id="4f9bd-140">相關連結</span><span class="sxs-lookup"><span data-stu-id="4f9bd-140">RELATED LINKS</span></span>

[<span data-ttu-id="4f9bd-141">AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4f9bd-141">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="4f9bd-142">移除-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4f9bd-142">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)

[<span data-ttu-id="4f9bd-143">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="4f9bd-143">Set-AzIntegrationAccount</span></span>](./Set-AzIntegrationAccount.md)


