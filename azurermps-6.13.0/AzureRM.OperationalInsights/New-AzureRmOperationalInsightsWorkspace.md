---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 4682807D-34E8-4057-8894-36820447067B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 97f8cba0641ed576cb187f3b995d400bc7f521a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "93450193"
---
# <span data-ttu-id="50aaa-101">New-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="50aaa-101">New-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="50aaa-102">摘要</span><span class="sxs-lookup"><span data-stu-id="50aaa-102">SYNOPSIS</span></span>
<span data-ttu-id="50aaa-103">建立工作區。</span><span class="sxs-lookup"><span data-stu-id="50aaa-103">Creates a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50aaa-104">句法</span><span class="sxs-lookup"><span data-stu-id="50aaa-104">SYNTAX</span></span>

```
New-AzureRmOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-Sku] <String>] [[-CustomerId] <Guid>] [[-Tag] <Hashtable>] [[-RetentionInDays] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50aaa-105">說明</span><span class="sxs-lookup"><span data-stu-id="50aaa-105">DESCRIPTION</span></span>
<span data-ttu-id="50aaa-106">**新的-AzureRmOperationalInsightsWorkspace** Cmdlet 會在指定的資源群組和位置中建立一個工作區。</span><span class="sxs-lookup"><span data-stu-id="50aaa-106">The **New-AzureRmOperationalInsightsWorkspace** cmdlet creates a workspace in the specified resource group and location.</span></span>

## <span data-ttu-id="50aaa-107">示例</span><span class="sxs-lookup"><span data-stu-id="50aaa-107">EXAMPLES</span></span>

### <span data-ttu-id="50aaa-108">範例1：依名稱建立工作區</span><span class="sxs-lookup"><span data-stu-id="50aaa-108">Example 1: Create a workspace by name</span></span>
```
PS C:\>New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Location "East US" -Sku "Standard"
```

<span data-ttu-id="50aaa-109">這個命令會在名為 [ContosoResourceGroup] 的資源群組中，建立名為 MyWorkspace 的標準 SKU 工作區。</span><span class="sxs-lookup"><span data-stu-id="50aaa-109">This command creates a standard SKU workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="50aaa-110">範例2：建立工作區並將其連結至現有的帳戶</span><span class="sxs-lookup"><span data-stu-id="50aaa-110">Example 2: Create a workspace and link it to an existing account</span></span>
```
PS C:\>$OILinkTargets = Get-AzureRmOperationalInsightsLinkTargets

PS C:\>$OILinkTargets[0] | New-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" -Sku "Standard"
```

<span data-ttu-id="50aaa-111">第一個命令使用 Get-AzureRmOperationalInsightsLinkTargets Cmdlet 來取得 Operational Insights 帳戶連結目標，然後將它們儲存在 $OILinkTargets 變數中。</span><span class="sxs-lookup"><span data-stu-id="50aaa-111">The first command uses the Get-AzureRmOperationalInsightsLinkTargets cmdlet to get Operational Insights account link targets, and then stores them in the $OILinkTargets variable.</span></span>
<span data-ttu-id="50aaa-112">第二個命令會使用管線運算子，將 $OILinkTargets 中的第一個帳戶連結目標傳遞給 **AzureRmOperationalInsightsWorkspace** Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50aaa-112">The second command passes the first account link target in $OILinkTargets to the **New-AzureRmOperationalInsightsWorkspace** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="50aaa-113">此命令會建立一個名為 MyWorkspace 的標準 SKU 工作區，該工作區已連結至 $OILinkTargets 中第一個 Operational Insights 帳戶。</span><span class="sxs-lookup"><span data-stu-id="50aaa-113">The command creates a standard SKU workspace named MyWorkspace that is linked to the first Operational Insights account in $OILinkTargets.</span></span>

## <span data-ttu-id="50aaa-114">參數</span><span class="sxs-lookup"><span data-stu-id="50aaa-114">PARAMETERS</span></span>

### <span data-ttu-id="50aaa-115">-CustomerId</span><span class="sxs-lookup"><span data-stu-id="50aaa-115">-CustomerId</span></span>
<span data-ttu-id="50aaa-116">指定此工作區將連結到哪個帳戶。</span><span class="sxs-lookup"><span data-stu-id="50aaa-116">Specifies the account to which this workspace will be linked.</span></span>
<span data-ttu-id="50aaa-117">您也可以使用 Get-AzureRmOperationalInsightsLinkTargets Cmdlet 來列出潛在的帳戶。</span><span class="sxs-lookup"><span data-stu-id="50aaa-117">The Get-AzureRmOperationalInsightsLinkTargets cmdlet can also be used to list the potential accounts.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50aaa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50aaa-118">-DefaultProfile</span></span>
<span data-ttu-id="50aaa-119">用於與 azure 進行通訊的認證、帳戶、租使用者及訂閱</span><span class="sxs-lookup"><span data-stu-id="50aaa-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50aaa-120">-Force</span><span class="sxs-lookup"><span data-stu-id="50aaa-120">-Force</span></span>
<span data-ttu-id="50aaa-121">強制執行命令，而不要求使用者確認。</span><span class="sxs-lookup"><span data-stu-id="50aaa-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="50aaa-122">-位置</span><span class="sxs-lookup"><span data-stu-id="50aaa-122">-Location</span></span>
<span data-ttu-id="50aaa-123">指定要建立工作區的位置，例如 [東美國] 或 [西部]。</span><span class="sxs-lookup"><span data-stu-id="50aaa-123">Specifies the location in which to create the workspace, for example, East US or West Europe.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50aaa-124">-名稱</span><span class="sxs-lookup"><span data-stu-id="50aaa-124">-Name</span></span>
<span data-ttu-id="50aaa-125">指定工作區的名稱。</span><span class="sxs-lookup"><span data-stu-id="50aaa-125">Specifies the name of the workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50aaa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50aaa-126">-ResourceGroupName</span></span>
<span data-ttu-id="50aaa-127">指定 Azure 資源群組的名稱。</span><span class="sxs-lookup"><span data-stu-id="50aaa-127">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="50aaa-128">工作區是在此資源群組中建立。</span><span class="sxs-lookup"><span data-stu-id="50aaa-128">The workspace is created in this resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50aaa-129">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="50aaa-129">-RetentionInDays</span></span>
<span data-ttu-id="50aaa-130">工作區資料保留天數（天）。</span><span class="sxs-lookup"><span data-stu-id="50aaa-130">The workspace data retention in days.</span></span> <span data-ttu-id="50aaa-131">730 days 是所有其他 Sku 允許的上限</span><span class="sxs-lookup"><span data-stu-id="50aaa-131">730 days is the maximum allowed for all other Skus</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50aaa-132">-Sku</span><span class="sxs-lookup"><span data-stu-id="50aaa-132">-Sku</span></span>
<span data-ttu-id="50aaa-133">指定工作區的服務層級。</span><span class="sxs-lookup"><span data-stu-id="50aaa-133">Specifies the service tier of the workspace.</span></span>
<span data-ttu-id="50aaa-134">有效值為：</span><span class="sxs-lookup"><span data-stu-id="50aaa-134">Valid values are:</span></span> 
- <span data-ttu-id="50aaa-135">空閒</span><span class="sxs-lookup"><span data-stu-id="50aaa-135">free</span></span>
- <span data-ttu-id="50aaa-136">標準</span><span class="sxs-lookup"><span data-stu-id="50aaa-136">standard</span></span>
- <span data-ttu-id="50aaa-137">佳</span><span class="sxs-lookup"><span data-stu-id="50aaa-137">premium</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: free, standard, premium, pernode, standalone

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50aaa-138">-Tag</span><span class="sxs-lookup"><span data-stu-id="50aaa-138">-Tag</span></span>
<span data-ttu-id="50aaa-139">工作區的資源標記。</span><span class="sxs-lookup"><span data-stu-id="50aaa-139">The resource tags for the workspace.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50aaa-140">-確認</span><span class="sxs-lookup"><span data-stu-id="50aaa-140">-Confirm</span></span>
<span data-ttu-id="50aaa-141">在執行 Cmdlet 之前提示您進行確認。</span><span class="sxs-lookup"><span data-stu-id="50aaa-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50aaa-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50aaa-142">-WhatIf</span></span>
<span data-ttu-id="50aaa-143">顯示在執行 Cmdlet 時會發生什麼情況。</span><span class="sxs-lookup"><span data-stu-id="50aaa-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50aaa-144">未執行 Cmdlet。</span><span class="sxs-lookup"><span data-stu-id="50aaa-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50aaa-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50aaa-145">CommonParameters</span></span>
<span data-ttu-id="50aaa-146">這個 Cmdlet 支援通用參數：-Debug、-ErrorAction、-ErrorVariable、-InformationAction、-InformationVariable、-OutVariable、-OutBuffer、-PipelineVariable、-WarningAction、-WarningVariable、-、-、-、-、-、-。</span><span class="sxs-lookup"><span data-stu-id="50aaa-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50aaa-147">如需詳細資訊，請參閱 about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216) 。</span><span class="sxs-lookup"><span data-stu-id="50aaa-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50aaa-148">輸入</span><span class="sxs-lookup"><span data-stu-id="50aaa-148">INPUTS</span></span>

### <span data-ttu-id="50aaa-149">System.object</span><span class="sxs-lookup"><span data-stu-id="50aaa-149">System.String</span></span>

### <span data-ttu-id="50aaa-150">系統. Nullable "1 [[System. Guid，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="50aaa-150">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="50aaa-151">[System.object] 集合. Hashtable</span><span class="sxs-lookup"><span data-stu-id="50aaa-151">System.Collections.Hashtable</span></span>

### <span data-ttu-id="50aaa-152">System.object "1 [[System. Int32，mscorlib，版本 = 4.0.0.0，Culture = 中性，PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="50aaa-152">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="50aaa-153">輸出</span><span class="sxs-lookup"><span data-stu-id="50aaa-153">OUTPUTS</span></span>

### <span data-ttu-id="50aaa-154">PSWorkspace 中的 OperationalInsights。</span><span class="sxs-lookup"><span data-stu-id="50aaa-154">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="50aaa-155">筆記</span><span class="sxs-lookup"><span data-stu-id="50aaa-155">NOTES</span></span>

## <span data-ttu-id="50aaa-156">相關連結</span><span class="sxs-lookup"><span data-stu-id="50aaa-156">RELATED LINKS</span></span>

[<span data-ttu-id="50aaa-157">Azure Operational Insights Cmdlet</span><span class="sxs-lookup"><span data-stu-id="50aaa-157">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="50aaa-158">AzureRmOperationalInsightsLinkTargets</span><span class="sxs-lookup"><span data-stu-id="50aaa-158">Get-AzureRmOperationalInsightsLinkTargets</span></span>](./Get-AzureRmOperationalInsightsLinkTargets.md)


